# Attrition-prediction
This repository contains code and explanations on IBM's Attrition rate. The prediction utilizes Logistic regression classifier.
This project makes use of 4 models in total using Logistic regression, with each model using a slightly altered dataset to improve recall.
Recall is the KPI, and not accuracy.

EDA:
	- The percent of attrition in the dataset is only 16%, non-attrition comes to 84% 
  - Age is largely distributed around the ages 25 - 40 in the dataset with the highest attrition occurring in ages 25 - 35
	- Under distance from home: attrition is seen largely for people living close by which is odd
	- Environment Satisfaction: Majority have rated a 3/4, which has the second highest attrition. Environment satisfaction of 1 has the highest attrition
	- Job Satisfaction: Highest number of people have rated 4/4. The highest attrition comes under people who have rated 3/4 which is odd, followed by people who rated 1
  
  
Correlation: 
	- Age and Number of companies worked are positively correlated
	- Number of companies and Hourly rate are positively correlated
	- Number of companies and Environment satisfaction are positively correlated
	- Total working years and Performance Rating are positively correlated

Transformation
	- Standard scaler is used to scale and transform the train datasets
  
  Modelling:
  - RFE is used in this project to choose the 5 most significant features
  - The five features are Overtime, Business Travel Frequently, Department Research & Development, Job role Laboratory Technician, Marital Status Single
  - **First Model**: A simple logistic regression model with the chosen probability cut off of 0.1 giving the least number of False Negatives and maximum False Positives (Recall comes to 80.2% and precision 27.6%)
  - **Second Model**: Oversampling the dataset reducing class 1s' imbalance. Choosing 0.2 as the probability cut off gives a recall of 98% and a precision of 55%
  - **Third Model**: Undersampling the dataset reducing class 0s' imbalance. Choosing 0.2 as the probability cut off gives a recall of 97% and a precision of 57%
  - **Fourth Model**: Using SMOTE gives a better accuracy than the other three, choosing 0.2 as the probability cut off gives a recall of 55% and a precision of 41%

**This project recommends using oversampling with a probability cut off of 0.2.**

The END

  





