# Module 12 Report Template

## Overview of the Analysis

Lending institutions provide loans or assets to borrowers with the anticipation that the borrower will either return the asset or repay the loan. Credit Risk arises when a borrower fails to return the asset or fulfill the loan repayment, resulting in financial losses for the lender. Lenders assess this risk through various methods, but in this study, we will employ Machine Learning to examine a dataset of past lending transactions from a peer-to-peer lending platform. The objective is to develop a model that can assess the creditworthiness of borrowers.

I used a machine learning model to determine if loans are safe (low-risk) or risky (high-risk) based on the loan status provided by the lending company. 

After analyzing the lending company's dataset, I developed a Logistic Regression Model that achieved an impressive accuracy score of 99%. However, when it comes to distinguishing non-healthy loans, the model's recall value is lower (0.91) compared to its recall value for healthy loans (0.99). This suggests that the model performs better at predicting loan status as healthy rather than identifying loan status as non-healthy. The reason behind this discrepancy lies in the dataset's imbalance, where the majority of the data corresponds to one class label (in this case, healthy loans greatly outnumber non-healthy loans).

As seen below, the data is highly imbalanced. 

<img width="350" alt="Screenshot 2023-07-12 at 12 54 05 PM" src="https://github.com/svafaeva93/credit-risk-classification/assets/124627601/139ed538-87dd-4989-943a-1211136afe7f">

To improve accuracy and enhance the model's ability to classify non-healthy loans, we can use the RandomOverSampler module from the imbalanced-learn library. This technique involves adding more copies of the minority class (non-healthy 
loans) to create a balanced dataset.
Oversampled data: 

<img width="504" alt="Screenshot 2023-07-12 at 12 57 12 PM" src="https://github.com/svafaeva93/credit-risk-classification/assets/124627601/ed29d7eb-feba-47f9-af07-fe833877a5b8">

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
