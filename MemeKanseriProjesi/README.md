# Breast Cancer Classification Using Deep Learning

## Overview

This project investigates breast cancer classification from histopathological images using deep learning techniques on the BreaKHis dataset.

A major focus of the study is preventing **patient-level data leakage** and obtaining reliable performance estimates through **Stratified Group K-Fold Cross Validation**.

---

## Dataset

**BreaKHis (Breast Cancer Histopathological Database)**

* Benign and Malignant tumor classes
* Multiple images per patient
* Histopathological breast tissue images

---

## Project Workflow

### Data Preparation

* Analyzed dataset folds and class distributions
* Extracted patient IDs from image filenames
* Performed patient-level overlap analysis
* Verified zero overlap between train, validation and test patients
* Resized images to 224×224 and normalized pixel values

### Initial DenseNet121 Experiment

* Built a DenseNet121 transfer learning model
* Evaluated performance using a patient-aware train/validation split
* Achieved approximately **0.82 Validation ROC-AUC**
* Performed ROC analysis, confusion matrix evaluation and learning curve analysis

### Overfitting Investigation

The initial DenseNet121 model showed strong training performance but weaker validation performance, indicating overfitting.

To improve generalization:

* Random Flip
* Random Rotation
* Random Zoom

augmentation techniques were applied.

### 5-Fold Cross Validation

Three architectures were compared:

* CNN
* EfficientNetB3
* DenseNet121

Using:

* Stratified Group K-Fold Cross Validation
* Patient-level separation
* ROC-AUC based evaluation

DenseNet121 achieved the strongest overall performance and was selected as the final model.

### Final Evaluation

The selected model was evaluated on the untouched test set to obtain an unbiased estimate of real-world performance.

---

## Technologies

* Python
* TensorFlow
* Keras
* Scikit-Learn
* Pandas
* NumPy
* Matplotlib

---

## Skills Demonstrated

* Deep Learning
* Medical Image Classification
* Transfer Learning
* Data Leakage Prevention
* Stratified Group K-Fold Cross Validation
* Model Comparison
* Overfitting Analysis
* TensorFlow Data Pipelines
* Performance Evaluation
