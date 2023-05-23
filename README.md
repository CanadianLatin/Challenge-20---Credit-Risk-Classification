# Challenge-20---Credit-Risk-Classification---Work
Challenge # 20. University of Toronto. Data Analisys Bootcamp



# Overview of the Analysis
Following is a basic overview of the analysis performed for credit risk classification:

*The purpose of this activity is use various techniques to train and evaluate a model based on loan risk. You’ll use a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

* Target is the data is the loan status for a Financial institution. 
  * The features in the financial data that are used to predict the loan status are:
        * Loan Size
        * Interest rate
        * Borrower Income
        *   Debt to Income Ratio
        *   Number of Accounts
        *   Derogatory marks
        *   Total debt.

* The target values of loan_status there are two variables to predict.
    1. Set of variables have a value of '0' (75036) healthy loans. 
    2. Set of variables have a value of '1' (2500)high risk or defaulting loans.

## ML (machine learning) process used to analyze is as follows:

* Create label sets and feature Dataframe from the provided dataset.
* Split the data into training and testing datasets by using train_test_split.
* Create a logistic regression model and fit our original data into the model.
* Make predictions on testing data labels by using the testing feature data and the fitted model.
* Evaluate the model's performance by calculating accuracy scores, confusion matrix, and classification report.
* First method used in this case is the LogisticRegression model on the original fitted data. As the data was highly overweighted towards one of the target variables (healthy loans), so RandomOverSampler was used to reduce the imbalances and LogisticRegression was then applied to the oversampled data.

# Results
This section describes the accuracy and balanced accuracy scores, and the precision and recall scores of the two machine learning models used for the acitivity:

* Machine Learning Model 1 - Logistic Regression:

  - Balanced accuracy score: 94.43%
  - Healthy Loan Precision: 100%, Healthy Loan Recall: 100%
  - High-Risk Loan Precision: 87%, High-Risk Loan Recall: 89%

Machine Learning Model 2 - RandomOverSampler:

  - Balanced accuracy score: 99.60%
  - Healthy Loan Precision: 100%, Healthy Loan Recall: 100%
  - High-Risk Loan Precision: 87%, High-Risk Loan Recall: 100%

# Summary
Based on the results described above The results indicate the second model (RandomOverSampler) works better as it has a higher accuracy porcentage and higher recall value for high-risk loans. It is critical for the models to be able to predict high-risk loans, as they can be eayly liabilities for the company. RandomOverSampler model has a very low number of false negatives and should be the one to use.
