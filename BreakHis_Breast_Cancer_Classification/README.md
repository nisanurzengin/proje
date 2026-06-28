# BreakHis Breast Cancer Classification

This project classifies breast cancer histopathology images from the **BreaKHis** dataset as **benign** or **malignant** using deep learning.

## Dataset

The project uses the BreaKHis dataset, which contains breast tumor images at different magnification levels.

## Methods

In this project, patient-level data leakage control was applied. Two transfer learning models were trained and compared:

- DenseNet121
- EfficientNetV2S

The models were evaluated using common classification metrics such as accuracy, ROC-AUC, recall, specificity, F1-score, and confusion matrix.
