# Credit Risk Classification

## Overview
The purpose of this analysis is to classify a given loan as healthy or high-risk using supervised machine learning. This will be accomplished by utilization of a logistic regression model; the model will be trained based on financial information of past loans. The model will then be evaulated using resampled data to determine the performance of the model is affected. 

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

