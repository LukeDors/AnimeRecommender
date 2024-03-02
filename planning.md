# Anime Recommender Plan

## Step 1: Data Collection

First, I will be collecting my data using the MyAnimeList API as well as the unofficial MAL API, Jikan.

I will use Jikan for much of the process, but only the official API allows for obtaining user watch lists, which contains their scores for completed anime

To begin, I need the data from thousands of users. I am beginning at a couple of starting points, which are a couple of randomly selected users from reviews of popular anime. This ensures the least possible chance for bias. From these 3-4 users, I will get their friend lists, and then repeat the process with all of the users on their friend lists. Eventually, I will end up with the data from thousands of users.

I will format the data as following: Each user/show combination will be a unique row.



**example**: $user | show | rating$


I will be adding additional columns as well to increase the likelihood of a user enjoying a series. These may include the genres, the producing company, or the animation studio.

## Step 2 Data Cleaning for NN usage

I will remove any instances of null values in the ratings section. In addtion, I will remove any users with 0 ratings, and users with nearly 0 ratings.

Next I will create columns for each genre

Finally, I will create train and test sets for my data

### NN version 1

execute code as seen in https://github.com/mdipietro09/DataScience_ArtificialIntelligence_Utils/blob/master/machine_learning/example_recommendation.ipynb and adapt as needed

this will be the primary usage NN

### NN version 2

wide and deep / dlrm

### NN version 3

graphing NN

## Step 3 Clustering

The data will be organized with each user being a row, and the columns being various variables to be organized into clusters with. This will be done in 2 ways:
* columns with binary variables for genres
* columns for binary variables for different anime

-------

this will then be graphed as a network graph using NetworkX