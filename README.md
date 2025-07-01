# Movie Recommendation System

This project is a simple content-based movie recommendation system built using Python and scikit-learn. It recommends movies based on their genres and overviews.

## Features

- Loads movie data from a CSV file.
- Combines genre and overview information for each movie.
- Uses CountVectorizer to convert text data into feature vectors.
- Calculates cosine similarity between movies.
- Recommends top 5 similar movies for a given title.

## How It Works

1. **Data Preparation:**  
   The system reads a dataset (`dataset.csv`) containing movie information such as `id`, `title`, `genre`, and `overview`.

2. **Feature Engineering:**  
   It combines the `genre` and `overview` columns into a single string for each movie to create a new feature called `pointers`.

3. **Vectorization:**  
   The combined text is vectorized using `CountVectorizer` with English stop words removed.

4. **Similarity Calculation:**  
   Cosine similarity is computed between all movie vectors.

5. **Recommendation:**  
   Given a movie title, the system finds the most similar movies based on the computed similarity scores.

## Usage

1. Place your `dataset.csv` file in the project directory.
2. Open and run the `movie_recommendation_system.ipynb` notebook.
3. Use the `recommend('Movie Title')` function to get recommendations.

## Example

```python
recommend('Iron Man')
```

## Requirements

1. Python 3.x
2. pandas
3. numpy
4. scikit-learn

Install dependencies with:

```bash
pip install pandas numpy scikit-learn
```
