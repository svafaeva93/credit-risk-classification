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

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.

- In comparison to the original dataset, similarly the number of healthy loans is greater than the number of unhealthy loans.
- The model has a good accuracy model of 99%, the precision score for `0` (healthy loans) is 100% and the precision for `1` labels is not bad at 85%.
- The recall score is also quite high at 99% for prediction of `0` labels and 91% for high-risk loans with the label `1`.

* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.

- The accuracy score for this model is also quite high at 99%. Looking at the confusion matrix, the oversampled data model did significantly better at predicting false negatives, meaning only 4 loans of 0 type were identified as false negative.
- Similar to the previous model, the precision score for 0 loans was 100% and 84% for loan type 1.
- The recall score improved for high-risk loans compared to the previous model. 

## Summary

A lending company wants a model that accurately distinguishes between healthy and non-healthy loans to minimize potential costs. Misclassifying healthy loans as non-healthy can lead to customer loss, while misclassifying non-healthy loans as healthy can result in financial losses for the company.

The Logistic Regression model trained with oversampled data performed better than the model trained with imbalanced data. The balanced dataset approach improved accuracy and recall, reducing errors in classifying non-healthy loans.

To minimize risks, the lending company prefers fewer false positives, where non-healthy loans are mistakenly classified as healthy. Looking at the confusion matrices:

Machine Learning Model 1 with imbalanced data:
- 56 false positives (actual value: healthy, predicted value: non-healthy)
- 102 false negatives (actual value: non-healthy, predicted value: healthy)

Machine Learning Model 2 with balanced data:
- 4 false positives (actual value: healthy, predicted value: non-healthy)
- 116 false negatives (actual value: non-healthy, predicted value: healthy)

Based on these results, the model with balanced data is recommended as it significantly reduces false positives and improves accuracy in classifying healthy and non-healthy loans.


