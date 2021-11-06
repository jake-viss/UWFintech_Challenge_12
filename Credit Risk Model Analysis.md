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

## Results

Below we highlight the important metrics for both our tested models.

+ Model 1 - Logistic Regression Model fit to the original data.
    + Accuracy Score: 95%
    + Average Precision Score: 99%
        + Healthy Loan Precision: 100%
        + High-Risk Loan Precision: 85%
    + Average Recall Score: 99%
        + Healthy Loan Recall: 99%
        + High-Risk Loan Recall: 91%  
        
+ Model 2 - Logistic Regression Model fit to the oversampled data.
    + Accuracy Score: 99%
    + Average Precision Score: 99%
        + Healthy Loan Precision: 100%
        + High-Risk Loan Precision: 84%
    + Average Recall Score: 99%
        + Healthy Loan Recall: 99%
        + High-Risk Loan Recall: 99%
  

## Summary

After comparing the performance of both models, our recomendation is to use Model 2 which uses the oversampled data to train the model. 

Prior to our analysis we determined that the most important thing to catch with our model was the actual high-risk loans (1's). The greatest cost to the business (regarding the loans) would be to misclassify a high-risk lendee as a healthy, good lendee. Therefore, we wanted to prioritize categorizing all the high-risk loans correctly even if that means categorizing some healthy loans incorrectly. 

Both models had similar scores across the board. They both performed quite well. However, Model 2 returned a higher recall score  for the high-risk loans and this was the determining factor in recomending this model. With a 99% recall score for the high-risk loans, it means the model correctly classified virtually all of the high-risk loans. 

