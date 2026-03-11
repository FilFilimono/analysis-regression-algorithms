# Comparative Analysis of ML Regression Algorithms

[![Python](https://img.shields.io/badge/Python-3.13.5-blue.svg)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/scikit--learn-Latest-orange.svg)](https://scikit-learn.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data_Analysis-yellow.svg)](https://pandas.pydata.org/)

This repository contains a comprehensive comparative analysis of various machine learning regression algorithms. The study is based on the task of predicting rock density using reflected X-ray signals (a dataset with complex, non-linear sinusoidal relationships).

## Project Goal
To evaluate and compare the efficiency of classical ML algorithms in modeling complex non-linear data, identify their strengths and weaknesses, and demonstrate the practical implications of underfitting and overfitting.

## Evaluated Algorithms

1. **Linear Regression**
   * *Strengths:* Fast computation, maximum interpretability.
   * *Weaknesses:* Too simple for this dataset. Fails to capture the wave-like (sinusoidal) nature of the data, resulting in severe underfitting.

<img width="1147" height="773" alt="image" src="https://github.com/user-attachments/assets/b2bafbe5-4005-4fe6-8d81-1f320ecc8076" />


2. **Polynomial Regression**
   * *Strengths:* Captures non-linearity and adapts flexibly to data curves when the polynomial degree is tuned correctly.
   * *Weaknesses:* High risk of overfitting with higher degrees. Poor extrapolation (predictions shoot to infinity at the edges of the dataset).

<img width="1146" height="602" alt="image" src="https://github.com/user-attachments/assets/241acdf7-c5a5-42ff-8d9b-668a451e5a41" />


3. **K-Nearest Neighbors (KNN) Regression**
   * *Strengths:* Excellent at capturing local non-linear patterns without complex mathematical feature transformations.
   * *Weaknesses:* Sensitive to outliers; results heavily depend on the `K` parameter. The model has a "step-like" nature and cannot extrapolate beyond the training data range.

<img width="1148" height="594" alt="image" src="https://github.com/user-attachments/assets/0d3c898c-c413-47d2-af55-817d5d4aac59" />


4. **Support Vector Regression (SVR)**
   * *Strengths:* Effective in high-dimensional spaces and robust to outliers.
   * *Weaknesses:* Requires careful feature scaling and hyperparameter tuning (C, epsilon, kernel type).

<img width="1151" height="594" alt="image" src="https://github.com/user-attachments/assets/2a2b1b3d-5f0b-4867-adcd-39f7df7d41ea" />


5. **Tree-Based Ensembles (Random Forest & Gradient Boosting)**
   * *Strengths:* Extremely powerful algorithms. Perfectly adapt to complex data structures. Random Forest is highly robust to outliers, while Gradient Boosting sequentially minimizes errors, achieving the highest accuracy metrics.
   * *Weaknesses:* More computationally expensive and harder to interpret ("black box" models) compared to linear approaches.

<img width="1150" height="600" alt="image" src="https://github.com/user-attachments/assets/d964b653-983e-4db8-b388-714ae1f2cc1f" />


## Conclusion
The analysis proves that basic linear models are ineffective for datasets with complex non-linear dependencies (like decaying sensor signals). Ensemble methods (**Random Forest** and **Gradient Boosting**) demonstrated the best performance, providing highly accurate and stable interpolations while avoiding the extreme extrapolation errors seen in Polynomial Regression.

