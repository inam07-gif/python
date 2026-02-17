
# Stress Prediction ML Analysis

##  Project Objective

The objective of this project is to predict `Stress_Level` using smartphone usage behavior and lifestyle features. The study evaluates both linear and non-linear machine learning models to understand the underlying relationship between stress and productivity metrics.

---

## Dataset Overview

The dataset contains 50,000 user records with the following features:

- Age  
- Daily_Phone_Hours  
- Social_Media_Hours  
- Work_Productivity_Score  
- Sleep_Hours  
- App_Usage_Count  
- Caffeine_Intake_Cups  
- Weekend_Screen_Time_Hours  
- Gender  
- Occupation  
- Device_Type  

Target Variable:
- `Stress_Level` (1–10)

---

## Workflow

1. Data Cleaning (No missing values, no duplicates)
2. Categorical Encoding (One-Hot Encoding)
3. Correlation Analysis
4. Linear Regression Modeling
5. Random Forest Regression
6. Feature Influence Testing

---

##  Model Results

| Model | R² Score |
|-------|----------|
| Linear Regression | ≈ 0.00 |
| Random Forest (with productivity) | ≈ 0.85 |
| Random Forest (without productivity) | ≈ 0.00 |

---

##  Key Findings

- Linear Regression failed to capture predictive structure.
- Random Forest achieved high performance due to non-linear modeling.
- `Work_Productivity_Score` was identified as the dominant feature.
- Other smartphone usage features had negligible predictive influence.
- The relationship between stress and productivity appears non-linear.

---

##  Conclusion

The analysis indicates that stress prediction in this dataset is primarily driven by productivity scores rather than direct smartphone usage metrics. Tree-based models outperform linear models due to their ability to capture non-linear patterns.

---

##  Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn

---



