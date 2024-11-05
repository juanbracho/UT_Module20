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

* Machine Learning Model 1: Logistic Regression\
    * Accuracy: 99% — The model correctly classified both healthy and high-risk loans in 99% of cases.
    * Precision:
        * Class 0 (Healthy Loan): 1.00 — All loans predicted as healthy were actually healthy.
        * Class 1 (High-Risk Loan): 0.84 — 84% of loans predicted as high-risk were indeed high-risk.
    * Recall:
        * Class 0 (Healthy Loan): 0.99 — The model successfully identified 99% of all healthy loans.
        * Class 1 (High-Risk Loan): 0.94 — The model captured 94% of all actual high-risk loans, effectively identifying most high-risk cases.

These metrics indicate that the Logistic Regression model is highly accurate and performs well in predicting both classes, with especially high recall for high-risk loans, making it valuable for managing credit risk.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. 

If you do not recommend any of the models, please justify your reasoning.

The Machine Learning Model demonstrates strong overall performance with high accuracy, precision, and recall. Based on the evaluation metrics, this model effectively distinguishes between healthy and high-risk loans, making it a suitable choice for the company’s needs.

* Performance Summary:
    * The model achieved 99% accuracy, indicating that it correctly classified loans in nearly all cases.
    * For healthy loans (Class 0), it demonstrated perfect precision (1.00) and high recall (0.99), meaning it accurately identifies and correctly labels most healthy loans.
    * For high-risk loans (Class 1), it achieved a precision of 0.84 and a recall of 0.94, showing it effectively identifies the majority of high-risk cases while maintaining a reasonable level of precision.
* Recommendation:
    * This model is recommended for deployment due to its ability to effectively identify high-risk loans (Class 1) with a high recall score. In the context of credit risk management, identifying high-risk loans is crucial to minimize potential financial losses. The high recall for high-risk loans ensures that most risky applicants are flagged, reducing the chance of issuing loans to potentially defaulting borrowers.
    * The slight trade-off in precision for high-risk loans (0.84) is acceptable within this context, as the model’s primary goal is to identify as many high-risk loans as possible. This approach prioritizes caution, even if some healthy loans are occasionally classified as high-risk.

In summary, the Logistic Regression model is recommended due to its high accuracy, especially in identifying high-risk loans, making it a valuable tool for improving the company's credit risk management strategy.