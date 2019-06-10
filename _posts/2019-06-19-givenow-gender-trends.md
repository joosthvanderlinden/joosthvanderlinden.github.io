---
layout: post
title: "Examining donor characteristics with d3.js"
excerpt: "A bubble chart to visualize the causes men and women prefer."
modified: 2019-06-09
tags: [data science, d3.js, donations]
comments: false
---

(A modified copy of this post first appeared on Our Community's [Innovation Lab page](https://www.ourcommunity.com.au/general/general_article.jsp?articleid=7659))

#### The causes men and women prefer when donating through GiveNow
We examined whether men and women give differently through GiveNow. We found that women are three times more likely to donate to Animal Welfare causes on GiveNow than men, and are also more likely to favour Women, International and Multicultural causes. Men, in turn, donate twice as frequently to Gay & Lesbian causes, and are also more likely to favour Science & Technology, Education & Scholarships and Sports & Recreation-focused causes. Women are more likely to give small amounts more frequently than men, while men are more likely to donate large amounts less frequently (the combined effect of which is more or less equal giving by women and men). People give more money in total through one-off donations than recurring donations through GiveNow. This trend Is particularly pronounced for donations to Animal Welfare and Arts & Culture causes.

For further details, refer to the full [blog post](https://www.ourcommunity.com.au/general/general_article.jsp?articleid=7659) and the [interactive chart](https://www.givenow.com.au/stats/gendertrends).

#### Bubble charts in D3.js
I had a lot of fun building this bubble chart, in which I sought to strike a balance between conveying as much information as possible while keeping the layout simple. The [Voronoi method](http://bl.ocks.org/nbremer/801c4bb101e86d19a1d0) turned out to be the perfect method to show the right tooltip for tightly clustered bubbles. Chart design was inspired by [The Words Men and Women Use When They Write About Love](https://www.nytimes.com/interactive/2017/11/07/upshot/modern-love-what-we-write-when-we-write-about-love.html) (NY Times, 7 Nov 2017).





