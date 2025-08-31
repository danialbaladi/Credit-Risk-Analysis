# Project Charter — Credit Risk Analysis (Simple Version)

## 1) Problem Statement
We want to predict the probability of loan default within the next 90 days in order to support better credit risk decisions.

## 2) Business Context
- Credit risk team needs to identify high-risk borrowers early.  
- Reducing default rate improves portfolio profitability.  
- Ensures compliance and better decision-making in lending.  

## 3) Target Definition (Label)
- Time horizon: 90 days  
- Default (1): Borrower fails to pay >90 days past due.  
- Non-default (0): Borrower pays normally.  

## 4) Success Metrics
- Main metric: AUC  
- Additional: Recall at fixed Precision threshold  
- Goal: AUC ≥ 0.70 in baseline model  

## 5) Scope, Assumptions, Risks
- Scope: Build a baseline model (Logistic Regression + simple Tree).  
- Assumption: Data is relatively clean and target label is available.  
- Risks: Class imbalance, data leakage, bias/fairness concerns, distribution shift.  

## 6) Ethics & Compliance
- Avoid discrimination by gender, ethnicity, or age.  
- Ensure transparency and explainability of the model.  
- Protect privacy of sensitive customer data.  

## 7) Deliverables
- Baseline notebook (01_baseline.ipynb)  
- Short report (docs/report.md)  
- requirements.txt file  

## 8) Repo Structure & Commit Policy
- Initial repo scaffold is ready (data/, notebooks/, src/, docs/).  
- First commit message should be:  
  ```
  chore(init): scaffold project + project charter
  ```
