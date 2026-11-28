# Netflix Movie Durations: Are Movies Getting Shorter?

Exploratory data analysis in Python to test the claim that the average duration of Netflix movies has been declining.

> Based on a DataCamp guided project. The dataset and the initial question were provided by the project; the analysis and code are mine.

## Overview
- **Question:** Is the average movie duration on Netflix really decreasing over time, and could genre explain it?
- **Dataset:** `netflix_data.csv`, 7,787 titles (5,377 movies and 2,410 TV shows) with 11 columns (title, type, country, release year, duration, genre, and more).
- **Tools:** Python, pandas, Matplotlib, Jupyter Notebook

## Process
1. **Built a DataFrame from raw data:** converted a friend's yearly averages (2011-2020) from a Python dictionary into a pandas DataFrame.
2. **Visualized the trend:** line plot of average movie duration by year.
3. **Loaded and filtered the full dataset:** kept only `Movie` rows (TV shows measure duration in seasons) and selected the relevant columns: title, country, genre, release year, duration.
4. **Explored individual movies:** scatter plot of duration vs. release year.
5. **Investigated short movies:** filtered movies under 60 minutes and checked their genres.
6. **Color-coded genres:** looped over the data to mark Children, Documentaries, and Stand-Up movies, then re-plotted to see whether they pull the average down.

## Key Findings
- The friend's yearly averages fall from **103 minutes (2011) to 90 minutes (2020)**, which looks like a decline.
- The full dataset shows that most movies on the platform are recent, and many short films were released in the last two decades.
- **420 movies (about 8% of all movies) run under 60 minutes**, and around **79% of them are Children, Documentaries, or Stand-Up** titles, which are naturally shorter than feature films.
- **Conclusion:** the decline is likely influenced by genre mix, so the data alone is not enough to say movies are getting shorter. Further statistical analysis would be needed.

## Visuals
<!-- Save your charts from the notebook into images/ and update the file names -->
![Average movie duration 2011-2020](images/avg_duration_line.png)
![Movie duration by release year](images/duration_scatter_colored.png)

## How to Run
```bash
pip install pandas matplotlib jupyter
jupyter notebook notebook.ipynb
```
The notebook reads the data from `datasets/netflix_data.csv`.

## Repository Structure
```
├── notebook.ipynb          # main analysis
├── datasets/
│   └── netflix_data.csv    # dataset
├── images/                 # exported charts
└── README.md
```

## Possible Next Steps
- Test the trend statistically (for example, compare average duration before and after removing the shorter genres).
- Plot average duration by year for each genre separately.
- Use Seaborn for more advanced visualizations.
