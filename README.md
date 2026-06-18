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

```text

hospital-readmission-diabetes/

├── README.md

├── requirements.txt

├── data/

│   └── diabetic_data.csv

├── notebooks/

│   └── hospital_readmission_prediction.ipynb

├── src/

│   └── hospital_readmission_prediction.py

└── figures/

    ├── model_comparison_auc.png

    ├── model_comparison_f1.png

    ├── correlation_matrix.png

    └── numeric_feature_distributions.png

```

## How to Run

### 1. Clone the Repository

```bash

git clone git@github.com:YOUR-USERNAME/hospital-readmission-diabetes.git

cd hospital-readmission-diabetes

```

### 2. Install Dependencies

```bash

pip install -r requirements.txt

```

### 3. Launch Jupyter Notebook

```bash

jupyter notebook

```

Open:

```text

notebooks/hospital_readmission_prediction.ipynb

```

### 4. Dataset

The dataset (`diabetic_data.csv`) is included in the `data/` folder, so no additional downloads are required.

### 5. Reproduce Results

Run the notebook cells from top to bottom

## Author

Ushna Khan
