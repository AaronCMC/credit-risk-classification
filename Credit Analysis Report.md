# Credit Analysis Report

## Overview of the Analysis

**Purpose:**

* Train and evaluate a model based on loan risk data (historical financial data) to successfully predict creditworthiness of borrowers (i.e. loan status: healthy or high-risk)

**Financial Data:**

* Label or Target Variable ("y" variable)
  * loan status (i.e. healthy or high-risk)
    * Note: dataset is heavily skewed towards loans with a healthy status, as opposed to high-risk status (75,036 healthy loans vs 2500 high-risk loans)
* Features ("X" variable)
  * loan size
  * interest rate
  * borrower income
  * debt to income ratio
  * number of accounts
  * derogatory marks
  * total debt

**Stages of Machine Learning Process:**

1. Load dataset into a Pandas DataFrame.
2. Separate data into independent (X) varables and dependent (Y) target varables.
3. Split 'X' and 'y' data (and stratified) into training and testing datasets.
4. Create a logistic regression model and fit it with 'X' and 'y' training data.
5. Predict target variables with the trained model using 'X' testing data.
6. Evaluate model's performance by comparing 'y' testing data and predicted target variables via a confusion matrix and classification report.

The logistic regression model is a statistical model used to predict the probability of a binary outcome based on one or more independent variables. It is commonly used in finance to predict loan defaults, helping lenders assess the likelihood of borrowers defaulting on their loans based on various factors.

## Results

**Logistic Regression Model:**

* Precision:
  * Healthy Loans: 100% (rounded up) of instances predicted as healthy were actally healthy.
  * High-Risk Loans: 87% of instances predicted as high-risk were actually high-risk.
* Recall:
  * Health Loans: 100% (rounded up) of all actual healthy loans were correctly predicted.
  * High-Risk Loans: 95% of actual high-risk loans were correctly predicted.
* Accuracy:
  * Overall: 99% of all loan instances were correctly predicted

## Summary

The logistic regression model fitted with the original training data performed extremely well in predicting healthy loans, with a score of 100% in both precision and recall. There are 18,673 true positives, 32 false positives, and 86 false negatives.

The model also scored well in predcting high-risk loans, however precision and recall were less at 85% and 91% respectively. There are 593 true negatives, but 86 false negatives, and 32 false positives. As such, there is room for improvement in predicting negatives.

Overall, the accuracy of the model is 99%. Note, the distribution of the data is heavily skewed towards the healthy loan status classification as reflected by the support scores of 18,759 for healthy loans, and 625 for high-risk loans. Consequently, the macro avg scores are lower then the weighted average scores.

With regards to predicting loan status (healthy vs high-risk), it is more important to be able to accurately identify high-risk loans, as these need be flagged by creditors.
