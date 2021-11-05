# Module 12 Report Template

## Overview of the Analysis

The purpose of this analysis is to create a model that accurately predicts whether an incoming loan will inevitably be a healthy loan or whether it will be a high-risk or dangerous loan to make. 

We started with a dataset that contained lending information for past loan customers. Each row of the dataset contained a label regarding whether the loan was a healthy(0) or high-risk(1) loan. We wanted to be able to predict whether future lendees would fall into the healthy or high-risk category based on the same features. The features that were used in our model are:
+ Loan Size
+ Interest Rate
+ Borrower Income
+ Debt to Income
+ Number of Accounts
+ Deragatory Marks
+ Total Debt

Heading into the analysis we knew that our dataset contained imbalanced data. That is, the amount of healthy loans far out-numbered the amount of high-risk loans. The high risk loans only made up about 3% of the total loans. For this reason we had to make sure that our model didn't over-favor the healthy loans or overfit itself to healthy loan criteria and therfore miss all of the high-risk loans. 

In the loan situation, the cost of failure is most likely highest when a high-risk loan is missed and eventually defaults. Therefore, we would rather identify all of the high-risk loans with the risk of also identifying some healthy loans in that basket.

With all of this in mind, we used Logistic Regression to model the data and then resampled the data using a random oversampler. We compared the orignal logistic regression predictions to the oversampled logistic regression predictions to determine which model worked better. 

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
+ Model 1 - Logistic Regression Model fit to the original data.
    + Accuracy Score: 95%
    + Average Precision Score: 99%
        + Healthy Loan Precision: 100%
        + High-Risk Loan Precision: 85%
        


* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.
