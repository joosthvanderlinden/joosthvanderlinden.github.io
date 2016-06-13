---
layout: post
title: "How to organize a datathon"
excerpt: "My tips and lessons learned from organizing the Melbourne Datathon"
modified: 2016-04-11
tags: [datathon]
comments: false
---

There is a lot of help available on running traditional hackathons (like [this](http://hackdaymanifesto.com/) page) but very little guidance tailored to running a hackathon for data science. Therefore, I am sharing my experiences here in hopes of helping other data-enthusiasts getting started.

### The concept
The concept is simple. You provide the dataset; participants provide insights. What is the value in the data? What are the business opportunities? What corporate or societal problems can we solve with this data? What could the data be connected with to create new insights? Outcomes may include visualizations, insights into specific variables, predictions or analyses involving external datasets. Essentially, a datathon is like a real data science consulting job: here's a dataset, tell me something interesting.

## Length
Traditional hackathons are often run over the course of a weekend. We decided against this. While it might work for you, we found that the process of data discovery takes a bit longer: as part of the competition, data needs to be cleaned and pre-processed before you can start to analyze something, and that doesn't even take into account "understanding" the various variables involved. If your datathon has a specific theme with some pre-defined objectives, and if your data is relatively clean and transparent, then a weekend might work for you. If you (like us) ask no specific questions, then my advice is to run the datathon over the course of one or two weeks. 

## Competitions involved
The Melbourne Datathon has so far consisted of two competitions: a traditial Kaggle "prediction" competition, and a pitching competition. In the former, the objective is to predict one of the variables in the dataset. For example, in the Melbourne Datathon 2016, we asked participants to predict whether or not a job was a hospitality job, based on the location, salary range, job description etc. We hosted the competition on [Kaggle In Class](https://inclass.kaggle.com/). Make sure you hold out part of the data to score each prediction. In the pitching competition, the objective is to come up with new insights. Participants submit a slide deck, explaining visually explaining their ideas. Next, the data owner and/or an industry panel consisting of data science "executives" assesses the entries and picks a top 5. The top 5 teams pitch their analysis to the panel and an audience on the final night of the datathon, after which the panel decides the top 3.

## Events involved
The Melbourne Datathon consists of four events: launch day, hackday, submission day and the pitch night:
- **Launch day**. I consider this optional, but it helps to create some buzz and get people excited. During the launch event (either over lunch or right after work hours) we share a "sneak-peek" data file, containing a small subset of the full dataset. Participants are not required to attend the launch event, but many will to get an early start. The launch event is also an opportunity to quickly run through the schedule and answer questions. We deliberately did not share anything about the data itself during our launch event, to give people a chance to discover the structure themselves. Lastly, launch day is an opportunity for people to sign the non-disclosure agreement (NDA), if you have one. We cross-checked NDAs against our online signup and emailed participants the sneak-peek file.
- **Hackday**. The hackday is the main event of the datathon. First and foremost, you should share the full dataset and organize a data walkthrough (run by your data owner) to explain all variables involved. Second, you should offer the space for teams to form and work together. If your datathon attracts a lot of "beginners" (close to 50% in our case) then running a series of tutorials is a good idea. At a minimum, I recommend a tutorial on loading and plotting the data in R/Python, and a tutorial on how to present data insights. You should also have some mentors floating around to help answer questions about the data and running an analysis in R or Python.
- **Submission day**. After hackday, teams go home and continue to work on their entries until the submission deadline. Directly after the submission deadline, have your data owner and/or industry panel assess the entries and pick a top 5. Next, communicate the top 5 to your participants.
- **Pitch night**. The pitch night is the conclusion of the datathon. Five selected teams pitch their ideas to an audience of participants and non-participants (this event can be open to everyone), as well as the industry panel. After the presentation, each panel member ranks the pitches, from which you can compute the final ranking. Prizes are subsequently awarded during the award ceremony. If you have the budget, a small afterparty at your local pub is a good idea.

### Tips and lessons learned

## Pitching to potential (data) sponsors
Unless you already have a dataset when you decide to organize a datathon, finding a previously unreleased dataset can be challenging. I have found that government departments are reluctant to release their data due to political bagage and the risks of anything "bad" being exposed, while our efforts to obtain a corporate dataset often ended at the legal department. 
That being said, there are a lot of benefits for a company/institution/government department to become your "data sponsor" and share their data with you. The data will be analyzed by a group of enthusiastic data scientists, and you would be surprised to see how many different angles are taken. Despite having 20-25 submissions, we have yet to see two teams doing the same thing. Moreover, having no previous knowledge of the data often helps people think "out of the box." The data sponsor also gets significant brand exposure and the opportunity to network and recruit. 

## Things to look for in a dataset
For a succesful competition, you want a rich and granular dataset. When people ask what you exactly you are looking for, I recommend listing the following:
- A **people** element, e.g. users, customers, participants, drivers, etc.
- A **time** element
- A **place** element, e.g. latitutde/longitude, city, country
- **Raw** data, e.g. granular, not aggregated
- Previously **unreleased** data, e.g. with no answers/questions on the internet
- **Medium-sized** data, e.g. 2-4 GB, should fit in memory on people's laptops
- (optional) **local** data, e.g. from your city, state, country

Regarding the size, larger datasets (5+ GB) are possible, but in that case the data should be cut up into manageable chunks. That way, everyone can get started on their laptop, and the more eager participants can go nuts with their database.

## Budgeting for a free event 
The Melbourne Datathon has so far been a free event. If you run your event for free as well, take into account that a lot of registrated participants will not show up. In 2015, we saw roughly 50% of our online registrations show, while in 2016 it was closer to 60%.

### Other advice
- Sharing the dataset
- NDAs: retain IP with participants
- Website
- Communication
- Social media
- Get a good photographer
- prize money from data sponsor to take away impression of free labour
- Audience vote: http://www.voxvote.com/
- Judging criteria: teamwork
