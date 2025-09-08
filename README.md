# Credit Risk Analysis

A simple project to predict the probability of loan default within 90 days.

## Structure
- `data/` → raw and processed datasets (not versioned in git)
- `notebooks/` → Jupyter notebooks
- `src/` → source code
- `docs/` → documentation

## Setup
```bash
python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements.txt



### Model Selection (Stage 10)

During the model selection phase, three baseline models were initially evaluated: **Logistic Regression**, **Decision Tree**, and **Naive Bayes**. The evaluation focused on metrics that are critical for credit risk analysis, where the dataset is highly imbalanced.

**Evaluation Metrics:**

* **Recall:** Prioritized to ensure that the majority of defaulting customers are correctly identified.
* **F1-score:** Used to balance Precision and Recall.
* **ROC-AUC:** Assessed the overall discriminative ability of each model.

**Results and Decisions:**

* **Decision Tree** showed lower performance across all key metrics, particularly Recall and F1-score, and was therefore not selected for further training.
* **Logistic Regression** demonstrated a good balance between Precision and Recall, achieving the highest F1-score among the tested models.
* **Naive Bayes** achieved the highest Recall, successfully identifying almost all defaulting customers, though its F1-score was lower than Logistic Regression.

**Conclusion:**
Based on the evaluation, **Logistic Regression** and **Naive Bayes** were selected as candidate models for further training and hyperparameter tuning. The final model decision will be made after hyperparameter optimization to ensure optimal performance on the imbalanced credit risk dataset.

