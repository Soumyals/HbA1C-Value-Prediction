# HbA1C-Value-Prediction

Predicting HbA1c (glycated hemoglobin) values using clinical and demographic features.  
This repository contains exploratory analysis and regression modeling notebooks that demonstrate linear regression and regularized regression (Lasso / Ridge) approaches.

## Table of contents
- [Project Overview](#project-overview)
- [Files](#files)
- [Data](#data)
- [Methods](#methods)
- [How to run](#how-to-run)
- [Reproducibility & Environment](#reproducibility--environment)
- [Results](#results)
- [Model Evaluation](#model-evaluation)
- [Potential Improvements](#potential-improvements)
- [License](#license)
- [Contact](#contact)

## Project Overview
This project explores prediction of HbA1c values (a measure of long-term blood glucose control) from available clinical/demographic features. Two main approaches are included:
1. Ordinary Least Squares Linear Regression (baseline)
2. Regularized regression with Lasso and Ridge (to control overfitting and perform feature selection)

Goals:
- Understand feature relationships with HbA1c
- Build baseline and regularized regression models
- Compare performance using appropriate regression metrics

## Files
- `Diabetes_linearregression.ipynb` — EDA, feature engineering, baseline linear regression, residual analysis, and evaluation.
- `Diabetes_lasso_ridge.ipynb` — Lasso and Ridge regression experiments with hyperparameter tuning (e.g., cross-validation) and comparison with baseline.
- (Optional) `requirements.txt` — list of Python dependencies (see Reproducibility section).

## Data
> **Note:** The notebooks expect a dataset (CSV or DataFrame). Replace `data.csv` with your actual file name.

Typical columns expected:
- `age`, `sex`, `bmi`, `blood_pressure`, `glucose`, `insulin`, `cholesterol`, `smoking_status`, `HbA1c` (target)
- Any other lab or demographic features available in your dataset.

If the dataset is not included in the repo, add a short `data/README.md` describing the source and column meanings or include a small sample CSV.

## Methods
The notebooks follow the usual supervised learning flow:

1. **Exploratory Data Analysis (EDA)**
   - Summary statistics
   - Missing values report and visualizations
   - Target distribution (HbA1c)
   - Correlation matrix / heatmap

2. **Preprocessing**
   - Handling missing values (drop/impute)
   - Encoding categorical variables (one-hot or ordinal)
   - Feature scaling (StandardScaler for models that need it)
   - Train/test split (e.g., 80/20) or cross-validation

3. **Baseline model**
   - LinearRegression from scikit-learn
   - Fit on training set, evaluate on test set

4. **Regularized models**
   - Lasso (L1) and Ridge (L2)
   - Hyperparameter tuning (GridSearchCV or cross_val_score over alpha/λ values)

5. **Evaluation**
   - Metrics: MAE (Mean Absolute Error), MSE (Mean Squared Error), RMSE, R²
   - Residual plots and diagnostics

## How to run
1. Clone the repo:
   ```bash
   git clone https://github.com/Soumyals/HbA1C-Value-Prediction.git
   cd HbA1C-Value-Prediction
