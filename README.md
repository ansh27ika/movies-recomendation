## movies recommendation system 


>>project idea : Recommendation systems are everywhere, be it an online purchasing app, movie streaming app or music streaming.
They all recommend products based on their targeted customers.

Have you ever been on an online streaming platform like Netflix, Amazon Prime, Voot? 
I watched a movie and after some time, that platform started recommending me different movies and TV shows.
I wondered, how the movie streaming platform could suggest me content that appealed to me. 
Then I came across something known as Recommendation System.
This system is capable of learning my watching patterns and providing me with relevant suggestions.

>>main goal: of this machine learning project is to build a recommendation engine that recommends movies to users


>>What is a Recommendation System?

A recommendation system provides suggestions to the users through a filtering process 
that is based on user preferences and browsing history.
The information about the user is taken as an input.
A recommendation system is a platform that provides 
its users with various contents based on their preferences and likings. 


>>DATASET

In order to build our recommendation system, 
we have used the dataset  Movies.csv file from kaggle  

>>Importing Essential Libraries

import pandas as pd
import numpy as np 
import difflib
from sklearn.feature_extraction.text import TfidfVectorizer
from sklearn.metrics.pairwise import cosine_similarity


>>defining the libraries 

1.pandas read and write the files used in model 
2.numpy used for read data in numpy arrays for manipulatiion purposes.
3.difflib is used for allow users to compare data sets
4. The sklearn. feature_extraction module can be used to extract features in a
format supported by machine learning algorithms from datasets consisting of formats such as text and image.
5.metrics.pairwise  Compute cosine similarity between samples in X and Y


>>columns in dataset(5 rows × 24 columns) 
1.  index : is serial number 
2.  budget : telling the total budget of the movie 
3.  genres : showing theme of the movie 
4.  homepage: the official site where we can watch the movie 
5.  id: every movie has unique id 
6.  keywords: giving the idea of the movie 
7.  original_language: 
8.  original_title:
9.  overwiew: general description or plot of the movie 
10. popularity: if popularity score is high then it means that the movie is very popular or vice a versa 
11. production_comapnies: telling which box house produced the movie 
12. production_countries:  
13. runtime	
14. spoken_language : language spoken by star cast 
15. status: showing realsed or not 	
16. tagline: each movie has its own tag lines called punch lines 
17. vote_average	
18. vote_count	
19. cast:  name of star cast actors , co actors etc	
20. crew: name of the movie makers 	
21. director: name of director who directs the movie 
22. revenue:
23. release date: 
24. title:


>>Similarity Score : How does it decide which item is most similar to the item user likes? Here we use the similarity scores.

It is a numerical value ranges between zero to one which helps to determine how much two items are similar to each other on a scale of zero to one. 
This similarity score is obtained measuring the similarity between the text details of both of the items. 
So, similarity score is the measure of similarity between given text details of two items. 
This can be done by cosine-similarity.

>>How Cosine Similarity works?
Cosine similarity is a metric used to measure how similar the documents are irrespective of their size.
Mathematically, it measures the cosine of the angle between two vectors projected in a multi-dimensional space.
The cosine similarity is advantageous because even if the two similar documents are far apart by the Euclidean distance (due to the size of the document), 
chances are they may still be oriented closer together. The smaller the angle, higher the cosine similarity.
>>observation 
>>on checking distribution of data: 
1. BUDGET 
we can clearly see that it is a right skewed data with its tail in the +ve side of the distribution.I.E most of the movies having budget more than 0 X 10^-8.
2. VOTE COUNT:
we can clearly see that it is a right skewed data with its tail in the +ve side of the distribution.I.E most of the movies having vote count between 0 to 2000 or above.
3.POPULARITY: 
we can clearly see that it is a right skewed data with its tail in the +ve side of the distribution.I.E most of the movies  having popularity between 0 to 200 or above 

	




