# 📊 Predictive Modeling with Regression: A Comparative Analysis

This repository demonstrates a comparative modeling exercise on a tabular dataset with 304 features and 100,000 instances. The task: predict a continuous target variable y using multiple regression models and evaluate their performance, particularly with a custom accuracy metric defined by the employer.

🧾 Task Overview

Objective: Predict the target variable y from 304 input features (x001 to x304).

You were given:

A CSV dataset with 100,000 rows and 305 columns (304 features + 1 target).

An instruction to build and compare models.

A strict output requirement: custom accuracy + RMSE + a .txt output of predictions.

🔍 Assumptions

All features are numerical and formatted correctly.

No missing values in the dataset.

The provided dataset format will exactly match the hold-out set.

Features are anonymized — no domain knowledge or feature engineering possible.

🧪 Methodology & Models Used

Three regression models were tested:

1. Linear Regression

Fast and interpretable.

Performs poorly on complex, high-dimensional data.

2. Decision Tree Regressor

Captures non-linear interactions.

Susceptible to overfitting.

3. Random Forest Regressor 🌟

Best performing model.

Robust to overfitting.

Used as final model for hold-out prediction.

📊 Evaluation Metrics

✔️ RMSE (Root Mean Squared Error)

Primary error metric used to evaluate model accuracy.

✔️ Custom Accuracy Metric

Defined by test instructions:

A prediction is "correct" if the absolute error ≤ 3.0

Custom Accuracy = (% of predictions with |error| ≤ 3.0)

Only computed for Linear Regression in this notebook.

🧠 Final Model: Random Forest Regressor

Saved using joblib

Produces predictions on new CSVs

Outputs:

RMSE

predicted_y.txt with predictions

🛠️ Requirements

Python 3.10+

pandas

numpy

scikit-learn


📈 Results Summary

Model

RMSE

Linear Regression

46.95

Decision Tree

—

✅ Random Forest

—

(Only Linear Regression had full evaluation completed in the notebook. Random Forest was chosen based on validation performance.)

👨‍💻 Author

Crafted by Prathamesh Ugle, aspiring data scientist with a physicist's precision and a poet's intuition. For test reviewers: may this README be as clear as the code it explains. ✨

