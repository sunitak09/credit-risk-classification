# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

**ANSWER:** 
The purpose of the analysis is to evaluate the performance of two logistic regression models in predicting the credit risk associated with loans. The analysis was conducted on financial data of loan sizes, interest rates, borrowers income, debt-to-income ratios, number of accounts, derogatory marks, and total debt. The objective was to predict the loan status, being either a healthy loan of ('0') or high-risk loan of ('1').

The stages of this machine learning process included the following:

    i) Split the datasets for training and testing
    ii) Create and fit a logistic regression model with data
    iii) Evaluate the model's performance by observing accuracy, precision, recall, and f1 scores
    iv) Resample the data with Random Over Sampler for class imbalance
    v) Create and fit a secondary logistic regression model with resampled data
    vi) Evaluate the secondary model's performance by observing the same accuracy, precision, recall, and f1 scores


## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.

**Answer:** 
Analyzing the confusion matrix, the accuracy of the model is 99.24%; Precision is 87.4%; Recall is 89.3% and f1 score is 88.3. The model correctly predicted all the observations of class 0 (i.e Healthy loan), so both precision and recall are 1, and the F1-score is 1. For class 1 (high risk loan), the recall is higher than precision, which means that there are fewer false negative than false positive.


* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
**Answer:**
Logistic regression model, fit with oversampled data, is able to predict (both the '0' (healthy loan) and '1' (high-risk loan labels)) with 99% of precision, recall, and f1-scores. The oversampling data has improved the model's performance significantly by 11% in predicting high-risk loans compared to the original model trained on imbalanced data of 88.3%.


## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.

Answer: 
After observing the model results, the secondary logistic regression model trained with resampled data performed significantly better than the first model trained with original data, especially with predicting high-risk loans ('1'). The model produced higher precision, recall, and f1 scores for high-risk loans, which is most important to aid the lending company in reducing the amount of bad loans and financial losses incurred. 

Based on the performance, model 2 using logictic regression trained with resampled data for this credit risk analysis is recommended since the oversampling data has improved the model's performance significantly by 11% in predicting high-risk loans compared to the original model trained on imbalanced data of 88.3%. The results show that it can better assess a higher difference when comparing healthy loan applications to high-risk loan applications, and avoid making loans that will lead to greater loss in the future.