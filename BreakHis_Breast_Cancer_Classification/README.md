# BreakHis Breast Cancer Classification

This project classifies breast cancer histopathology images from the **BreaKHis** dataset as **benign** or **malignant** using transfer learning.

## Dataset

- Dataset: BreaKHis
- Total images: 7909
- Total patients: 82
- Classes: Benign, Malignant
- Magnification levels: 40X, 100X, 200X, 400X

Patient-level data leakage control was applied because multiple images belong to the same patient.

## Models

Two pretrained CNN models were compared:

- DenseNet121
- EfficientNetV2S

Both models were trained using transfer learning and fine-tuning. Class imbalance was handled with class weights, and data augmentation was applied only to the training set.

## Evaluation

The models were evaluated using:

- Accuracy
- ROC-AUC
- PR-AUC
- Precision
- Recall
- Specificity
- F1-score
- Balanced accuracy
- Confusion matrix
