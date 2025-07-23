# 🎬 IMDb Movie Recommender System

Welcome to the **Movie Recommender System** project based on the TMDB 5000 dataset. This system suggests similar movies to the one you input using metadata like genre, cast, director, and keywords.

---
<p float="left"> <img src="https://i.pinimg.com/736x/87/ce/f0/87cef0375e611123a7a53f157b2cf196.jpg" width="200"/>
  <img src="https://i.pinimg.com/736x/96/0e/a6/960ea61c1e824f8c98055cf8f4efaf85.jpg" width="200"/>
  <img src="https://i.pinimg.com/1200x/e3/c5/35/e3c535ac3bb37e216ebad126f578a6ff.jpg" width="200"/> 
  <img src="https://i.pinimg.com/1200x/05/a9/95/05a9951138f51d653a00b27423c4b7e4.jpg" width="200"/> </p>
## 📌 Project Objective

To build a **content-based movie recommendation engine** using NLP techniques and cosine similarity.

---

## 📁 Dataset

We used the **TMDB 5000 Movie Dataset** available on Kaggle. It consists of:
- `tmdb_5000_movies.csv`
- `tmdb_5000_credits.csv`

> You can download it [here](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)

---

## 🧠 How It Works

We extract and clean features from both datasets, focusing on:
- Genres
- Keywords
- Cast (top 3 actors)
- Director
- Movie overview

We then combine all of them into a single `tags` column. These tags are vectorized and compared using **cosine similarity** to recommend similar movies.

---

## 🧮 Formula Used

### 📘 Cosine Similarity:

We calculate the similarity between two movies A and B as:

Where:
- `A · B` is the dot product of vectors
- `||A||` is the magnitude of vector A
- `||B||` is the magnitude of vector B

This helps us find how close two movies are based on their text features.

---

## 🔧 Libraries Used
pandas 

numpy 

ast

 pickle

## CLASS AND FUNTION

CountVectorizer

Cosine_similarity

## 🏗️ Steps to Build
Load and merge movies and credits datasets.

Extract important features: cast, crew, overview, genres, keywords.

Use ast.literal_eval to convert stringified lists to Python lists.

Keep top 3 actors and the director.

Combine all into a tags column.

Convert text into vectors using CountVectorizer.

Compute cosine similarity matrix.

Use this similarity matrix to recommend 5 similar movies.

## 💾 Output Files
After preprocessing and computing similarity, we save:

movie_list.pkl — contains all movie data

similarity.pkl — contains similarity matrix

These files can be used for deployment or future use without re-processing.
