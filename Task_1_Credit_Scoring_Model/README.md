
# Credit Scoring Model

## CodeAlpha Machine Learning Internship — Project 1

## Project Overview

This project develops a machine learning-based credit scoring model to classify applicants into **Good Credit** and **Bad Credit** categories using financial and customer-related information.

The project follows an end-to-end machine learning workflow, including data acquisition, exploratory data analysis, preprocessing, model training, evaluation, cross-validation, feature importance analysis, and final prediction.

---

## Problem Statement

Financial institutions need reliable methods to assess the credit risk of applicants before approving loans or credit facilities.

The objective of this project is to develop a classification model that can identify potentially risky credit applicants based on historical financial and customer-related attributes.

---

## Dataset

The project uses the **Statlog (German Credit Data)** dataset from the **UCI Machine Learning Repository**.

### Dataset Information

- Dataset: Statlog (German Credit Data)
- Number of instances: 1,000
- Number of features: 20
- Target classes: Good Credit and Bad Credit
- Missing values: 0

### Target Encoding

The original target values were encoded as:

- `0` = Good Credit
- `1` = Bad Credit

### Target Distribution

- Good Credit: 700 (70%)
- Bad Credit: 300 (30%)

### Dataset Attribution

Hofmann, H. (1994). Statlog (German Credit Data). UCI Machine Learning Repository.

DOI: 10.24432/C5NC77

---

## Features

The dataset contains both numerical and categorical attributes.

### Numerical Features

- Duration in months
- Credit amount
- Installment rate
- Residence duration
- Age
- Existing credits
- Dependents

### Categorical Features

- Checking account status
- Credit history
- Purpose
- Savings account
- Employment duration
- Personal status/sex
- Other debtors
- Property
- Other installment plans
- Housing
- Job
- Telephone
- Foreign worker

---

## Exploratory Data Analysis

The following analyses were performed:

- Credit risk distribution
- Numerical feature statistics
- Numerical feature distributions
- Correlation analysis
- Missing-value analysis
- Duplicate-value analysis

### Data Quality

| Data Quality Check | Result |
|---|---:|
| Total records | 1,000 |
| Total features | 20 |
| Missing values | 0 |
| Duplicate rows | 0 |
| Numerical features | 7 |
| Categorical features | 13 |

---

## Machine Learning Workflow

The project follows these steps:

1. Dataset acquisition
2. Data inspection
3. Target encoding
4. Feature renaming
5. Exploratory Data Analysis
6. Train-test splitting
7. Numerical feature scaling
8. Categorical feature one-hot encoding
9. Model training
10. Model evaluation
11. Confusion matrix analysis
12. ROC-AUC analysis
13. Five-fold cross-validation
14. Feature importance analysis
15. Final model selection
16. Credit risk prediction demonstration

---

## Models Evaluated

Three classification algorithms were evaluated:

1. Logistic Regression
2. Decision Tree
3. Random Forest

Class balancing was applied during model training to improve the handling of the imbalanced target distribution.

---

## Model Performance

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC

| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|---|---:|---:|---:|---:|---:|
| Logistic Regression | 75.00% | 55.81% | 80.00% | 65.75% | 80.58% |
| Decision Tree | 58.00% | 36.36% | 53.33% | 43.24% | 59.78% |
| Random Forest | 75.50% | 66.67% | 36.67% | 47.31% | 79.61% |

---

## Final Model Selection

### Logistic Regression

**Logistic Regression** was selected as the final model.

It achieved:

- Accuracy: **75.00%**
- Precision: **55.81%**
- Recall: **80.00%**
- F1-Score: **65.75%**
- ROC-AUC: **80.58%**

The model achieved the highest recall, F1-score, and ROC-AUC among the three evaluated models.

The higher recall is particularly useful for identifying a larger proportion of applicants belonging to the Bad Credit class.

---

## Google Colab Link
https://colab.research.google.com/drive/1SC-9-T0bwzPUOCe_zyk0YeASNgvDE6tI?usp=sharing

## Confusion Matrix

The final Logistic Regression model produced the following confusion matrix on the 200-sample test set:

```text
[[102  38]
 [ 12  48]]

## Conclusion

This project successfully developed and evaluated machine learning models for credit risk classification using the Statlog (German Credit Data) dataset. Three classification algorithms—Logistic Regression, Decision Tree, and Random Forest—were implemented and compared using accuracy, precision, recall, F1-score, and ROC-AUC.

Among the evaluated models, Logistic Regression was selected as the final model because it achieved the highest recall (80.00%), F1-score (65.75%), and ROC-AUC (80.58%). The confusion matrix shows that the model correctly identified 48 out of 60 Bad Credit applicants while maintaining a reasonable overall accuracy of 75.00%.

The project demonstrates an end-to-end machine learning workflow for credit risk classification, from data preprocessing and exploratory analysis to model evaluation, cross-validation, feature importance analysis, and final prediction.

## Author

**Saripalle Suresh**

Machine Learning Intern — CodeAlpha

## Internship Project

**CodeAlpha Machine Learning Internship — Project 1**
