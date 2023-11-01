# credit-risk-classification
Repo for Module 20 Assignment

This repo contains the resources folder that contains the data used for the analysis, the Jupyter Notbook file used to perform the analysis, and this Readme containing the written analysis of the results below. 

**Written Analysis**

## Analysis Overview

The purpose of this analysis was to use machine learning models to explore peer-to-peer leaning services data and predict whether a loan is high-risk or healthy.

The financial information used in this analysis for our x-values included the loan size (amount of the loan), the interest rate on that loan, the borrower's income, the ratio of debt to income, the number of accounts, the number of derogatory marks, and the total debt. The loan status, our y-variable was classified by either a 0 (healthy loan) or 1 (high-risk loan). 

In total, there were 75,036 - healthy loans and 2,500 high-risk loans in the data set that were used to train the model. 

In the analysis, our x and y values were seperated. The data was then split into train and tests groups with a random state of 1. Once split the daata was fit to a logistic regression model and predictions were made based on that model. Once predictions were made, the balanced accuracy score, a confusion matrix and a classification report were created to show the accuracy of the model. 

This same process was done on resampeled data using RandomOversample to create a more balanced data set of target labels. In this resample there were 56,271 healthy loans and the same number of high-risk loans used to create new test data and new predictions to evaluate the accuracy of the model. 

## Results

* Machine Learning Model 1 - Original Data:
  * Balanced Accuracy: 0.99
  * Accuracy: 0.99
  * Precision: 1.00 healthy loans, 0.85 high-risk loans
  * Recall: 0.99 healthy loans, 0.91 high-risk loans

* Machine Learning Model 2 - Resampled Data:
  * Balanced Accuracy: 0.99
  * Accuracy: 0.99
  * Precision: 1.00 healthy loans, 0.84 high-risk loans
  * Recall: 0.99 healthy loans, 0.99 high-risk loans

## Summary

Both models have high accuracy in predicting healthy vs. high-risk loans. For both models, the models have more difficulty correctly predicting high-risk loans, more often mislabeling a high-risk loan as a healthy loan (a false positive) vs. a healthy loan as a high-risk loan (a false negative). The first model with the original data has even more dificulty with this likely because there are so fewer instances of high-risk data available (2500 high risk data points vs. 75,036 healthy data points).

While the difference is very small, I recommend using Model 2 with resampled data because more healthy lendees will be able to be approved for loans (meaning more money for the bank or lender). This will outweigh the slight difference in high-risk lenders who will be labeled as healthy (16% in model 2, vs 15% in model 1). Model 2 overall was able to find more instances of high-risk loans than model 1 (based on recall) - meaning even though there is some slight mislabeling, overall model 2 catches more high risk cases than model 1. 
