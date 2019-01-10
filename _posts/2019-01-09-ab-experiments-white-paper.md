---
layout: post
title: "Optimizing suggested donations through AB experiments"
excerpt: "A series of experiments to maximize fundraising income"
modified: 2019-01-09
tags: [white paper, data science, AB experiments, fundraising]
comments: false
---

(A modified copy of this post first appeared on the[Innovation Lab](https://www.ourcommunity.com.au/general/general_article.jsp?articleid=7545) page)

We explored how suggested donations on our fundraising platform [GiveNow](https://www.givenow.com.au/) influence giving, and how not-for-profit causes can increase their giving by altering these suggested amounts. In the past, default suggested donation amounts were based on extensive experience with fundraising, as well as feedback from the organisations that use GiveNow to raise money. While the default values had worked well (GiveNow has raised close to $100 million dollars over its 15-year history) we were intrigued by the possibility of boosting donations by changing the suggested amounts.

There is some evidence in academic literature that donors are influenced by suggested donations. We wondered if there might be some "optimal" suggested donation values (not too high as to turn people off, not too low as to leave money on the table) that would maximise the total amount raised by an organisation using GiveNow. We set out to answer these questions using a series of AB experiments.

For detailed discussion of the experimental setup, ethical/privacy considerations and detailed results, read [our White Paper](https://www.ourcommunity.com.au/general/general_article.jsp?articleid=7545).

#### Summary of our findings
Tweaking suggested donation amounts on a GiveNow cause page tends to create a self-cancelling effect - the benefits of influencing some donors to donate a bit more are offset by those who donate less than they otherwise would have. However, individual causes can tailor donation amounts to suit the particular profile of their donors (e.g. period since last donation) to maximise their fundraising income.

#### Other considerations
I repeatedly wondered whether or not we were falling prey to the [Multiple Comparison Problem](https://en.wikipedia.org/wiki/Multiple_comparisons_problem) in our analysis of the results, given the many (many) p-values I calculated over the course of this project. The issue is not discussed in the white paper, but I have gone over the conclusions several times and applied stricter significance thresholds. So far, all the results have held up.



