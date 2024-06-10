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
{{< katex >}}

## Slides linkout
[LINK](https://docs.google.com/presentation/d/1fXcqpzLVSoFwaYzdTRdtBE8xQRvwlK4YNPJwMhhC31o/edit?usp=sharing)

## This Week in Review

This week marked the completion of Phase 4 and, by extension, the project as a whole. For both the data and computer science teams, the week was a sprint. Key milestones included the development and implementation of a cosine similarity model to match users to countries, refinement of the web app interface, further development of the database/Rest API, and more. While previous talks had leaned toward machine learning designs in the area of K-Nearest Neighbors, these were ultimately abandoned in the interest of streamlining development while also understanding the relative limitations these types of models imposed given a lack of true training data. Because of this, a cosine similarity approach was adopted. Despite being a “softer” machine learning approach, it provided a more efficient method of matching, allowing users to input percentile scores per feature based on importance.

Machine learning model 1, a linear regression used to predict crime rates over time by country, was further integrated into the web app as an accessory function on the country profiles page. Ultimately, this allows a user to view projected net crime rates for five years.

To complete these changes, additional data was processed and written into the database, along with column refactoring to ensure consistency. This also included designing new routes to allow the Python programs to access MySQL content.



## Linear Regression

Linear regression is a commonly used method of determining and utilizing the relationship between a dependent variable \( Y \) and one or more independent variables \( X \). While other versions analyze with the use of multiple \( X \) variables, the model used here is known as a simple linear regression, drawing data from one \( Y \) and \( X \) variable to create predictions. 

The general form of a linear regression is:

\\( Y = \beta_0 + \beta_1X\\) 

Where:
- \( Y \) is the dependent variable
- \( X \) is the independent variable
- \( \beta_0 \) is the intercept
- \( \beta_1 \) is the slope of the independent variable

## Model 1

For our first model, we utilized linear regression to predict crime per 100k residents based on country and time. We used a dataset from Eurostat to get the total amount of crime per 100k residents in every country for every year. This wasn’t the easiest task to get the data into the by year format as every country recorded data based on the types of crime, so we had to loop through the whole dataset and manually record the amount of crimes per 100k for that given year.

![Pre-sum](https://i.ibb.co/sH16wPT/Screenshot-2024-06-10-at-7-59-19-PM.png)
Pre Sum


![Post-sum](https://i.ibb.co/m4PjJ7S/Screenshot-2024-06-10-at-7-59-33-PM.png)
Post sum

This is the data that is stored in our database to be used to train the model. When we retrieve the data in the backend, we create a dataframe with one-hot-encoding and do simple linear regression on that data. 

![Dummies](https://i.ibb.co/VYKdGg2/Screenshot-2024-06-10-at-8-09-29-PM.png)

Note: the drop_first parameter is important here. Without that, we overfit the data, leading to a very inaccurate model (found this out very recently)

![Crime](https://i.ibb.co/P1MCppJ/Screenshot-2024-06-10-at-7-59-45-PM.png)
Graph of total crime

![Regression1](https://i.ibb.co/fQSScyk/Screenshot-2024-06-10-at-8-00-03-PM.png)
Here, I set up X and Y and find the line of best fit

![Helper](https://i.ibb.co/Sr2dZtK/Screenshot-2024-06-10-at-8-00-09-PM.png)
Helper function

Turns out, this model is very accurate, with an R^2 of about 0.93. This makes sense considering the following plot of y values vs. predicted y values.

![ypred](https://i.ibb.co/Vp11qCL/Screenshot-2024-06-10-at-8-00-19-PM.png)

Furthermore, looking at the residual plots, it appears none of the assumptions are violated

![Residuals1](https://i.ibb.co/cJ8mP5H/Screenshot-2024-06-10-at-8-00-37-PM.png)
![Residuals2](https://i.ibb.co/5LpLSwS/Screenshot-2024-06-10-at-8-00-29-PM.png)






## Cosine Similarity 

Cosine similarity works by calculating the cosine of the angle between two vectors across an n-dimensional plane. The potential range of outputs spans -1 to 1, where -1 represents angle theta resting close to 180 degrees (indicating opposite vectors), 0 represents theta at roughly 90 degrees (indicating orthogonal vectors), and 1 represents theta at roughly 0 degrees (indicating identical vectors). Additionally, this means that a negative cosine similarity value will exclusively represent a vector angle greater than 90 degrees, which doesn’t tend to occur when the system is implemented in the correct use cases.

When considering vectors \( A \) and \( B \):


\\(\cos(\theta) = \frac{A \cdot B}{||A|| \cdot ||B||}\\)

Where:
- \( A \cdot B \) is the dot product of vectors \( A \) and \( B \)
- \( ||A|| \) is the Euclidean magnitude (norm) of vector \( A \); i.e. the square root of the sum of the squares of its components
- \( ||B|| \) is the Euclidean magnitude (norm) of vector \( B \)
- \( \theta \) is the angle between vectors \( A \) and \( B \)

**Step-by-step methodology**:
1. Calculate the dot product of vectors \( A \) and \( B \)
2. Calculate the magnitude of the vectors
3. Calculate the cosine similarity

![cosine_similarity](https://github.com/bpalazzi512/doc-blog/blob/main/assets/cos_sim_code.png?raw=true)

This code segment represents the meat of the cosine similarity model implemented for our purposes. After verifying that the array dimension is not 1 (and if it is, computing the absolute difference), the sklearn cosine similarity function is employed. The top n matches are then determined and ordered using argsort(). Their corresponding nations are then ready to be returned to the frontend.

## Software Architecuture Overview

Our web app incorporates 3 major layers: the frontend, middleware, and backend. To create the frontend UI we are using streamlit which has been a great and relatively simple solution. For the middleware we are using Flask and a rest api to interface with the database using GET, POST, PUT, and DELETE  requests. The database is hosted in a mySQL docker container; we created approximately 40 routes across 5 different blueprints to access this data in the middleware. This integration was crucial to ensure that every button press—whether for saving, editing, deleting, selecting, or switching—had the intended after-effect. It was essential that the frontend displays weren't just for show but were functional and responsive to user interactions. Our personas were so well connected and the entire application was connected to the database and updated cleanly. This was thanks to the design of our database which connected our personas in a clean manner for routes to work well.

## Moving Companies Features

We dedicated significant effort to building and refining the moving companies' personas features. This included the ability to display, edit, delete, and post information to the database in a clean and structured format. These features were seamlessly linked to other components on the country pages, making moving companies not only visible but also easily contactable via a button. The development of these features required meticulous attention to detail and a robust understanding of database interactions.

## Frontend Enhancements

The frontend underwent substantial enhancements. We redesigned the website's theming, added additional stats to the moving company pages, and made table data more easy to modify/delete. These improvements were not just about aesthetics but also about ensuring a smooth and intuitive user experience. Integrating existing UI elements with the backend was a significant task that required modifications to the database to support these connections. We were strongly going for better UI and displays of data instead of just showing a dataframe in a table. We did this successfully by abstracting and making more routes! 

## Dynamic and Scalable Page Generation

Our application features 3 abstract page templates that dynamically generate 27 unique country pages by pulling data from the database. Additionally, we have 27 admin pages corresponding to each country, using Mockaroo data, and 100 pages for the 100 moving companies also generated with Mockaroo data. This design ensures scalability, allowing us to easily add more companies and different countries, and even expand to include specific cities in the future. We also would like to add more features for country admins. This would include a forum with questions and responses. The moving company reviews should also be displayed in depth with comments and allow users to write reviews.

## Challenges and Learning
We came a long way from phase 2 and phase 3. We put a lot of features and emphasis on connecting moving companies and users, when just a few weeks ago moving companies was not even part of the idea! The amount of new features, routes, and intergration between the database and frontend was insane! 

We learned how to develop a full stack application! It is so cool seeing everything work together! 

Implementing POST and PUT requests presented initial challenges, but through perseverance and collaboration, we overcame these obstacles. Debugging became a daily activity, teaching us the intricacies of software development and the patience required to get everything working correctly. We discovered the importance of precise implementation—sometimes, errors as minor as a misplaced comma could cause significant issues. One of the most challenging aspects of our project was integrating the machine learning models into both the frontend and backend. This involved significant adaptations to ensure compatibility and functionality. Collaborating closely, we managed to integrate the second ML model, which was a significant hurdle due to its complexity and the need for extensive backend modifications. Adding an interactive map to the rankings page was another major hurdle. This feature highlights countries on a spectrum from green to red based on their current ranking. It required parsing a large JSON file with data on the borders of every country. Initially, we used GeoPandas for this task, but compatibility issues with Macs running Apple Silicon led us to seek alternatives. After much troubleshooting, including manually compiling missing C dependencies, we found an alternative geo-parsing package that worked after some tweaks.

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
