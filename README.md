# Movie Recommendation System

A simple content-based movie recommendation project built in Jupyter Notebook. The system recommends movies similar to a selected movie by comparing movie information such as keywords, cast, genres, and director.

## Project Files

- `MovieRecommendation.ipynb` - main notebook containing the recommendation system code
- `movie_dataset.csv` - movie dataset used for recommendations

## Project Overview

This project uses a content-based filtering approach. Instead of using user ratings, it compares movies based on their textual features.

The selected features are:

- `keywords`
- `cast`
- `genres`
- `director`

These features are combined into one text column, converted into numeric form using `CountVectorizer`, and then compared using cosine similarity.

## How It Works

1. Import required libraries such as `pandas`, `numpy`, `CountVectorizer`, and `cosine_similarity`.
2. Load the movie dataset.
3. Select important text features from the dataset.
4. Fill missing values with empty strings.
5. Combine selected features into one column called `combined_features`.
6. Convert text data into a numeric count matrix using `CountVectorizer`.
7. Calculate similarity between movies using cosine similarity.
8. Select a movie, such as `Avatar`.
9. Sort all movies by similarity score.
10. Print the most similar movie recommendations.

## Example Output

For the movie:

```text
Avatar
```

The notebook recommends movies such as:

```text
Guardians of the Galaxy
Aliens
Star Wars: Clone Wars: Volume 1
Star Trek Into Darkness
Star Trek Beyond
Alien
```

These movies are recommended because their combined features are most similar to `Avatar`.

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Jupyter Notebook

## Installation

Install the required Python libraries:

```bash
pip install pandas numpy scikit-learn notebook
```

## How To Run

1. Clone this repository or download the project files.
2. Open `MovieRecommendation.ipynb` in Jupyter Notebook or VS Code.
3. Run all cells from top to bottom.
4. Change the movie name in this line to get recommendations for another movie:

```python
movie_user_likes = "Avatar"
```

Example:

```python
movie_user_likes = "The Dark Knight"
```

## Dataset

The notebook loads the dataset from this URL:

```text
https://raw.githubusercontent.com/rashida048/Some-NLP-Projects/master/movie_dataset.csv
```

A local copy named `movie_dataset.csv` is also included in the project folder.

## Future Improvements

- Add a user input option for entering any movie name.
- Show similarity scores with the recommended movies.
- Build a simple web app using Flask or Streamlit.
- Improve recommendations by adding more features such as overview, production company, or ratings.

## Conclusion

This project demonstrates how content-based recommendation systems work using text processing and cosine similarity. It is a beginner-friendly project for learning recommendation systems in Python.
