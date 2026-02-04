# README


## Problem

Traditional collaborative filtering recommendation systems rely heavily on historical user–item interactions, making them ineffective for new users with little or no rating data. This project investigates whether a content-based recommendation approach can provide more accurate and diverse movie recommendations in cold-start scenarios. Using the MovieLens dataset, the performance of content-based filtering is compared against collaborative filtering under simulated cold-start conditions.

Collaborative filtering ❌ struggles
Content-based methods   ✔ can still work

## The Process

I'll be implementing two systems
- Collaborative Filtering
- Content-Based Filtering

## How to simlulate "cold start"

For a user
- Keep 0-3 ratings
- Hide the rest
Generate recommendations
Compare against hidden ratings

Inputs
- Movie metadata
- Sparce user ratings (0-3 movies)

Output
- Top-N movie recommendations (5 or 10)

## Algorithm
Content-Based appraoch
1. Represent each movie as a vector
- Genres -> one-hot encoding
- Tags -> TF-IDF
2. Build a user profile vecotr
- Average of liked movie vectors
3. Compute similarity
- Cosine simularity
4. Rank movies by similarity score
Collaborative filtering baseline
- User-based CF with cosine similarity
- item-based CF

## Evaluation
- Precision@K
- Recall@K
- Coverage



## MovieLens Dataset Description

The **MovieLens dataset** is a widely used benchmark dataset for building and evaluating recommendation systems. It contains user ratings of movies along with movie metadata.

## 1. Dataset Structure

The dataset typically includes the following tables:

### Ratings Table

| Column      | Type   | Description                                  |
|------------|-------|----------------------------------------------|
| `user_id`   | int   | Unique identifier for each user             |
| `movie_id`  | int   | Unique identifier for each movie            |
| `rating`    | float | User’s rating of the movie (e.g., 1–5)     |
| `timestamp` | int   | Time when the rating was submitted          |

**Example:**

| user_id | movie_id | rating | timestamp  |
|---------|----------|--------|------------|
| 1       | 101      | 5      | 874965758  |
| 1       | 102      | 3      | 874965759  |
| 2       | 101      | 4      | 874965760  |

> Each row represents **one user’s rating of one movie**. By grouping all rows by `user_id`, we can see **all movies rated by a particular user**, which is useful for simulating cold-start scenarios.

---

### Movies Table

| Column     | Type   | Description                                   |
|------------|--------|-----------------------------------------------|
| `movie_id` | int    | Unique identifier for each movie             |
| `title`    | string | Movie title                                  |
| `genres`   | string | Genres associated with the movie (e.g., Comedy\|Romance) |

**Example:**

| movie_id | title             | genres                       |
|----------|-----------------|-------------------------------|
| 101      | Toy Story (1995) | Animation\|Children\|Comedy  |
| 102      | Jumanji (1995)   | Adventure\|Children\|Fantasy |

---

## 2. How It’s Used in Cold-Start Recommendation

- **User ratings** provide the ground truth for simulation:
  - Some ratings are **visible** to the model (simulating initial user input)
  - Remaining ratings are **hidden** for evaluation
- **Movie metadata** (genres, tags, etc.) is used in **content-based filtering** to generate recommendations for new users.

---

## 3. Dataset Variants

- **MovieLens 100k**: ~100,000 ratings from 943 users and 1,682 movies  
- **MovieLens 1M**: ~1,000,000 ratings from 6,000 users and 4,000 movies  
- **MovieLens 20M**: ~20,000,000 ratings for large-scale research

> For a cold-start project, **MovieLens 100k** is sufficient — small enough to experiment but rich enough for meaningful evaluation.

---

## 4. Key Features for Cold-Start

- **Sparse ratings**: many users rate only a few movies  
- **Rich movie metadata**: genres, tags, and sometimes keywords  
- **Widely used**: makes results reproducible and comparable to prior research
