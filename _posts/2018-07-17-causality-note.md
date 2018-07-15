---
layout: post
title: "An introduction to conditional independence, causality and Probabilistic Graphical Models"
excerpt: "Academic note converted to blog post."
modified: 2018-07-17
tags: [causality, pgm, statistics]
comments: false
---

<!-- Inline math replace:  -->
<!-- \$(.*?)\$  -->
<!-- \\\\($1\\\\)  -->
\\(
	\newcommand{\CI}{\mathrel{\perp\mspace{-10mu}\perp}}
	\newcommand{\nCI}{\centernot{\CI}}
\\)

This post summarizes my notes from a brief detour during my PhD to study causality and conditional independence. At the time, we had just finished a piece of research on identifying the *most relevant* and *least redundant* set of features for a prediction problem related to fluid flow in porous media[^fn1]. I then wondered if Probabilistic Graphical Models could provide even more rigorous (perhaps even causal) statistical relationships. I concluded, in the end, that causality was beyond reach due to a lack of causal sufficiency in our data. Establishing conditional independence might have been feasible, but at the time I found that most established methods could not deal with non-Gaussian, continuous data. There have been some exciting developments since then, especially in the area of [additive noise models](https://arxiv.org/abs/1309.6779).

- Under construction

## Introduction
In this note, I discuss the use of probabilistic graphical models (PGMs) as a tool to analyze conditional dependencies. PGMs aid in the discovery of marginal, conditional and (under strict assumptions) even causal relations between a set of variables. Before proceeding, we have to ask ourselves: are we dealing with a *prediction* problem or an *inference* (*discovery*) problem? Given a set of features, do we aim to predict the target variable of interest, or "explain" it? Understanding the difference is crucial in order to avoid erroneous inductions (See Aliferis et al.[^fn2] and [To Explain or To Predict?](https://projecteuclid.org/euclid.ss/1294167961)). In a supervised prediction problem, the goal is to 1) establish a predictive model including a choice of features, learning algorithm and performance metric, and 2) train the model on labeled instances and predict the permeability on unlabeled instances. An inference task, on the other hand, is more focused on testing causal relations between variables, accepting or rejecting hypotheses and understanding conditional (in)dependencies in the data. 

At first sight, feature selection (for the purpose of prediction) seems to transcend the boundary between prediction and inference problems. After all, shouldn't we able to use the prediction performance of a chosen feature set to infer the (causal) dependence of these features on the permeability? It turns out that this is not the case. Aliferis et al.[^fn2] show that *good prediction performance can be completely misleading as a criterion for the quality of causal hypotheses*, if non-causal feature selection algorithms are used. The authors also note a number of existing studies that made this error. As an alternative, Aliferis et al. highlight the existence of principled causal feature selection algorithms, in the form of structure learning methods for probabilistic graphical models. These algorithms *do* do allow "safe" feature selection both for prediction and inference tasks. The difference between non-causal and causal feature selection algorithms relates to the ability of the latter to identify both the most relevant and the least redundant features. Non-causal feature selection algorithms cannot distinguish between redundant features, and may end up selecting features that have no direct (causal) relation with the target variable.

While discovering causal relations is highly desirable from a research perspective, in practice the required assumptions for discovery of such relations are not satisfied. Instead, conditional (in)dependence may be the "next-best" inference mechanism. That being said, some of the causal feature selection algorithms can be used to discover conditional dependencies, without drawing any conclusions about the causality involved. To this end, structure learning for graphical models will be discussed in the upcoming sections. 

## Methods
In this section, I summarize some basic probability and causal theory, followed by a discussion of feature selection and probabilistic graphical models.

### Theory

#### Notation
The uppercase letters \\(X,Y,Z\\) denote (random) variables with lowercase letters \\(x\in Val(X),\ y\in Val(Y),\ z\in Val(Z)\\) denoting their respective values. For sets of variables, we use the bold notation \\(\mathbf{X},\mathbf{Y},\mathbf{Z}\\) with values \\(\mathbf{x}\in Val(\mathbf{X}),\ \mathbf{y}\in Val(\mathbf{Y}),\ \mathbf{z}\in Val(\mathbf{Z})\\). The target variable is denoted as \\(T\\) and a set of variables \\(\mathbf{X}\\) has a joint probability distribution \\(J\\).

For graphs, we use \\(\mathbf{V}\\) to denote the set of vertices (nodes) and \\(\mathbf{E}\\) to denote the set of edges (connections). \\(G = (V,E)\\) denotes a graph, either directed or undirected. An edge is usually denoted \\(\{u,v\}\in E,\ u,v\in V\\). We say that two vertices \\(u\\) and \\(v\\) are \textit{adjacent} (or \textit{neighbors}) if there is an edge that directly connects them, i.e. \\(\{u,v\}\in E\\). Furthermore, in directed graphs, we define \\(\text{\textbf{Parents}}(X)\\) as the set of vertices that directly point to \\(X\\) and \\(\text{\textbf{Children}}(X)\\) as the set of vertices that \\(X\\) directly points to. Because, as we will see, variables are assigned to vertices in a graphical model, we will use the terms vertices, nodes, variables and features interchangeably.

#### Conditional independence
Formally, conditional independence is defined as follows. Variables \\(X\\) and \\(Y\\) are conditionally independent given a set of variables \\(\mathbf{Z}\\) if and only if

$$ 
	P(X=x,Y=y\mid\mathbf{Z}=\mathbf{z}) = P(X=x\mid\mathbf{Z}=\mathbf{z})P(Y=y\mid\mathbf{Z}=\mathbf{z}),\\
	\forall x\in Val(X),\ y\in Val(Y),\ \mathbf{z}\in Val(\mathbf{Z})\ \text{where}\ P(\mathbf{Z}=\mathbf{z}) > 0 \nonumber
$$

If this equation holds, we write \\(X\CI Y\mid\mathbf{Z}\\). Conditional independence implies that given the knowledge of \\(\mathbf{Z}\\), there is no additional evidence that \\(X\\) has any influence on \\(Y\\) and vice-versa. For example[^fn3], let \\(X\\) be the variable stating whether or not a child is a member of a scouting club, and let \\(Y\\) be the variable stating whether or not a child is a delinquent. Survey data might show that \\(X\\) and \\(Y\\) are *marginally* dependent, i.e. members of a scouting club have a lower probability of being a delinquent. What if, however, we consider the socio-economic status of the child, measured by a variable \\(Z\\)? Survey data could now show that, given knowledge of \\(Z\\), there is no additional effect of \\(X\\) on \\(Y\\). In other words, the socio-economic status fully explains any relationship we observe between scouting membership and delinquency.

The relationship between \\(X\\), \\(Y\\) and \\(Z\\) can be represented in a *graphical model*, as shown in the next figure. 
<figure>
	<a href="/images/pgm_conditional_independence.png"><img src="/images/pgm_conditional_independence.png"></a>
</figure>
Nodes represent variables and edges (link) represent influence.



[^fn1]: van der Linden, J. H., Narsilio, G. A., & Tordesillas, A. (2016). Machine learning framework for analysis of transport through complex networks in porous, granular media: a focus on permeability. Physical Review E, 94(2), 022904.

[^fn2]: Aliferis, C. F., Statnikov, A., Tsamardinos, I., Mani, S., & Koutsoukos, X. D. (2010). Local causal and markov blanket induction for causal discovery and feature selection for classification part ii: Analysis and extensions. Journal of Machine Learning Research, 11(Jan), 235-284.

[^fn3]: Example based on [STAT504 - Analysis of Discrete Data](https://onlinecourses.science.psu.edu/stat504/node/112)

