---
layout: post
title: "An introduction to conditional independence, causality and Probabilistic Graphical Models"
excerpt: "Academic note converted to blog post."
modified: 2018-07-17
tags: [causality, pgm, statistics]
comments: false
---

This post summarizes my notes from a brief detour during my PhD to study causality and conditional independence. At the time, we had just finished a piece of research on identifying the *most relevant* and *least redundant* set of features for a prediction problem related to fluid flow in porous media. I then wondered if Probabilistic Graphical Models could provide even more rigorous (perhaps even causal) statistical relationships. I concluded, in the end, that causality was beyond reach due to a lack of causal sufficiency in our data. Establishing conditional independence might have been feasible, but at the time I found that most established methods could not deal with non-Gaussian, continuous data. There have been some exciting developments since then, especially in the area of [additive noise models](https://arxiv.org/abs/1309.6779).

- Under construction -

### Introduction
In this note, we introduce the use of probabilistic graphical models (PGMs) as a tool to analyze conditional dependencies in granular, porous media. In particular, we are interested in the dependencies of the permeability on microstructural parameters describing the geometry and connectivity of the pore space. In previous work[^fn1], we applied a range of feature selection algorithms to further our understanding of the permeability relationships. We build on this research by introducing a more rigorous, holistic approach (PGMs) to selecting the most relevant and least redundant feature set. In the process, under certain assumptions, PGMs aid in the discovery of marginal, conditional and (under strict assumptions) even causal relations between features. Learning the relation structure around the permeability benefits our understanding of granular, porous media because we learn how variables relate.



[^fn1]: van der Linden, J. H., Narsilio, G. A., & Tordesillas, A. (2016). Machine learning framework for analysis of transport through complex networks in porous, granular media: a focus on permeability. Physical Review E, 94(2), 022904.