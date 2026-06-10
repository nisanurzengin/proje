# Credit Card Fraud Detection

## Overview

This project aims to detect fraudulent credit card transactions using machine learning techniques on a highly imbalanced dataset.

The study focuses on handling class imbalance, comparing multiple machine learning models, and selecting the best-performing fraud detection approach.

---

## Dataset

* 284,807 credit card transactions
* 492 fraud cases
* Highly imbalanced classification problem

---

## Project Workflow

* Performed Exploratory Data Analysis (EDA)
* Analyzed transaction amount and time distributions
* Investigated feature correlations
* Split data into Train / Validation / Test sets
* Applied feature scaling
* Tested SMOTE and NearMiss sampling methods
* Compared Logistic Regression, Random Forest and XGBoost models
* Optimized model selection using Validation AUPRC
* Applied class-weighted learning using XGBoost

---

## Results

### Best Model

**XGBoost + SMOTE + Class Weighting**

### Final Performance

* AUPRC: 0.872
* Recall: 0.878

Key findings:

* SMOTE outperformed NearMiss.
* XGBoost achieved the best overall performance.
* AUPRC was more informative than accuracy for this imbalanced classification task.

---

## Technologies

* Python
* Pandas
* NumPy
* Scikit-Learn
* XGBoost
* Imbalanced-Learn
* Matplotlib
* Seaborn

---

## Skills Demonstrated

* Exploratory Data Analysis (EDA)
* Imbalanced Classification
* Feature Engineering
* Model Evaluation
* XGBoost
* Fraud Detection

