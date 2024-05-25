---
title: "Project - Phase I"
date: 2024-05-21
draft: false
description: "Our Idea"
slug: "phase1post"
tags: ["authors", "config", "docs"]
authors:
  - "bobby_palazzi"
  - "brady_li"
  - "gavin_sanders"
  - "seamus_coyne"
showAuthorsBadges : false
---

# Introduction

Hi, We are Team **Gerbies!** Our team is named after the beloved Dr. Gerber

## CONTEXT Project Description:

We propose an app called “CONTEXT.” Our aim is to provide prospective immigrants/expats with the context they need to decide where to move. Our app will specialize specifically in European locations. When the user opens the webpage, they will enter information including their age, marital status, whether or not they have kids, etc. From there, the site will present them with a number of sliders to gauge their personal preferences. For example, if the user cares deeply about safety/crime rate, they would adjust this slider to the right. Doing so would update the weight values and thus their “best fit” country ranking. We’ve identified several other preference categories with supporting data from Eurostat including population age, happiness index, access to transit, and average engagement in leisure activities. We’ll continue to add more relevant fields as we see fit. 

The app will also have predictive features enabled by ML for some of these categories; for example, the user may be able to see what the average income in country X might be in 5 years (following current trends). We want to make our app as user-friendly as possible; the ranking will be aesthetically pleasing, including a picture of each country, its name, the number in the list, and a short description. We would also like to explore the possibility of using the ChatGPT API to deliver the rankings in a more digestible, organic way. Through CONTEXT, we hope to provide users with a clear picture of their lives in Europe and help them narrow down the many potential options. We hope we can be the catalyst to help people make that jump and experience all the world has to offer. 


## What it Solves / Questions:
Usually a Google search of how much one aspect of living abroad does not quantify or paint a realistic picture of what it will be like moving/living abroad. An example is how software engineers make less in other countries, but what about quality of life and cost of living? Can we provide a better way for prospective college students to consider studying abroad and attending a university abroad? What does living abroad look like for families long term? There has to be a better way than to rely on saved Instagram reels and websites that say too much. We propose CONTEXT which provides the actual context and information of what it will be like living abroad. 

## Datasets:
We’ll primarily be using the Eurostat API which contains extensive information on every European country maintained by the EU. Here are some links to some preliminary data we plan on including:


[Happiness Index](https://ec.europa.eu/eurostat/databrowser/view/ilc_pw08$dv_426/default/table?lang=en&category=qol.qol_lif.qol_life_aff)

[Popularity of Rail Transit](https://ec.europa.eu/eurostat/databrowser/view/ttr00015/default/table?lang=en&category=t_rail)

[Criminal Offenses By Year and Crime Type](https://ec.europa.eu/eurostat/databrowser/view/crim_off_cat$dv_348/default/table?lang=en&category=qol.qol_saf.qol_safe_sec) (we will most likely use this for ML)

[Engagement in Leisure Activities](https://ec.europa.eu/eurostat/databrowser/view/ilc_scp01/default/table?lang=en&category=qol.qol_lei.qol_lei_le.qol_lei_qnt)

[Social Exclusion by Age](https://ec.europa.eu/eurostat/databrowser/view/ilc_peps01n__custom_11481642/default/table?lang=en)

[Population Demographic by Age](https://ec.europa.eu/eurostat/databrowser/view/demo_pjangroup/default/table?lang=en&category=eq.eq_demo.eq_pop1)

 
 
## Archetypes / User Personas:
### 1) Sarah
 has never really traveled before and is from a small town in Alaska. She came from a poor background but got a big scholarship for pursuing higher education. Her family wants her to stay close but she thinks college in Europe could be cheaper and fun. She wants to get away from the cold weather but is afraid of what life abroad could be like. 

A College Graduate Working in the U.S. thinking about getting a job abroad cares about job prospects, unemployment, language, cost of living, transportation, salary, and quality of life

- As a new traveler, I am looking for locations that are safe and where I can speak English. I want to find a place with low crime rates and see a map to help me visualize areas to avoid. As someone who has not traveled far from my small town, safety is a priority. CONTEXT can also help me convince my parents to let me study abroad via indisputable statistics & data.

- As a low-income individual, I want to find locations that are not too expensive in terms of food, housing, school, and transportation. I want to be able to see my top options and what expenses will add up if I go to a country. I want to be able to budget and see how much I might spend a day or month in certain locations. This is so I can prepare myself financially before I go abroad and be smart with my travels.

- As a young person, I want to find places that are fun for college students; I want to see the age demographic in different regions to make sure I will be somewhere with youthful energy. This is so I enjoy myself while studying abroad and better understand the kind of people I will meet / befriend.


### 2) David and Rachel 
 have always dreamed of living in a picturesque European town. They both work as high school teachers. They need to know about the cost of living, educational opportunities, language barriers, and how to integrate into a new community with their kids. David and Rachel speak Chinese and are hoping to have their child grow around people who are also Chinese. 

A Family with 2 young kids thinking about moving there wants to ensure a good environment for their kids growing up, they care about safety, happiness, education, violent crimes, cost, healthcare, quality of life, and how likely the kid is to be excluded, language, population data, and the exchange rate of current assets.


- As Chinese speakers, we want to live in a country where others speak our language and where we are welcomed. We want to be able to see/rank the places we are thinking about moving to in terms of language and friendliness to immigrants. We also want to be able to see that places have good Chinese culture. This is so we can maintain our culture and identity while raising our children. 

- As parents, we are deeply concerned with our children’s safety. We want to explore countries that are safe and inclusive environments for them to grow up in. We want to be able to raise the importance of safety and education to the top and then from there, select other important factors like cost to see what countries are the best for us. This is so we feel confident and safe in the place our children will grow up in.

- As high school teachers and workers, we want to ensure we are able to transition our skills as math and language teachers to the new country we plan to move to. We want to be able to see if our jobs are in demand and if the salaries are sufficient for raising a family. We want to be able to enter our details of having two children, their ages, and our current jobs to ensure we can have a good future wherever we find ourselves. 


### 3) Bob 
 is a software engineer from NYC. He always loved traveling but felt he was tied down by his field and career to stay in the U.S. He is in the process of looking for a new job, and with his curiosity he started to consider applying to some jobs in London because he has some friends studying there. Bob stumbles across the site and starts to scroll the map on the site and hovers over England which displays some interesting statistics from EuroStat that he did not know before. He clicks on the U.K. and it zooms in to display more statistics and asks more individualized questions about living there and jobs. 

A College Graduate Working in the U.S. thinking about getting a job abroad cares about job prospects, unemployment, language, cost of living, transportation, salary, and quality of life

- As a software engineer, I want to quickly and easily visualize what pay and work life is like in a different country. I want to be able to see the salaries and see what the job market is like for my field specifically as I scroll through countries on a map. This is so I can better see what my job is like abroad and see if it will be sustainable and if it would work out. 

- As a young college graduate, I want to see what my future might look like in a different place. I want to be able to plan out the next 10 years and see how I might grow financially. I want to see housing costs, rent, and how my assets might look. This is so I can set myself up long-term. 

- As a passionate traveler, I want to be able to find places that fit me as a person. I want to be able to find places that have easy access to transportation so I can visit my friends. I want to be able to socialize and still have fun while I’m enjoying the last years of my youth, so I want to be able to find a palace with an enjoyable social scene while factoring in my professional growth. I want to be able to easily travel to other cities to visit my friends so dense public transit is a must. 