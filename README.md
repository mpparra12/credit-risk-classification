# Credit-Risk-Classification

# Background

In this Challenge, you’ll use various techniques to train and evaluate a model based on loan risk. You’ll use a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

# Instructions

The instructions for this Challenge are divided into the following subsections:

Split the Data into Training and Testing Sets

Create a Logistic Regression Model with the Original Data

Write a Credit Risk Analysis Report


# Split the Data into Training and Testing Sets

Open the starter code notebook and use it to complete the following steps:

Read the lending_data.csv data from the Resources folder into a Pandas DataFrame.

Create the labels set (y) from the “loan_status” column, and then create the features (X) DataFrame from the remaining columns.

Split the data into training and testing datasets by using train_test_split.

# Create a Logistic Regression Model with the Original Data

Use your knowledge of logistic regression to complete the following steps:

Fit a logistic regression model by using the training data (X_train and y_train).

Save the predictions for the testing data labels by using the testing feature data (X_test) and the fitted model.

Evaluate the model’s performance by doing the following:

Generate a confusion matrix.

Print the classification report.

Answer the following question: How well does the logistic regression model predict both the 0 (healthy loan) and 1 (high-risk loan) labels?

# Write a Credit Risk Analysis Report

Write a brief report that includes a summary and analysis of the performance of the machine learning models that you used in this homework. You should write this report as the README.md file included in your GitHub repository.

Structure your report by using the report template that Starter_Code.zip includes, ensuring that it contains the following:

An overview of the analysis: Explain the purpose of this analysis.

The results: Using a bulleted list, describe the accuracy score, the precision score, and recall score of the machine learning model.

A summary: Summarize the results from the machine learning model. Include your justification for recommending the model for use by the company. If you don’t recommend the model, justify your reasoning.


# Overview of the Analysis

The analysis considered various factors such as loan size, interest rate, borrower's income, debt-to-income ratio, number of accounts, derogatory marks, and total debt as independent variables (X). These variables were used to train two models to predict loan status (y), where 0 represents a healthy loan and 1 indicates a high risk of default.

The first model employed logistic regression and sampled the data points once for prediction. The second model utilized the Random Over Sampler technique, which involved using some data points more than once to balance the counts of the minority class (high-risk loans). This resampled data was then subjected to logistic regression with the aim of improving overall accuracy, particularly in identifying high-risk loans.

# Results

Machine Learning Model 1:

* Overall Accuracy: 0.95.
* Precision: for healthy loans, the precision is 1.00 and for high-risk loans, the precision is 0.85.
* Recall: for healthy loans, the recall score is 0.99 and for high-risk loans, the recall score is 0.91.
* F1-Score: for healthy loans, the f1-score is 1.00, for high-risk loans, the f1-score is 0.88.

Machine Learning Model 2 (Resampled Data):

* Overall Accuracy: 0.99.
* Precision: for healthy loans, the precision is 1.00 and for high-risk loans, the precision is 0.84.
* Recall: for healthy loans, the recall score is 0.99 and for high-risk loans, the recall score is 0.99.
* F1-Score: for healthy loans, the f1-score is 1.00 and for high-risk loans, the f1-score is 0.91.

# Summary

The logistic regression model with resampled data (Model 2) demonstrates precision of 100% for healthy, low-risk loans and 84% for high-risk loans, with a balanced accuracy of 100%. While the classification report overall remains similar between the two models, the notable change is the increase in balanced accuracy from 99% to 100%. However, caution is advised, as this improvement could be attributed to overfitting, emphasizing the need for additional cross-validation techniques to validate the models.

Model 2 is more adept at avoiding false negatives (missed high-risk loans). Despite slightly more false positives (predicting low-risk when the actual is high-risk) compared to Model 1, the overall lower rate of false predictions in the testing data makes Model 2 the preferable choice, particularly due to its high accuracy and recall in identifying high-risk loans. It's worth noting that neither model achieves precision above 90% for high-risk loans, acknowledging the inherent challenge of achieving extremely high precision in scenarios with imbalanced classes.