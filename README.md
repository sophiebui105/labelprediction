# Data Mining Assignment: Data Preparation and Classification

This project focuses on data preparation and classification as part of a practical data mining assignment. The primary goal is to predict the target label (`class`) in a dataset using various machine learning techniques, addressing challenges such as missing values, duplicates, class imbalance, and feature extraction.

## Table of Contents
- [Overview](#overview)
- [Data Preparation](#data-preparation)
- [Data Classification](#data-classification)
- [Models Used](#models-used)
- [Key Results](#key-results)
- [Lessons Learned](#lessons-learned)
- [Setup and Usage](#setup-and-usage)
- [Future Work](#future-work)

---

## Overview
- **Dataset**: 5000 training samples and 32 attributes with missing values, duplicates, and class imbalance.
- **Objective**: Predict the `class` column for 500 test samples using machine learning models.
- **Steps**: The project is divided into two main parts:
  - **Data Preparation**: Cleaning, encoding, feature extraction, and standardization.
  - **Data Classification**: Training and evaluating models using stratified K-fold cross-validation.

---

## Data Preparation
Key steps:
1. **Handling Missing Values**:
   - Attributes with >20% missing values (`Oven` and `Office`) were dropped.
   - Missing values in `Tennis` (1% missing) were replaced with the column mean.
2. **Duplicate Removal**:
   - 50 duplicates were removed from the training data.
3. **Encoding**:
   - Label Encoding for categorical columns (`Music`, `Storage`, `Guitar`).
   - One-Hot Encoding to avoid ordinal biases.
4. **Feature Extraction**:
   - Highly correlated attributes (correlation > 0.8) were removed.
5. **Standardization**:
   - Numerical features were scaled to zero mean and unit variance.

---

## Data Classification
### Challenges:
- **Class Imbalance**:
  - The `class` column was imbalanced, addressed using **SMOTE** (Synthetic Minority Oversampling Technique).
- **Model Selection**:
  - Stratified K-fold cross-validation ensured class balance during model training.

### Models Used:
1. **K-Nearest Neighbors (KNN)**
2. **Decision Tree**
3. **Naïve Bayes**
4. **Random Forest**

---

## Key Results
- **Best Models**:
  - **KNN**: Accuracy = 82.54%
  - **Random Forest**: Accuracy = 91.64%
- The predictions for the test data are stored in the `Predict1` (Random Forest) and `Predict2` (KNN) columns of the output file.

---

## Lessons Learned
- Effective data cleaning improves model reliability and prediction accuracy.
- Techniques like **SMOTE** and **Stratified K-fold Cross-Validation** are crucial for handling imbalanced datasets.
- Parameter tuning and feature extraction significantly impact model performance.
- Random Forest and KNN demonstrated their robustness in handling this dataset.

---
