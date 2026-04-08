# FraudXGBoost

Machine Learning-based fraud detection system that analyzes complex patterns in highly imbalanced data to identify fraudulent transactions, optimizing the trade-off between recall and precision through threshold tuning.

---

## Overview

Fraud detection is a challenging problem due to the extreme class imbalance and the need to balance detection performance with operational costs.

This project implements an end-to-end ML pipeline to:

- Detect fraudulent transactions  
- Handle highly imbalanced data (~1% fraud)  
- Optimize model decisions using threshold tuning  
- Evaluate performance using appropriate metrics  

---

## Problem Statement

- Only ~1% of transactions are fraudulent  
- Traditional metrics like accuracy are misleading  
- Missing fraud (FN) is significantly more costly than blocking a legitimate user (FP)

The objective is to maximize fraud detection while controlling false positives.

---

## Pipeline

### 1. Data Validation
- Dataset inspection (duplicates, nulls, anomalies)
- Detection of encoded missing values (-1 → NaN)
- Removal of constant features

---

### 2. Exploratory Data Analysis
- Class imbalance visualization  
- Feature distribution comparison (fraud vs non-fraud)  
- Fraud rate analysis across categorical variables  

---

### 3. Data Preprocessing
- Numerical features:
  - Median imputation  
  - Standard scaling  
- Categorical features:
  - Most frequent imputation  
- Implemented using ColumnTransformer

---

### 4. Model Training

Models evaluated:

- Logistic Regression  
- Decision Tree  
- Random Forest  
- XGBoost (selected model)  

Evaluation metrics:

- PR-AUC  
- ROC-AUC  
- Recall  
- Precision  
- F1-score  

---

## Future Improvements

- Incorporation of behavioral features (time-based patterns, frequency of actions)  
- Use of more advanced ensemble techniques  
- Deployment as a risk scoring system instead of binary classification  
- Integration into a real-time fraud detection pipeline  

---

## Tech Stack

- Python  
- Pandas / NumPy  
- Scikit-learn  
- XGBoost  
- Matplotlib / Seaborn  

---

## Author

Hugo Agreda