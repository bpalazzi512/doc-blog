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

## Wireframe Sketches can be found [HERE](https://github.com/coyne1313/cs4973_project/blob/main/wireframe.pdf)

## Jupyter Notebook Test Bed [HERE](https://github.com/coyne1313/cs4973_project/blob/main/4973_testbed.ipynb) 
## Data Cleaning [HERE](https://github.com/coyne1313/cs4973_project/blob/main/eurostat_EDA.ipynb)

## And the link to the SQL schema for our global ERD: [HERE](https://github.com/coyne1313/cs4973_project/blob/main/context.sql)


## Here are the images of our ER diagrams:

![Standard User ER](https://github.com/bpalazzi512/doc-blog/blob/main/assets/standard%20user.png?raw=true)

![Admin ER](https://github.com/bpalazzi512/doc-blog/blob/main/assets/admin.png?raw=true)

![Mover ER](https://github.com/bpalazzi512/doc-blog/blob/main/assets/mover.png?raw=true)

![Global ER](https://github.com/bpalazzi512/doc-blog/blob/main/assets/global.png?raw=true)



## Graphs of Data
![homicide](https://github.com/bpalazzi512/doc-blog/blob/main/assets/homicide_bar.png?raw=true)
![homicide2](https://github.com/bpalazzi512/doc-blog/blob/main/assets/homicide_bp.png?raw=true)
![robbery](https://github.com/bpalazzi512/doc-blog/blob/main/assets/robbery_linreg.png?raw=true)
