# Box Office Trends and Insights: Microsoft New Movie Studio

### Introduction

In this analysis for Microsoft, we will make use of everything we have learned about pandas, data cleaning, and

exploratory data analysis. In order to complete this analysis, you will have to import, clean, combine, reshape

and visualize data to answer the questions provided.Even as a junior data scientist, you can produce interesting

analyses by combining multiple datasets .You will get a chance to practice all of these skills with the movie  

datasets which contains information about movies.

### Objectives

You will be able to:

.Practice loading data with pandas
  
.Practice identifying and handling missing values
  
.Practice joining multiple dataframes
  
.Practice using data visualizations to explore data, and interpreting those visualizations
  
.Perform a full exploratory data analysis process to gain insight about a dataset


### Your Task : Analyzing movies datasets to provide insights for Microsoft New Movie Studio






### Data Understanding

The data sets offered contain a wide range of data essential to understanding our business concerns.There are three selected 

datasets.The data is contained in three separate CSV files:

1.imdb.title.basics.csv: which provides information about movies that emphasize various genres,titles,start years and their      running times.
    
2.imdb.title.ratings.csv: which provides information about average rating of movies and their number of votes.
    
3.bom.movie_gross.csv: that highlights the box office earnings of movies over a particular period of time.
 
4.tn.movie_budgets.csv: that highlights the production budgets and domestic,worldwide profits.




### Business Understanding


Microsoft sees all the big companies creating original video content and they want to get in on the fun. They have 

decided to create a new movie studio, but they don’t know anything about creating movies. You are charged with exploring 

what types of films are currently doing the best at the box office. You must then translate those findings into actionable 

insights that the head of Microsoft's new movie studio can use to help decide what type of films to create.


The business questions to be answered  are:

.Analyzing the distribution of genres in movies dataset and the mean runtime minutes by 
 genre to find out how long most movies run.

.Analyzing the most popular and profitable genres to invest in.

.Analyzing studios with the highest  average total gross.

.Analyzing the relationship between total gross profit and the production budget.




### Requirements

1.Import the required libraries and load the data with pandas.
Import pandas,seaborn,numpy and matplotlib.Create  dataframes that represent the three CSV files. 
Use pandas methods to inspect the shape and other attributes of these dataframes. 

2.Perform Data Cleaning and answer the first question.
You will be required to check for and deal with missing values,extract and split the genres then create a 
visualization of distribution of genres.

3.Get the mean runtime minutes by genre.
You will be required to split the genres, find the mean runtime_minutes by genre and provide a visualization.

4.Analyze the most popular and profitable genres to invest in.
You will be required to merge dataframes,perform data cleaning on merged dataframe, grooup by genres and number of votes 
or averagerating and create a visualization.

5.Analyzing studios with the highest  average total gross.
You will be required to find average total gross of different studios and create a visualization to find most profitable
studios.




### Import the required libraries

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
%matplotlib inline
import seaborn as sns



There are three deliverables for this project:

* A **GitHub repository**
* A **Jupyter Notebook**
* A **non-technical presentation**

Review the "Project Submission & Review" page in the "Milestones Instructions" topic for instructions on creating and submitting your deliverables. Refer to the rubric associated with this assignment for specifications describing high-quality deliverables.

### Key Points

* **Your analysis should yield three concrete business recommendations.** The ultimate purpose of exploratory analysis is not just to learn about the data, but to help an organization perform better. Explicitly relate your findings to business needs by recommending actions that you think the business (Microsoft) should take.

* **Communicating about your work well is extremely important.** Your ability to provide value to an organization - or to land a job there - is directly reliant on your ability to communicate with them about what you have done and why it is valuable. Create a storyline your audience (the head of Microsoft's new movie studio) can follow by walking them through the steps of your process, highlighting the most important points and skipping over the rest.

* **Use plenty of visualizations.** Visualizations are invaluable for exploring your data and making your findings accessible to a non-technical audience. Spotlight visuals in your presentation, but only ones that relate directly to your recommendations. Simple visuals are usually best (e.g. bar charts and line graphs), and don't forget to format them well (e.g. labels, titles).

## Getting Started

Please start by reviewing this assignment, the rubric at the bottom of it, and the "Project Submission & Review" page. If you have any questions, please ask your instructor ASAP.

Next, we recommend you check out [the Phase 1 Project Templates and Examples repo](https://github.com/learn-co-curriculum/dsc-project-template) and use the MVP template for your project.

Alternatively, you can fork [the Phase 1 Project Repository](https://github.com/learn-co-curriculum/dsc-phase-1-project), clone it locally, and work in the `student.ipynb` file. Make sure to also add and commit a PDF of your presentation to your repository with a file name of `presentation.pdf`.

## Project Submission and Review

Review the "Project Submission & Review" page in the "Milestones Instructions" topic to learn how to submit your project and how it will be reviewed. Your project must pass review for you to progress to the next Phase.

## Summary

This project will give you a valuable opportunity to develop your data science skills using real-world data. The end-of-phase projects are a critical part of the program because they give you a chance to bring together all the skills you've learned, apply them to realistic projects for a business stakeholder, practice communication skills, and get feedback to help you improve. You've got this!
