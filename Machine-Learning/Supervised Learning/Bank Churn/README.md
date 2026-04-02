# Bank Customer Churn Prediction
This project was built entirely around XGBoostClassifier - not because it was the only option, but because the goal was to get hands-on with XGBoost specifically. Every decision in this pipeline, from handling class imbalance to tuning hyperparameters, was made with the intent of understanding how XGBoost behaves on real-world tabular data. No other model was used.
# What this project does
Given a bank's customer data, the model predicts whether a customer will churn (leave the bank) or stay. It is a binary classification problem where the target variable is Exited - 1 for churned, 0 for stayed.
# Dataset
The dataset is the classic Bank Customer Churn dataset available on Kaggle. It contains roughly 10,000 rows and 14 features including credit score, age, tenure, balance, number of products, and estimated salary. The class distribution is approximately 80% stayed and 20% churned, making it a moderately imbalanced dataset.
# Exploratory Data Analysis
EDA was done using box plots and KDE plots split by churn status, along with correlation analysis and VIF (Variance Inflation Factor) for multicollinearity detection.
Key findings:

Age was the strongest predictor. Churners peaked around 45-50 years while non-churners peaked around 35-40. Clear distributional separation between the two classes.
Balance showed an interesting pattern. Non-churners had a spike at zero balance while churners had a smooth distribution peaking around 100k-125k, suggesting customers with money in their accounts were more likely to leave.
CreditScore had near-zero correlation with churn (-0.027) and a VIF of 20, indicating it was both non-predictive and highly collinear with other features.
Tenure and EstimatedSalary showed virtually identical distributions for both classes and near-zero correlation with churn. Both were dropped.
NumOfProducts and IsActiveMember showed moderate signal and were retained.
# Pipeline Structure
1-
ColumnTransformer (OneHotEncoder on Gender and Geography)
        |
      
        |
  XGBClassifier
2-ColumnTransformer (OneHotEncoder on Gender and Geography)
        |
      SMOTE  [skipped in the scale_pos_weight variant]
        |
  XGBClassifier
# Results
Model with scale_pos_weight (threshold = 0.5)
ScoreAUC-ROC0.867
Recall (churned)0.762
Precision (churned)0.506
F1 (churned)0.608
Accuracy0.80
**Confusion matrix: 310 churners correctly identified, 97 missed, 303 false alarms on loyal customers.**

Model with SMOTE (threshold = 0.5)
ScoreAUC-ROC0.->866
Recall (churned)0.523
Precision (churned)0.758
F1 (churned)0.619
Accuracy0.87

**Confusion matrix: 213 churners correctly identified, 194 missed, only 68 false alarms.**
# Tech Stack

Python
XGBoost
scikit-learn
imbalanced-learn
pandas, numpy
seaborn, matplotlib

# **Author**
*Muhammed Inam — FYIMP Data Science and AI, University of Kashmir*
