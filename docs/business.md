# Business Understanding — Credit Risk Analysis

## Overview
This document provides the business context and high-level understanding for the Credit Risk Analysis project.
It defines objectives, key performance indicators (KPIs), constraints, strategic rationale, stakeholders, and deliverables.

## Objectives
- Predict the probability that a customer will default (fail to repay) on a loan within the next 90 days.
- Reduce portfolio losses by accurately identifying high-risk borrowers.
- Provide a simple, explainable baseline model for the credit risk team to evaluate.

## Key Performance Indicators (KPIs)
| KPI | Definition |
| --- | --- |
| Precision for Default | Percentage of predicted defaults that are actual defaults — minimizes false alarms. |
| Recall for Default | Percentage of actual defaults that are correctly predicted — captures most high-risk borrowers. |
| Default Rate Reduction | Reduction in default incidents after model deployment. |
| Net Profit from Lending | Increase in net profit while maintaining acceptable risk levels. |
| Decision Time Reduction | Decrease in manual loan assessment time through automated scoring. |

> **Note:** The positive class (1) corresponds to **Default**. Model outputs can be translated into actionable **Approve/Reject** decisions.

## Constraints
| Constraint | Description |
| --- | --- |
| Time | Limited time for initial implementation. |
| Human Resources | Availability of data scientists, engineers, and credit experts. |
| Data | Historical labeled loan data with default information must be available. |
| Business Risk | High cost of false negatives (failing to identify a default risk) and false positives (rejecting good borrowers). |
| Internal Policies | Some complex black-box models may not be allowed due to explainability requirements. |

## Strategic Rationale
| Question | Answer |
| --- | --- |
| Why now? | Rising default rates and pressure to improve loan decision accuracy. |
| What is changing? | Competitors are using ML for credit scoring and automated approvals. |
| Long-term goal | Automate decision-making, reduce manual workload, and control credit risk. |
| Management pressure | Stakeholders expect higher efficiency and lower human error in credit assessments. |

## Stakeholders
- Credit Risk Team (primary consumers of model predictions)
- Loan Officers / Underwriting Team
- Data Science / Engineering Team
- Compliance & Legal
- Product / Business Managers

## Success Criteria
- Baseline model developed and evaluated with acceptable metrics (e.g., AUC ≥ 0.70).  
- Model output is explainable and can support actionable loan decisions.  
- Monitoring plan defined for default rate, profit impact, and decision latency.

## Scope & Assumptions
- Scope: Build a baseline explainable model (e.g., Logistic Regression, simple Decision Tree) and conduct exploratory data analysis.
- Assumptions:
  - Historical labeled data (including default labels) is available.
  - Relevant features (demographics, credit history, repayment history) exist.
  - Data privacy and regulatory requirements are respected.

## Risks & Mitigations
- Class Imbalance: Use resampling, threshold tuning, and appropriate metrics.  
- Data Leakage: Maintain proper separation between training and validation datasets.  
- Bias/Fairness: Monitor sensitive attributes and implement fairness checks.  
- Distribution Shift: Plan for post-deployment monitoring and retraining.

## Ethics & Compliance
- Avoid discriminatory decisions based on protected attributes (gender, ethnicity, etc.).  
- Provide explainability via feature importance or simple rules.  
- Protect personally identifiable information (PII) and comply with data retention policies.

## Deliverables
- `docs/business.md` — business understanding and KPIs document.  
- `notebooks/02_eda.ipynb` — placeholder for exploratory data analysis.  
- `docs/report_stage2.md` — placeholder for summary report.

