# A Comparative Analysis of Movie Ratings by IMDb and Rotten Tomatoes

To view the interactive plots you can check the python notebook at - 
[NB Viewer Jupyter Notebook](http://nbviewer.jupyter.org/github/palakbhatia/IMDB_VS_Rotten_Tomatoes-A_Comparison/blob/fd477949e6681e86aece97dc4582fb1e8d03e13b/Notebook/RT%20vs%20IMDB%20v3.ipynb)

## Overview
Do you always look at the rating of a movie before watching it? Has it ever happened to you that you wait for a movie to release but after the release you check out the ratings and end up not watching it? What is your favourite go to movie ratings website? 

If the answers to all the above questions is a "Yes", this is the project for you. If you would always check either IMDb or Rotten Tomatoes for the movie ratings and the decision to watch a particular movie relied heavily on that, this project is an attempt to help you understand, how much should you trust the ratings, and which one between IMDB and Rotten Tomatoes should you use more often to get the ratings. 

## Getting Started
In this Github, the directory "Notebook" contains the .ipnyb file with details of data reading, cleaning and various analysis. Alternatively, a link for the interactive NBViewer file for the same has also been added at the top of the readme. Corresponding dataset has also been added to the directory "Data". 

## Prerequisites/Tech Stack
* Python 3.1
* Pandas 0.23.0
* Plotly 3.0.0
* Seaborn 0.8.1
* Matplotlib 

## Dataset Background
For a particular movie, the dataset contains
* Imdb score
* Rotten Tomatoes Score
* Scorer (For Rotten Tomatoes Score)
* Release Year
* Time Period(5 Years period) <br>
Data related to the highest grossing movies of the past 10 years has been fetched from this [Wikipedia Page](https://en.wikipedia.org/wiki/List_of_highest-grossing_films) <br>

## IMDb vs Rotten Tomatoes Ratings Comparison - A time trend
The first step was to view how the means of the two ratings' websites vary over time. For this analysis, IMDb and Rotten Tomatoes scores are first visualised as a boxplot, to check the distributions. After that the mean scores of IMDb and Rotten Tomatoes over the years are plotted as a line plot. The x-axis on the plot contains the time period values in years and the y-axis shows the mean scores/ratings. The interactivity of the plot has been implemented using plotly. Hovering over a particular year, the mean IMDb & rotten tomatoes ratings becomes visible. 
![alt text][time-trend]

[time-trend]: https://raw.githubusercontent.com/palakbhatia/IMDB_VS_Rotten_Tomatoes-A_Comparison/master/Charts/mean%20scores%20comparison.PNG "IMDb vs Rotten Tomatoes Mean Scores Comparison over Time"

Rotten Tomatoes ratings mean has always been lower than the IMDb ratings mean. Is this the result of IMDb always giving higher scores, or is it because Rotten Tomatoes always gives lower scores? 

So, another analysis was done to compare the maximum and minimum scores for both over the years. Two different dynamically interactive plots, each for maximum scores comparison and for minimum scores comparison are created for this purpose. Hoveing over the particular year, the minimum or maximum values for both IMDb and Rotten Totamoes ratings becomes visible. The link below is for the line graph for the maximum values for both IMDb and Rotten Tomatoes
![alt text][minimum-maximum]

[minimum-maximum]: https://raw.githubusercontent.com/palakbhatia/IMDB_VS_Rotten_Tomatoes-A_Comparison/master/Charts/maximum%20scores%20comparison.PNG "IMDb vs Rotten Tomatoes Maximum Scores Over the Years"

Rotten Tomatoes always has a maximum greater than IMDb ratings and minimum lower than IMDb. On further analysis, it was found that there are a total of 140 movies with a rotten tomatoes score of either 0 or 100, and all of these scores have been given by the critics. Audiences do not generally score the movies to the extreme, whereas, the critics do not hold back in giving a 0 if the movie is bad. 
Another conclusion from here can be that IMDb ratings is more close to how the audiences percieve a movie, and maybe the rotten tomatoes movie give a crtics' perspective for a movie. 

## Are the genre(s) of top rated movies same as the genre(s) of worldwide top grossing( in terms of earnings) movies? 
![alt text][top-grossing-movies-genre]

[top-grossing-movies-genre]: https://raw.githubusercontent.com/palakbhatia/IMDB_VS_Rotten_Tomatoes-A_Comparison/master/Charts/Highest%20grossing%20genre.PNG "Top Grossing Movies Genre(s) in the past 10 Years"

This horizontal bar chart is a seaborn countplot, which depicts the number of movies in a genre(s) that were the top grossing movies in the past 10 years. The x-axis depicts the count of movies in the genre(s) and the y-axis shows the genre(s) name. The genre(s) with the most movies as the highest grossing for a year is "Action,Adventure,Fantasy", including the movies like 
- Pirates of the Caribbean
- Avatar
- Star Wars

![alt text][top-rated genre]

[top-rated genre]: https://raw.githubusercontent.com/palakbhatia/IMDB_VS_Rotten_Tomatoes-A_Comparison/master/Charts/Rotten%20tomatoes%20top%20rated%20genre.PNG "Top Rotten Tomatoes Rated Genre(s) in the past 10 Years"

On the other hand, the top rated rotten tomatoes movies genre(s) are not the same as the top grossing. Have you heard about the movies Sound City(2013), Wild Bill(2011) or LOL(2012)? These were a few of the top rated movies in the past decade. Is it again because the critically acclaimed movies are not really what the audiences prefer? <br>
- Has IMDb ranked the same genre(s) as the highest grossing genre(s) highest over the years? 
- Has IMDb ranked the same movies as the highest grossing movies highest over the years? <br>

All of these unanswered analysis have been added to the jupyter notebook. Visit [NB Viewer Jupyter Notebook] (http://nbviewer.jupyter.org/github/palakbhatia/IMDB_VS_Rotten_Tomatoes-A_Comparison/blob/fd477949e6681e86aece97dc4582fb1e8d03e13b/Notebook/RT%20vs%20IMDB%20v3.ipynb) to view the interactive plots.
