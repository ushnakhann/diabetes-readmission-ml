# Predicting Hospital Readmission in Diabetic Patients

Machine learning project that predicts hospital readmission risk for diabetic patients using the Diabetes 130-US Hospitals Dataset from the UCI Machine Learning Repository.

## Overview

Hospital readmissions are a major challenge for healthcare systems, leading to increased costs and poorer patient outcomes.

This project uses demographic, clinical, and hospital utilization data from over 100,000 patient encounters to predict whether a diabetic patient will be readmitted after discharge.

The original multi-class target was converted into a binary classification problem:

- Readmitted
- Not Readmitted

The project evaluates multiple machine learning approaches and examines which factors contribute most to readmission risk.

## Dataset

Source:
- Diabetes 130-US Hospitals Dataset (1999–2008)
- UCI Machine Learning Repository

After cleaning and preprocessing:

- 67,329 patient encounters
- Demographic features
- Admission information
- Diagnosis codes
- Medication information
- Hospital utilization metrics

## Methods

### Data Preprocessing

- Removed invalid and missing records
- Converted categorical variables
- Grouped diagnosis codes into broader disease categories
- Created binary readmission target
- Feature engineering and transformation

### Class Imbalance Handling

- Baseline models
- SMOTE oversampling

### Models

- ZeroR Baseline
- Logistic Regression
- Random Forest
- Logistic Regression + SMOTE
- Random Forest + SMOTE

## Results

| Model | Accuracy | F1 Score | AUC |
|---------|---------|---------|---------|
| Logistic Regression | 0.615 | 0.320 | 0.625 |
| Random Forest | 0.614 | 0.417 | 0.624 |
| LR + SMOTE | 0.592 | 0.526 | 0.625 |
| RF + SMOTE | 0.610 | 0.445 | 0.622 |

### Key Findings

- Hospital utilization variables were among the strongest predictors.
- Number of medications, laboratory procedures, diagnoses, and length of stay contributed significantly.
- Demographic variables provided relatively limited predictive power.
- Class balancing improved recall but did not substantially improve overall AUC.

## Technologies

- Python
- Pandas
- NumPy
- Scikit-learn
- Imbalanced-learn (SMOTE)
- Matplotlib
- Seaborn

## Project Structure

project/
├── data/
├── notebooks/
├── src/
├── figures/
└── README.md

## Future Improvements

- XGBoost and LightGBM models
- Hyperparameter optimization
- Explainability with SHAP
- Deployment as a web application

## Author

Ushna Khan
