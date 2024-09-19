# Movie Recommender System

This repository contains a Movie Recommender System built using Streamlit, pandas, and scikit-learn. The system recommends movies based on a selected movie and displays the posters of the recommended movies.

## Features

- Recommends top 5 similar movies based on the input movie.
- Displays posters of the recommended movies.
- Utilizes cosine similarity for recommendation.
- Data processing and feature extraction using pandas and scikit-learn.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/movie-recommender-system.git
   cd movie-recommender-system
   ```

2. Install required dependencies
  ```pip install -r requirements.txt```

3. Download the dataset and place it in the repository:
- tmdb_5000_movies.csv
- tmdb_5000_credits.csv

## Usage
1. Run the Jupyter Notebook to preprocess the data and generate the necessary pickle files:
```bash
jupyter notebook movie_recommender.ipynb
```

2. Run the Streamlit app:
```bash
streamlit run app.py
```

3. Open your browser and go to http://localhost:8501 to access the Movie Recommender System.

## Data Preprocessing (movie_recommender.ipynb)
The Jupyter Notebook performs the following steps:

1. Load and merge the datasets.
2. Select relevant features.
3. Preprocess the data (handle missing values, convert genres, keywords, cast, and crew to lists).
4. Create a tags column by combining the overview, genres, keywords, cast, and crew.
5. Convert tags to lowercase and apply stemming.
6. Create a count matrix using CountVectorizer.
7. Compute cosine similarity between movie vectors.
8. Save the processed data and similarity matrix using pickle.
