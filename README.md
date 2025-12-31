# Netflix Content Strategy: 1990s Cinematic Trends Analysis

## 📌 Project Overview
This project performs an Exploratory Data Analysis (EDA) on Netflix's dataset to characterize cinematic trends from the 1990s. The analysis was conducted to support a production company specializing in nostalgic content, providing data-driven insights into movie durations and genre-specific patterns (specifically Action) from that decade.

## 🚀 Key Business Questions
* What was the standard runtime distribution for movies in the 1990s?
* How prevalent were "short" feature films (< 90 minutes) within the Action genre?
* What data characteristics define the "nostalgic" era of entertainment?

## 🛠️ Technical Stack
* **Language:** Python 3.x
* **Data Manipulation:** Pandas (DataFrames, boolean masking, logical filtering)
* **Visualization:** Matplotlib (Histograms, distribution analysis)
* **Environment:** Jupyter Notebook

## 📊 Methodology & Insights
1.  **Data Cleaning & Filtering:**
    * Isolated `Movie` content type from TV Shows.
    * Filtered temporal data to strictly capture the 1990–1999 decade.
2.  **Distribution Analysis:**
    * Generated a frequency distribution of movie runtimes.
    * **Finding:** The most frequent movie duration in the 1990s stabilized around **100 minutes**, establishing a baseline for feature-length productions of that era.
3.  **Genre-Specific Drill Down:**
    * Performed granular analysis on the **Action** genre.
    * Utilized both iterative loops and vectorized operations to calculate count metrics.
    * **Finding:** Short-form action movies (< 90 mins) were a niche category, with only **7 titles** identified in the dataset, suggesting a market preference for longer runtime in this genre.

## 💻 Code Highlight: Vectorized vs. Iterative Analysis
The project demonstrates efficiency in data aggregation by comparing iterative approaches with Pandas vectorization.

```python
# Efficient Vectorized Calculation for Action Movies < 90 mins
short_movies_count = (action_movie_1990['duration'] < 90).sum()
print(f"Short Action Movies count: {short_movies_count}")
