
  # Catalog Demand Prediction (Marketing ROI Analysis)

## Overview
This project uses predictive analytics to determine whether a company should send catalogs to 250 customers based on expected profitability.

The goal is to estimate customer spending and calculate whether the campaign will exceed a $10,000 profit threshold.

## Business Problem
Should the company send marketing catalogs to 250 customers?

The decision depends on whether the expected profit from the campaign exceeds the cost.

## Approach

### 1. Model Training
- Used historical data from ~2300 customers
- Built a regression model to predict average sales

### 2. Feature Selection
- Selected key predictor: Avg_Num_Products_Purchased
- Identified linear relationship using scatterplots
- Verified statistical significance (p-value < 0.05)
<img width="826" height="720" alt="scatterplot" src="https://github.com/user-attachments/assets/86ec674c-d12c-4558-bab5-db263d1ece18" />
- This visualization shows a strong positive relationship between the number of products purchased and average sale amount, supporting the use of this variable in the regression model.
### 3. Model Performance
- R² ≈ 0.837 → strong model fit
<img width="867" height="500" alt="model_results" src="https://github.com/user-attachments/assets/d26124ed-233e-4f86-8ff5-618c4ec3578a" />

### 4. Prediction
- Applied model to 250 new customers
- Estimated expected revenue per customer

### 5. Profit Calculation
Expected Profit Formula:

Expected Profit = (Revenue * Probability) - Cost

Implemented as:
(Sum_Revenue * 0.5) - (6.5 * 250)
Expected Profit: $21,987

## Key Result Workflow
<img width="896" height="417" alt="model_workflow" src="https://github.com/user-attachments/assets/243a3f18-e4e0-4b00-83e9-03311743a82a" />
- trains the regression model on historical data
- applies predictions to new customers
- calculates expected profit
- aggregates results to support a business decision


## Recommendation
Send the catalogs, as expected profit exceeds the $10,000 threshold.

## Tools Used
- Alteryx
- Excel
- Regression modeling
- Business decision analysis

## Key Takeaways
- Predictive models can guide marketing spend decisions
- Even simple regression can produce high business value
- Combining probability with revenue estimation improves decision quality

## Limitations
- Linear model assumptions
- Limited feature set
- No cross-validation
