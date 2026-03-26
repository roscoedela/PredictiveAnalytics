# Credit Risk Modeling for Loan Approval

## Overview
This project builds a classification system to determine whether a customer should be approved for a loan based on financial and demographic data.

The goal is to simulate a real-world lending scenario where a bank must evaluate creditworthiness and minimize the risk of default while still approving qualified applicants.

---

## Business Problem
Financial institutions must decide:

- Which customers are creditworthy  
- Which customers pose a risk of default  

Incorrect decisions can lead to:
- Financial losses (approving risky applicants)  
- Missed opportunities (rejecting good customers)  

This project uses historical customer data to build predictive models that support loan approval decisions.

---

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

---

## Data Preparation
- Removed low-value or low-variance fields (e.g., occupation, guarantors, dependents)  
- Handled missing values by imputing age  
- Cleaned and standardized input variables  

---

## Modeling Approach
Multiple classification models were built and compared:

- Logistic Regression (with stepwise selection)  
- Decision Tree  
- Boosted Model  
- Random Forest  

---

## Model Performance

| Model                | Accuracy |
|---------------------|----------|
| Logistic Regression | 76%      |
| Decision Tree       | 67%      |
| Boosted Model       | 78%      |
| Random Forest       | **80%**  |

The Random Forest model achieved the highest overall performance.

---

## Model Comparison

<img width="845" height="637" alt="Model_Comparison_report_Creditworthiness" src="https://github.com/user-attachments/assets/bc741ff5-34d6-4e31-827c-3391538807eb" />


---

## Feature Importance

### Random Forest
<img width="792" height="595" alt="Forest_Tree_Creditworthiness" src="https://github.com/user-attachments/assets/1873f4bc-7cee-4c81-8b62-420ed9d4f7e2" />

### Decision Tree
<img width="845" height="404" alt="Decision_Tree_Creditworthiness" src="https://github.com/user-attachments/assets/0f085401-4c9e-4b02-8f94-42eefa3ca423" />

### Boosted Model
<img width="822" height="651" alt="Boosted_Model_Creditowthiness" src="https://github.com/user-attachments/assets/039f126b-8d13-4bc7-84a8-05442f3960d0" />


## Logistic Regression Summary
<img width="820" height="392" alt="Screenshot 2026-03-26 at 11 10 18 AM" src="https://github.com/user-attachments/assets/4f2e1c29-9984-465c-a05a-bca3ed334e4b" />



## Model Evaluation

### Confusion Matrix (Random Forest)

<img width="842" height="141" alt="Bias_Creditworthiness" src="https://github.com/user-attachments/assets/729085a3-6d69-4121-9cfc-edcd42c1d9dd" />

### ROC Curve Comparison
<img width="834" height="526" alt="Creditworthiness_Roc_Curve" src="https://github.com/user-attachments/assets/38ac0540-99df-49bc-b9ee-8751bca0c748" />


## Key Drivers of Creditworthiness
The most important variables across models:

- Credit Amount  
- Account Balance  
- Age  
- Duration of Credit  
- Payment History  


## Model Bias & Insights
The models showed a tendency to favor predicting customers as creditworthy.

This creates risk in real-world lending:
- False positives → approving risky customers  
- False negatives → rejecting good customers  

Balancing this tradeoff is critical in financial systems.


## Final Model Selection
The Random Forest model was selected because:

- Highest overall accuracy (~80%)  
- Strong performance across both classes  
- Best balance between creditworthy and non-creditworthy predictions  


## Results
- 408 customers were classified as creditworthy  
- The model provides a scalable approach to evaluating future loan applicants  


## Workflow

<img width="782" height="435" alt="Workflow_Creditworthiness" src="https://github.com/user-attachments/assets/1bf7162f-7061-4f9b-876d-5ad4afca7232" />

## Real-World Considerations

In a production lending system, accuracy alone is not enough.

Key tradeoffs include:
- False Positives → approving risky customers (financial loss)
- False Negatives → rejecting qualified applicants (lost revenue)

This model highlights the importance of balancing both outcomes rather than optimizing for accuracy alone.

## Business Impact
This model can help financial institutions:

- Improve loan approval decisions  
- Reduce default risk  
- Automate credit evaluation workflows  
- Support data-driven lending strategies  


## Tools Used
- Alteryx (data preparation and modeling)  
- Statistical modeling techniques  

---

## Future Improvements
- Rebuild model in Python (scikit-learn)  
- Hyperparameter tuning  
- Address class imbalance and bias  
- Deploy as an API for real-time scoring  
