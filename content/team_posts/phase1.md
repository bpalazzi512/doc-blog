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

Hi, We are Team **Gerbies!** Our team members include Seamus, Gavin, Brady, and Bobby

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





