# Predicting-Donors-Choose-Project-Outcomes-with-Naive-Bayes-Classification

# Donors Choose Dataset - Naive Bayes Classification

## Project Overview
This Jupyter Notebook project focuses on applying the Naive Bayes classification algorithm to the Donors Choose dataset. The objective is to build a model that predicts whether a project proposal on the Donors Choose platform will be accepted or rejected. The primary tasks and highlights of the project are as follows:

## Key Tasks

### 1. Data Preparation
- Minimum data points are considered based on RAM (50k for 4GB RAM, 100k for 8GB RAM).
- When using random search or grid search, data doesn't need to be split into X_train, X_cv, and X_test as these methods use k-fold cross-validation.
- For hyperparameter tuning with for-loops, data is split into X_train, X_cv, and X_test.
- Explore the stratify parameter when splitting the data.

### 2. Feature Sets
Apply Multinomial Naive Bayes (NB) on different feature sets:
- Set 1: Categorical and numerical features + preprocessed essay (Bag of Words - BOW).
- Set 2: Categorical and numerical features + preprocessed essay (TF-IDF).

### 3. Hyperparameter Tuning
Tune the smoothing parameter (alpha) for Multinomial NB by exploring alpha values in the range from 10^-5 to 10^2. Consider class_prior = [0.5, 0.5] and check how results might change.

### 4. Model Evaluation
- For hyperparameter tuning, use k-fold cross-validation (GridsearchCV or RandomsearchCV) and plot the performance of the model on train and cross-validation data.
- Train the model with the best hyperparameter and find the AUC on the test data.
- Plot the Receiver Operating Characteristic (ROC) curve on both train and test data.
- Display confusion matrices with predicted and original labels of test data points in heatmap format.

### 5. Feature Analysis
Find the top 20 features from feature Set 1 or feature Set 2 using the `feature_log_prob_` parameter of Multinomial NB. Print both positive and negative corresponding feature names.

---

*Note: Please refer to the actual Jupyter Notebook for detailed code implementations and visualizations.*

---
