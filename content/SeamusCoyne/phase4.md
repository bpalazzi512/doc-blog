---
title: "Phase 4 Contributions"
date: 2024-06-10
draft: false
description: "Seamus's post #4"
tags: ["authors", "config", "docs"]
slug: "SCp4"
authors:
  - "seamus_coyne"
showAuthorsBadges : false
---

## Project update

This phase has been revolutionary for our app. In the past few days, its styling, functionality, and overall usability have increased multifold. But these changes didn’t come without challenges. The first major challenge of the phase was with failures in post requests that prevented our front end code (or, frankly, any Python code) from accessing the MySQL databases. To resolve this and better facilitate connections, a handful of database alterations had to be put in place. These changes allowed for the sliders to collect and process data with the help of put requests. Probably the most significant complication of the project came with the integration of the ML2 model that I built and further refined in this phase. The model, responsible for matching users to countries based on preferences, acted as the primary tool of the app and, despite having been thoroughly tested in its standalone file, struggled to fit within the Streamlit scripts. Bobby, Gavin, and I worked to debug the numerous errors surrounding its integration. This was particularly cumbersome given the sheer number of alterations that had to be made to get the model to work. I was also responsible for the final preparation of data for Gavin to then transfer into the tables within the database. While most of the datasets had been mostly cleaned, there were small but important inconsistencies between datasets that prevented them from being used together. Gavin and I worked to resolve these issues and create transferable and usable files to be added in the database.

## Personal update

I truly can’t believe the program has run its course. While it feels like our time in Belgium has flown by, the thought of flying out of Boston seems like it was months ago. My favorite speaker of the phase (maybe of the program) was the law researcher from KU Leuven. Having learned a great deal about Belgium’s policies in tech, it was so fascinating hearing about his real world interactions with these laws and the corporations that defy them. A close second was EnergyVille. I admit to having low expectations going in, but the last two presentations were very interesting, as they related to the intersection between data and outside industries. All in all, this month has been absolutely unforgettable. Not only have the outings and experiences been fun and informative, I can genuinely say that I have learned so much from both classes. I didn’t have the highest expectations for Leuven coming in, but I absolutely love it here and will miss it greatly. I am very ready to get back to a healthy sleep schedule and ice water once I’m home again, though.
