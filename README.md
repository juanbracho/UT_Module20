# UT_Module20
# Credit Risk Classification

## Overview

This repository contains a machine learning project focused on predicting the creditworthiness of loan applicants. Using historical lending data from a peer-to-peer lending platform, we developed a Logistic Regression model to classify loans as either "healthy" (low-risk) or "high-risk." The goal of this analysis is to assist the company in managing credit risk more effectively by identifying high-risk loans early on, thereby informing lending decisions and reducing potential financial losses.

## Files in the Repository

- **credit_risk_classification.ipynb**: Jupyter Notebook with the code for data loading, preprocessing, model training, prediction, and evaluation.
- **lending_data.csv**: Dataset used for training and testing the model. This file contains various financial attributes of loan applicants.
- **report-template.md**: Template for the credit risk analysis report, which includes summaries of the model’s performance metrics, interpretation, and recommendations.
- **README.md**: Overview of the repository and the purpose of the project (this file).

## Machine Learning Model

The model used for this analysis is Logistic Regression, chosen for its effectiveness in binary classification tasks like distinguishing between low-risk and high-risk loans. We trained the model on historical loan data, tuning it to optimize its performance in predicting the target variable, `loan_status`.

## Key Results

- **Accuracy**: 99% — The model correctly classified nearly all loans in the dataset.
- **Precision and Recall**:
  - **Class 0 (Healthy Loan)**: Precision = 1.00, Recall = 0.99
  - **Class 1 (High-Risk Loan)**: Precision = 0.84, Recall = 0.94

The model performed well, particularly in identifying high-risk loans with a high recall score. This characteristic is crucial in credit risk management, as it minimizes the chances of missing high-risk applicants.

## Recommendation

Based on the model’s strong performance, it is recommended for deployment. The model's high recall for high-risk loans is particularly beneficial for reducing credit risk, as it helps to flag risky applicants effectively. This tool can assist in improving the company's credit evaluation process by providing reliable insights into applicant risk levels.

## Usage

To reproduce the analysis, follow these steps:

1. Clone this repository.
2. Open the `credit_risk_classification.ipynb` notebook.
3. Run each cell in sequence to load the data, preprocess it, train the model, and evaluate its performance.

---

This project provides an example of using machine learning to solve a real-world business problem by improving risk assessment practices in lending.
