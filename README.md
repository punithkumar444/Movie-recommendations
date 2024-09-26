# Movie Recommendation System

This repository contains a **Movie Recommendation System** that uses machine learning techniques to recommend movies to users based on their preferences, historical data, and movie attributes. This project is built using Python and multiple datasets, employing collaborative filtering, content-based filtering, and hybrid approaches to provide accurate recommendations.

This is a **Group Project** 
- **Authors** 
- **1**-A.Sree Tharun Raju
- **2**-T.Punith Kumar Naidu
## Project Overview
The **Movie Recommendation System** leverages three different datasets to recommend movies to users. The system is designed to analyze users' viewing habits, ratings, and content features of movies to suggest relevant movies. It supports several recommendation algorithms, including user-based and item-based collaborative filtering, content-based filtering, and hybrid models.

### Key Features
- **Collaborative Filtering**: Based on user-item interaction, either user-user or item-item similarity.
- **Content-Based Filtering**: Recommends movies based on their content features (e.g., genres, actors, directors).
- **Hybrid Model**: Combines both collaborative filtering and content-based filtering for enhanced recommendations.
- **Custom Recommendations**: Allows for personalized movie recommendations based on user profiles.
- **Scalable and Modular Design**: Designed to handle large datasets and allow easy experimentation with different models.

## Datasets

This project uses three datasets for training and evaluation:

1. **MovieLens Dataset**
   - Source: [MovieLens 20M Dataset](https://grouplens.org/datasets/movielens/)
   - Description: The MovieLens dataset contains 20 million ratings for 27,000 movies by 138,000 users. It includes user IDs, movie IDs, ratings (from 1 to 5 stars), and timestamps.
   
   **File Structure**:
   - `movies.csv`: Contains movie information (movie ID, title, genres).
   - `ratings.csv`: Contains user ratings (user ID, movie ID, rating, timestamp).

2. **IMDb Dataset**
   - Source: [IMDb Datasets](https://www.imdb.com/interfaces/)
   - Description: The IMDb dataset provides movie metadata such as genres, actors, directors, and release dates. This dataset is used for the content-based filtering part of the project.
   
   **File Structure**:
   - `title.basics.tsv`: Contains movie titles, genres, and release years.
   - `name.basics.tsv`: Contains actors, directors, and other crew members.
   - `title.principals.tsv`: Links actors, directors, and crew to movies.

3. **The Movies Dataset**
   - Source: [Kaggle - The Movies Dataset](https://www.kaggle.com/rounakbanik/the-movies-dataset)
   - Description: This dataset contains metadata on over 45,000 movies, including cast, crew, plot keywords, budget, and revenue. This dataset helps to refine content-based filtering by including additional movie metadata.
   
   **File Structure**:
   - `movies_metadata.csv`: Contains detailed movie metadata, such as budget, revenue, and release date.
   - `credits.csv`: Contains cast and crew information for each movie.

## Project Architecture

The Movie Recommendation System consists of the following components:

1. **Data Preprocessing**
   - **Cleaning**: Handling missing values, removing duplicates, and normalizing data formats.
   - **Merging Datasets**: Combining data from MovieLens, IMDb, and The Movies Dataset into a unified format.
   - **Feature Engineering**: Extracting meaningful features such as user preferences, movie attributes, and ratings.

2. **Recommendation Algorithms**
   - **Collaborative Filtering**:
     - User-based and item-based collaborative filtering using cosine similarity and matrix factorization (e.g., Singular Value Decomposition - SVD).
   - **Content-Based Filtering**:
     - Using metadata such as genres, keywords, cast, and crew to recommend movies similar to what the user has already liked.
   - **Hybrid Approach**:
     - A combination of collaborative filtering and content-based filtering to overcome the limitations of each method when used in isolation.

3. **Evaluation Metrics**
   - **Root Mean Squared Error (RMSE)**: Used to measure the accuracy of predicted ratings compared to actual ratings.
   - **Precision, Recall, and F1 Score**: Used to evaluate the performance of the recommendation system, especially for binary relevance tasks.
   - **Mean Average Precision (MAP)**: Evaluates the relevance of the ranked recommendations.

## Installation

To set up the project locally, follow these steps:

### Prerequisites

- **Python 3.x**: Ensure you have Python installed. You can download it from [here](https://www.python.org/downloads/).
- **Required Libraries**:
  - `numpy`
  - `pandas`
  - `scikit-learn`
  - `surprise` (for collaborative filtering)
  - `tensorflow` (optional, if neural network-based recommendation is implemented)

### Setup

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/movie_recommendation_system.git
