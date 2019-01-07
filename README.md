# Personal_Movie_Recommender

In this project I conducted movie recommendation among students under the instruction of Professor Dennis Zhang:
1. recommended the most popular movie to the specific student that he/she hasn't watched yet.

2. recommended the favoriate movie of the specific student's movie soul mate(based on calculated jaccard similarity) that the specific person hasn't watched yet.


## Recommender System

The objective of a Recommender System is to recommend relevant items for users, based on their preference. Recommender system is prevalent in the digital space. For example, when you go shopping on Amazon, you will notice that Amazon is recommending products on the front page before you even type anything in the search box. Similarly, when you go on YouTube, the top bar of Youtube is typically "videos recommended to you." All these features are based on recommmender system. 

What item to recommend to which user is arguably the most important business decision in many digital platforms. For instance, YouTube cannot control which videos that users upload to it. It cannot control which videos users like to watch. Moreoveor, since watching videos is free, YouTube cannot change the price of its items. It does not have inventory either since each video can be viewed as many times as possible. In this case, what could YouTube control? Or in other words, what differentiates a good video streaming service from a bad one? The answer is recommender system. 

## Types of Recommender Systems

There are **three** types of recommender system. **In this bonus project, we will implement the first one.**

### Popularity-based Recommendation 

The most obvious system is popularity-based recommendation. In this case, this model recommends to a user the most popular items that the user has not previously consumed. In the movie setting, we will recommend the movie that most users have liked and consumed. In other words, this system utilizes the "widom of the crowds." It usually provides good recommendations for most of the people. Since it is easy to implement, people normally use popularity-based recommendation as a baseline. *Note: this system is not personalized. If both consumers did not watch Movie A and Movie A is the most popular one, both of them will be recommended Movie A.*

### Content-based Recommendation 

This recommender system leverages the data of one customer's historical actions. This recommender systems first utilizes a set of features to describe an item (for example, for movies, we can use the movie's director, main actor, main actress, genre, etc. to describe the movie). When a user comes in, the system will recommend the movies that are closest to the movie that the users have consumed and liked before in terms of the features. For instance, if a user likes action move from Nolan the most, this system will recommend another action movie from Nolan that this user has not consumed. *Note: we will not implement this system in this bonus project since it requires knowledge about supervised learning. We will come back to this topic at the end of this semester.*

### Collaborative Filtering Recommendation

The last type of recommender system is called collaborative filtering. This approach uses the memory of previous users interactions to compute users similarities based on items they've interacted (user-based approach) or compute items similarities based on the users that have interacted with them (item-based approach).

A typical example of this approach is User Neighbourhood-based CF, in which the top-N similar users (usually computed using Pearson correlation) for a user are selected and used to recommend items those similar users liked, but the current user have not interacted yet. 
