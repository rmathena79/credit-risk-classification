# credit-risk-classification
Data Analytics Boot Camp Module 20

## Contents
- **credit_risk_classification.ipynb**: Completed challenge notebook
- **Resources/lending_data.csv**: Data provided
- **report-template.md**: Template for report, used below
        
## Instructions
With a standard environment from class, just run all cells in credit_risk_classification.ipynb

# Report

## Overview of the Analysis

The purpose of this analysis is to create and evaluate a model for predicting credit worthiness of borrowers. This analysis is based on certain characteristics of loans and borrowers:

* Loan size
* Loan interest rate
* Borrower income
* Borrower debt-to-income ration
* Borrower number of accounts
* Borrower derogatory marks
* Borrower total debt

The prediction is to classify a loan as either "healthy" or "high-risk". Note these terms have not been defined in the source data.

To build the model, the features (listed above) are all scaled. Then features and labels are split into training (75%) and test (25%) sets. A Logistic Regression is done to build the model from the training data. Finally, predictions are done with the test feature set and compared to the test labels to measure the model's usefulness.

## Results

* Logistic Regression Model:
    * 

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
    * **Healthy Loans**: Precision 1.00, Recall 0.99, F-Scoare 1.00
    * **High-Risk Loans**: Precision 0.84, Recall 0.94, F-Scoare 0.89
    * **Macro Average**: Precision 0.92, Recall 0.97, F-Scoare 0.94
    * **Weighted Average**: Precision 0.99, Recall 0.99, F-Scoare 0.99
    * **Overall Accuracy**: 0.99

## Summary

If a loan is actually healthy, this model correctly determines it to be healthy over 99% of the time. So there is little risk of falsely classifying a loan as high-risk. Loans which are actually high-risk are harder to handle. Precision is only 0.84 in this category, meaning that 16% of the time, a high-risk loan will be incorrectly classified as healthy.

Overall, if the model predicts that a loan is high-risk, it can be trusted. But if it predicts that a loan is healthy, further analysis is recommended.

Recommendations depend on business needs. This model could be helpful to quickly reject most potential high-risk borrowers, but to further reduce the risk of issuing a high-risk loan, further analysis will be needed for any application who passes through that initial check. I do not recommend relying on this model to make final determinations of loan risk, since a significant number of high-risk loans will be incorrectly determined to be health.
