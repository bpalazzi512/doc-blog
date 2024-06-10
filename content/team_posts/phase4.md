---
title: "Project - Phase IV"
date: 2024-06-10
draft: false
description: "Phase 4"
slug: "phase4post"
tags: ["authors", "config", "docs"]
authors:
  - "bobby_palazzi"
  - "brady_li"
  - "gavin_sanders"
  - "seamus_coyne"
showAuthorsBadges: false
---

## This Week in Review

This week marked the completion of Phase 4 and, by extension, the project as a whole. For both the data and computer science teams, the week was a sprint. Key milestones included the development and implementation of a cosine similarity model to match users to countries, refinement of the web app interface, further development of the database/Rest API, and more. While previous talks had leaned toward machine learning designs in the area of K-Nearest Neighbors, these were ultimately abandoned in the interest of streamlining development while also understanding the relative limitations these types of models imposed given a lack of true training data. Because of this, a cosine similarity approach was adopted. Despite being a “softer” machine learning approach, it provided a more efficient method of matching, allowing users to input percentile scores per feature based on importance.

Machine learning model 1, a linear regression used to predict crime rates over time by country, was further integrated into the web app as an accessory function on the country profiles page. Ultimately, this allows a user to view projected net crime rates for five years.

To complete these changes, additional data was processed and written into the database, along with column refactoring to ensure consistency. This also included designing new routes to allow the Python programs to access MySQL content.

## Linear Regression

Linear regression is a commonly used method of determining and utilizing the relationship between a dependent variable \( Y \) and one or more independent variables \( X \). While other versions analyze with the use of multiple \( X \) variables, the model used here is known as a simple linear regression, drawing data from one \( Y \) and \( X \) variable to create predictions. 

The general form of a linear regression is:

\[ Y = \beta_0 + \beta_1X \]

Where:
- \( Y \) is the dependent variable
- \( X \) is the independent variable
- \( \beta_0 \) is the intercept
- \( \beta_1 \) is the slope of the independent variable

## Cosine Similarity 

Cosine similarity works by calculating the cosine of the angle between two vectors across an n-dimensional plane. The potential range of outputs spans -1 to 1, where -1 represents angle theta resting close to 180 degrees (indicating opposite vectors), 0 represents theta at roughly 90 degrees (indicating orthogonal vectors), and 1 represents theta at roughly 0 degrees (indicating identical vectors). Additionally, this means that a negative cosine similarity value will exclusively represent a vector angle greater than 90 degrees, which doesn’t tend to occur when the system is implemented in the correct use cases.

When considering vectors \( A \) and \( B \):

\[ \cos(\theta) = \frac{A \cdot B}{||A|| \cdot ||B||} \]

Where:
- \( A \cdot B \) is the dot product of vectors \( A \) and \( B \)
- \( ||A|| \) is the Euclidean magnitude (norm) of vector \( A \); i.e. the square root of the sum of the squares of its components
- \( ||B|| \) is the Euclidean magnitude (norm) of vector \( B \)
- \( \theta \) is the angle between vectors \( A \) and \( B \)

**Step-by-step methodology**:
1. Calculate the dot product of vectors \( A \) and \( B \)
2. Calculate the magnitude of the vectors
3. Calculate the cosine similarity

## API Development and Backend Integration

One of our primary focuses was on developing the API routes. We created approximately 40 routes across 5 different route blueprints, ensuring they were thoroughly integrated with the backend and the database. These routes included POST, PUT, GET, and DELETE operations, providing comprehensive CRUD functionality. This integration was crucial to ensure that every button press—whether for saving, editing, deleting, selecting, or switching—had the intended after-effect. It was essential that the frontend displays weren't just for show but were functional and responsive to user interactions.

## Moving Companies Features

We dedicated significant effort to building and refining the moving companies' personas features. This included the ability to display, edit, delete, and post information to the database in a clean and structured format. These features were seamlessly linked to other components on the country pages, making moving companies not only visible but also easily contactable via a button. The development of these features required meticulous attention to detail and a robust understanding of database interactions.

## Frontend Enhancements

