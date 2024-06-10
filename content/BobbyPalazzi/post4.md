---
title: "Phase 4 Individual Post"
date: 2024-06-10
draft: false
description: "bobby's phase 4 post"
tags: ["authors", "config", "docs"]
slug: "phase4"
authors:
  - "bobby_palazzi"
showAuthorsBadges: false
---

# Individual Contributions to Phase 4

Over this last week, I have felt I have contributed significantly to our project. This is mostly due to the fact that I had some prior SQL experience, so I was, for the most part, able to work on both sides of the project. My main contributions to our project include designing the crime linear regression model, implementing both models into the app, creating many of the API routes (mostly the ML ones), and debugging interactions with the database.

Honestly, I had a lot of fun building this project because of the many challenges we had to overcome. The most challenging (and most fun) part of the project was implementing both of the models. At first, I struggled to find an efficient and clean way to get access to the training and inference functions. It needed to be self contained, able to train and predict on the fly. So, I used the object-oriented side of python that we hadn’t explored in class and created Python classes for both of our models. This allowed object creation and a clean way to call training/inference functions. Actually implementing the methods with data from the database took excruciatingly long. It probably took me around 2 hours just to get the cosine similarity function to output the right values, then a solid amount of time afterwards to get the site to display the information accurately. I also had to make an api endpoint just for debugging both of these classes. Despite the work involved, it was so satisfying to see it all work in the end. 

Besides the challenging part, the second-most fun part was creating the frontend. Streamlit gives us an extremely sleek and modern UI built-in, so all we had to do was add our components. Even though I do love CSS and the immense customizability, I will admit it does speed up development and for our purposes more than did the job. 

The highlight of my week was definitely the soccer game. The atmosphere in the stadium was undescriable, espcially for a match that didn't mean a whole lot. I was expecting it to be a smaller crowd, but a international soccer match nontheless. I was pleasantly surprised. It was packed, even in the nosebleeds where we were sitting. The sense of community there was crazy, nothing like anything I've experienced in the US. It also a much-needed break from the looming pressure of the project due date. 

# Context
- Full-stack web application that matches users based in the US looking to relocate with EU countries and available movers
- Ranks countries using cosine similarity machine learning model
- Displays metrics including predicted crime rate (linear regression model) , population, happiness index, and information provided  by a country administrator
- Built using Streamlit, and Flask; Containerized with Docker


