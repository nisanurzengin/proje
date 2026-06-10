# Breast Cancer Classification Using Deep Learning

## Project Overview

This project focuses on the classification of breast cancer histopathological images using deep learning techniques on the BreaKHis dataset.

The primary objective is to distinguish between benign and malignant breast tumor samples while ensuring a reliable evaluation process through patient-level data separation and robust validation strategies.

A major emphasis of this study was preventing patient-level data leakage, which is a common issue in medical imaging applications and can lead to overly optimistic performance estimates.

---

## Dataset

### BreaKHis Dataset

The BreaKHis dataset contains breast cancer histopathological images collected from multiple patients.

Characteristics:

* Benign and Malignant tumor classes
* Multiple images per patient
* Different magnification factors
* Medical image classification task

---

## Research Motivation

In medical imaging datasets, multiple images often belong to the same patient.

If images from the same patient appear in both training and testing sets, the model may learn patient-specific patterns rather than disease-related characteristics.

This issue is known as:

**Patient-Level Data Leakage**

Preventing this problem was one of the main goals of this project.

---

## Data Preparation

### Patient-Level Data Leakage Analysis

* Patient IDs were extracted from image filenames.
* Train, validation and test sets were analyzed separately.
* Patient overlap between datasets was checked.
* Zero overlap was verified before model training.

This ensured a realistic evaluation of model generalization performance.

### Image Preprocessing

* Image resizing (224 × 224)
* RGB conversion
* Pixel normalization
* TensorFlow data pipeline creation
* Batching, caching and prefetching

---

## Experimental Design

The project was conducted in three stages:

### Stage 1 – Initial DenseNet121 Analysis

The first objective was to understand the behavior of DenseNet121 on the dataset.

The following aspects were analyzed:

* Training performance
* Validation performance
* Error patterns
* Overfitting behavior
* Class-specific performance

### Stage 2 – Data Augmentation Experiments

To reduce overfitting and improve generalization:

* Random Flip
* Random Rotation
* Random Zoom

techniques were applied and evaluated.

### Stage 3 – 5-Fold Cross Validation

A patient-aware validation strategy was implemented using:

**Stratified Group K-Fold Cross Validation**

This approach ensured:

* Class balance preservation
* No patient overlap between folds
* More reliable performance estimation

---

## Models Evaluated

### DenseNet121

* Transfer Learning
* ImageNet pretrained weights
* Global Average Pooling
* Batch Normalization
* Dropout regularization

### EfficientNetB3

* Transfer Learning baseline

### Custom CNN

* Convolutional Neural Network architecture developed for comparison

---

## Model Evaluation

Performance was evaluated using:

* Accuracy
* Precision
* Recall
* ROC-AUC
* Confusion Matrix
* Classification Report

Special attention was given to Recall because missing malignant cases can have serious clinical consequences.

---

## Key Findings

### DenseNet121 Performance

* Validation ROC-AUC ≈ 0.82
* Strong malignant detection capability
* High sensitivity for cancerous samples

### Error Analysis

The model demonstrated:

* High recall for malignant tumors
* Lower recall for benign tumors
* A tendency to classify uncertain samples as malignant

### Overfitting Observation

Training and validation curves revealed:

* Strong training performance
* Validation plateau after early epochs
* Generalization limitations

These findings motivated the use of augmentation and cross-validation strategies.

---

## Technologies Used

* Python
* TensorFlow
* Keras
* Scikit-Learn
* NumPy
* Pandas
* Matplotlib

---

## Skills Demonstrated

* Deep Learning
* Medical Image Classification
* Transfer Learning
* Data Leakage Prevention
* Cross Validation
* Model Evaluation
* Error Analysis
* TensorFlow Pipeline Development
* Research-Oriented Experiment Design

---

## Author

Nisa Zengin

Yildiz Technical University

Control and Automation Engineering
