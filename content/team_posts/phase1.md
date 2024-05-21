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

Hi, We are Team **Gerbies!** 

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


## Personas:
### A College Graduate Working in the U.S. thinking about getting a job abroad cares about job prospects, unemployment, language, cost of living, transportation, salary, and quality of life
	
Bob always loved traveling but felt he was tied down by his field and career to stay in the U.S. He is in the process of looking for a new job and with his curiosity he started to consider applying to some jobs in London because he has some friends studying there. Bob stumbles across the site and starts to scroll the map on the site and hovers over England which displays some interesting statistics from EuroStat that he did not know before. He clicks on the U.K. and it zooms in to display more statistics and asks more individualized questions about living there and jobs. 

Emily is a recent college graduate working as a marketing coordinator in New York City. She has always been fascinated by different cultures and is considering moving to Barcelona for its vibrant culture and emerging marketing industry. Emily needs information on the job market, salary expectations, and language requirements in Spain. Emily opens up the site and scrolls to see if Spain and the countries nearby are English-friendly. She goes on the job search bar and it displays some potential jobs and what the cost of living is like in Spain.

Priya is a financial analyst in Chicago, working at a major investment firm. She has heard great things about the financial sector in Germany and is considering relocating there for better career growth. Priya is interested in understanding the financial job market, salary ranges, and lifestyle differences between Chicago and Germany. Priya wonders what her assets will be like over in Europe and what would happen if she moved there. She clicks her currency and provides her current assets and salary. The website provides her a map dictated by color (green for a very lavish life style there with her income). 


### A College Student thinking about studying abroad or transferring cares about costs over the quality of life, ease of transportation, location, (safety?), language, education, leisure, and social interaction.

Sarah has never really traveled before and is from a small town in Alaska U.S. She came from a poor background but got a big scholarship for pursuing higher education. Her family wants her to stay close but she thinks college in Europe could be cheaper and fun. She wants to get away from the cold weather but is afraid of what life abroad could be like. Sarah uses CONTEXT to find a warm location in Europe with relatively cheap prices. 

Jake is a junior at a large state university and has always wanted to experience life in Europe. He is exploring options for a semester abroad in Italy. Jake is primarily concerned with ease of getting around and ability to communicate with others. With CONTEXT, he finds that Italy is a good match for him due to its high percentage of English speakers and dense rail network.

Emma is a sophomore studying environmental science who wants to transfer to a university known for its strong sustainability programs. She has heard great things about Scandinavian countries and is particularly interested in universities in Sweden and Denmark. Emma wants information on average tuition and cost of living. She goes on the CONTEXT site and enters her preferences. She discovers that while the Nordic countries have low college tuition, they are otherwise very expensive. Her personal ranking presents her with alternatives that better suit her needs.


### A Family with 2 young kids thinking about moving  wants to ensure a good environment for their kids growing up. They care about safety, happiness, education, violent crimes, language, cost, healthcare, quality of life, and their child's future.

Sheryl and Sam have two middle-aged children. Sheryl’s husband got a job in the NATO HQ in Belgium and has some job offers in France. They are well off and loved their travels to Europe on their honeymoon. However, Sheryl has a lot of friends back home in NYC and is worried about raising a family in Europe because it is so different. She and her family have a lot to consider with money and family. Sheryl and Sam put in their incomes and attempted to look for housing. As they scroll the map they find that the average household cost in  France fits their ideal range. After dragging a line between Belgium and France they see that transportation between Belgium and France is very good and that they are similar in cost.

Michael and Laura have two young children and currently live in the suburbs of Chicago. Michael received a job offer in Sydney, Australia. They are excited about the adventure but concerned about finding good schools, healthcare options, and a safe neighborhood for their kids. Michael and Laura scroll on preferences and importance that safety and healthcare are very important for their decision. The website then provides a map that highlights the best options. They then also scroll high on the education so the map colors start to change to highlight the new best countries to move to.

David and Rachel have always dreamed of living in a picturesque European town. David’s company is opening a new office in Zurich, Switzerland, and they see this as a perfect opportunity. They need to know about the cost of living, educational opportunities, language barriers, and how to integrate into a new community with their kids. David and Rachel speak Chinese and are hoping to have their child grow around people who are also Chinese. They enter their language and scroll that language and population distribution are important to them. The website then highlights the countries to further explore that are better for their situation. 




