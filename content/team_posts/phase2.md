---
title: "Project - Phase II"
date: 2024-05-28
draft: false
description: "Our Idea"
slug: "phase2post"
tags: ["authors", "config", "docs"]
authors:
  - "bobby_palazzi"
  - "brady_li"
  - "gavin_sanders"
  - "seamus_coyne"
showAuthorsBadges : false
---

This week we spent a lot of time re-thinking many aspects of the project. Upon examining our user stories, we realized that the student, college graduate, and family archetypes were all very similar. We decided to merge these 3 archetypes into one umbrella “standard user” and put our minds together to come up with 2 others. Taking inspiration from Wikipedia, our first new archetype is the country admin. The admin has the ability to edit their respective country’s page on the site; these pages will contain crowd-sourced information relevant to the moving process (i.e., Visa application, how to find accommodation, etc). We think this extra information will further the app’s goal of providing users with as much context as possible to aid their move (hence the app’s name). We also elected to add features to support a “moving company” archetype. We already connect users to countries; it was a natural extension that we also connect users to moving companies. In each country’s page, we’ll have a section dedicated to moving companies which operate between the user’s home state and that country. Once the user selects their anticipated move load (full house, personal items, vehicle only, etc) they will see a list of eligible companies, their quotes, and their star rating. The user will be able to click a button which sends the moving company their information so they can be contacted. This info will be visible in the Mover Portal, which also acts as the destination for movers to update their routes and prices.

We also began work on our first ML model which consisted of a simple linear regression demonstrating the relationship of crime rate over time by crime category in each European country. We are pleased with the results so far. We have been talking about what data to use for our next ML model. One option we discussed was predicting the annual cost of living for each country as a function of time. This would be useful information to someone moving to Europe since cost is a big factor in the decision to move somewhere. We are also discussing the possibility of using ML to do the country ranking itself using clustering. The alternative method of computing the ranking would be formulaic. 


## Here are the images of our ER diagrams:

![Standard User ER](https://github.com/bpalazzi512/doc-blog/blob/main/assets/standard%20user.png?raw=true)

![Admin ER](https://github.com/bpalazzi512/doc-blog/blob/main/assets/admin.png?raw=true)

![Mover ER](https://github.com/bpalazzi512/doc-blog/blob/main/assets/mover.png?raw=true)

![Global ER](https://github.com/bpalazzi512/doc-blog/blob/main/assets/global.png?raw=true)

## And here is the link to the SQL schema for our global ERD: [SQL File](https://github.com/coyne1313/cs4973_project/blob/main/context.sql)


## Graphs of Data
![homicide](https://github.com/bpalazzi512/doc-blog/blob/main/assets/homicide_bar.png?raw=true)
![homicide2](https://github.com/bpalazzi512/doc-blog/blob/main/assets/homicide_bp.png?raw=true)
![robbery](https://github.com/bpalazzi512/doc-blog/blob/main/assets/robbery_linreg.png?raw=true)

## Changes From Phase1
We made some changes to our Personas and user stories after working out the ER diagram with Dr. Fontenot. Below are our new Personas and user stories for each! 

# PERSONAS

**Bob** is a software engineer from NYC. He always loved traveling but felt he was tied down by his field and career to stay in the U.S. He is in the process of looking for a new job, and with his curiosity he started to consider applying to some jobs in London because he has some friends studying there. 

## General User - Person Thinking About Moving Abroad
- Inputs their info and preferences
- Individualized country ranking generated (with maps)
- Can see the projected future cost of living for each country
- Can click on each country in the ranking list to view its page
- Can browse moving company options for each country, compare prices by move load
- Move load categories: full household, part household (including furniture), personal effects (more than 10 boxes), excess baggage, vehicle only

## User stories 
- As a someone thinking about moving abroad, I want to know the logistics of moving abroad including visas and moving all my assets. I want to learn what are the steps I have to complete in order to legally and physically move abroad. This is so I feel content and can start planning with potentially useful resources. 
- As a software engineer working in the United States, I want to know if the countries I’m interested in moving to will be sustainable for me long term in terms of salary, unemployment, and demand of my job. This is so I feel secure that I can live in abroad long term. 
- As a traveler, I want to find a location that suits me as a person. I want to be able to input my preferences and what I find the most important to me like ease of transportation. This is so I can better picture myself abroad and ensure my happiness. 


**Sarah** works as a marketing manager at Fontemoves, a moving company that helps individuals move their households across states and countries.

## Moving company
- Updates their costs/services per move load, adds countries, connect with users (get user data)

## User Stories
- As a moving company, we want to connect with users and have access to potential/current customers data. This is so we can contact users of our service and make revenue. 

- As a growing company, we want to be able to update our profile, biography, and services. This is so that we can provide potential customers with our most recent achievements and services. We are expanding our coverage of places we can help move to so we want users to know we are an option for them. We also want to be able to adjust our prices as the market changes.

- As a marketting manager, I want to be able to advertise our company to users. I want to show off our reviews, coverage, and successful stories. This is so I can effectively market the company to potential users. 

Maddy is from Belgium and has lived in Brussels for 29 years. She is retired now and occasionally works in nonprofits giving waffle tours around the city. She is very passionate about sharing the culture and beauty of Belgium. 

## Country Admin
- Admin Status: Responsible for updating their country’s page with the most relevant info. This includes the high-level bio as well as more specific info like visa application process etc. 

## User Stories
- As the CONTEXT country admin of Belgium, I want to be able to edit and add to the biography and tips for Belgium. This is because when I stumble across new experiences and tips, I can share it to many individuals.
- As a passionate belgium resident, I want to be able to share my experiences, weekly updates, and pictures to show off what life is like in Belgium. This is so I can expand on my person bio and blog on the page.
- As a food tour guide on the side, I want to be able to recommend amazing locations and food places that intices people to visit and move here. This is so I can share my expertise and feel valued after my retirement. 
