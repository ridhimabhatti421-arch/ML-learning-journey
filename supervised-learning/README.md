# Supervised Learning

Part of my [ML-learning-journey](../README.md). This notebook walks through the main supervised learning classifiers on a single binary classification problem.

## Problem
Classify high-energy particle events as gamma or hadron using the
[MAGIC Gamma Telescope dataset](https://archive.ics.uci.edu/dataset/159/magic+gamma+telescope) (UCI). Each sample has 10 numeric features ('fLength', 'fWidth', 'fSize', 'fConc', 'fConc1', 'fAsym', 'fM3Long', 'fM3Trans', 'fAlpha', plus the class label).

## What's covered
1. Dataset: loading, label encoding, and class-wise feature histograms
2. Train / Validation / Test split: 60% / 20% / 20%
3. Preprocessing: 'StandardScaler' and 'RandomOverSampler' (training set only) to fix class imbalance
4. Models
   - K-Nearest Neighbours (k=7)
   - Gaussian Naive Bayes
   - Logistic Regression
   - Support Vector Machine (SVC)
   - Neural Network (TensorFlow/Keras) with a grid search over nodes, dropout, learning rate and batch size

## Results (test set, 3,804 samples)

| Model                |   Accuracy |
|----------------------|----------|
| KNN (k=7)            | 0.81 |
| Naive Bayes          | 0.73 |
| Logistic Regression  | 0.77 |
| SVM                  | 0.85 |
| Neural Network       | see notebook |


## Tech stack
Python, pandas, NumPy, Matplotlib, scikit-learn, imbalanced-learn, TensorFlow/Keras

## Run it yourself
```bash
pip install pandas numpy matplotlib scikit-learn imbalanced-learn tensorflow
```