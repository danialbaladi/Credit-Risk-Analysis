# Business Understanding — Credit Risk Analysis (Stage 2)

## Objectives
- Predict the probability of loan default within the next 90 days.
- Support faster and more accurate credit decisions to reduce portfolio losses.
- Provide a simple, explainable baseline model for the credit risk team to evaluate.

## Key Performance Indicators (KPIs)
| KPI | Definition |
| --- | --- |
| Precision for "Approve" class | High precision for approved loans to avoid approving high-risk borrowers. |
| Recall for "Reject" class | Ensure the model captures actual bad borrowers (minimize false negatives for the reject decision). |
| Default Rate Reduction | Percentage reduction in default incidents after model deployment. |
| Net Profit from Lending | Increase in net profit while keeping acceptable risk levels. |
| Decision Time Reduction | Decrease in manual decision time due to automated scoring. |

## Constraints
| Constraint | Description |
| --- | --- |
| Time | Limited time for initial implementation (e.g., 1 month). |
| Human Resources | Availability of data scientists, engineers, and credit experts. |
| Data | Historical labeled loan data availability and data quality. |
| Business Risk | High cost of false positives (approving bad loans). |
| Internal Policies | Restrictions on using highly complex black-box models. |

## Strategic Rationale
| Question | Suggested Answer |
| --- | --- |
| Why now? | Recent increase in default rates and pressure to improve decision accuracy. |
| What is changing? | Competitors use ML for loan screening; automation is becoming standard. |
| Long-term goal | Automate decisioning, reduce manual workload, and keep risk under control. |
| Management pressure | Yes — stakeholders expect higher efficiency and lower manual errors. |

## Stakeholders
- Credit Risk Team (primary consumer of model scores)
- Credit Underwriting / Loan Officers
- Data Science / Engineering Team
- Compliance & Legal
- Product / Business Managers

## Success Criteria
- Baseline model is developed and evaluated with AUC ≥ 0.70 (training/validation).  
- Business approves a deployable scoring prototype (explainability and acceptable business metrics).  
- Clear measurement plan to monitor default rate, profit impact, and decision latency post-deployment.

## Scope & Assumptions
- Scope (initial): Build a baseline explainable model (Logistic Regression + simple Decision Tree) and a short EDA notebook.
- Assumptions:
  - Historical labeled data (including default label) is available.
  - Appropriate features (demographics, credit history, repayment history) exist.
  - Data privacy and regulatory constraints will be respected.

## Risks & Mitigations
- Class Imbalance: Use resampling or thresholding and appropriate metrics (AUC, Precision-Recall).
- Data Leakage: Carefully separate training/validation data and avoid future information in features.
- Bias/Fairness: Exclude or monitor sensitive attributes; run fairness checks.
- Distribution Shift: Plan for monitoring and retraining strategy after deployment.

## Ethics & Compliance
- Avoid discriminatory features or decisions based on protected attributes (e.g., gender, ethnicity).
- Provide basic explainability (feature importance, simple rule summaries).
- Protect personally identifiable information (PII) and adhere to data retention policies.

## Deliverables (Stage 2)
- `docs/business.md` (this file) — business understanding and KPIs.
- `notebooks/02_eda.ipynb` — exploratory data analysis notebook (to be created).
- `docs/report_stage2.md` — short summary report (1–2 pages) of findings from Stage 2.

## Next Steps (Stage 3 preview)
1. Data selection: choose a public or internal dataset for EDA.
2. EDA checklist: data load, schema check, missing values, target distribution, basic plots.
3. Create `notebooks/02_eda.ipynb` and produce `docs/report_stage2.md`.
4. Commit and review with stakeholders.

