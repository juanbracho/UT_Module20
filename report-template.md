# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis:

The purpose of this analysis is to develop a machine learning model that can predict the creditworthiness of loan applicants based on historical data from a peer-to-peer lending platform.

* Explain what financial information the data was on, and what you needed to predict:

The dataset contains financial information related to loan applicants, specifically variables that provide insights into each applicant's financial situation and loan risk profile. Key features in the dataset include:
    * Loan Size: The amount of the loan requested by the applicant.
    * Interest Rate: The interest rate assigned to the loan.
    * Borrower Income: The income level of the borrower, which reflects their ability to repay.
    * Debt-to-Income Ratio: A measure of the applicant's monthly debt payments relative to their income.
    * Number of Accounts: The total number of credit accounts held by the applicant.
    * Derogatory Marks: The number of derogatory marks on the applicant’s credit history, such as late payments or defaults.
    * Total Debt: The total amount of debt held by the applicant.

* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).

The target variable we aimed to predict is loan_status, which indicates the credit risk level of a loan:
    * 0 (Healthy Loan): Represents low-risk loans that are expected to be repaid without issue. There are significantly more loans in this category.
    * 1 (High-Risk Loan): Represents loans with a higher likelihood of default. This is the minority class in the dataset.

* Describe the stages of the machine learning process you went through as part of this analysis.
The machine learning process for this analysis involved several key stages:

1. Data Preparation:
    * Loaded the dataset and examined its structure to understand the features and target variable.
    * Separated the data into features (predictors) and labels (target variable, loan_status).
2. Data Splitting:
    * Split the data into training and testing sets to evaluate the model's performance on unseen data. The training set was used to train the model, while the testing set was used to assess its predictive accuracy.
3. Model Selection and Training:
    * Chose Logistic Regression as the model due to its suitability for binary classification problems like this one.
    * Trained the model on the training data, adjusting parameters (e.g., max_iter) to ensure it converged properly.
4. Prediction:
    * Used the trained model to make predictions on the testing data. This step provided the predicted labels for each loan in the test set, allowing us to compare them against the actual labels.
5. Model Evaluation:
    * Evaluated the model’s performance using metrics such as accuracy, precision, recall, and F1-score. These metrics, particularly precision and recall for the high-risk class, helped assess the model's ability to distinguish between healthy and high-risk loans.
6. Interpretation and Recommendation:
    * Interpreted the evaluation metrics to understand the model's strengths and limitations.
    * Provided a recommendation based on the model's effectiveness in identifying high-risk loans, focusing on its suitability for deployment in a real-world credit risk assessment setting.

Each stage was essential to building a reliable model that could accurately classify loans, helping the company make informed lending decisions.

* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithms).

For this analysis, we used the Logistic Regression algorithm. Logistic Regression is a commonly used method for binary classification tasks, which makes it suitable for predicting the loan_status variable (healthy vs. high-risk loans). It calculates the probability of each class and assigns a label based on a threshold, allowing us to distinguish between low-risk and high-risk loans.

Logistic Regression was chosen for its simplicity, interpretability, and efficiency with binary classification problems. By tuning parameters like max_iter to ensure convergence, we achieved a high level of accuracy and reliable predictions for both loan categories.

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
    * Description of Model 1 Accuracy, Precision, and Recall scores.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.
