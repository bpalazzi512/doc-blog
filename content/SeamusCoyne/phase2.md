---
title: "Phase 2 Contributions"
date: 2024-05-28
draft: false
description: "Seamus's post #2"
tags: ["authors", "config", "docs"]
slug: "SCp2"
authors:
  - "seamus_coyne"
showAuthorsBadges : false
---

During this phase of the project, my team worked to revise our initial project plan, as well as refining our goals with data and API usage. The Data Science aspect, completed by Bobby and I, worked to gather and clean data from the Eurostat API, which required the use of the PyJstat json-stat library. With this completed, we were able to implement our first linear regression models showing patterns in the data. The Computer Science group worked to design SQL components, including ER diagrams, as well as wireframes to gain better clarity on the overall design of the database as well as any additional data sources or components that may be necessary.

Working on the Data Science side, my main goals of the stage were to clean half of the datasets (this work being split with Bobby), to generate EDA plots illustrating the content of the datasets where it wasn't immediately clear, and to formulate manual linear regressions of data. This process started by research related to why the Eurostat API was returning unexpected values. Upon exploring documentation further, it became apparent that an additional step was required to convert the return datatype into a more usable format. With this completed, I then transitioned to cleaning the data, scaling data and converting values where necessary (ex. strings to floats/ints). Finally, I designed functions to plot linear regressions for a selected crime (in this case robbery) over time per nation in the dataset.