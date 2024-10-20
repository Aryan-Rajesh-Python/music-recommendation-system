# Music Recommendation System

## Overview

The **Music Recommendation System** leverages a dataset of Spotify lyrics to recommend songs based on lyrical similarities. Utilizing natural language processing (NLP) techniques and machine learning algorithms, this project aims to provide users with personalized song suggestions based on their preferences.

## Key Components

### Data Collection and Preprocessing
- Imported a dataset containing song information, including artist, song title, and lyrics.
- Cleaned the data by removing unnecessary columns and handling inconsistencies in the lyrics.
- Standardized the text by transforming lyrics to lowercase and eliminating special characters.

### Text Processing
- Utilized the **NLTK** library for natural language processing tasks, including tokenization and stemming.
- Implemented a custom tokenization function to reduce words to their base forms, enhancing similarity calculations.

### Feature Extraction
- Employed **TF-IDF (Term Frequency-Inverse Document Frequency)** vectorization to convert cleaned lyrics into a numerical format suitable for analysis.
- Limited the feature space to the top 5,000 terms to improve computational efficiency.

### Similarity Calculation
- Applied **cosine similarity** to compute the similarity between songs based on their TF-IDF vectors, resulting in a similarity matrix.
- This matrix enables the identification of songs with similar lyrical content.

### Recommendation Function
- Developed a function to retrieve song recommendations based on user input, returning the top 20 songs most similar to the input song.

### Persistence
- Used **Pickle** to save the similarity matrix and DataFrame for future use, ensuring efficient loading and quick access to the recommendation system.

## Technologies Used
- Python
- Pandas
- NLTK
- Scikit-Learn
- Pickle

## How to Use

Steps to run this application:
   ```bash
   
   git clone https://github.com/yourusername/music-recommendation-system.git
   cd music-recommendation-system
   pip install -r requirements.txt
   python recommendation.py
