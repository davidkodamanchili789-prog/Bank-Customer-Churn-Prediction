# Bank Customer Churn Prediction

A Machine Learning approach to predicting customer attrition in the banking sector using behavioral and demographic data.

## 📌 Project Overview
The objective of this project is to build a classification model that identifies customers at risk of leaving the bank (churning). By identifying these customers early, the bank can implement targeted retention strategies to minimize revenue loss.

## ⚙️ Core Workflow
1. **Data Preprocessing & Cleaning**: 
   - Dropped identifying columns (RowNumber, CustomerId, Surname) that do not contribute to predictive power.
   - Handled categorical data using **One-Hot Encoding** to convert text labels into a machine-readable format.
2. **Feature Scaling**: 
   - Applied **StandardScaler** to numerical features like Income, Balance, and Credit Score. This ensures that features with larger ranges don't dominate the model's learning process.
3. **Class Imbalance Management**: 
   - Utilized **Stratified Splitting** to ensure the training and testing sets maintain the same ratio of churned vs. non-churned customers as the original dataset.

## 🤖 Models & Performance
I evaluated multiple algorithms to find the best fit for this classification task:

| Model | F1-Score | AUC-ROC |
| :--- | :--- | :--- |
| **Logistic Regression** | **0.9950** | **1.0000** |
| Random Forest | 0.9151 | 0.9975 |

### Why these models?
- **Logistic Regression**: Chosen for its efficiency and high interpretability. It provided a near-perfect baseline for this specific dataset.
- **Random Forest**: Used to capture non-linear relationships between features (like how Income might interact with Credit Score).

## 🚀 Key Takeaways
- **Data Scaling matters**: Normalizing the features significantly improved the convergence speed of the Logistic Regression model.
- **Top Predictors**: Features like Number of Complaints and Outstanding Loans were critical indicators of potential churn.

**- 🔍 Model Explainability**

Used SHAP values to prove that "Number of Complaints" was the #1 driver of churn, shifting the business focus from "Pricing" to "Customer Service Quality."
