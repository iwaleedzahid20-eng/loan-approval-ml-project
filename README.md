# Loan Approval Prediction – Retail Credit Risk Analytics

## Business Problem
Commercial banks receive thousands of personal loan applications every month.  
Manually evaluating these applications is time-consuming and may lead to inconsistent decisions.

The objective of this project is to:
- Understand key factors influencing loan approval decisions
- Build predictive machine learning models to estimate loan approval probability
- Design an explainable and risk-aware underwriting approach
- Ensure the solution is production-ready and interpretable for business stakeholders

This project simulates a **real-world retail credit underwriting use case** in a commercial bank.

---

## Dataset Overview
The dataset contains **~20,000 personal loan applications** with demographic, financial, and credit-behavior variables.

### Key feature groups:
- **Demographics:** Age, Marital Status, Education Level
- **Financials:** Annual Income, Loan Amount, Debt Ratios
- **Credit Behavior:** Credit Score, Payment History, Previous Defaults
- **Account Information:** Assets, Liabilities, Account Balances
- **Target Variable:** `LoanApproved` (1 = Approved, 0 = Rejected)

---



---

## Approach & Methodology

### 1. Data Understanding & Cleaning
- Validated data types and ranges (age, credit score, ratios)
- Converted date fields to datetime format
- Removed invalid or inconsistent records
- Checked for duplicates and missing values
- Created credit score bands for risk segmentation

### 2. Exploratory Data Analysis (EDA)
- Overall loan approval rate analysis
- Approval rate by:
  - Employment Status
  - Education Level
  - Home Ownership
  - Loan Purpose
- Risk impact analysis using:
  - Credit Score
  - Debt-to-Income Ratio
  - Previous Defaults and Bankruptcy History
- Identification of high-risk customer segments

### 3. Modeling & Evaluation
Models trained and evaluated:
- K-Nearest Neighbors (KNN)
- Decision Tree
- Random Forest

Techniques used:
- Train/Test split with stratification
- Feature scaling where required
- ROC-AUC, Precision, Recall, F1-score
- Confusion Matrix and Classification Report

### 4. Model Interpretability
- Logistic Regression coefficients for directional impact
- Random Forest feature importance ranking
- Business interpretation of high-impact risk drivers

---

## Key Insights
- High debt-to-income ratio and long loan duration significantly reduce approval probability
- Previous loan defaults and bankruptcy history are strong negative indicators
- Income, assets, and credit history length positively influence approval
- Random Forest captured non-linear credit risk patterns effectively

---

## Final Model Performance
- **Best Model:** Random Forest
- **ROC-AUC:** ~0.86
- Strong balance between risk control (recall) and approval precision
- Suitable for deployment with explainability support

---

## How to Run the Project

### Requirements
Install dependencies using:
```bash
pip install -r requirements.txt


## Project Structure
