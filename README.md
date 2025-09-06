# Credit-Card-Default-Prediction
A Machine learning model for predicting credit card default

## Overview
In today’s competitive financial environment, lending institutions face a growing challenge in managing credit risk. With the increasing use of credit cards and installment-based credit, ensuring timely repayment is critical to maintaining financial health and minimizing losses from customer defaults.

## Business Understanding

we are partnering with Guardian Banking Systems, a leading financial institution committed to responsible lending and risk management. The primary goal is to leverage machine learning techniques to develop a predictive system that can identify customers at risk of defaulting on their credit card payments before it happens.

The objective of this project is to build a robust machine learning model capable of predicting whether a customer will default on their credit card payment in the next month. The model will analyze customer demographics, historical billing information, payment behaviors, and credit utilization patterns. Key challenges and business objectives include:

- Early Risk Identification: Detect high-risk customers before default occurs, allowing the institution to take preventive actions such as credit limit adjustments or proactive outreach.

- Data Complexity: The dataset contains various time-dependent variables, including monthly bill amounts and payments, requiring careful feature engineering to extract meaningful signals.

- Cost of Misclassification: Incorrect predictions have consequences. Flagging a reliable customer as a defaulter may damage customer relationships, while missing a true defaulter could result in financial losses.

- Actionable Insights: Beyond prediction, the model should provide explainable insights to help the credit risk team understand the drivers behind customer default risk and shape lending policy accordingly.

## Data Understanding

The Credit Card default dataset Dataset from UC Irvine Machine Learning Repository consists of 30,000 instances and 23 features(Before Feature Engineering) including :

- X1: Amount of the given credit (NT dollar): it includes both the individual consumer credit and his/her family (supplementary) credit.
- X2: Gender (1 = male; 2 = female).
- X3: Education (1 = graduate school; 2 = university; 3 = high school; 4 = others).
- X4: Marital status (1 = married; 2 = single; 3 = others).
- X5: Age (year).
- X6 - X11: History of past payment. We tracked the past monthly payment records (from April to September, 2005) as follows: X6 = the repayment status in September, 2005; X7 = the repayment status in August, 2005; . . .;X11 = the repayment status in April, 2005. The measurement scale for the repayment status is: -1 = pay duly; 1 = payment delay for one month; 2 = payment delay for two months; . . .; 8 = payment delay for eight months; 9 = payment delay for nine months and above.
- X12-X17: Amount of bill statement (NT dollar). X12 = amount of bill statement in September, 2005; X13 = amount of bill statement in August, 2005; . . .; X17 = amount of bill statement in April, 2005. 
- X18-X23: Amount of previous payment (NT dollar). X18 = amount paid in September, 2005; X19 = amount paid in August, 2005; . . .;X23 = amount paid in April, 2005.

## Modeling and Evaluation

We trained two models which are:

- RandomForest.
- XGBOOST.

Cross Validation technique was applied , the dataset was splitted to 70% for training , 15% for validation and 15% for unseen testing data which will be used to evaluate our champion model.

considering accuracy measures , for each model , we output a confusion matrix and four accuracy measures , they are

- Accuracy
- Precision
- Recall
- F1 Score
  
Considering the given Scenario:

False positives may lead to unnecessary restrictions on good customers, causing frustration and potential loss of loyalty.

False negatives, however, could result in real financial losses, missed payments, and reduced recovery likelihood.

Since both misclassification types carry substantial risk, we will optimize and evaluate the model using the F1-score, which balances precision and recall.

