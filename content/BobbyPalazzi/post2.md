---
title: "Phase 2 Individual Post"
date: 2024-05-11
draft: false
description: "bobby's phase 2 post"
tags: ["authors", "config", "docs"]
slug: "phase2"
authors:
  - "bobby_palazzi"
showAuthorsBadges: false
---

# Individual Contributions to Phase 2

This week started off with some troubles on the data side. When Seamus and I started to explore cleaning and analyzing the data from the eurostat api, we realized that eurostat returns the data in a format that we had never seen before. Upon a few hours of research, I realized that the data was being returned in the json-stat format -  a format specific to very few apis available on the web. The format involved each piece of data being a value in key-value pairs of numbers in the returned json. The data was there but it was unreadable in the given format. Luckily, with some research, we found two libraries- jsonstat.py and pyjstat- which claimed to get the job done. The jsonstat.py ended up not working (as it was not maintained anymore), but the pyjstat did. Given this, we could now start cleaning and interpreting the data.

I focused on the crime dataset, consisting of nearly 25,000 rows of data relating countries, years, and types of crime. To start off, I decided to exclusively use the data that was in the “per 100k” category, as that could be easily compared between countries. Once I had that, I started to look at individual countries and individual crimes over time. The relationship between many of the crimes seemed relatively inverse (as time moved forward crime decreased). Because there were so many types of crime, I decided to aggregate all types of crime together and predict the amount of crime in general. I added up all of the crimes for each year (thus getting the total amount of crimes), and plotted them. 

Alongside the cleaning of the crime data, I was also tasked with creating the linear regression model by hand, which ended up not being too tedious. I developed a model that was relatively accurate for most of the 27 countries in our dataset, with the most extreme values being off by between 600 and 2000 crimes. The model is also easy to use, only having to input a year and a country to a function. In the upcoming week, I’ll be continuing to refine this model while cleaning other eurostat data we have accumulated.

Myself alongside Seamus also worked to collaborate with Gavin and Brady to iron out the exact details we wanted in the app, which helped Seamus and I figure out exactly what data we needed.

Apart from the work, I've had a lot of fun this past week. I've discovered my new favorite activity - using lime scooters. Ramsey and I went to Antwerp on Sunday and paying 8 bucks to use the scooters for an hour allowed us to see parts of the city that we would have never been able to see if we were just walking. I also got these awesome fish and chips from a place called Bia Mara. Overall a great day besides getting poured on by the rain for an hour. It also allowed us to explore even more of the city (outside of the very touristy places) when we went back on Thursday and essentially had a free day there. 
