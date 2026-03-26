# A/B Testing: Market Test Analysis

## Overview
This project analyzes the impact of a new menu rollout using an A/B testing framework. The goal was to determine whether the updated menu increased profitability compared to control stores.

The analysis includes experimental design, data aggregation, control matching, and statistical evaluation to support a business recommendation.

---

## Business Problem
A company tested a new menu in select stores and needed to determine:

- Did the new menu increase profit?
- Should the company roll it out across all stores?

---

## Methodology

### 1. Experiment Design
- **Metric:** Profit growth
- **Test Period:** 12 weeks (April 29 – July 21, 2016)
- **Granularity:** Weekly, store-level data

---

### 2. Data Preparation
- Combined transaction and store datasets
- Aggregated transactions to **weekly store-level**
- Filtered to consistent time windows across stores

---

### 3. Treatment vs Control Matching
To ensure fair comparison, each treatment store was matched with two control stores using:

- **Trend & Seasonality** (transactions per week)
- **Average Monthly Sales** (strong correlation with profit)

Key insight:
- Average Monthly Sales had a strong correlation with profit
- Store size (square footage) had little impact

---

### 4. A/B Test Analysis

#### Regional Results
- **West Region Lift:** ~37.9%
- **Central Region Lift:** ~43.5%
- **Statistical Significance:** ~99.5%

#### Overall Results
- **Total Lift:** ~40.7%
- **Statistical Significance:** 100%
- **Estimated Profit Impact:** Significant positive increase

---

## Recommendation
The new menu resulted in a substantial and statistically significant increase in profit.

**Recommendation: Roll out the updated menu to all stores.**

---

## Key Skills Demonstrated
- A/B testing & experimental design
- Control vs treatment matching
- Time series considerations (trend & seasonality)
- Business impact analysis
- Data aggregation and transformation

---

## Files
- [Full Project Report](./market-test-ab-analysis.pdf)

---

## What I Learned
- Proper control matching is critical for valid A/B testing
- Correlation analysis helps identify meaningful variables
- Aggregation level (weekly vs daily) impacts analysis reliability
- Statistical significance is essential before making business decisions

