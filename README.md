# Prediction of Pitcher Saves
Predicting Saves: A Baseball Statistics Project

This project explores the use of baseball statistics to predict the number of saves a pitcher will earn based on past performance using linear regression and other machine learning techniques.
___

1. Repository Contents

*Notebooks*
Predicting_Saves
Objective: Scrapes data, processes it into clean, usable formats, and builds regression models to predict saves.
Processes:
Scraping URLs and parsing HTML using BeautifulSoup.
Data cleaning and organization into structured dataframes.
Exploratory Data Analysis (EDA) through visualizations.
Model creation, testing, and performance analysis, including error visualization.

Predicting_Saves_NOZEROS
Objective: Investigates methods for handling data seasons where pitchers recorded no saves.
Focus Areas:
Addressing whether to exclude seasons with zero saves or identify specific reasons behind these values.
Ensuring erroneous data from pitchers' final seasons is corrected or excluded to improve model accuracy.
___

2. Presentation
   
A concise project overview PDF for a 5-minute presentation. It summarizes the objectives, methodologies, results, and next steps.
Objective
Goal: Build a regression model to predict the number of saves a pitcher will earn based on previous performance metrics.
___

3. Approach
   
Feature Selection
Final model features include:
Opportunity Indicators: Games finished, appearances, saves, save opportunities, holds, team change, and two-year running sum of saves.
Performance Metrics: FIP (Fielding Independent Pitching), SO/BB (Strikeouts-to-Walks ratio), BB/9 (Walks per nine innings), H/9 (Hits per nine innings), ERA+ (Adjusted ERA), "mistakes" per game, and batters faced per game.
Demographic Factors: Age.

5. Modeling Techniques
   
Linear regression.
Ridge regression.
LASSO regression.
Feature scaling to optimize performance based on R² and MSE.

7. Data and Feature Engineering
   
*Data Source*
Data for over 300 pitchers spanning approximately 1,500 seasons was scraped from Baseball-Reference.
*Data Preparation*
Entire careers were analyzed, enabling exploration of time-series trends.
Features were evaluated using:
Correlation heatmaps.
Pairplots to avoid collinearity and identify relationships.
Interaction terms created in polynomial models.
LASSO cross-validation to streamline feature selection.
___

8. Results Summary
   
Final Model: LASSO regression.
Performance Metrics:
𝑅2 = 0.41
Mean Absolute Error (MAE): 10.2 saves.
Interpretation: The model explains 41% of the variability in saves and predicts saves within an average error of 10.2 saves per season.

*Key Contributing Features*
***Opportunity Metrics***
Games finished.
Holds.
Saves.
Games.
***Dominance Metrics***
FIP.
SO/BB.
SO/9.

9. Next Steps
    
Improving Opportunity Metrics:
Investigate team and managerial trends in reliever usage and saves distribution.
Enhancing Dominance Metrics:
Incorporate advanced metrics such as:
Spin rate.
Velocity.
Swing-and-miss percentage.
Leverage external data sources to enrich the feature set.
Exploring Classification Models:
Transition from strict regression to a classification approach for pitcher roles (e.g., closer, setup man).
___

Featured Techniques
Web Scraping: Utilized BeautifulSoup for data extraction.
Machine Learning:
Linear regression.
Regularization techniques: Ridge and LASSO regression.
Feature Engineering: Polynomial interaction terms and cross-validation for feature selection.
Exploratory Data Analysis:
Visualizations for identifying feature relationships and collinearity.
___

Best Practices
How to Use This Repository
Data Collection: Use the scraping scripts to gather updated baseball statistics.
Data Cleaning & Analysis: Follow the steps in the Predicting_Saves notebook to preprocess and analyze the data.
Modeling: Experiment with different regression models or classification approaches using the provided frameworks.
Interpretation: Use visualizations and model metrics to evaluate and interpret results.
Prerequisites
Python libraries: pandas, numpy, matplotlib, scikit-learn, BeautifulSoup.
