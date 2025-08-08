# Employee Attrition Prediction using Logistic Regression

## 📌 Overview
This project focuses on predicting **employee attrition** using a **Logistic Regression model**. Employee attrition refers to the loss of employees through resignation or termination. Identifying potential attrition in advance helps HR departments to take preventive actions.

## 📂 Dataset
- **Source:** IBM HR Analytics Employee Attrition Dataset  
- **File Used:** `WA_Fn-UseC_-HR-Employee-Attrition.csv`  
- **Target Column:** `Attrition` (`Yes` or `No`)  

## 🧹 Data Preprocessing
- Removed irrelevant columns: `BusinessTravel`, `Department`, `EducationField`, `MaritalStatus`
- Applied:
  - Label Encoding to binary/categorical values
  - One-Hot Encoding to nominal categories
- Combined encoded features into one final dataset for training

## 🤖 Model Details
- **Model Used:** Logistic Regression  
- **Library:** `sklearn.linear_model.LogisticRegression`  
- **Target Variable:** Attrition (converted to binary: `1` = Yes, `0` = No)  
- **Model File Saved As:** `EmployAttrition_model.pkl` or `EmployAttrition_model.h5`

### ✅ Usage
```python
import joblib

# Load the model
model = joblib.load("EmployAttrition_model.pkl")

# Predict on new data
y_pred = model.predict(X_new)
