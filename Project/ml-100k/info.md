# MovieLens 100K Dataset - File Documentation

## Overview
The MovieLens 100K dataset contains 100,000 ratings from 943 users on 1,682 movies. It was collected by the GroupLens Research Project at the University of Minnesota.

## Core Data Files

### u.data
**Complete dataset file**
- Contains all 100,000 ratings
- Format: tab-separated values
- Columns: `user_id`, `item_id`, `rating`, `timestamp`
- Each user has rated at least 20 movies
- Ratings are on a 5-star scale (1-5)
- Timestamps are Unix epoch time

### u.user
**User demographic information**
- Format: pipe-separated (`|`)
- Columns: `user_id`, `age`, `gender`, `occupation`, `zip_code`
- 943 users total
- Gender: M (Male) or F (Female)
- Age and occupation are demographic categories

### u.item
**Movie information**
- Format: pipe-separated (`|`)
- Columns: `movie_id`, `movie_title`, `release_date`, `video_release_date`, `IMDb_URL`, followed by 19 binary genre columns
- 1,682 movies total
- Movie titles include release year in parentheses
- Genre columns are binary (0 or 1) for each of the 19 genres

### u.genre
**List of genres**
- Format: pipe-separated (`|`)
- Columns: `genre_name`, `genre_id`
- Contains the 19 genres used in the dataset
- Genres include: Action, Adventure, Animation, Children's, Comedy, Crime, Documentary, Drama, Fantasy, Film-Noir, Horror, Musical, Mystery, Romance, Sci-Fi, Thriller, War, Western, Unknown

### u.occupation
**List of occupations**
- Simple text file with one occupation per line
- 21 different occupation categories
- Used to categorize users in u.user file

### u.info
**Dataset statistics summary**
- Contains basic information about the dataset
- Number of users, items, and ratings
- Useful for quick reference

## Train-Test Split Files

### Cross-Validation Splits (u1-u5)
**Five-fold cross-validation splits**

Each split consists of:
- **u1.base, u2.base, u3.base, u4.base, u5.base** - Training sets (~80% of data)
- **u1.test, u2.test, u3.test, u4.test, u5.test** - Test sets (~20% of data)

Format: Same as u.data (tab-separated)
Columns: `user_id`, `item_id`, `rating`, `timestamp`

These splits are designed for 5-fold cross-validation:
- Each user appears in both training and test sets
- Ratings are randomly distributed across splits
- Use all 5 splits to get robust performance estimates

### Special Splits

#### ua.base / ua.test
**Temporal split**
- Training set: Earlier ratings (by timestamp)
- Test set: Later ratings (by timestamp)
- Useful for testing temporal recommendation scenarios
- Simulates predicting future preferences

#### ub.base / ub.test
**User-based split**
- Subset of users for training
- Different subset for testing
- Useful for testing cold-start scenarios with new users

## Utility Scripts

### allbut.pl
**Perl script for creating custom splits**
- Creates leave-one-out or all-but-n splits
- Used to generate custom train/test partitions
- Requires Perl to run

### mku.sh
**Shell script for dataset preparation**
- Unix shell script for data processing
- May be used to regenerate splits or process data
- Requires bash/sh shell to run

## Usage Tips

### Loading in Python (pandas)
```python
import pandas as pd

# Load ratings data
ratings = pd.read_csv('u.data', sep='\t', names=['user_id', 'item_id', 'rating', 'timestamp'])

# Load user data
users = pd.read_csv('u.user', sep='|', names=['user_id', 'age', 'gender', 'occupation', 'zip_code'])

# Load movie data
movies = pd.read_csv('u.item', sep='|', encoding='latin-1', 
                     names=['movie_id', 'title', 'release_date', 'video_release_date', 'imdb_url'] + 
                     [f'genre_{i}' for i in range(19)])
```

### File Size Reference
- u.data: ~2 MB
- u.item: ~200 KB
- u.user: ~20 KB
- Each base/test file: ~1.5-2 MB

## Common Use Cases

1. **Standard Evaluation**: Use u1.base/u1.test through u5.base/u5.test for 5-fold cross-validation
2. **Temporal Analysis**: Use ua.base/ua.test to test time-based predictions
3. **Cold Start Research**: Use ub.base/ub.test or create custom splits to simulate new users
4. **Content-Based Filtering**: Use u.item genre information
5. **Demographic Analysis**: Use u.user demographic data

## Important Notes

- All files use 1-based indexing (IDs start at 1, not 0)
- Timestamps are in Unix epoch time (seconds since 1970-01-01)
- Some movie titles may contain special characters
- Use `encoding='latin-1'` when reading u.item to handle special characters
- The dataset is from the 1990s, so movies and cultural references reflect that era