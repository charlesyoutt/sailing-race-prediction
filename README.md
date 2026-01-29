# Sailing Race Performance Prediction

## Overview
I built this project to analyze and predict college sailing race performance using real regatta data scraped from College Sailing Scores. I was drawn to this problem because sailing outcomes depend heavily on context rather than simple rankings or win–loss records, which makes it a natural challenge for data-driven modeling.

The focus of this project is building an **end-to-end data science pipeline** that captures that complexity and translates it into an interpretable machine learning model, rather than forcing a single deterministic prediction.

## What This Does
Given historical regatta data, the system:

- **Scrapes and consolidates race-level sailing results**
- **Performs exploratory analysis across sailors, teams, and venues**
- **Engineers contextual performance features**
- **Trains a Random Forest regression model to predict finish position**
- **Evaluates model performance on held-out race data**

Rather than aiming for perfect predictions, the goal is to understand which factors consistently influence performance and how much signal exists in historical results.

## How It’s Built
The project is organized into three core components:

- **`Scraping.ipynb`** — collects and cleans historical regatta data from College Sailing Scores  
- **`Graphing.ipynb`** — performs exploratory analysis and visualizes feature relationships, prediction errors, and model behavior  
- **`RandomForestModel.ipynb`** — handles feature engineering, model training, and evaluation using a Random Forest regression model  

Together, these notebooks form a modular and reproducible pipeline from raw data to evaluated predictions.

## Technical Concepts
This project touches a mix of data science and machine learning concepts, including:

- **Web scraping and data cleaning**
- **Feature engineering and aggregation**
- **Exploratory data analysis**
- **Supervised learning with Random Forests**
- **Regression model evaluation (MSE, R², MAE)**
- **Model interpretation and error analysis**
- **Modular, notebook-based pipeline design**

## Results & Interpretation
Model performance reflects both meaningful structure in the data and the inherent variability of sailing outcomes:

- Holdout performance: **MSE ≈ 13.47**, **R² ≈ 0.43**
- Average race-level error: **~1.6–2.3 finish positions**
- Most influential features:
  - Historical average finish
  - Partner aggregate performance
  - Venue aggregate performance

Accuracy is naturally limited by unobserved race-day factors such as wind, weather, and fleet dynamics, which are not captured in the dataset.

## Potential Improvements
There are several clear paths to improving the model:

- Incorporate weather and wind conditions at race time  
- Include fleet size and event competitiveness metrics  
- Add richer sailor experience indicators (years racing, program strength)  

Sailing outcomes are inherently noisy, but adding more contextual features would likely improve generalization and robustness.

*For full analysis and experimentation, the notebooks can be run locally.*
