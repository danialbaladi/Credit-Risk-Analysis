
# Credit Risk Analysis

## Overview

A machine learning project for credit risk classification. The workflow follows a structured process up to model validation (Step 14 of a 19-step data science pipeline). The aim is to assess model performance, ensure stability through cross-validation, and prepare a final trained model for reuse.

---


## Dataset

* Binary classification dataset for credit risk prediction.
* Provided as preprocessed CSV files split into training, validation, and test sets.
* The target variable indicates default risk.
* The dataset is imbalanced, making F1-score an important metric in addition to accuracy.

---

## Requirements and Installation

```bash
git clone https://github.com/your-username/Credit-Risk-Analysis.git
cd Credit-Risk-Analysis
python3 -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

---

## Usage

1. Launch Jupyter Notebook.

   ```bash
   jupyter notebook notebooks/credit_risk_analysis.ipynb
   ```
2. Run the notebook cells to:

   * Load the processed data.
   * Train and evaluate Logistic Regression and Gaussian Naive Bayes models.
   * Perform Stratified K-Fold Cross Validation.
   * View accuracy and F1-score summaries.
   * Optionally load the pre-trained models from the `models/` folder.

---

## Modeling Approach

* **Logistic Regression** with `C=0.01`, `solver='lbfgs'`, `max_iter=10000`.
* **Gaussian Naive Bayes** with `var_smoothing=1e-07`.
* Validation performed using 5-fold Stratified Cross Validation.
* The final Logistic Regression model was trained on the combined training and validation sets.
* The test set was held out for unbiased evaluation.

---

## Results

| Model                | Accuracy (mean ± std) | F1-Score (mean ± std) |
| -------------------- | --------------------- | --------------------- |
| Logistic Regression  | 0.8077 ± 0.0022       | 0.3942 ± 0.0121       |
| Gaussian Naive Bayes | 0.8022 ± 0.0019       | 0.3273 ± 0.0217       |

Low standard deviations indicate consistent performance across folds. Logistic Regression outperformed GaussianNB on both metrics. The F1-score reflects class imbalance but is sufficient for a baseline model.

---

## Key Points

* Stratified K-Fold cross-validation was used to handle class imbalance.
* Logistic Regression was selected as the final model due to its slightly better performance.
* Saved model files in `models/` allow reuse without retraining.

---

## Possible Improvements

* Add model explainability methods such as SHAP or LIME.
* Explore additional classifiers (e.g., Random Forest, XGBoost).
* Apply techniques for class imbalance, such as SMOTE or adjusted class weights.
* Extend the workflow with deployment or a simple API.

