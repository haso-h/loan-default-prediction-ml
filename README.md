# Loan Default Prediction – Machine Learning Project

## Overview
This project demonstrates the complete process of building a **Machine Learning solution** for predicting the credit grade (`grade` A–G) of loans based on clients' financial and demographic data.  
It was developed in Python using popular libraries for data processing, analysis, and model building.

---

## Dataset
- **Number of samples:** 10,000 records  
- **Number of features:** 92 (loan amount, interest rate, employment length, annual income, home ownership status, credit history, and more)  
- **Target variable:** `grade` – credit grade of the loan (classes A–G).  
- The dataset is not included in this repository due to licensing restrictions. The notebook can be executed locally after adding the dataset to the `/data` directory.

---

## Data Preprocessing
- Removed columns that could lead to **data leakage** (e.g., total payment amounts, last payment dates).  
- Applied **log transformation** to skewed numerical variables (`annual_inc`, `revol_bal`).  
- Performed **one-hot encoding** for categorical variables.  
- Filled missing values.  
- **Standardized** all features using `StandardScaler`.  
- **Label encoded** the target variable (`A–G → 0–6`).  
- Split the data into **train (80%) and test (20%) sets** with stratification.

---

## Machine Learning Models
The project implements and compares several classification algorithms:

1. Logistic Regression  
2. Random Forest Classifier  
3. XGBoost Classifier  
4. Voting Ensemble (Soft Voting) – combining the best-performing models for aggregated predictions.  

For all models:
- **GridSearchCV** with 5-fold cross-validation was used for hyperparameter tuning.  
- Evaluation metrics include Accuracy, Precision (macro), Recall (macro), F1-score (macro).  
- **Confusion matrix** and **classification report** were generated for a detailed analysis.

