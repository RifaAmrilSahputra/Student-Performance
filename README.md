# Student Performance Prediction

This repository contains data analysis and machine learning models to predict students' **Performance Index** based on study hours, previous scores, sleep hours, practice sheets, and extracurricular participation.

## Dataset
The dataset is sourced from Kaggle: [Student Performance Dataset](https://www.kaggle.com/datasets/khansaafreen/student-performance)  
- 10,000 observations  
- 6 columns: Hours.Studied, Previous.Scores, Extracurricular.Activities, Sleep.Hours, Sample.Question.Papers.Practiced, Performance.Index  
- No missing values  

## Exploratory Data Analysis
- Numeric descriptive statistics  
- Distribution of Performance.Index  
- Analysis of relationship with extracurricular activities  
- Correlation between features

## Machine Learning Models
1. **Linear Regression**  
2. **Random Forest**  
3. **XGBoost**  

**Evaluation Results (RMSE on Test Set):**
- Linear Regression: ~2.05  
- Random Forest: ~8.17  
- XGBoost: ~2.13  

## Insights
- Previous scores (`Previous.Scores`) are the main predictor.  
- Study hours and extracurricular participation have a positive but smaller impact.  
- Simple linear models perform well because the dataset has strong linear relationships.

## Tools
- R, RStudio  
- Packages: `dplyr`, `ggplot2`, `caret`, `randomForest`, `xgboost`, `corrplot`, `summarytools`, `Metrics`

## Development Environment

This project is developed using **R** and can be run in a standard R environment (`.R` scripts) or in **Jupyter Notebook (`.ipynb`)** using the **IRKernel**.  
- Using Jupyter allows combining **R code, visualizations, and markdown analysis** in a single interactive notebook.  
- Compatible with Kaggle Notebooks for easy execution and sharing.
