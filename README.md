# Sailing Race Prediction & Performance Analysis

This project builds an end-to-end data science pipeline to analyze and predict college sailing race performance using real regatta data. I was particularly interested in this problem because sailing outcomes are highly context-dependent, making it a strong candidate for machine learning rather than traditional ranking-based approaches.

## Project Overview

The project is organized into three main stages:
1. Data Collection – Scrape and consolidate race-level results across multiple seasons
2. Exploratory Analysis – Analyze performance patterns by sailor, team, and venue
3. Modeling – Train a Random Forest model to predict race outcomes

Each stage is implemented in a separate notebook to keep the pipeline modular and reproducible.

## Repository Structure

sailing-race-prediction/
- Scraping.ipynb
- Graphing.ipynb
- RandomForestModel.ipynb
- races.csv
- README.md

## Data Collection (Scraping.ipynb)

This notebook scrapes regatta results across multiple seasons and parses race tables, sailor roles (skipper and crew), partners, divisions, venues, and scores. It handles real-world edge cases such as regattas with no posted scores, missing skipper or crew entries, and combined versus separated scoring formats. The output is a single consolidated dataset (races.csv) used throughout the project.

## Exploratory Analysis (Graphing.ipynb)

This notebook computes performance metrics including average finish position, normalized ratio scores, and regatta participation counts. It analyzes performance by sailor, team, and venue and uses interactive visualizations to explore team-level distributions, venue-specific trends, and experience versus performance relationships. The goal is to identify meaningful signals for modeling.

## Modeling (RandomForestModel.ipynb)

This notebook engineers features capturing sailor experience, team and partner context, and venue history. High-cardinality categorical variables are handled using aggregated statistics rather than one-hot encoding. A Random Forest regression model is trained to predict race finish outcomes, and feature importance is evaluated to understand which factors drive performance. The modeling approach prioritizes robustness and interpretability.

## Tools & Technologies

Python, Pandas, NumPy, BeautifulSoup, Plotly, scikit-learn
