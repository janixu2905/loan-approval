# 🌲 Loan Approval Prediction using Random Forest

A machine learning project that predicts whether a loan application will be **Approved** or **Not Approved** using a Random Forest Classifier.

The project includes data preprocessing, model training, evaluation, feature-importance analysis, and an interactive web dashboard for visualizing the model's performance.

## 🚀 Project Overview

The model was trained on **598 loan applications** using an 80/20 train-test split.

* **Algorithm:** Random Forest Classifier
* **Number of trees:** 100
* **Train samples:** 478
* **Test samples:** 120
* **Features:** 12
* **Test Accuracy:** 79.2%
* **ROC-AUC:** 0.774

## 📊 Model Evaluation

### Confusion Matrix

|                       | Predicted Rejected | Predicted Approved |
| --------------------- | -----------------: | -----------------: |
| **Actually Rejected** |                 15 |                 20 |
| **Actually Approved** |                  5 |                 80 |

### Classification Metrics

| Class        | Precision | Recall | F1-Score |
| ------------ | --------: | -----: | -------: |
| Not Approved |       75% |    43% |      55% |
| Approved     |       80% |    94% |      86% |

The model performs substantially better at identifying approved applications than rejected applications in this particular test split.

## 🔍 Feature Importance

The most influential features according to the Random Forest's Gini importance were:

1. **Credit History — 26.3%**
2. **Applicant Income — 20.7%**
3. **Loan Amount — 18.4%**
4. **Coapplicant Income — 11.3%**
5. **Dependents — 4.8%**

These values represent the model's feature-importance calculation and should not be interpreted as causal relationships.

## 🧹 Data Preprocessing

The dataset contained missing values in several columns, including:

* Dependents
* Loan Amount
* Loan Amount Term
* Credit History

Numeric values were handled using median imputation, while categorical values were handled using mode-based replacement.

## 🖥️ Dashboard

The project includes an interactive dashboard showing:

* Model accuracy
* ROC-AUC
* Dataset statistics
* Confusion matrix
* Classification metrics
* Feature importance
* Approval rates by different attributes
* Missing-value information
* Multiple visual themes

### Dashboard Preview

![Loan Approval Dashboard](images/dashboard.png)

Open `dashboard/index.html` in a browser to view the dashboard.

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Random Forest
* HTML
* CSS
* JavaScript

## 📌 What I Learned

Through this project, I practiced:

* Preparing a real-world tabular dataset
* Handling missing values
* Splitting data into training and testing sets
* Training a Random Forest classifier
* Understanding classification metrics
* Reading a confusion matrix
* Comparing precision, recall and F1-score
* Understanding feature importance
* Building a dashboard to communicate ML results

## ⚠️ Disclaimer

This project is intended for educational purposes. The predictions and model metrics should not be used for real-world lending decisions without appropriate validation, fairness analysis, regulatory compliance, and additional financial-domain safeguards.
