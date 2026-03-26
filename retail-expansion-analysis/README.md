# Retail Expansion Analysis (Pawdacity)

## Overview

This project analyzes historical sales and demographic data to recommend an optimal location for a new retail store.

The objective is to understand how population, household composition, and geographic factors influence store performance.

---

## Business Problem

Pawdacity, a pet retail company, is planning to expand to a 14th location.

The key question:
> Which locations are most likely to generate strong sales based on demographic characteristics?

---

## Data Used

- Historical store sales (2010)
- Census population data
- Household data (under 18 population)
- Land area and population density
- Total families
- Competitor data (NAICS)

---

## Data Preparation Workflow

The project was completed using Alteryx. The workflow included:

1. Data ingestion from multiple sources
2. Joining datasets on geographic identifiers
3. Feature engineering:
   - Population density
   - Households with children
   - Total families
4. Aggregation and validation of dataset totals
5. Outlier detection using IQR methodology
6. Final dataset creation for analysis

---

## Data Validation

The final dataset was validated using column-level aggregation.

| Metric | Total | Average |
|------|------|------|
| Census Population | 213,862 | 19,442 |
| Total Sales | 3,773,304 | 343,027.64 |
| Households Under 18 | 34,064 | 3,096.73 |
| Land Area | 33,071 | 3,006.49 |
| Population Density | 63 | 5.71 |
| Total Families | 62,653 | 5,695.71 |

---

## Outlier Analysis

Outliers were identified using the Interquartile Range (IQR) method.

- **Cheyenne**:
  - High across multiple metrics
  - Retained due to real-world significance as a capital city

- **Gillette**:
  - Weak relationship between sales and demographic variables
  - Removed to prevent distortion in analysis

Given the small dataset (11 cities), only one outlier was removed to preserve data integrity.

---

## Key Takeaways

<img width="496" height="157" alt="Screenshot 2026-03-26 at 8 44 37 AM" src="https://github.com/user-attachments/assets/51252134-4302-42a3-8092-898b6552c7ee" />

- Demographic factors such as population and number of families are strong indicators of retail performance
- Outlier handling is critical when working with small datasets
- Data preparation and validation are essential before predictive modeling

---

## Tools Used

- Alteryx (data cleaning and transformation)
- Excel (data validation)

---

## Project File

See the original project submission here:

[Pawdacity Data Cleaning](Pawdacity_Data_Cleaning.pdf)

---

## Note

This project was completed as part of the Udacity Predictive Analytics program.  
The focus is on data preparation, feature engineering, and analytical reasoning.
