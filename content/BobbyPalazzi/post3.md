---
title: "Phase 3 Individual Post"
date: 2024-05-11
draft: false
description: "bobby's phase 3 post"
tags: ["authors", "config", "docs"]
slug: "phase3"
authors:
  - "bobby_palazzi"
showAuthorsBadges: false
---

# Individual Contributions to Phase 3

This, week, I mainly focused on trying to find data and decide next steps for our next model, considering our first model was pretty solid. I wanted to get at least the idea for the second model out of the way but Seamus and I ended up going a little further than that. The second model was going to the be the matching one, and weighted categories according on what the user inputted. We decided to go with one that found the vector distances between what the user inputted and data from each country. Therefore, we needed data for every country. So, I scraped about 70% of the data we needed for this new model (Seamus doing the other 30%). This was mostly wikipedia pages containg info about weather, cost of living, and healthcare. It was overall pretty straightforward. I also had to use the eurostat api once, but we already had code set up to make that easy. 

The part that ended up being the one that sucked was transferring the code from jupyter notebook to a python file. I thought it would be straightforward, but somewhere along the way either the data or the code for the data got messed up, causing or model to be every so slightly off. This is a bug that I'm still activley trying to fix, but should not take me too long. The bug causes some country's data to show up as slightly less than the model. It should be resolved very shortly. 

In addition, I also transferred our model and training data to csv so that Gavin and Brady could put that data in the database. 

Outside of school, I've been having so much fun. Living here the last few weeks has made me appreciate many things, like ice and AC (for the very few times it's been needed). However, I can confidently say that I would want to live here when I'm older, maybe even living in Leuven. Leuven has been by far the best city I've visited. I love how quiet it is, while still having the city-feel of all the shops in the city center. Luxembourg didn't have that same feel. Besides the public transit, it felt very American (specifically how many cars there were). The one thing I did appreciate about Luxembourg is that it took American Express everywhere, so I could actually use that card instead of my visa that has been taking a beating financially over the last few weeks. Overall, I'm going to miss Leuven and all the places I've been.

