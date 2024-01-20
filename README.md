# Credit Card Fraud Detection

This project involved building models to detect fraudulent credit card transactions using a public dataset from Kaggle: https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

## Data Overview

- The dataset contains 284,807 transactions with 30 numeric features (PCA transformed due to confidentiality) and a target class indicating fraud or not.

- Highly imbalanced dataset with only 0.17% of transactions being fraudulent.

- No feature information provided due to privacy reasons. 'Time' and 'Amount' columns left untouched.

## Analysis Steps

The main analysis steps included:

- Data exploration - distributions, correlations, anomalies
- Handling class imbalance via undersampling and oversampling
- Modeling with Logistic Regression, Random Forest, XGBoost
- Evaluating models using AUC-ROC metric due to imbalance  
- Anomaly detection with Isolation Forest
- Feature engineering - simple moving average over time

## Key Observations

- Random Forest and XGBoost models achieved perfect AUC-ROC scores of 1.0
- Oversampling increased minority class samples, undersampling decreased majority class
- Isolation Forest detected ~15% transactions as outliers
- New features like moving average improved fraud detection capability
