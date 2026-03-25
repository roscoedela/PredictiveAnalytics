
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

### 3. Model Performance
- R² ≈ 0.837 → strong model fit

### 4. Prediction
- Applied model to 250 new customers
- Estimated expected revenue per customer

### 5. Profit Calculation
Expected Profit Formula:

Expected Profit = (Revenue * Probability) - Cost

Implemented as:
(Sum_Revenue * 0.5) - (6.5 * 250)

## Key Result

Expected Profit: $21,987

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
