# Waze User Churn Prediction Project

## Overview
This project aims to analyze and predict user churn for the Waze navigation app using various machine learning models. The dataset contains user information and usage patterns. Our goal is to identify the key factors contributing to user churn and build models to predict whether a user will stop using the app.

## Business Understanding
User churn is a critical issue for Waze, as it can lead to a decreased user base, loss of potential revenue, and reduced effectiveness of community-based features. Understanding the factors that lead to user churn can help Waze implement effective retention strategies, enhance user experience, and improve overall user satisfaction.

## Data Understanding
The dataset consists of user information and usage patterns, with the following features:
- **ID**: Unique identifier for each user
- **label**: Churn label (whether the user has churned or retained)
- **sessions**: Total number of sessions the user has had
- **drives**: Total number of drives recorded for the user
- **total_sessions**: Total time spent in sessions (in minutes)
- **n_days_after_onboarding**: Number of days since the user completed onboarding
- **total_navigations_fav1**: Total number of navigations to the user's first favorite location
- **total_navigations_fav2**: Total number of navigations to the user's second favorite location
- **driven_km_drives**: Total kilometers driven by the user
- **duration_minutes_drives**: Total duration of drives in minutes
- **activity_days**: Total number of days the user was active
- **driving_days**: Total number of days the user drove
- **device**: Device type used by the user (e.g., Android, iOS)

## Modeling and Evaluation
Various machine learning models were applied to predict user churn. Here are the performance metrics for two key models:

### Logistic Regression
- **Precision**: 68%
- **Recall**: 68%
- **F1-score**: 68%
- **Accuracy**: 68%

### Tree-based Machine Learning and XGBOOST
The Random Forest model was identified as the champion model, achieving the highest performance metrics:
- **Precision**: 82%
- **Recall**: 99%
- **F1-score**: 90%
- **Accuracy**: 82%

Also, the random forest model was used to determine feature importance in predicting whether a user churned or not. The plot below shows that in this random forest model `activity days`, `driving days`, `km per driving day`, `n days after onboarding`, and `total sessions per day` have the highest importance, in that order. These variables are most helpful in predicting the outcome variable, `label`.
![w1](https://github.com/user-attachments/assets/f357f115-3670-4f2e-a9e0-f56f0bd0549a)

## Conclusion
The analysis provides valuable insights into the factors influencing user churn in the Waze app. The Random Forest model emerged as the most accurate predictor, indicating that it is the most suitable for identifying users at high risk of churning. By leveraging these insights, Waze can optimize its retention strategy, enhance user experience, and make data-driven decisions about product development, ultimately reducing churn rates and promoting user growth.
