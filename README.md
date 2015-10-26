# Neo4J_MovieRecommendation

Movie Recommendation System using Neo4J and MySQL

For this project, you will use the data from the MovieLens dataset to develop a movie recommendation system in Neo4J and MySQL and compare the performance. You will use two different criteria to generate recommendations. This project will be done in two parts.
Two Parts

Part 1 (Neo4J)

You will model the dataset as a graph and use Neo4J to build the recommendation system. Neo4J will be used as an embedded database in a Java application. You will parse the input data and store it in a graph form in Neo4J. Write a separate Java program, called CreateNeo4JDB.java to do this (the database folder may be created inside Project5 folder, alongside dataset, src, and lib). You are free to choose your data model, but make sure to explain it in the project report. You will then execute the two algorithms described below on the created database to generate movie recommendations. Name your program Neo4JRecommend.java.
Part 2 (MySQL)

You will use the same data and build the recommendation engine using MySQL and Java. Provide a SQL script file, called schema.sql, that contains create table statements to create the relational database and a java program, CreateMySQLDB.java that will load the dataset into the MySQL database. You will use JDBC to connect to the database. Name your program MySQLRecommend.java.
Dataset

The dataset consists of movie ratings provided by a set of individuals for a set of movies. The details of each movie is given in the u.item file. Each movie consists of a release date, a video release date, IMDB url, and belongs to one of the 19 genres given in the u.genre file. The u.user file contains demographic information about the users like age, gender, occupation and zipcode. The movie ratings given by the users along with the timestamp is contained in the u.data file. The included README file has further information.
Ranking Criteria

Suppose we need to generate movie recommendations for user U1. You will use the following algorithms to rank the movies:
Collaborative filtering: Analyze the similarities between user U1 and the other users who had also given high ratings (rating r) to the same movies as U1. Rank the users based on their similarities (age, gender, occupation, zipcode) with U1. Extract top x% of the users and explore the other movies (not rated by U1) rated highly by the users with top similarity to U1. Rank the movies based on the overall ranking and display the top 10 movies as the recommendation list for U1.
Item-based filtering: Analyze the different movies rated highly by U1. Try to find similarities (genre, release date) between them and extract other movies in the database that have similar characteristics. Rank the movies based on the overall rankings and display the top 10 movies
You may ask the user to input the rating (r) that needs to be considered for the collaborative filtering case. Try experimenting with different values. The similarities need not be an exact match. You can assign weights to users based on the number of attributes that match with the target user. A similar approach can be used to rank the movies based on similarities.
