# Credit Default Risk Prediction & Customer Risk Segmentation

## Project Overview:

This project develops an end-to-end Credit Risk Analytics framework using the Home Credit Default Risk dataset. The objective is to identify customers with a higher probability of default, understand the drivers of credit risk, segment customers into risk categories, and design an underwriting framework that can support lending decisions.

The project simulates a real-world credit risk analytics workflow followed by banks, credit card issuers, and financial institutions such as American Express, Capital One, Wells Fargo, JPMorgan Chase, Goldman Sachs, Mastercard, and Visa.

The project combines data cleaning, exploratory analysis, feature engineering, machine learning, risk segmentation, and business intelligence reporting to create a complete risk management solution.


## Business Problem:

Financial institutions face significant losses when borrowers fail to repay their obligations.

The primary objectives of this project are:

- Predict customer default risk
- Identify key drivers of credit default
- Segment customers into actionable risk categories
- Support underwriting decisions
- Improve portfolio risk management
- Reduce expected credit losses

By identifying high-risk applicants before credit approval, lenders can improve portfolio quality while maintaining profitable customer growth.


## Dataset 

### Source:

Home Credit Default Risk Dataset

### Target Variable

- TARGET = 1 → Customer experienced payment difficulties (default risk)
- TARGET = 0 → Customer did not experience payment difficulties

### Dataset Size

- Observations: 307,511 customers
- Variables: 122 original features

### Data Categories

The dataset contains:

- Customer demographics
- Income information
- Employment details
- Housing characteristics
- Credit information
- Historical bureau information
- Behavioral and application variables


## Project Methodology

### Phase 1: Data Understanding

- Dataset inspection
- Target variable analysis
- Missing value assessment
- Data type review
- Class imbalance evaluation

### Phase 2: Data Cleaning

- Removed 41 variables with more than 50% missing values
- Missing value imputation
- Duplicate checks
- Data consistency validation
- Categorical variable standardization

### Phase 3: Exploratory Data Analysis

Key analyses performed:

- Default rate analysis
- Age-based risk profiling
- Income-based risk profiling
- Occupation-level risk analysis
- Credit exposure analysis
- Customer characteristic comparisons

### Phase 4: Feature Engineering

Created business-relevant risk variables:

- Age Years
- Income Groups
- Credit Groups
- Loan-to-Income Ratio
- Credit-to-Income Ratio
- Annuity Burden Ratio
- Employment Tenure

These variables mimic metrics commonly used in retail credit underwriting.

### Phase 5: Model Development

Three machine learning models were developed and compared:

1. Logistic Regression (Balanced)
2. Random Forest
3. XGBoost

## Model Performance

Model	                            Accuracy	  Precision    Recall	   ROC-AUC
Logistic Regression (Balanced)	     0.69	      0.16	       0.68	     0.75
Random Forest	                      0.72	      0.16	       0.60	     0.73
XGBoost	                            0.72	      0.17	       0.65	     0.76


### Best Performing Model: 

XGBoost

Key performance metrics:

- ROC-AUC: 0.755
- Precision: 0.173
- Recall: 0.647
- F1 Score: 0.273

XGBoost provided the strongest balance between identifying risky customers and minimizing false classifications.


## Key Business Findings

### Age Risk

Younger customers demonstrated significantly higher default rates.

Age Group	    Default Rate
 20-30	         11.46%
 30-40	          9.58%
 40-50	          7.65%
 50-60	          6.13%
 60-70	          4.92%

Default risk decreases steadily with age.

### Income Risk

Higher-income customers exhibited lower default rates compared to lower-income segments.

### Occupation Risk

Highest-risk occupations included:

- Low-skill Laborers
- Drivers
- Waiters/Barmen Staff
- Security Staff
- Cooking Staff

### Risk Segmentation

Customers were segmented into four risk buckets:

Risk Segment	     Default Rate	         Decision
  Low Risk	         1.89%	               Approve
 Medium Risk	       3.97%	         Approve with Conditions
  High Risk	        7.60%	             Manual Review
Very High Risk	    18.83%	               Reject


## Underwriting Framework

### Low Risk

- Standard approval
- Competitive pricing
- Higher credit limits

### Medium Risk

- Conditional approval
- Moderate exposure limits
- Additional monitoring

### High Risk

- Manual credit review
- Additional documentation required

### Very High Risk

- Decline application
- Avoid exposure concentration


## Feature Importance

The most influential predictors of default risk were:

1. EXT_SOURCE_3
2. EXT_SOURCE_2
3. Higher Education Indicator
4. Gender
5. FLAG_DOCUMENT_3
6. Employment Years
7. Income Type
8. Revolving Loan Indicator

These variables contributed most significantly to model predictions.


## Power BI Dashboard

The project includes a four-page interactive dashboard:

### Executive Summary

- Total customers
- Risk segmentation overview
- Portfolio default rates
- Model selection summary

### Portfolio Risk Analysis

- Age group risk analysis
- Income segment analysis
- Occupation risk profiling

### Model Performance

- Model comparison
- ROC-AUC comparison
- Feature importance analysis

### Risk Segmentation & Underwriting

- Risk buckets
- Underwriting decisions
- Portfolio recommendations


## Dashboard Screenshots

### Executive Summary

[Executive Summary](images/dashboard_1_executive_summary.png)

### Portfolio Risk Analysis

[Portfolio Risk Analysis](images/dashboard_2_portfolio_risk_analysis.png)

### Model Performance

[Model Performance](images/dashboard_3_model_performance.png)

### Risk Segmentation & Underwriting

[Risk Segmentation & Underwriting](images/dashboard_4_risk_segmentation.png)


## Technologies Used

### Programming

- Python

### Libraries

- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- XGBoost

### Business Intelligence

- Power BI

### Development Environment

- Jupyter Notebook
- Anaconda


## Repository Structure

Credit Risk Project/
│
├── README.md
├── data/
├── dashboard/
├── images/
├── notebooks/
└── outputs/


## Business Impact

This project demonstrates how predictive analytics can be applied to improve lending decisions and portfolio management.

The framework enables financial institutions to:

- Identify high-risk borrowers
- Reduce expected credit losses
- Improve underwriting quality
- Prioritize manual reviews
- Allocate credit more efficiently
- Support risk-based pricing strategies

The solution combines statistical modeling, machine learning, and business intelligence reporting to deliver an end-to-end credit risk analytics workflow.
