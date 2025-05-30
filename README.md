# CineSycn-Movie-Recommendation-System-Pre-Trained-Model
🎬 CineSync: Hybrid Movie Recommendation System

CineSync is a hybrid movie recommendation system that combines collaborative filtering, content-based filtering, and sentiment analysis of user reviews. It’s designed for use in Google Colab, with user-friendly input for recommending movies by title, genre, or user behavior.
📁 Features

    🎞 Content-Based Filtering: Suggests movies based on similar plot keywords or genre.

    👤 Collaborative Filtering: Recommends based on what similar users liked (using SVD).

    💬 Sentiment Analysis: Converts text reviews into ratings using VADER from NLTK.

    🤖 Fuzzy Matching: Typing a close match like Conjuring will still find The Conjuring.

    💾 Model Persistence: Trained models and similarity matrices are saved via pickle.

🛠 Requirements

Run this in Google Colab and install the following libraries:

!pip install numpy==1.23.5
!pip install --prefer-binary scikit-surprise
!pip install rapidfuzz

📂 Dataset Required

Upload or mount these files:

    movie_metadata.csv — contains movie info with movie_title, plot_keywords, genres, etc.

    data.csv — userId, movieId, rating (collaborative data).

    reviews.txt — reviews in format: userId<TAB>movie_title<TAB>review_text.

Example line for reviews.txt:

1	The Conjuring	It was really scary and enjoyable!

🚀 How to Use

    Open in Google Colab.

    Run all setup and installation cells.

    Mount Google Drive and make sure CSV and TXT files are correctly placed.

    At the end, the system will prompt:

Enter a movie title, genre, or user ID:

You can input:

    A movie title (e.g. Avengers, The Conjuring)

    A genre (e.g. Horror, Action)

    A user ID (e.g. 1) to get collaborative filtering results

After results are shown, it will ask:

Would you like to search again? (yes/no):

📦 Outputs

    cosine_sim.pkl — saved similarity matrix for plot keywords

    collab_model.pkl — trained SVD model

    Recommended movie titles printed in the console

✅ Example

Input: Conjuring
Output: 
Top 10 Recommended Movies:
['The Conjuring', 'Annabelle', 'Insidious', ...]


Notes

    Make sure your dataset titles match what users will type (or use fuzzy matching as included).

    Preprocess your review file for accurate sentiment-derived ratings.
