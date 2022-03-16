# Movies Recommendation System 


## Project Idea :
Recommendation Systems are everywhere, be it an online purchasing app, movie streaming app or music streaming.
They all recommend products based on their targeted customers.

Have you ever been on an online streaming platform like Netflix, Amazon Prime, Voot? 
I watched a movie and after some time, that platform started recommending me different movies and TV shows.
I wondered, how the movie streaming platform could suggest me content that appealed to me. 
Then I came across something known as Recommendation System.
This system is capable of learning my watching patterns and providing me with relevant suggestions.

# Main Goal: 
The goal of this machine learning project is to build a recommendation engine that recommends movies to users


# What is a Recommendation System?

A recommendation system provides suggestions to the users through a filtering process 
that is based on user preferences and browsing history.
The information about the user is taken as an input.
A recommendation system is a platform that provides 
its users with various contents based on their preferences and likings. 


## DATASET

In order to build our recommendation system, 
we have used the dataset  Movies.csv file from kaggle  

## Importing Essential Libraries

import pandas as pd
import numpy as np 
import difflib
from sklearn.feature_extraction.text import TfidfVectorizer
from sklearn.metrics.pairwise import cosine_similarity


## Defining the Libraries 

- `pandas` 
- `Numpy`
- `Difflib` 
-  `seaborn`
- `sklearn` 
-  `metrics.pairwise`  


## Columns in dataset(5 rows × 24 columns) 
1.  Index : is serial number 
2.  Budget : telling the total budget of the movie 
3.  Genres : showing theme of the movie 
4.  Homepage: the official site where we can watch the movie 
5.  Id: every movie has unique id 
6.  Keywords: giving the idea of the movie 
7.  Original_language
8.  Original_title
9.  Overwiew: general description or plot of the movie 
10.Popularity: if popularity score is high then it means that the movie is very                    popular or vice a versa 
11. Production_comapnies: telling which box house produced the movie 
12. production_countries  
13. Runtime	: Time duration of movie
14. Spoken_language : language spoken by star cast 
15. Status: showing realsed or not 	
16. Tagline: each movie has its own tag lines called punch lines 
17. Vote_average	
18. Vote_count	
19. Cast:  name of star cast actors , co actors etc	
20. Crew: name of the movie makers 	
21. Director: name of director who directs the movie 
22. Revenue
23. Release date
24. Title
## Similarity Score 
How does it decide which item is most similar to the item user likes? Here we use the similarity scores.

It is a numerical value ranges between zero to one which helps to determine how much two items are similar to each other on a scale of zero to one. 
This similarity score is obtained measuring the similarity between the text details of both of the items. 
So, similarity score is the measure of similarity between given text details of two items. 
This can be done by cosine-similarity.

## How Cosine Similarity works?
Cosine similarity is a metric used to measure how similar the documents are irrespective of their size.
Mathematically, it measures the cosine of the angle between two vectors projected in a multi-dimensional space.
The cosine similarity is advantageous because even if the two similar documents are far apart by the Euclidean distance (due to the size of the document), 
chances are they may still be oriented closer together. The smaller the angle, higher the cosine similarity.

	




