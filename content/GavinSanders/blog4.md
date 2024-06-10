---
title: "Gavin's post #4"
date: 2024-06-10
draft: false
description: "Gavin's post #4"
tags: ["authors", "config", "docs"]
slug: "BLp4"
authors:
  - "gavin_sanders"
showAuthorsBadges : false
---

## Personal Update:

Wow... I can't believe it's already over -- the time really flew by! Though most of my time this week was dedicated to the project, this week still had some highlights. My favorite speaker of the trip was the lawyer from KU Leuven; it was so cool to hear about his legal battles with tech giants like Meta. The C-Mine Expedition was also a welcome break from project stress. One good memory from this day was when we went into the noise room underground and had a mini-rave, jamming out to the "explosion button". I also just wanted to say thanks so much for putting this dialogue together and allowing me to come along. It's been an unforgettable experience that I will absolutely carry with me for the rest of my life. I'd even venture to say that I've grown as a person in many ways over the past 4 weeks (for example, I'm now a coffee-drinker thanks to the project). I'm going to miss this group and hope we can do a reunion (at an Indian restaraunt?) at some point in the Fall!


![CMINE 1](https://lh3.googleusercontent.com/pw/AP1GczOzm8BFe3c05x-9-EqfFfTc9v4rjkHy_r-SYubnZKcoRRRoAUITwgAYMOjCHgKA2mEfRIpqyBuiMoSBxVGcajj9HjdyoM-Ld0vbOV9EBkY5RaDOTUjt=w2400)

![CMINE 2](https://lh3.googleusercontent.com/pw/AP1GczNhqoeYf861ZJCtaNe4Fbq4zrIKNXmBoHO7A3gHGFVx0_urrH8WhjpBpx-lBAavbQ-jDwx7nhJH7O6KrqrJc4SSy47gQjeQpsaGK9i7yY_9JhCtLsIq=w2400)


## Project Contribution:

Our app has gotten a complete face-lift over this week. It's transformed like a butterfly from a chrysalis. But it was by no means an easy transformation. I continued to expand the front-end while integrating existing UI elements to the backend. The database had to be modified in many areas to support such connections. We initially struggled with implementing post and put requests and also had to consider when/how to push modifications to the database. As an example, for the sliders we added a "generate ranking" button which stores the slider values in a new entity in the database. The button also runs a get request to generate the new ranking with the updated slider inputs, then runs a put request to publish these rankings. I worked with Bobby and Seamus to integrate the second ML model into our the front and backend of our project. This was the biggest hurdle of the project as so much had to be adapted for compatability. I was also responsible for adding an interactive map to the rankings page which highlights countries on a spectrum from green to red depending on their current ranking. This involved parsing a massive json file containing data on the borders of every country in the world. I originally used geopandas to parse this file which worked on my computer but my teammates were unable to build it. We learned that some of geopandas' requirements are incompatible with Macs running Apple Silicon. This was a big headache and we tried a bunch of things to troubleshoot, including manually compiling the missing C dependencies. Ultimately I found an alternative geo-parsing package which worked after some tweaks. I was also responsible for adding the Mockaroo data.

