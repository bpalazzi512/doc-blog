---
title: "Gavin's post #3"
date: 2024-06-05
draft: false
description: "Gavin's post #3"
tags: ["authors", "config", "docs"]
slug: "BLp3"
authors:
  - "gavin_sanders"
showAuthorsBadges : false
---

## Personal Update:
I had so much fun this week in Luxembourg -- it was definitely a highlight of the trip! On Saturday I went with a large group on a hike in Schengen (Dr. Gerber came too). It was quite the trek and I'm not sure it qualified as a "trail" at times, though we all made it! Sunday was also great; I went with Brady and Aahil to Vianden castle in the North. We happened to be visting during a historical reenactment so there were tons of people dressed in costume carrying out "olden-day" chores like melting iron ore and carving bowls. We got to take a ski lift up which was fun.

![Vianden Castle](https://lh3.googleusercontent.com/pw/AP1GczOodX5Wx_ly5i6uyP6LqFqYC2njnkljvjwWBRMHhJ_osvkhDsrh9XBizGfNOrmohs165RpHs23NBSGM2LnmNpjX1wQNirrOIxz68witxBzziAQHSn2q=w2400)


## Project Contribution:

Phase 3 was incredibly stressful. At tht time of writing this, it's 4:00AM and unfortunately there's still no end in sight. I began phase 3 by working on the front-end, creating  pages for the country rankings, country profiles, country admins, and movers. This took a while but was fairly straightforward. Unfortunately when it came time to work on the backend, Brady and I got left behind, encountering a number of issues with Docker / streamlit. For example, the json data was getting messed up, reporting the field name twice instead of the actual value of the field. With the help of Dr. Fontenot, we eventually figured this out. Next we were having problems with pulling the api data into streamlit, then with posting updates to the sql database, etc. Needless to say, we've been doung a lot of troubleshooting this phase. I was able to convert all of our DS team's data from csv format into SQL insert statements so now everything is stored in our database. I was also able to integrate the front-end and the back-end, pulling data from our database to populate countrys' name / text fields. 
