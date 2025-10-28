# Student Performance Prediction

Repository ini berisi analisis data dan implementasi model machine learning untuk memprediksi **Performance Index** siswa berdasarkan jam belajar, nilai sebelumnya, jam tidur, latihan soal, dan partisipasi ekstrakurikuler.

## Dataset
Dataset digunakan berasal dari Kaggle: [Student Performance Dataset](https://www.kaggle.com/datasets/khansaafreen/student-performance)  
- 10.000 observasi  
- 6 kolom: Hours.Studied, Previous.Scores, Extracurricular.Activities, Sleep.Hours, Sample.Question.Papers.Practiced, Performance.Index  
- Tidak ada missing value  

## Analisis Eksploratif
- Statistik deskriptif numerik
- Distribusi Performance.Index
- Analisis hubungan dengan ekstrakurikuler
- Korelasi antar fitur

## Model Machine Learning
1. **Linear Regression**  
2. **Random Forest**  
3. **XGBoost**  

**Hasil Evaluasi RMSE (Test Set):**
- Linear Regression: ~2.05
- Random Forest: ~8.17
- XGBoost: ~2.13

## Insight
- Nilai sebelumnya (`Previous.Scores`) adalah prediktor utama.  
- Jam belajar dan partisipasi ekstrakurikuler berpengaruh positif tapi lebih kecil.  
- Model linear sederhana sudah optimal karena dataset sangat linear.


## Tools
- R, RStudio
- Packages: `dplyr`, `ggplot2`, `caret`, `randomForest`, `xgboost`, `corrplot`, `summarytools`, `Metrics`


## Development Environment

This project is developed using **R** and can be run in a standard R environment (`.R` scripts) or in **Jupyter Notebook (`.ipynb`)** using the **IRKernel**.  
- Using Jupyter allows combining **R code, visualizations, and markdown analysis** in a single interactive notebook.  
- Compatible with Kaggle Notebooks for easy execution and sharing.
