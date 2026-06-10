# Credit Card Fraud Detection Using Machine Learning

## Project Overview

This project focuses on detecting fraudulent credit card transactions using machine learning techniques. One of the main challenges of fraud detection is the highly imbalanced nature of the dataset, where fraudulent transactions represent only a very small fraction of all observations.

The objective of this project is to compare different machine learning approaches and sampling strategies to improve fraud detection performance while minimizing false negatives.

---

## Dataset

The dataset contains anonymized credit card transactions, including both legitimate and fraudulent operations.

Key characteristics:

* Highly imbalanced class distribution
* Fraud cases represent a very small percentage of total transactions
* Numerical features obtained through PCA transformation
* Transaction amount and transaction time information included

---

## Project Workflow

### 1. Exploratory Data Analysis (EDA)

* Investigated class distribution
* Examined transaction amount and time features
* Visualized data imbalance
* Identified challenges related to fraud detection

### 2. Data Preprocessing

* Train, validation and test split
* Feature scaling where required
* Prevention of data leakage during model development

### 3. Handling Class Imbalance

Different imbalance handling techniques were evaluated:

* Original dataset
* SMOTE (Synthetic Minority Oversampling Technique)
* NearMiss undersampling

Different sampling ratios were compared using validation performance.

### 4. Model Development

The following machine learning models were implemented and compared:

* Logistic Regression
* Random Forest
* XGBoost

Class-weighted learning strategies were also investigated to improve minority class detection.

### 5. Model Evaluation

Models were evaluated using metrics suitable for imbalanced classification:

* Precision
* Recall
* F1-Score
* ROC-AUC
* PR-AUC (AUPRC)

Special attention was given to Recall and PR-AUC because missing fraudulent transactions is more costly than generating false alarms.

---

## Results

Among the tested approaches, ensemble-based methods demonstrated stronger performance in detecting fraudulent transactions compared to baseline models.

The experiments showed that:

* Class imbalance significantly affects model performance.
* Sampling techniques can improve fraud detection capability.
* PR-AUC is a more informative metric than accuracy for fraud detection tasks.
* Model selection should prioritize fraud capture performance rather than overall accuracy.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-Learn
* XGBoost
* Matplotlib
* Seaborn

---

## Skills Demonstrated

* Exploratory Data Analysis (EDA)
* Data Preprocessing
* Imbalanced Learning
* Feature Analysis
* Machine Learning Model Development
* Model Evaluation and Comparison
* Fraud Detection Analytics

---

## Author

Nisa Zengin

Yildiz Technical University – Control and Automation Engineering

