# Credit Risk Classification

## Overview
The purpose of this analysis is to classify a given loan as healthy or high-risk using supervised machine learning. This will be accomplished by utilization of a logistic regression model; the model will be trained based on financial information of past loans. The model will then be evaulated using resampled data to determine the performance of the model is affected. 

## Data
Description of features that the model will be trained on:
* _loan_size_: the original loan amount
* _interest_rate_: rate of interest 
* _borrower_income_: annual income of loan borrower
* _debt_to_income_: all monthly debt payments divided by borrower_income
* _num_of_accounts_: number of open accounts under borrower's name
* _derogatory_marks_: number of late payments or past due payments
* _total_debt_: total accumulated debt under loan

Our target feature:
* _loan_status_: loans marked as 0 are considered healthy loans while loans marked as 1 are considered high-risk loans.

## Machine Learning Process
### Methods
Methods to create and evaluate models will be used from: 
1. SKLearn: 
 * train_test_split
 * LogisticRegression
 * confusion_matrix
 * classification_report

2. imbalanced-learn
 * RandomOverSampler

The logistic regression model is a type of supervised learning. We will be using existing data in order to train a model to accurately predict the status of a loan. The data must first be split into training data and testing data to feed into the model. This means that our target variable (y) is the loan_status, and the rest of the dataset will be out features (X).  

In the original dataset, 75036 loans are marked as healthy, while 2500 loans are marked as high-risk. The distribution of healthy and high-risk loans is heavily skewed; in order to ensure that the data is properly split into training and testing data, we will using the _stratify_ parameter on our target feature in the instantiation of the Logistic Regression model.

![credit_risk_Screenshot](https://user-images.githubusercontent.com/114107454/235744288-507ac467-63a9-4ec3-b0c5-c4f5c1a07d15.jpg)



