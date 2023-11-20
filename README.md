# Credit-Risk-Classification

# Background
In this Challenge, you’ll use various techniques to train and evaluate a model based on loan risk. You’ll use a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

# Instructions

The instructions for this Challenge are divided into the following subsections:

Split the Data into Training and Testing Sets

Create a Logistic Regression Model with the Original Data

Write a Credit Risk Analysis Report


# Overview of the Analysis
The analysis considered various factors such as loan size, interest rate, borrower's income, debt-to-income ratio, number of accounts, derogatory marks, and total debt as independent variables (X). These variables were used to train two models to predict loan status (y), where 0 represents a healthy loan and 1 indicates a high risk of default.

The first model employed logistic regression and sampled the data points once for prediction. The second model utilized the Random Over Sampler technique, which involved using some data points more than once to balance the counts of the minority class (high-risk loans). This resampled data was then subjected to logistic regression with the aim of improving overall accuracy, particularly in identifying high-risk loans.

# Results
Machine Learning Model 1:

*- Overall Accuracy: 0.99.
Precision: for healthy loans, the precision is 1.00, for high-risk loans, the precision is 0.87.
Recall: for healthy loans, the recall score is 1.00, for high-risk loans, the recall score is 0.89.
F1-Score: for healthy loans, the f1-score is 1.00, for high-risk loans, the f1-score is 0.88.
Machine Learning Model 2 (Resampled Data):

Overall Accuracy: 1.00.
Precision: for healthy loans, the precision is 1.00, for high-risk loans, the precision is 0.87.
Recall: for healthy loans, the recall score is 1.00, for high-risk loans, the recall score is 1.00.
F1-Score: for healthy loans, the f1-score is 1.00, for high-risk loans, the f1-score is 0.93.
