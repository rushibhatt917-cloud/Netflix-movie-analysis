# Netflix-movie-analysis

![Python](https://img.shields.io/badge/Python-3.x-blue) ![Pandas](https://img.shields.io/badge/Pandas-EDA-green) ![Status](https://img.shields.io/badge/Status-Completed-success)

## Overview
Analysed a dataset of **9,800+ movies** to answer 5 key business questions that help understand content trends, audience preferences, and movie performance on Netflix.

## Business Questions Answered
| # | Question | Answer |
|---|----------|--------|
| 1 | Most frequent genre? | **Drama** (3,744 movies) |
| 2 | Highest vote average movie? | **Kung Fu Master Huo Yuanjia** (10.0) |
| 3 | Most popular movie & genre? | **Spider-Man: No Way Home** — Action, Adventure, Sci-Fi |
| 4 | Least popular movie & genre? | **The United States vs. Billie Holiday** — Music, Drama, History |
| 5 | Year with most releases? | **2021** (714 movies) |

## Dataset
- **Source:** TMDB Movie Database (mymoviedb.csv)
- **Rows:** 9,837 movies
- **Columns:** 9 (Release_Date, Title, Overview, Popularity, Vote_Count, Vote_Average, Original_Language, Genre, Poster_Url)
- **Time period:** 2000 – 2024

## Tools & Technologies
| Tool | Purpose |
|------|---------|
| Python 3 | Core programming language |
| Pandas | Data loading, cleaning & analysis |
| NumPy | Numerical operations |
| Matplotlib | Data visualization |
| Seaborn | Statistical charts |
| Jupyter Notebook | Analysis environment |

## Key Insights
- **Drama dominates** — Drama is the most produced genre with 3,744 movies, followed by Comedy and Thriller
- **2021 was peak production year** — 714 movies released, likely due to post-pandemic content surge
- **English content is dominant** — 77% of all movies are in English; Japanese content is second at ~7%
- **Spider-Man: No Way Home** holds the highest popularity score of 5,083 — nearly 2x the second highest
- **High discounts hurt ratings** — movies with very few votes often show extreme ratings (10.0 or 0.0), showing the importance of filtering by vote count

## Project Structure
```
netflix-movie-analysis/
├── Netflix.ipynb          ← Main Jupyter notebook
├── mymoviedb.csv          ← Dataset
├── outputs/               ← Saved chart images
│   ├── top10_popular.png
│   ├── genre_counts.png
│   ├── movies_per_year.png
│   ├── rating_distribution.png
│   ├── top_rated.png
│   └── language_breakdown.png
└── README.md              ← This file
```

## How to Run
1. Clone this repository
2. Make sure Python 3 is installed
3. Install dependencies:
```bash
pip install pandas numpy matplotlib seaborn jupyter
```
4. Open the notebook:
```bash
jupyter notebook Netflix.ipynb
```
5. Run all cells (`Kernel → Restart & Run All`)

## Data Cleaning Steps
- Used `engine='python'` to handle buffer overflow in CSV parsing
- Dropped rows with missing Title, Genre, or Vote_Average
- Converted Release_Date to datetime format
- Converted Vote_Average, Vote_Count, Popularity to numeric types
- Extracted Year and Month from Release_Date
- Split multi-value Genre column using `.str.split().explode()`

## Author
**Rushi Bhatt**
- Email: rushibhatt917@gmail.com
- LinkedIn: linkedin.com/in/rushibhatt
- Open to Data Analyst roles — Immediate joiner
