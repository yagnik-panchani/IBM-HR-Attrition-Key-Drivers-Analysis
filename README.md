# Employee Attrition Prediction

## Project Overview
This project predicts whether an employee is likely to leave the company using Machine Learning classification models on the IBM HR Analytics Employee Attrition dataset.

## Objective
Build a classification model that can identify employees at risk of attrition so that HR teams can take preventive actions.

## Dataset
- **Source:** IBM HR Analytics Employee Attrition Dataset (Kaggle)
- **Target Column:** Attrition
  - `Yes` / `1` → Employee left
  - `No` / `0` → Employee stayed

## Project Pipeline
1. Data Loading
2. Exploratory Data Analysis (EDA)
3. Data Cleaning
4. Encoding categorical variables
5. Feature scaling (where required)
6. Train-Test Split
7. Model Training and Comparison
8. Model Evaluation
9. Final Model Selection

## Models Used
- Logistic Regression
- Support Vector Machine (SVM)
- Random Forest
- XGBoost

## Evaluation Metrics
- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

## Model Comparison

| Model | Accuracy | Attrition Recall | Attrition Precision | Attrition F1 |
|-------|----------|------------------|---------------------|--------------|
| SVM | 0.89 | 0.23 | 0.90 | 0.37 |
| Random Forest | 0.88 | 0.13 | 0.83 | 0.22 |
| Logistic Regression (Balanced) | 0.75 | 0.64 | 0.30 | 0.41 |
| **XGBoost** | **0.88** | **0.49** | **0.54** | **0.51** |

## Final Model
**XGBoost Classifier**

### Why XGBoost was selected
- Better balance between precision and recall for attrition class
- Strong overall F1-score for employees likely to leave
- High overall accuracy
- Better practical performance than SVM and Random Forest

### Final Result (XGBoost)
- Accuracy: **0.88**
- Attrition Precision: **0.54**
- Attrition Recall: **0.49**
- Attrition F1-Score: **0.51**

### Confusion Matrix
```text
[[239  16]
 [ 20  19]]
