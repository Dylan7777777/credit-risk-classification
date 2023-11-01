# Module 12 Report Template

## Overview of the Analysis

All lending institutions provide loans to borrowers with the anticipation The models used the lending_data.csv which contained factors such as  loan_size, borrower_income, interest_rate,total_debt, debt_to_income, num_of_accounts, derogatory_marks and loan_status. The loan_status column contains 0 or 1 where 0 indicates a healthy loan and 1 indicates a high-risk loan.

The dataset which has 77536 data points was split into training and testing sets. The training set was used to build Machine Learning Model 1 using the LogisticRegression module from sklearn. The model was then applied to testing data. This initial model was drawing from a dataset that was unbalanced that had 75036 healthy loans and 2500 high-risk loans. We had to resample the training data and ensure the LogisticRegression model had an equal number of points to draw from using the RandomOverSampler module from imbalanced-learn. This generated 
75036 data points for both healthy(0) and high-risk (1) loans. The Machine Learning Model 2 was then applied to the training data to determine whether the loan to a borrower in the testing set would be healthy or high-risk.


## Results

#### Machine Learning Model 1:
 * Accuracy - the model displays 18663 true positive results and 563 true negative results.
 * Precision - the model performs better predicting healthy loans(precision 1) than high-risk loans (precision 0.85)
 * Recall - the model does perform better predicting healthy loans (recall 0.99) than high-risk loans (recall 0.95)
 * Support - according to the support column, the model is very unbalanced in training data (healthy loans are 18765 while high-risk loans are 619) 
    

#### Machine Learning Model 2:
 * Accuracy - the model displays 74614 true positive results and 74633 true negative results.
 * Precision - the model performs equally well for predicting healthy loans (precision 0.99) and high-risk loans (precision 0.99)
 * Recall - the model performs equally well for predicting healthy loans (recall 0.99) and high-risk loans (recall 0.99).
 * Support - according to the support column, the model is balanced in training data(healthy loans and high risk loans are 75036) which in the evaluation process indicates strength in the report results.


## Summary

* My recommendation is to use the Machine Learning Model 2 as its reported results are balance and show high levels of Accuracy, Precision and Recall for both healthy loans and high-risk loans. With more data points after resampling the model 'Machine Learning Model 2' exhibited better performance, being more suitable to predict the riskiness in loans and classify them as healthy loans or high-risk loans.
