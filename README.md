# Bank Marketing Campaign Analysis

## Project Overview
Analysis of Portuguese bank marketing campaigns to predict term deposit subscriptions using various machine learning classification models (Logistic Regression, KNN, Decision Tree, SVM). The project aims to improve campaign efficiency and reduce unnecessary customer contacts.

## Key Findings
### 1. Model Performance
- **Best Model**: Decision Tree
  - Accuracy: 85.29%
  - ROC AUC: 0.7751
  - F1-score (minority class): 0.47
  - Training time: 3.44s
- **Model Comparison**:
  - Logistic Regression: 68.61% accuracy, ROC AUC 0.7397
  - KNN: 78.35% accuracy, ROC AUC 0.7121
  - SVM: 68.65% accuracy, ROC AUC 0.7413

### 2. Business Insights
  1. Customer Segments
  - Highest success rates:
    * Students: 33.28%
    * Retired: 29.36%
    * Unemployed: 17.07%

  2. Timing Patterns
  - Best performing months:
    * March: 51.04% success rate
    * December: 47.13% success rate
    * September: 44.85% success rate
  - Clear end-of-quarter pattern in success rates

## Recommendations
### 1. Campaign Optimization
- **Timing**:
  * Focus campaigns on end-of-quarter months (March, June, September, December)
  * Reduce volume during historically low-performing months
  * Schedule calls during optimal hours/days

- **Targeting**:
  * Prioritize student and retired segments
  * Develop specialized scripts for high-potential segments
  * Reduce focus on low-probability segments

- **Resource Allocation**:
  * Adjust staffing based on predicted success rates
  * Balance workload across peak months
  * Optimize contact attempts per client

### 2. Model Implementation
- **Deployment Strategy**:
  * Use Decision Tree classifier with optimized parameters:
    - max_depth: 5
    - min_samples_leaf: 4
    - min_samples_split: 5
  * Implement SMOTE for handling class imbalance
  * Regular model retraining (quarterly recommended)

- **Monitoring Plan**:
  * Track ROC-AUC and F1-score for model performance
  * Monitor class distribution in predictions
  * Validate predictions against actual outcomes
    
## Data
- **Source**: Portuguese banking institution
- **Scope**: 17 marketing campaigns (May 2008 - November 2010)
- **Size**: 41,188 records
- **Features**: 21 attributes including:
  * Client demographics
  * Campaign information
  * Economic indicators
- **Target**: Term deposit subscription (yes/no)

## Methodology
1. **Data Preprocessing**:
   - Handled missing values
   - Encoded categorical variables
   - Scaled numerical features

2. **Feature Engineering**:
   - Selected relevant features
   - Created derived features
   - Applied SMOTE for class balancing

3. **Model Development**:
   - Implemented multiple classifiers 
   - Performed hyperparameter tuning
   - Conducted comparative analysis

## Repository Structure
```
project/
├── README.md
├── requirements.txt
├── bank-marketing-analysis.ipynb 
└── data/
    └── bank-additional-full.csv
```

## Setup and Installation
1. Clone the repository
```bash
git clone [repository-url]
```

2. Install required packages
```bash
pip install -r requirements.txt
```

3. Run Jupyter notebook
```bash
jupyter notebook
```

## Acknowledgments
- Data provided by [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Bank+Marketing)
