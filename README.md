# Movie-Recommender-Streamlit
movie-recommender-streamlit is a content-based movie recommendation web app built with Streamlit that suggests similar movies based on a movie selected by the user. It uses preprocessed movie metadata and a similarity matrix to return the top recommended titles in an interactive UI


# Movie Recommendation System

This project is a **Movie Recommendation System** that suggests movies similar to a movie selected by the user. It uses content-based filtering to recommend titles based on movie metadata such as genres, keywords, cast, and overview. The goal is to provide personalized movie suggestions in a simple and interactive way.


## How it works

- The system is built using content-based filtering. For each movie, important features like genres, keywords, cast, crew, and overview are combined into a single text representation.
- Natural Language Processing (NLP) techniques are applied to convert this text into numerical feature vectors (for example using CountVectorizer or TF-IDF).  
- A similarity matrix is computed between all movie vectors (using cosine similarity), and stored in `similarity.pkl` for fast lookup during recommendations.  
- When the user selects a movie, the system finds the most similar movies from the similarity matrix and returns the top N recommendations.

## Similarity Matrix File

This project uses a precomputed **similarity matrix** stored in `similarity.pkl`.  
It contains the pairwise similarity scores between movies, computed using content-based features such as genres, keywords, cast, and overview text.

You can download the `similarity.pkl` file from the link below and place it in the project root directory:

👉 [Download similarity.pkl](https://drive.google.com/file/d/13IH2o72s6kX_PzZZWyVBsAXqb9nikHU5/view?usp=drive_link)



## Dataset

- The project uses a publicly available movie dataset (such as the TMDB 5000 Movies dataset), which contains movie titles, genres, overviews, cast, crew and other metadata.  
- The raw data is preprocessed to keep only the relevant columns and to clean and normalize the text fields before building the recommendation model.


## Technologies Used

- **Python** for data processing and model building.  
- **Pandas** and **NumPy** for data manipulation and numerical operations.
- **scikit-learn** for vectorization (CountVectorizer / TF-IDF) and cosine similarity calculation. 
- **Streamlit**  for building the web interface of the recommender. 
- **Pickle** to save the processed movie data and similarity matrix (`movies.pkl`, `similarity.pkl`).


## Features

- Search for a movie by name from a dropdown or input box.  
- Get a list of similar movies based on content similarity.  
- Display additional information like poster, release year, rating and overview for each recommended movie using TMDB API or dataset fields.

## How to Run

1. Clone this repository.  
2. Install the required packages:

pip install -r requirements.txt


3. Download `similarity.pkl` and place them in the project root:
similarity.pkl
movies.pkl
app.py / main.py


4. Run the application (example for Streamlit):

streamlit run app.py



5. Open the local URL shown in the terminal and start exploring movie recommendations.



Make sure that `similarity.pkl` is in the same folder as `app.py` / `main.py` before running the application.
