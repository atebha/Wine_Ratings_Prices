# Wine Reviews and Ratings Analysis

## Overview:
This project is meant to determine whether the rating of a particular wine can be predicted the following year via the use of a machine learning model. Through the duration of the project, the model has evolved using ratings/points and prices.

## Purpose:
The team has selected the topic of wine. The reason why this topic was selected is the wine industry is increasingly incorporating Machine Learning and AI into their business models and operations. Wine's popularity has increased among consumers and especially more so during this pandemic. Our source data is from the website winemag.com (2017 wine review data set: https://www.kaggle.com/zynicide/wine-reviews). The data had a variety of data points such as review of each particular type of wine, its variety, the region it was grown in, country, price, and a finally a rating (e.g. points) of that particular wine. The question we hoped to answer initially was, "Is the rating/ quality of a wine predictive from one to the following year?", but through the course of the project, the question evolved to, "Is rating predictive of price for a given year?"

## Project Details:

### Project Administration
The team will be using GitHub, Slack, WhatsApp, and Zoom meetings to communicate, collaborate on activities, and provide updates on the project.

### Tech Stack
This project will be using Google Colaboratory, Pandas, Python, PostgreSQL, AWS, Machine Learning and Tableau. We will be utilizing Google Colaboratory as our main platform to build our queries, dataframes and for our machine learning. With Python, we will be building our data structures around Pandas and Matplotlib to import, clean and sift through our data. We will be using AWS and PostgreSQL to host our dataframes, and will be utilizing Tableau's storyboard functions to showcase some of our findings as well as to display our data in an easy to digest format.

### Project Outline/RoadMap
The RoadMap is as follows:

  - Review that data set found and preform an exploratory analysis to formulate the question to be answered.
  - Clean that data to start to formulate the answer to our ask.
  - Create the appropriate machine learning model to answer the question we are studying.
  - Train the model selected.
  - Run a confirmation analysis of our results to determine if our model was accurate and correctly deciphered the data.
  - Create the visuals and dashboard that support our conclusion from the data.
  - Written report and presentation based on the findings.

#### Presentation

The project presentation google slides are available at the following link with a final copy uploaded into this repository. The presentation was equally divided between the five members to share project intent, pre-processing actions, machine learning details, additional analysis performed, dashboard details, and conclusions. The final presentation deck uploaded into this repository was downloaded in powerpoint format which includes speaker notes:

https://docs.google.com/presentation/d/1IyK6k_uIQB_v4gubVBGAtbeW--437SMfIlbHgc69sVU/edit#slide=id.p

#### Data Cleaning and Analysis
We will be using Pandas and Matplotlib to clean the data and perform an exploratory data analysis. Further analysis will be completed using a variety of Python libraries as suited for the task such as Numpy. We are using Matplotlib for its statistical powers to clean up information and preliminary graphing. Beginning our process for feature engineering the team took a high level view of the data. A group concensus was reached to drop data columns not relevant to the analysis and to drop the Null values. Because our original data set was made of 150,000 rows, dropping the null values would not negatively impact the final data set used to train the model (for the machine learning portion of the project). Once dropping the data columns not relevant to the machine learning analysis and dropping the null value rows, the data set still had 59,000 rows with focused columns of data for analysis. The Database Storage section below describes the final dataset.

#### Database Storage
Postgres is the database we intend to use, and AWS RDS to host.

For the database, we will be using one main table to reflect the final, cleansed dataset with the intention to build another table in PostgreSQL that groups the countries within the cleansed data set into self-defined regions. These two tables are then joined for data analysis work included in the Tableau dashboard.

The main, cleansed data set contains the following fields: 	  
country
wine_type
price_dollars
ratings_points

The ML Model will use these columns from the dataset.
  The second, country_regions data set contains the following fields:
  country
  region

In PostgreSQL a new server called CodeAvengers was created in which we establish the host as our AWS endpoint. Then, we created a new database called MachineLearningProject, which contained the tables above.

The final, cleansed data set database table schema in PostgreSQL was created through Python Pandas. To establish the connection for our AWS RDS and PostgreSQL database, psycopg2 was imported and cursor.execute used. Next, the country_regions data table was populated via csv import so the joined tables (creating a new table called DATA_COMBINED), could be queried or exported as a csv file for import into other tools such as Tableau.

#### Machine Learning
SciKitLearn is the ML library we'll be using to create a classifier. Our training and testing setup is a supervised learning model. The specificed model that will be deployed for the project will be a logistic regression model.

Data set links:

2017 data set: https://drive.google.com/file/d/1zFHNHw6mTh4kyx8pVd27rh2ttV8b7zfU/view?usp=sharing

2018 data set: https://drive.google.com/file/d/1zFHNHw6mTh4kyx8pVd27rh2ttV8b7zfU/view?usp=sharing

We will be using the 2017 data set to train and test our machine learning model. In order to affirm the relationship between rating/points and price, we scraped the same data source for the following year (2018) with similar data fields in order to perform a linear regression analysis and compare between 2017 and 2018 data.

#### Dashboard
We will be using Tableau to visualize and story board our data.


### Machine Learning Model
(Describe model)
Which model did you choose and why?
How are you training your model?
What is the model's accuracy?
How does this model work?


### Database
(Describe database)
create a document describing the schema of the database (this can be a markdown document, or an ERD).



## Challenges and Difficulties Encountered
