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
1. **SKLearn**: 
    * train_test_split
    * LogisticRegression
    * confusion_matrix
    * classification_report

2. **imbalanced-learn**
    * RandomOverSampler

The logistic regression model is a type of supervised learning. We will be using existing data in order to train a model to accurately predict the status of a loan. The data must first be split into training data and testing data to feed into the model. This means that our target variable (y) is the loan_status, and the rest of the dataset will be out features (X). The logistic regression model is then created and fit to the training data.

![credit_risk_Screenshot](https://user-images.githubusercontent.com/114107454/235744288-507ac467-63a9-4ec3-b0c5-c4f5c1a07d15.jpg)

The model is then used to make predictions on the classification of a loan as healthy (0) or high-risk (1). These results can be evaulated through a confusion matrix and a classification report. 

This process is then repeated using randomly oversampled data. In the original dataset, 75036 loans are marked as healthy, while 2500 loans are marked as high-risk. Due to the heavily imbalanced dataset, random oversampling seems to be a solid choice to test if it has an effect on the model's performance.


## Results
### Logistic Regression with Original Dataset
![image](https://user-images.githubusercontent.com/114107454/235751252-cf808db9-d5a0-43bc-9b42-9d14b16b0e17.png)

The model is correctly labeling every healthy loan, as indicated by its precision and recall scores of 1.00. These two scores suggest that the model is working perfectly in terms of classifying health loans. 

On the other hand, the logistic regression model is not performing as well in classifying the high-risk loans. The model's precision score was 0.87, while the model's recall score was 0.89. 

All in all, the logistic regression model is working relatively well on this data set, as its precision and recall scores for high-risk loans are still worth noting.

### Logistic Regression with Randomly Oversampled Data
![image](https://user-images.githubusercontent.com/114107454/235751159-8a19c164-ab84-43cc-b8e2-ef2682a4cbf8.png)

When the logistic regression model is fit with the oversampled data, it is still predicting healthy loans perfectly, as indicated by the precision and recall scores of 1.00. 

The logistic regression model is now performing much better with the oversampled data in terms of classifying high-risk loans. It has a precision score of 0.87. It is now correctly predicting all the high-risk loans, as indicated by the recall score of 1.00.

Using resampled training data, the performance of the logistic regression model drastically increased.

## Summary
The logistic regression model using the original dataset as well as the model with randomly oversampled data both performed perfectly in terms of classification of the healthy loans (0). However, the model using the randomly oversampled data performed much better than the model using the original data when predicting high-risk loans. 
The recall score for the model using the original data was 0.89, while the recall score for the model with the randomly oversampled data was 1.00. Based on the classification report, it is clear that the model with the randomly oversampled model is a good choice to classify loans as it it correctly predicting loans 100% of the time, given the features that were included in the dataset. 
The model is performing perfectly on this dataset, but before implementing this model in a real world situation, different datasets should be used on the same model to confirm the accuracy of the model; perfect performance on one dataset alone should not be the determining factor in model implementation.
