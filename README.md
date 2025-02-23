# Bank Marketing Campaign Analysis

## Project Overview
Analysis of Portuguese bank marketing campaigns to predict term deposit subscriptions using various machine learning classification models (Logistic Regression, KNN, Decision Tree, SVM). The project aims to improve campaign efficiency and reduce unnecessary customer contacts.

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


# Bank Marketing Campaign Analysis

## Overview
This project analyzes the effectiveness of telephone marketing campaigns conducted by a Portuguese banking institution. Using machine learning techniques, we develop predictive models to identify customers most likely to subscribe to term deposits, aiming to improve campaign efficiency and ROI.

## Data Description
The dataset includes information from 17 marketing campaigns conducted between May 2008 and November 2010, containing:
- 41,188 records with 21 features
- Client demographic data
- Campaign interaction details
- Economic indicators
- Target variable: term deposit subscription (yes/no)




## Business Recommendations


---
**Note**: This project is part of a data science portfolio and uses publicly available data from the UCI Machine Learning Repository.
