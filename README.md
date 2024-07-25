# Movie-Recommendation-System
This project implements a movie recommendation system using collaborative filtering based on user-item interactions. The main steps include loading and preprocessing data, encoding genres, splitting data into train and test sets, creating a user-item matrix, and calculating item similarity. The system recommends movies based on cosine similarity of user ratings.

Files:

ratings.csv: Contains user ratings for movies.

movies.csv: Contains movie information including titles and genres.

Setup:

1.Load Data in Chunks-
Load the ratings data in chunks to handle large datasets efficiently.

2.Merge and Preprocess Data-
Merge the ratings and movies datasets on the movieId column. Strip any leading or trailing spaces from the movie titles and convert genres into a list of genres. Encode the genres using one-hot encoding and drop the original genres column.

3.Split Data-
Split the merged dataset into training and testing sets to evaluate the model's performance.

4.Create User-Item Matrix-
Create a user-item matrix where rows represent users, columns represent movies, and values represent the ratings given by users to movies. Fill any missing values with zero.

5.Calculate Item Similarity-
Compute the cosine similarity between items (movies) based on the user-item matrix. This helps in finding similar movies based on user ratings.

6.Movie Recommendation Function-
Implement a function to recommend movies based on the input movie title. The function finds the index of the input movie, retrieves similar movies based on item similarity, and returns the top N recommended movies.

Usage:

Run the script in a Python environment with the necessary libraries installed (pandas, scikit-learn).

Libraries:

1.pandas

2.scikit-learn
