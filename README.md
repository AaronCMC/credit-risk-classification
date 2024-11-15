# credit-risk-classification

## Overview of the Analysis

## Results

Logistic Regression Model:

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
