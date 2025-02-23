# Bank Marketing Campaign Analysis

## Overview
This project analyzes the effectiveness of telephone marketing campaigns conducted by a Portuguese banking institution. Using machine learning techniques, developed predictive models to identify customers most likely to subscribe to term deposits, aiming to improve campaign efficiency and ROI.

## Data Description
The data is from a Portugese banking institution and is a collection of the results of multiple marketing campaigns. The dataset is publicly available from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/222/bank+marketing)
- **Scope**: 17 marketing campaigns (May 2008 - November 2010)
- **Size**: 41,188 records
- **Features**: 21 attributes including:
  * Client demographics
  * Campaign information
  * Economic indicators
- **Target**: Term deposit subscription (yes/no)

## Methodology
The analysis was conducted in three comprehensive phases, each building upon the previous to create a robust predictive system for bank marketing campaigns:
#### 1. Data Cleaning & Preprocessing:
##### a. Data Cleaning Process:
   - Performed initial quality assessment and structure validation
   - Selected relevant features for analysis (client demographics, banking relationship, economic indicators)
   - Checked for and handled missing values ("unknown" values)
   - Removed records with incomplete information
##### b. Data Preprocessing Pipeline:
   - Implemented comprehensive data cleaning:
     - Standardized categorical variables
     - Encoded categorical features
     - Scaled numerical features
     - Prepared target variable encoding
   - Resulted in a clean dataset of 30,488 records with validated features
     
#### 2. Feature Engineering & Representation:
Developed a comprehensive feature engineering pipeline combining multiple feature types:
##### a. Feature Processing:
   - Numerical Features: Applied StandardScaler for normalization
   - Categorical Features: Implemented one-hot encoding
##### b. Feature Selection:
   - Selected relevant features based on correlation analysis and domain knowledge
   - Final feature set included 22 dimensions after encoding:
     - Client demographics (age, job, marital status, education)
     - Banking relationship indicators (default, housing, loan)
     - Economic context features (employment rate, consumer indices)

#### 3. Model Development & Evaluation:
##### a. Model Selection & Implementation:
Implemented four different machine learning models:
   - Logistic Regression: For baseline linear classification
   - K-Nearest Neighbors: For pattern-based prediction
   - Decision Trees: For interpretable rule-based classification
   - Support Vector Machines: For complex boundary detection
##### b. Baseline Model Development:
   - Implemented evaluation framework based on:
     - Overall accuracy and classification performance
     - Training time and computational efficiency
     - Class-wise precision, recall, and F1-scores
   - Established baseline performance with default parameters
##### c. Model Optimization:
   - Implemented hyperparameter optimization using HalvingGridSearchCV
   - Addressed class imbalance through:
     - SMOTE implementation
     - Balanced class weights
     - Stratified sampling
   - Performed cross-validation for robust performance estimation
##### d. Performance Results:
Base Models:
   - Logistic Regression: 87.34% accuracy (0.05s training)
   - KNN: 86.37% accuracy (0.00s training)
   - Decision Tree: 85.45% accuracy (0.06s training)
   - SVM: 87.41% accuracy (24.47s training)

Optimized Models:
   - Logistic Regression: 68.61% accuracy with balanced prediction
   - KNN: 78.35% accuracy with optimized neighbors
   - Decision Tree: 85.29% accuracy with best overall balance
   - SVM: 68.65% accuracy with balanced classes

## Key Findings
#### 1. Client Segmentation:
- Students show highest subscription rate (33.28%)
- Retired clients have second-highest rate (29.36%)
- Unemployed customers show surprisingly high success rate (17.07%)

#### 2. Temporal Patterns:
- End-of-quarter months perform best
- March (51.04%), December (47.13%), September (44.85%)
- May shows highest contact volume but lower success rate

#### 3. Economic Indicators:
- Strong correlations between employment rate and success
- Consumer confidence index influences subscription probability
- Market indicators provide valuable context for timing

## Model Performance

After optimization, our final Decision Tree model achieved:
- Accuracy: 85.29%
- ROC AUC: 0.775
- F1-Score (Subscription class): 0.47

Comparison of model performance:

| Model | Accuracy | ROC AUC | Training Time |
|-------|----------|----------|---------------|
| Decision Tree | 85.29% | 0.775 | 16.30s |
| KNN | 78.35% | 0.712 | 10.27s |
| Logistic Regression | 6861% | 0.739 | 9.09s |
| SVM | 68.65% | 0.741 | 685.38s |

## Recommendations
#### 1. Campaign Optimization:
- Focus on student and retired segments
- Prioritize end-of-quarter timing
- Develop segment-specific marketing approaches

#### 2. Resource Allocation:
- Implement predictive scoring for contact prioritization
- Adjust staffing based on predicted success rates
- Balance workload across peak months

#### 3. Implementation Strategy:
- Deploy optimized Decision Tree model
- Retrain quarterly with new data
- Monitor performance metrics regularly




## Repository Structure
```
project/
├── README.md
├── requirements.txt
├── bank-marketing-analysis.ipynb 
└── data/
    └── bank-additional-full.csv
```

## Acknowledgments
- Data provided by [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Bank+Marketing)


