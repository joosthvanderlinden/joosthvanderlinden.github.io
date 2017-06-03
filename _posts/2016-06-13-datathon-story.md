---
layout: post
title: "The Melbourne Datathon - How it came about"
excerpt: "The story behind founding and organizing a hackathon for data science."
modified: 2016-06-13
tags: [datathon]
comments: false
---

In this blog post, I will share my story and experiences on running a datathon in Melbourne. Running one yourself? Make sure you check out my [other post](http://joosthvanderlinden.github.io/datathon-tips/), in which I share my tips and lessons learned, and the [overview video](http://joosthvanderlinden.github.io/datathon-video/) for a quick intro.

### Founding the Melbourne Datathon
Back in December 2014, I read a few [articles](http://www.datanami.com/2014/11/24/datathons-emerge-training-recruitment-tool/) about the concept of a datathon and I thought it would be fun to organize one in Melbourne. But where to start? I had just started going to the local data science Meetup. I got in touch with the organizer ([Phil Brierley](https://au.linkedin.com/in/philbrierley)) who was immediately excited about the idea too. Lucky for me, Phil knows practically everyone and everything doing data science in Melbourne. I had found myself a co-organizer.

Countless meetings and coffees followed, during which time we hashed out the format. We got together with a small web development startup ([Zuse Digital](http://www.zusedigital.com/)) to set up a website for us. Thanks to the Meetup, finding venues and sponsors proved relatively straightforward. Our friends and colleagues (even my wife!) got involved to help out with logistics and communication. We attracted a group of data "executives" to serve as our jury and got a group of experts together to be the mentors during the event. I also saw an opportunity in making our event part of the [Melbourne Knowledge Week](http://www.melbourne.vic.gov.au/arts-and-culture/events-partnerships/melbourne-knowledge-week/Pages/melbourne-knowledge-week.aspx), adding to our exposure outside the Meetup and integrating our event with the city's objective of promoting the knowledge sector.  

The most challenging aspect of organizing the datathon turned out to be finding the dataset. We wanted a new, previously unreleased dataset, to make sure there were no questions/answers out there, and to make the datathon more attractive. Initially, we set our sights on data from the local smartcard ticketing system (Myki) for public transport. Unfortunately for us, the Myki system carries A LOT of political baggage. Even though we got as high as the state's Minister for Public Transport, there was just not enough incentive (and too much risk) in the government to release the data. 

Moving on from our "holy grail," we started chasing down countless other leads. We continued searching in the government sector for a while, talking to the Health Department, Economic Development, VicRoads, Australia Post, Forest Management and Ambulance Victoria, but nothing really seemed to pan out. Although open data is gaining momentum in [Melbourne](https://data.melbourne.vic.gov.au/) and [Victoria](https://www.data.vic.gov.au/), often we found that a dataset was too politically senstive, already public or was to be made public on a date that did not align with our planning. We also searched in the corporate sector, meeting with representatives from various banks and IT companies, as well as a credit rating agency and an employment marketplace. Here, our main roadblock was often the legal team. Despite the benefit of having a group of eager data-enthusiasts sifting through the data and our offer to set up a non-disclosure agreement, not everyone was too keen on the idea of having their data out in the open. 

After months of searching, we finally found a corporate partner (Betfair) who was willing to share a really interesting dataset from their betting marketplace. Although not everyone was too happy about the idea of working with betting data, the data did offer everything we were looking for: a temporal element, a spatial element and a "people" element. Interestingly, some teams ended up using the dataset "for good" by analyzing suspicious betting behaviour and money laundering.

The 2015 edition itself was a success. About 120 people showed up on the hackday. We ran tutorials on getting started with R and pitching your insights. 22 teams submitted an entry and close to 200 people saw the top 5 contenders pitch their insights, visualisations and predictions to our industry panel. Between the pitching competition and the subsequent Kaggle competition, winning teams took home $4,000 in prize money. [Mat Kelcey](http://matpalm.com/blog/) from Google talked about recurrent neural networks in between the pitches. Finally, arguably most appreciated was the free bartab afterwards!
<figure>
	<a href="/images/datathon2015_hackday.jpg"><img src="/images/datathon2015_hackday.jpg"></a>
	<figcaption>Melbourne Datathon 2015 - Hackday.</figcaption>
</figure>
<figure>
    <a href="/images/datathon2015_pitchnight.jpg"><img src="/images/datathon2015_pitchnight.jpg"></a>
    <figcaption>Melbourne Datathon 2015 - Pitch night.</figcaption>
</figure>

### Scaling up in 2016
Seeing the potential to scale up and make the event even better, our team launched straight into organizing the Melbourne Datathon 2016. This time, having actually demonstrated what was possible, it turned out to be much easier to find a dataset, sponsors and venues. The dataset was provided by [Seek](http://www.seek.com.au/), an employment marketplace, who shared their website activity (millions of impressions and clicks) and a few hundred thousand job ads with us. [Telstra](http://www.telstra.com.au) was kind enough to host our hackday in their brand new innovation lab (curved screens everywhere!) and [Hortonworks](http://hortonworks.com/) sponsored 150 (!) pizzas. Finally,  [KPMG](https://home.kpmg.com/au/en/home.html) chipped in part of the prize money and bartab. Our friend [Yuval Marom](https://au.linkedin.com/in/yuvalmarom) got together with a student employment startup ([prevyou](https://www.prevyou.com.au/)) and set up a bunch of student internship prizes, which participants could apply for. We scaled up our communication with MailChimp and Hootsuite, after which we were ready to go.

Budgeting for a free event is difficult. When hackday came around, we expected upwards of 200 people to show up. We were quite amazed to see 350 people walk through the door, nearly tripling our attendance compared to the previous year. Our pizza order was quickly adjusted and although the presentation area got a bit (too) cozy, everyone managed to find a spot for their team. We ran tutorials on text mining in R and Python, exploring data with SQL and Tableau, submitting to Kaggle and pitching insights. Between the Kaggle competition and the pitching competition, we received about 75 team entries. The Kaggle competition proved to be especially exciting, with the winning team joining forces on the last day (to ensemble their models) and spending over $200 on AWS credits (lucky for them they won first prize!). In the pitching competition we saw teams analyze the data from all sorts of different angles, from text mining job descriptions to suggest better job tags to visualizing the entire job market with a network model. 
<figure>
	<a href="/images/datathon2016_hackday.png"><img src="/images/datathon2016_hackday.png"></a>
	<figcaption>Melbourne Datathon 2016 - Hackday.</figcaption>
</figure>
<figure>
    <a href="/images/datathon2016_pitchnight.png"><img src="/images/datathon2016_pitchnight.png"></a>
    <figcaption>Melbourne Datathon 2016 - Pitch night.</figcaption>
</figure>

### Onwards
Looking back, it has been incredibly exciting and I feel very fortunate to have had the opportunity to peek into everyone's "data kitchen" while searching for a dataset, venues and sponsors. Even though we were turned down 9/10 times, I met a lot of passionate people, which, combined with our event's current growth rate, strengthens my belief that data science is gaining a lot of momentum in Melbourne. Our data science Meetup, for example, has grown to almost 4,000 members in just 2 years and every event is packed (is it really just the free pizza and beer? who knows).

To ensure everyone's on the same page, I set up a long-term strategy for the Melbourne Datathon. I think it is most important for Melbourne Datathon to remain an independent, community-driven event. The Meetup should always be the sole organizer and fully in charge. We attract sponsors on the premises of contributing to the data science community in Melbourne, networking/hiring opportunities and brand exposure. If the dataset is corporate, the data sponsor should pitch in most of the prize money to take away any impression of "free labour." As beneficial (sponsoring-wise) as a corporate dataset may be, ultimately a community dataset would fit best with a community event. Hence, a societal dataset (in healtcare) is on our radar for next year. We are excited to see what the future holds!
