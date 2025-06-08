# 🎯 Regression Modeling: Predicting Continuous Target 'y'

This project tackles a regression problem involving 100,000 data points and 304 anonymized features labeled `x001` to `x304`. The goal was to predict the target variable `y` using machine learning techniques, then evaluate and communicate the methodology, results, and assumptions clearly.

---

## 📦 Dataset Summary

* **Shape**: (100000, 305)
* **Features**: `x001` to `x304` (numerical, anonymized)
* **Target**: `y` (continuous numerical value)

---

## 🚧 Assumptions

* Dataset contains no missing values.
* All features are numerical and ready for model consumption.
* No external feature engineering was attempted due to lack of semantic context.
* Final test data (hold-out set) will follow the same structure.

---

## 🔍 Methodology

1. **Exploratory Data Analysis**

   * Checked for missing values and feature distributions.
   * Visualized target distribution.

2. **Preprocessing**

   * No categorical encoding required.
   * Standard scaling was not applied due to tree-based model usage.

3. **Modeling Approaches**

   * Baseline: **Linear Regression**
   * Tree-based: **Decision Tree**, **Random Forest**
   * Evaluated using RMSE and a custom accuracy metric.

---

## 📊 Evaluation Metrics

### 1. **Root Mean Square Error (RMSE)**

* Standard metric to measure regression performance.

### 2. **Custom Accuracy**

* Defined as: A prediction is "correct" if |predicted − actual| ≤ 3.0
* Accuracy = (Number of Correct Predictions / Total Predictions) × 100
* Calculated only for Linear Regression in this submission.

---

## ✅ Final Model: Random Forest Regressor

Chosen for its robustness and superior performance in validation tests.
Model was trained using `RandomForestRegressor` from scikit-learn.

All code has been modularized and saved to support future inference on any similarly structured dataset.

---

## 📈 Performance Summary

| Model             | RMSE  | Notes                         |
| ----------------- | ----- | ----------------------------- |
| Linear Regression | 46.95 | Also included custom accuracy |
| Decision Tree     | 38.49 | Better than Linnear Regression|
| Random Forest     | 28.83 | Final selected model          |

---

## 🧠 Observations

* Linear Regression is limited by its inability to capture non-linear patterns.
* Decision Trees are prone to overfitting on high-dimensional data.
* Random Forest strikes a balance between bias and variance, making it a robust choice.

---

## 📁 Contents

* `Data Science Test Dataset.ipynb`: Analysis, modeling, and results
* `final_model.joblib`: Serialized Random Forest model
* `predict_holdout.py`: Script for running predictions on unseen data
* `predicted_y.txt`: Example output predictions

---

## 🧾 Author Note

This project emphasizes clarity of thought, clean implementation, and a bias for practical models over flashy techniques. It reflects not only technical skill, but the ability to reason through ambiguity — as demanded by the task.

> *“Precision is not in the model, it’s in the mind that designs it.”*
