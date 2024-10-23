# Bank Marketing Campaign Analysis

## Project Overview
Analysis of Portuguese bank marketing campaigns to predict term deposit subscriptions using various classification models (Logistic Regression, KNN, Decision Tree, SVM).

## Key Findings
- Decision Tree emerged as best model (Accuracy: 85.29%, ROC AUC: 0.7751)
- Successfully balanced class imbalance using SMOTE
- Achieved significant improvement in minority class prediction

## Data
- Source: Portuguese banking institution
- Scope: 17 marketing campaigns (May 2008 - November 2010)
- Size: 41,188 records with 21 features
- Target: Term deposit subscription (yes/no)

## Methodology
1. Data Preprocessing
2. Feature Engineering
3. Model Comparison (Logistic Regression, KNN, Decision Tree, SVM)
4. Hyperparameter Tuning
5. Performance Evaluation

## Results
Best performing model (Decision Tree):
- Accuracy: 85.29%
- ROC AUC: 0.7751
- F1-score (minority class): 0.47
- Training time: 3.44s

## Repository Structure
- `bank-marketing-analysis.ipynb`: Main analysis notebook
- `README.md`: Project documentation
- `bank-additional-full.csv`: Dataset

## Requirements
- Python 3.x
- Required libraries: pandas, numpy, scikit-learn, imbalanced-learn, matplotlib, seaborn
