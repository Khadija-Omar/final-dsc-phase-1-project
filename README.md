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


1.import pandas as pd


2.import numpy as np


3.import matplotlib.pyplot as plt


4.%matplotlib inline



5.import seaborn as sns



### 1.Load the Data

1.Load the content on title.basics.csv








2.Write a code that displays a summary of , providing useful information about its structure and contents.





#Run this cell without changes

#There should be 146144 rows


assert title_basics.shape[0] == 146144

#There should be 6 columns. If this fails, make sure you got rid of
#the extra index column


assert title_basics.shape[1] == 6



#These should be the columns


assert list(title_basics.columns) == [
    "tconst",
    "primary_title",
    "original_title",
    "start_year",
    "runtime_minutes",
    "genres",
]


# Perform Data Cleaning

1.Write a code that displays how many null values we have in the title_basics DataFrame



2.Assert the number of null values


assert null_values0 == 37168, "Expected 37168 null values, but found {}".format(null_values0)
      
      
      
3.Write a code that shows if we have duplicates in the title_basics DataFrame      




4.Drop the rows with null values in the columns original_title,runtime_minutes and genre




5.Convert start year to datetime object


### Analyzing Distribution of Genres in the dataset  


Extract and split the genres,Loop through the genre_data and add individual genres to the all_genres list,Create a DataFrame of Genre counts,Create a bar plot to visualize the distribution of genres,Print the top 10 most common genres.




### Analyzing the mean runtime minutes by genre

Find summary statistics of runtime,Split genres into separate rows,Merge genre_df with title_basics,Get the mean runtime_minutes by genre
Create a bar plot of mean runtime_minutes by genre.



### Answering the first Question

Based on the analysis of genre distruibution in the movie dataset we see that Documentary,Drama,Comedy,Thriller and horror

have the highest number of movies,Microsoft should consider investing in creating films in these genres.



Based on the analysis of the mean runtimes by genres we see that most of these genres have a runtime of 80-100

minutes,Microsoft should consider in investing in films that have a runtime of 80-100 minutes.



### 2.Load the data

Load the data on imdb.title.ratings.csv, Write a code that displays a summary of , providing useful information about its structure and contents,Merge the 'title_ratings' and 'title_basics' DataFrames on 'tconst',Drop rows with missing values in 'runtime_minutes' and 'genres' columns.




### Analyzing the most popular and profitable genres to invest in.


Find the top 5 most popular genre (The ascending parameter to False is used to sort data in descending order.),create a DataFrame named liked_genre by grouping the numvotes column  by the genres column.Create a bar plot of the top genre against the number of votes.Creates a DataFrame named liked_genre1 by grouping the averagerating column  by the genres column(the iloc method is used to select the top 15 rows of the sorted DataFrame). Create a bar plot of the top genre against averagerating.



### Answering the second question


The top 3 most popular genres combination according to the number of votes are: (Action,Fantasy,War), (Action,Adventure,SciFi) and (Adventure,Mystery, SciFi).


The top three genre combinations with the highest ratings are :(Comedy,Documentary,Fantasy),(Documentary,Family,Medical),(History,Sport)




Microsoft should should consider creating films that combine elements from these genres.By creating films that combine elements

from popular genres ,Microsoft can appeal to a wide audience and increase their chances of success at the Box office .For

example they could create an action-adventure film that has elements of fantasy.




### 3.Load the data


Load the content on bom.movie_gross.csv,Write a code that displays a summary of , providing useful information about its structure and contents,Write a code to  generate descriptive statistics of the dataframe.



### Perform Data cleaning

Check for null values,Drop any rows with missing values,Convert the domestic_gross column to integer datatype, Convert the 'year' column to a datetime datatype, Remove non-numeric characters (e.g., commas) from 'foreign_gross' column,Convert the cleaned strings to integer values,
Convert the foreign_gross column to integer datatype,Drop any rows with missing or invalid values again.


### Analyzing studios with the highest average total gross.


Create a new column "total_gross" in the movie_gross1 that adds the domestic_gross and foreign_gross columns,Check to see if the new column was added,Write a  code that calculates the mean total_gross revenue for each movie studio in the movie_gross DataFrame.Create the movie_gross1_grouping into a new data frame.Sort the groups by ascending domestic gross,Create a bar plot of the top 10 studios by  total_gross.



### Answering the third question

From the graph above, HC and P/DW are the top 2 studios with the highest average total gross.


-Also, Par. and Uni. are the bottom 2 studios with the lowest average total gross hence the least market share.


-Microsoft should consider partnering with HC and P/DW to create high grossing films.By partnering with them ,Microsoft can

leverage their expertise in creating successful films that appeal to a wide audience increasing their success at the box

office.



### 4.Load the data


Load the data on imdb.title.ratings.csv and write a code that displays a summary of , providing useful information about its structure and contents.   



### Perform Data Cleaning


Convert 'production_budget' to numeric data type,Convert 'domestic_gross' to numeric data type,Convert 'foreign_gross' to numeric data type.



### Analyzing the relationship between total gross profit and the production budget.

Calculate domestic gross profit for each movie,Calculate worldwide gross profit for each movie,Calculate total gross profit for each movie,Check for the new columns.Find the correlation between 'production_budget' and 'total_gross_profit',Create the scatter plot.




### Answering the fourth question

Microsoft should consider investing in high budget films.There is a moderate positive correlation between production budget

and total gross profit which suggests that in general as the production budget increases ,gross profit also tends to increase.

However, it is important to note that there is still a variability in the data and other factors might influence the

relationship.




### Summary


From the above analysis of the four business problems, Microsoft may create a film production company that

successfully competeswith current studios and creates engaging material for audiences by investing in high

budget films, partnering with HC and P/DW to create high grossing films,consider creating films that combine

elements from the most popular genres,consider in investing in films that have a runtime of 80-100 minutes.







Aside from the analysis other recommendations i would give to Microsoft new movie studio include creating movies

with strong character development with high quality content.Microsoft should consider partnering with well known

directors and actors to help bring their movies to life and create a distinct brand and strategy.



