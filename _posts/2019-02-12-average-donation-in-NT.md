---
layout: post
title: "The multiple comparisons problem in practice"
excerpt: "An example of comparing multiple averages, using Python's statsmodels."
modified: 2019-02-12
tags: [data science, tukey HSD, fundraising]
comments: false
---

(A modified copy of this post first appeared on Our Community's [Innovation Lab page](https://www.ourcommunity.com.au/general/general_article.jsp?articleid=7632))

#### Northern Territory donors among the most generous in Australia
Following a recent inquiry by ABC News Northern Territory, I investigated (1) whether or not the average [GiveNow](https://www.givenow.com.au/) donation value in the Norther Territory (NT) was not just larger, but also statistically significantly larger than the average donation in other states, and (2) the underlying reasons for the apparent generosity of NT donors. We found that NT donors do indeed donate statistically significantly higher amounts, on average, compared to most other states (with the exception of NSW). Where this difference stems from remains an open question, because observed correlations do not imply causation. Part of the difference may be attributed to the above-average generosity to Indigenous causes, and the observation that men in the NT donate higher amounts than men in other states (but keep in mind that women donate more frequently than men, especially in the NT).

For further details, refer to the full [blog post](https://www.ourcommunity.com.au/general/general_article.jsp?articleid=7632).

#### Multiple comparisons
In this investigation, the `statsmodels` function [multicomp.TukeyHSDResults.plot_simultaneous](https://www.statsmodels.org/dev/generated/statsmodels.sandbox.stats.multicomp.TukeyHSDResults.plot_simultaneous.html) provided a nice way to visualize and compare multiple averages. I found this plot to be particularly useful to demonstrate (a lack of) statistical significance for a non-technical audience. Interval widths are computed using Tukey’s Q critical value. 



