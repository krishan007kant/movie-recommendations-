# movie-recommendations- system 

This project implements a content-based movie recommendation system using Python

data set link -->https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata

Overview
This project aims to develop a movie recommendation system using cosine similarity based on movie descriptions, genres, keywords, cast, and crew.

Implementation Steps

Data Collection:

The project utilizes two datasets: tmdb_5000_movies.csv and tmdb_5000_credits.csv, obtained from TMDb, which contain information about movies, including their titles, overviews, genres, keywords, cast, and crew.

Data Preprocessing:

Merged the two datasets based on movie titles to create a comprehensive movie dataset.
Removed irrelevant columns and handled missing values.
Converted string representations of lists into actual lists using ast.literal_eval().
Processed text data by removing spaces, converting to lowercase, and applying Porter stemming algorithm to remove suffixes.

Feature Engineering:

Extracted relevant features from the dataset to build movie profiles, including descriptions, genres, keywords, cast, and crew.
Concatenated these features to create movie tags for each movie.

Vectorization:

Used CountVectorizer to transform the textual movie tags into numerical vectors.
Applied cosine similarity to compute similarity scores between movies based on their tags.
Recommendation Function:

Developed a function to recommend similar movies based on a given movie title.
Implemented the recommendation function using cosine similarity scores to find the most similar movies to the input movie.
Future Scope
Incorporate more advanced techniques such as collaborative filtering or matrix factorization to enhance recommendation accuracy.
Improve the user interface for a more interactive and user-friendly experience.

How to Use
Usage Example
python

recommend('Spider-Man')
recommend('Avatar')
