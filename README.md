# MovieRecommendationSystem
This repository hosts a content-based movie recommendation system developed using Python and core data science libraries. The system is designed to provide movie recommendations by analyzing metadata associated with film titles.

# Project Overview
The core objective of this project is to implement an effective content-based filtering algorithm. This approach recommends movies by identifying similarities between a target movie and all other films in the dataset, primarily based on shared features such as genre, keywords, cast, and crew.
The entire process, from data acquisition and cleaning to model development and testing, is contained within the included Jupyter Notebook: Movie_Recommendation.ipynb.

# Methodology
The recommendation algorithm is structured around the following key phases:Data Acquisition and Preparation: Relevant datasets (e.g., movie metadata and credits) are imported, merged, and preprocessed. This involves cleaning data, handling missing values, and extracting the most informative features (e.g., primary cast members, top crew, genres).Feature Engineering: The selected text-based metadata fields are consolidated into a single string per movie. Text is normalized (e.g., converted to lowercase, spaces removed) to prepare for vectorization.Content Vectorization (TF-IDF): The combined text features are transformed into a matrix of TF-IDF (Term Frequency-Inverse Document Frequency) vectors. This method weights words based on their frequency in a movie's description relative to their frequency across the entire corpus.Similarity Calculation: The cosine similarity is computed between every pair of movie vectors in the TF-IDF matrix. Cosine similarity is a highly effective metric for determining the angular distance between vectors in high-dimensional space, yielding a similarity score between 0 and 1.

# Recommendation Generation:
Upon receiving a target movie title, the system identifies its corresponding vector index, retrieves the similarity scores from the matrix, and returns the top $N$ movies with the highest similarity scores as recommendations.

