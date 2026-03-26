# Credit Risk Modeling for Loan Approval

## Overview
This project builds a classification system to determine whether a customer should be approved for a loan based on financial and demographic data.

The goal is to simulate a real-world lending scenario where a bank must evaluate creditworthiness and minimize the risk of default while still approving qualified applicants.


## Business Problem
Financial institutions must decide:

- Which customers are creditworthy  
- Which customers pose a risk of default  

Incorrect decisions can lead to:
- Financial losses (approving risky applicants)  
- Missed opportunities (rejecting good customers)  

This project uses historical customer data to build predictive models that support loan approval decisions.


## Dataset & Features
The dataset includes customer financial and behavioral attributes such as:

- Account Balance  
- Credit Amount  
- Duration of Credit  
- Payment Status of Previous Credit  
- Employment Length  
- Age  
- Purpose of Loan  
- Number of Existing Credits  
- Installment Percentage  

Two datasets were used:
- Training dataset (historical labeled data)  
- Scoring dataset (new customers to evaluate)  


## Data Preparation
- Removed low-value or low-variance fields (e.g., occupation, guarantors, dependents)  
- Handled missing values by imputing age  
- Cleaned and standardized input variables  

These steps ensured that the models were trained on relevant and high-quality features.


## Modeling Approach
Multiple classification models were built and compared:

- Logistic Regression (with stepwise selection)  
- Decision Tree  
- Boosted Model  
- Random Forest  

This approach allowed for evaluation of different modeling techniques and selection of the most effective one.


## Model Performance

| Model                | Accuracy |
|---------------------|----------|
| Logistic Regression | 76%      |
| Decision Tree       | 67%      |
| Boosted Model       | 78%      |
| Random Forest       | **80%**  |

The Random Forest model achieved the highest overall performance and was selected as the final model.


## Key Drivers of Creditworthiness
Across models, the most important variables included:

- Credit Amount  
- Account Balance  
- Age  
- Duration of Credit  
- Payment History  

These features had the strongest influence on whether a customer was classified as creditworthy.


## Model Evaluation & Bias
Model evaluation included:

- Confusion matrices  
- Segment-level accuracy (creditworthy vs non-creditworthy)  
- ROC curve comparison  

### Key Insight
The models showed a tendency to favor predicting customers as creditworthy, resulting in higher accuracy for approved applicants than rejected ones.

In lending, balancing false positives (approving risky customers) vs false negatives (rejecting good customers) is critical.


## Final Model Selection
The Random Forest model was selected because:

- Highest overall accuracy (~80%)  
- Strong performance across both classes  
- Better balance between predicting creditworthy and non-creditworthy customers  


## Results
- 408 customers were classified as creditworthy  
- The model provides a scalable approach to evaluating future loan applicants  


## Business Impact
This model can help financial institutions:

- Improve loan approval decisions  
- Reduce default risk  
- Automate credit evaluation workflows  
- Support data-driven lending strategies  


## Tools Used
- Alteryx (data preparation and modeling)  
- Statistical modeling techniques (classification, feature importance, model comparison)  


## Project Screenshots
_Add screenshots here:_

- Model comparison report  
- ROC curve  
- Confusion matrix  
- Workflow diagram  

