# README

## Project Title
**MVP Prediction for the 2023-2024 NBA Season**

## Project Description
This project aims to predict the NBA's Most Valuable Player (MVP) for the 2023-2024 season using various statistical modeling techniques. The goal is to build a predictive model that uses both traditional and advanced basketball statistics to forecast MVP voting patterns based on player performance metrics.

## Table of Contents
- [Executive Summary](#executive-summary)
- [Background](#background)
- [Data Processing](#data-processing)
- [Feature Engineering](#feature-engineering)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Models](#models)
  - [Multi Linear Regression](#multi-linear-regression)
  - [Random Forest](#random-forest)
  - [Boosted Random Forest](#boosted-random-forest)
  - [H2O Stacked Ensemble](#h2o-stacked-ensemble)
- [Conclusion](#conclusion)
- [Limitations](#limitations)
- [Appendix](#appendix)

## Executive Summary
This case study utilizes statistical modeling to predict the NBA MVP for the 2023-2024 season. Nikola Jokic emerges as the top candidate across various models, with Giannis Antetokounmpo, Shai Gilgeous-Alexander, Luka Dončić, and Joel Embiid also featuring prominently. Random Forest and Boosted Random Forest models provided high prediction accuracy, correctly identifying 17 to 18 out of 20 past MVPs. The final model, a stacked ensemble, shows a slight improvement in prediction accuracy.

## Background
The MVP is awarded to the best-performing player of the NBA regular season, as decided by a panel of sportswriters and broadcasters. This project aims to predict the MVP using statistical methods, considering traditional box score statistics and advanced metrics.

## Data Processing
Data was sourced from Basketball Reference, covering player statistics from the 2004 to 2023 seasons, and partially from the 2023-2024 season. The data includes traditional stats (e.g., points, assists) and advanced stats (e.g., PER, TS%).

### Example Cleaning of Datasets: 2024 Season (Test Set)
Datasets include:
- `totals`: Regular counting statistics
- `adv`: Advanced statistics
- `pbp`: Play-by-play data

## Feature Engineering
Features were engineered by cleaning and combining the datasets, removing redundant and highly correlated features. Players with low playtime or game counts were excluded to focus on potential MVP candidates.

## Exploratory Data Analysis (EDA)
Correlation analysis and visualization helped identify key variables influencing MVP award shares. Metrics like VORP, PER, BPM, and WS were found to be highly correlated with award shares.

## Models

### Multi Linear Regression
A simple linear regression model was built, achieving an R² of 0.3681. This model correctly predicted 10 out of 20 past MVPs.

### Random Forest
The Random Forest model outperformed the linear regression model, correctly identifying 18 out of 20 past MVPs. Key variables included VORP, PER, BPM, WS, and FTA per game.

### Boosted Random Forest
Boosted Random Forest further refined predictions, maintaining high accuracy and a lower RMSE score compared to the Random Forest model.

### H2O Stacked Ensemble
A stacked ensemble model using H2O improved prediction accuracy slightly, achieving an RMSE score of 0.074 on the test set. This model consistently ranked Nikola Jokic as the top MVP candidate.

## Conclusion
Nikola Jokic is the predicted MVP for the 2023-2024 season, with other top candidates being Giannis Antetokounmpo, Shai Gilgeous-Alexander, Luka Dončić, and Joel Embiid. The models highlight the importance of advanced statistics in predicting MVP outcomes.

## Limitations
The study focuses on predicting MVP based on statistical performance, not identifying the best player overall. Defensive stats and newer metrics (e.g., Second Spectrum data) were not included, which could provide further insights.

## Appendix
A detailed list of features and their descriptions is provided, including traditional and advanced basketball statistics.

## Installation
To reproduce this project, install the required R packages:
```r
install.packages(c("tidyverse", "readxl", "magrittr", "tinytex", "ggplot2", "skimr", "randomForest", "caret", "ISLR", "ranger", "Metrics", "pdp", "dplyr", "lares", "stats", "pROC", "sampling", "plotrix", "corrplot", "h2o"))
```

## Usage
1. Load the project in R.
2. Ensure the datasets (`2024 NBA Totals.xlsx`, `2024 NBA Advanced.xlsx`, `2024 NBA PBP.xlsx`, `FINALFINALDATASETNBA.xlsx`) are in the working directory.
3. Run the R Markdown file to reproduce the analysis and results.

## License
This project is licensed under the MIT License. Feel free to use and modify the code for your own purposes.

## Contact
For any inquiries or further information, please contact:
**Martin Lim**  
Yale-NUS College  
Email: [martinl@u.yale-nus.edu.sg]  

---
