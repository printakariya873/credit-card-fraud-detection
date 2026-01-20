# Credit Card Fraud Detection System

## Overview
This project implements a machine learning–based credit card fraud detection system using real-world transaction data.  
The goal is to identify fraudulent transactions while handling extreme class imbalance commonly found in financial datasets.

The system focuses on **recall and ROC-AUC** rather than accuracy to minimize undetected fraud cases.

---

## Problem Statement
Credit card fraud detection is challenging due to:
- Highly imbalanced data (fraud cases are rare)
- Privacy constraints on transaction features
- High cost of false negatives (missed fraud)

This project addresses these challenges using appropriate preprocessing, resampling, and evaluation techniques.

---

## Dataset
- Dataset: European Credit Card Transactions Dataset
- Source: Kaggle
- Transactions: 284,807
- Fraud cases: 492 (≈0.17%)

Features are anonymized using **PCA transformation** to protect sensitive financial information.

---

## Technologies Used
- Python
- Pandas, NumPy
- Scikit-learn
- Imbalanced-learn (SMOTE)
- XGBoost
- Matplotlib, Seaborn
- Gradio (for model inference demo)

---

## Methodology
1. Data loading and exploration
2. Feature scaling and preprocessing
3. Handling class imbalance using SMOTE
4. Training multiple ML models:
   - Logistic Regression
   - Random Forest
   - XGBoost
5. Model evaluation using:
   - Precision
   - Recall
   - F1-score
   - Confusion Matrix
   - ROC-AUC Curve
6. Deployment of a simple Gradio interface for real-time prediction

---

## Model Evaluation
- Accuracy is not used as the primary metric due to class imbalance
- Emphasis is placed on **recall** to reduce missed fraud cases
- ROC-AUC is used to evaluate ranking capability of the model

---

## Results
The XGBoost model achieved strong performance with high recall and ROC-AUC, making it suitable for fraud detection tasks where minimizing false negatives is critical.

---

## How to Run
1. Open the notebook in Google Colab
2. Run all cells sequentially
3. The dataset is automatically downloaded
4. Gradio interface launches for testing predictions

---

## Limitations
- PCA features are not human-interpretable
- Model may not detect completely new fraud patterns
- Further improvements can include anomaly detection or threshold tuning

---

## Author
Developed as an academic and portfolio project to demonstrate applied machine learning in financial fraud detection.
