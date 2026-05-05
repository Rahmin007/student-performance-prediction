# Student Performance Prediction

A machine learning project that predicts student dropout risk using Virtual Learning Environment (VLE) interaction data from the Open University Learning Analytics Dataset (OULAD).

## Problem Statement

Early identification of at-risk students allows institutions to intervene before a student withdraws. This project builds a binary classifier that predicts whether a student will drop out (`Withdrawn`) based on their demographic information, assessment scores, and VLE activity patterns.

## Dataset

**Open University Learning Analytics Dataset (OULAD)**

The dataset contains data from 22 courses over multiple semesters, including:
- Student demographics (age band, region, education level, disability)
- Assessment records (submission timing, scores)
- VLE interaction logs (clicks per activity type per week)

Key preprocessing steps:
- Missing score values filled with the median
- Features aggregated per student: average score, total VLE clicks, assessment count, max score, submission timing
- Final modelling table: one row per student per course presentation

## Models Compared

| Model | Notes |
|-------|-------|
| XGBoost | Best overall performer |
| Random Forest | Strong baseline, robust to outliers |
| K-Nearest Neighbours | Distance-based, sensitive to feature scaling |
| Naive Bayes | Probabilistic baseline |
| Decision Tree | Interpretable, prone to overfitting |

Evaluation metrics: accuracy, precision, recall, F1 score, ROC-AUC, PR-AUC.

## Tech Stack

- Python, Pandas, NumPy
- Scikit-learn, XGBoost
- Matplotlib, Seaborn
- Google Colab / Jupyter Notebook

## Usage

Open `student_dropout_prediction.ipynb` in Jupyter or Colab.

Install dependencies:
```bash
pip install pandas numpy scikit-learn xgboost matplotlib seaborn
```

## Course

CSE437 — Data Mining / Machine Learning, BRACU
