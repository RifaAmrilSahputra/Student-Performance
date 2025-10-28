# Student Performance Prediction

This repository contains exploratory data analysis (EDA) and machine learning models to **predict student performance** based on study hours, previous scores, sleep hours, practice sheets, and extracurricular participation.

## Dataset
The dataset comes from Kaggle: [Student Performance Dataset](https://www.kaggle.com/datasets/khansaafreen/student-performance)  
- 10,000 observations  
- 6 columns: `Hours.Studied`, `Previous.Scores`, `Extracurricular.Activities`, `Sleep.Hours`, `Sample.Question.Papers.Practiced`, `Performance.Index`  
- No missing values  

## Exploratory Data Analysis (EDA)
### Summary Statistics
- Numeric features show symmetric distributions, no extreme outliers.  
- `Performance.Index` mean ≈ 55, median ≈ 55, min = 10, max = 100.

### Distribution of Performance
- Most students fall in the **40–75** range.  
- Peak frequency around **45–55**, few students with very high (>90) or very low (<25) scores.  
- Slightly negatively skewed but overall fairly symmetric.

### Extracurricular Participation vs Performance
| Activity | Count | Mean | Median | SD | Min | Max |
|----------|-------|------|--------|----|-----|-----|
| No       | 5052  | 54.8 | 55     | 19.2 | 10  | 99  |
| Yes      | 4948  | 55.7 | 55     | 19.3 | 11  | 100 |

- Students participating in extracurricular activities show slightly higher mean performance.  
- Median and variation (SD) are similar across groups.

### Feature Correlations
| Variable | Correlation with Performance.Index |
|----------|----------------------------------|
| Previous.Scores | 0.92 |
| Hours.Studied   | 0.37 |
| Sample.Question.Papers.Practiced | 0.04 |
| Sleep.Hours     | 0.05 |

- `Previous.Scores` is the strongest predictor.  
- `Hours.Studied` has a moderate positive effect.  
- Other features show weak correlations.

### Visualizations Included
- Histogram of `Performance.Index`  
- Boxplot of `Performance.Index` vs `Extracurricular.Activities`  
- Correlation heatmap of numeric features  
- Scatter plots between key features (`Previous.Scores` and `Hours.Studied`) and target

## Machine Learning Models
Three models were trained on this dataset:

1. **Linear Regression**  
   - RMSE (Test Set): ~2.05  
   - High R² (~0.988) → simple linear model is very effective.

2. **Random Forest**  
   - RMSE (Test Set): ~8.17  
   - Less accurate because relationships are mostly linear; tree-based complexity not needed.

3. **XGBoost**  
   - RMSE (Test Set): ~2.13  
   - Slightly higher RMSE than linear regression; captures interactions but linearity dominates dataset.

### Feature Importance
- `Previous.Scores` contributes most to prediction.  
- `Hours.Studied` and `Extracurricular.Activities` provide minor predictive power.  


## Tools & Libraries
- R, RStudio  
- Packages: `dplyr`, `ggplot2`, `caret`, `randomForest`, `xgboost`, `corrplot`, `summarytools`, `Metrics`

## Insights
- Linear Regression is sufficient due to strong linear relationship between previous scores and performance.  
- Extracurricular participation slightly correlates with better performance.  
- Hours studied moderately improves predictions.  
- Tree-based models are less necessary for this dataset but can be used for comparison or feature importance analysis.
