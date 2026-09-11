
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
- Duplicate rows: 0

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

## Data Preprocessing

The dataset contains both numerical and categorical variables.

The preprocessing pipeline applies:

- **StandardScaler** to numerical features
- **OneHotEncoder** to categorical features
- `handle_unknown="ignore"` for categorical encoding

The data was divided into training and testing sets using an **80:20 stratified split** with `random_state=42`.

This ensured that the class distribution was maintained between the training and testing sets.

---

## Models Evaluated

Three classification algorithms were evaluated:

1. Logistic Regression
2. Decision Tree
3. Random Forest

The models were compared using multiple evaluation metrics rather than relying only on accuracy.

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

Although Random Forest achieved slightly higher accuracy and precision, Logistic Regression achieved the highest recall, F1-score, and ROC-AUC among the evaluated models.

The higher recall is particularly useful for identifying a larger proportion of applicants belonging to the Bad Credit class.

---

## Confusion Matrix

The final Logistic Regression model produced the following confusion matrix on the 200-sample test set:

    [[102  38]
     [ 12  48]]

The model correctly classified:

- 102 Good Credit applicants as Good Credit
- 48 Bad Credit applicants as Bad Credit

It incorrectly classified:

- 38 Good Credit applicants as Bad Credit
- 12 Bad Credit applicants as Good Credit

The model therefore identified **48 out of 60 Bad Credit applicants**, resulting in a **Bad Credit recall of 80.00%**.

---

## Classification Report

The final Logistic Regression model achieved the following classification performance:

| Class | Precision | Recall | F1-Score |
|---|---:|---:|---:|
| Good Credit | 89% | 73% | 80% |
| Bad Credit | 56% | 80% | 66% |

Overall accuracy: **75%**

The model shows stronger recall for the Bad Credit class, which is important when the objective is to identify potentially risky applicants.

---

## Five-Fold Cross-Validation

Five-fold cross-validation was performed on the Logistic Regression model to evaluate the consistency of its performance across different data splits.

| Metric | Mean | Standard Deviation |
|---|---:|---:|
| Accuracy | 71.90% | 2.75% |
| Precision | 52.39% | 3.41% |
| Recall | 72.00% | 4.14% |
| F1-Score | 60.61% | 3.42% |
| ROC-AUC | 78.55% | 1.92% |

The cross-validation results indicate relatively consistent performance across the five folds.

---

## Feature Importance Analysis

Feature importance was analyzed using the absolute coefficients of the final Logistic Regression model.

The top contributing features were:

| Feature | Importance |
|---|---:|
| Purpose | 4.2958 |
| Savings Account | 1.9696 |
| Checking Account Status | 1.8917 |
| Credit History | 1.8181 |
| Employment Duration | 1.3897 |
| Property | 1.3538 |
| Foreign Worker | 1.2197 |
| Personal Status/Sex | 1.0065 |
| Housing | 1.0039 |
| Other Installment Plans | 0.9392 |

These values represent the magnitude of the model coefficients after preprocessing and help identify which transformed features contributed most strongly to the model's predictions.

---

## Sample Predictions

The final model was also tested on sample records to demonstrate individual credit-risk predictions.

| Sample | Actual | Predicted | Bad Credit Probability |
|---|---|---|---:|
| 30 | Good | Good | 40.66% |
| 128 | Good | Good | 18.67% |
| 289 | Bad | Bad | 78.13% |
| 216 | Good | Bad | 71.57% |
| 966 | Bad | Good | 31.02% |

These predictions demonstrate how the trained model can be used to classify individual applicants based on their input characteristics.

---

## Google Colab

The complete implementation is available in Google Colab:

https://colab.research.google.com/drive/1SC-9-T0bwzPUOCe_zyk0YeASNgvDE6tI?usp=sharing

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Google Colab
- GitHub

---

## Project Structure

    CodeAlpha_Credit-Scoring-Model/
    │
    ├── CodeAlpha_Credit_Scoring_Model.ipynb
    ├── README.md
    ├── requirements.txt
    └── results/

---

## Results

The project demonstrates a complete credit-risk classification workflow, including:

- Dataset analysis
- Data quality checking
- Exploratory data analysis
- Feature preprocessing
- Multiple machine learning models
- Model comparison
- Confusion matrix analysis
- ROC-AUC evaluation
- Five-fold cross-validation
- Feature importance analysis
- Sample credit-risk predictions

The final Logistic Regression model achieved **75.00% accuracy**, **80.00% recall**, **65.75% F1-score**, and **80.58% ROC-AUC** on the held-out test set.

---

## Limitations

The model is developed using a historical public dataset and should not be considered a production-ready financial decision system.

Real-world credit decisions require additional financial information, regulatory considerations, fairness analysis, continuous monitoring, and validation on current institutional data.

The predictions generated by this project are intended for educational and research purposes.

---

## Conclusion

This project successfully developed and evaluated machine learning models for credit risk classification using the Statlog (German Credit Data) dataset.

Three classification algorithms—Logistic Regression, Decision Tree, and Random Forest—were implemented and compared using accuracy, precision, recall, F1-score, and ROC-AUC.

Among the evaluated models, Logistic Regression was selected as the final model because it achieved the highest recall (**80.00%**), F1-score (**65.75%**), and ROC-AUC (**80.58%**).

The confusion matrix shows that the model correctly identified **48 out of 60 Bad Credit applicants**, demonstrating its ability to detect a substantial proportion of potentially risky applicants.

The project demonstrates an end-to-end machine learning workflow, from dataset acquisition and exploratory analysis to preprocessing, model comparison, cross-validation, feature importance analysis, and final credit-risk prediction.

---

## Author

**Saripalle Suresh**

Machine Learning Intern — CodeAlpha

## Internship Project

**CodeAlpha Machine Learning Internship — Project 1**
