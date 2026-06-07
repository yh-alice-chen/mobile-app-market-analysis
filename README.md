# Mobile App Market Analysis: Maximising User Engagement and Ad Revenue

## Introduction

This project analyses data from Android and iOS mobile apps available on Google Play and the App Store. The focus is on exploring app datasets to uncover trends and patterns within the mobile app market, from the perspective of a data analyst working for a company that builds free-to-download mobile apps.

## The Goal

The primary source of revenue is in-app ads, meaning profitability is directly tied to user volume. The main goal of this project is to determine what types of apps are most likely to attract a large user base. These data-driven insights will inform app development decisions aimed at maximising user engagement and ad revenue.

## Data Sources

| Dataset | Platform |
|---|---|
| [googleplaystore.csv](https://dq-content.s3.amazonaws.com/350/googleplaystore.csv) | Google Play |
| [AppleStore.csv](https://dq-content.s3.amazonaws.com/350/AppleStore.csv) | App Store |

## Repository Structure

```
├── mobile-app-market-analysis.ipynb    # Main analysis notebook
├── googleplaystore.csv                 # Google Play dataset
├── AppleStore.csv                      # App Store dataset
└── README.md
```

## Data Cleaning

The raw datasets were cleaned before analysis:

- Removed one Google Play row with missing columns (row 10,472)
- Removed 1,181 duplicate Google Play entries, keeping the row with the highest review count per app
- Filtered out non-English apps using ASCII character range detection
- Isolated free apps only

**Final dataset: 8,864 Android apps · 3,222 iOS apps**

## Data Analysis

The analysis examines genre frequency and average installs/ratings across both platforms to identify which genres attract the most users. The App Store dataset lacks install data, so total user ratings are used as a proxy.

## Conclusion

The books and reference genre shows consistent potential in both markets. The recommended direction is to build an app centred around a popular book, enhanced with features beyond the raw text such as daily quotes, an audio version, chapter quizzes, or an in-app discussion forum. This profile avoids the saturation seen in games and communication apps, while targeting a genre with demonstrated user demand across both platforms.

## Tools and Techniques

- **Language:** Python 3
- **Libraries:** Standard library only (`csv`)
- **Concepts applied:** Data cleaning, frequency tables, nested loops, custom functions, dictionary-based aggregation, tuple sorting, ASCII-based language detection

## How to Run

1. Clone the repository
2. Ensure `googleplaystore.csv` and `AppleStore.csv` are in the same directory as the notebook
3. Open `mobile-app-market-analysis.ipynb` in Jupyter Notebook or JupyterLab
4. Run all cells in order

## Source

Built as part of the Dataquest guided project series.
