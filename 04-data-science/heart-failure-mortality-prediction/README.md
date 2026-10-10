# Project 4 — Heart Failure Mortality Prediction

**Category:** Data Science · **Built:** Week 4, Days 20–24 (~5 hours)

## Question

Can clinical features recorded during a heart failure patient's follow-up (ejection fraction, serum creatinine, age, etc.) predict whether the patient died during the follow-up period?

## Dataset

[UCI Heart Failure Clinical Records](https://archive.ics.uci.edu/dataset/519/heart+failure+clinical+records) (also on [Kaggle](https://www.kaggle.com/datasets/andrewmvd/heart-failure-clinical-data)) — 299 patients, 12 clinical features, binary outcome `DEATH_EVENT`, plus a follow-up `time` column (reused for survival analysis in Project 5).

## Approach

1. **Setup** — load data, define target (`DEATH_EVENT`), stratified train/test split, check class balance.
2. **Feature engineering** — handle skewed features (e.g. `creatinine_phosphokinase`), bucket continuous variables where it aids interpretability (e.g. age bands, ejection fraction categories), encode categoricals.
3. **Modeling** — logistic regression and a tree-based model (random forest) with scikit-learn `Pipeline`s and cross-validation.
4. **Evaluation** — confusion matrix, ROC-AUC, precision/recall; address class imbalance (`class_weight` or resampling) if needed; pick a final model with justification.
5. **Interpretation** — feature importance / coefficients, and an honest discussion of limitations (small sample, no external validation, not for clinical use).

## Tools

Python (pandas, scikit-learn, matplotlib).

## What "done" looks like

- `src/` — feature pipeline and training/evaluation scripts
- `notebooks/` — EDA recap, evaluation, and interpretation with charts
- A findings write-up below with the final model, its metrics, and its limitations

## Findings

_(Fill in after completing the project: which model was chosen, its ROC-AUC/precision/recall, top predictive features, and caveats.)_