The frontend underwent substantial enhancements. We redesigned the home page, developed the moving company pages, and added new features to the country pages. These improvements were not just about aesthetics but also about ensuring a smooth and intuitive user experience. Integrating existing UI elements with the backend was a significant task that required modifications to the database to support these connections.

## Dynamic and Scalable Page Generation

Our application features 3 abstract page templates that dynamically generate 27 unique country pages by pulling data from the database. Additionally, we have 27 admin pages corresponding to each country, using Mockaroo data, and 100 pages for the 100 moving companies also generated with Mockaroo data. This design ensures scalability, allowing us to easily add more companies and different countries, and even expand to include specific cities in the future.

## Challenges and Learning

Implementing POST and PUT requests presented initial challenges, but through perseverance and collaboration, we overcame these obstacles. Debugging became a daily activity, teaching us the intricacies of software development and the patience required to get everything working correctly. We discovered the importance of precise implementation—sometimes, errors as minor as a misplaced comma could cause significant issues.

## Machine Learning Integration

One of the most challenging aspects of our project was integrating the machine learning models into both the frontend and backend. This involved significant adaptations to ensure compatibility and functionality. Collaborating closely, we managed to integrate the second ML model, which was a significant hurdle due to its complexity and the need for extensive backend modifications.

## Interactive Map and Geospatial Data

Adding an interactive map to the rankings page was another major achievement. This feature highlights countries on a spectrum from green to red based on their current ranking. It required parsing a large JSON file with data on the borders of every country. Initially, we used GeoPandas for this task, but compatibility issues with Macs running Apple Silicon led us to seek alternatives. After much troubleshooting, including manually compiling missing C dependencies, we found a geo-parsing package that worked after some tweaks.

## Final Database Architecture Overview

**Key Relationships and Functionalities**:
- **Users and Movers**: Users can interact with movers, as tracked in the `moverContacts` table, to facilitate moving to a new country.
- **Routes**: Define the available moving options, specifying the starting state, destination country, mover involved, type of move load, and cost.
- **Preferences and Rankings**: Users can set preferences for various factors using sliders, which are then used to rank countries and store these rankings in the `countryRankings` table.
- **Crime Data**: Provides statistical insights and predictions about crime rates in different countries, potentially influencing user decisions.

## Final Database ER Diagram
![ER DIAGRAM](https://lh3.googleusercontent.com/pw/AP1GczPAs0Wx9XliCULe2nYRTsmqQZ5xyFXUH72Gk-XHQJUHHUgcrtZioCMUtYTpZOonBpIDrZki69Hh7gd193c6-bzkrxw5Ww2U4IMrVmskhHqQwgRB1qoA=w2400)

## App Screenshots
![MAP](https://lh3.googleusercontent.com/pw/AP1GczOksXtT8oe-ohjXbEHUeV5y1FqXNV6NKrCY8Ks4NN5BmHGBmML4BrDTygbc012rmTdA4GTk6YFldybSyHWBYa9RqrgqNUHRGMLDsqpEEIMEhc-0AyxH=w2400)

![COUNTRY1](https://lh3.googleusercontent.com/pw/AP1GczNJDg7C4nWrdGl4W8cU3OnPGb-ZhbhQhZeB6dNb4hI_Or0J_6U6ULwv88D2xBa7H9_kYModxiSGbZwzMOJudlsndWv4ZVYTrnYrpG7IMKSwl7T90YJe=w2400)

![COUNTRY2](https://lh3.googleusercontent.com/pw/AP1GczOTZS10Jiz3gcFGKwh1vjstzlchwHemS8thN8mXmcczJ5yy13Q9EKbEh4yDU4dmcjy-OWcWM1VQpCIGzUSy4jy-WPP-FrSKWcgAUjtkhzm5Xq_SJhwB=w2400)

![MOVER](https://lh3.googleusercontent.com/pw/AP1GczNa1GZKGvSr-EVS0RJSe7cUoeK9Lj3Jt-taJTaR6e_cfztFnhSEohEVNZ9e9DcsbIYTVZ7cJO4ES6fqWFtjiSRYYYYj4Dy63QcFg09yVPw-rIshJsBS=w2400)
