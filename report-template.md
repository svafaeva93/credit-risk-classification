# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

Lending institutions provide loans or assets to borrowers with the anticipation that the borrower will either return the asset or repay the loan. Credit Risk arises when a borrower fails to return the asset or fulfill the loan repayment, resulting in financial losses for the lender. Lenders assess this risk through various methods, but in this study, we will employ Machine Learning to examine a dataset of past lending transactions from a peer-to-peer lending platform. The objective is to develop a model that can assess the creditworthiness of borrowers.

I will use a machine learning model to determine if loans are safe (low-risk) or risky (high-risk) based on the loan status provided by the lending company.

To achieve this, I will employ the Logistic Regression Model, which is commonly used to predict the likelihood of a specific outcome in classification problems.

After analyzing the lending company's dataset, I developed a Logistic Regression Model that achieved an impressive accuracy score of 99%. However, when it comes to distinguishing non-healthy loans, the model's recall value is lower (0.91) compared to its recall value for healthy loans (0.99). This suggests that the model performs better at predicting loan status as healthy rather than identifying loan status as non-healthy. The reason behind this discrepancy lies in the dataset's imbalance, where the majority of the data corresponds to one class label (in this case, healthy loans greatly outnumber non-healthy loans).







## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.



* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.
