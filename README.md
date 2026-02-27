# San Jose Housing Affordability Analysis

## Overview

This project analyzes long-term housing affordability trends in the San Jose Metropolitan Statistical Area (MSA). It examines the relationship between median home prices, rental costs, and median household income to evaluate whether housing costs have outpaced income growth over time.

The goal is to quantify affordability changes, construct meaningful economic ratios, and explore forecasting models to assess future trends.

---

## Research Question

How has housing affordability in the San Jose MSA evolved relative to household income, and what do recent trends suggest about future affordability?

---

## Data Sources

- **Zillow Research Data (Metro-Level)**
  - Zillow Home Value Index (ZHVI)
  - Zillow Observed Rent Index (ZORI)
- **U.S. Census Bureau**
  - Median Household Income (Santa Clara County)

All Zillow values represent metro-level averages — not individual homes.

---

## Data Structure

- Frequency: Monthly (rent & home price), Annual (income)
- Geographic Unit: San Jose, CA (MSA)
- Observations: ~130 monthly time points
- Format: Time-series (one row per date after reshaping)

---

## Key Affordability Metrics

**Home Price-to-Income Ratio**
median_home_price / median_household_income

**Rent Burden**
(annual_rent) / median_household_income

These ratios measure how expensive housing is relative to earnings over time.

---

## Methodology

### 1. Data Collection
- Downloaded Zillow metro-level housing and rent data
- Retrieved income data from Census
- Organized raw data into structured directories

### 2. Data Cleaning
- Filtered datasets to San Jose MSA
- Reshaped wide Zillow datasets into long time-series format
- Handled missing values using interpolation where appropriate
- Merged rent, home price, and income into unified dataset

### 3. Exploratory Analysis
- Trend visualization
- Growth rate comparison
- Correlation analysis between housing and income

### 4. Modeling (In Progress)
- Time-series regression
- Chronological train/test split
- Forecasting future affordability trends

---

## Tools Used

- Python
  - pandas
  - numpy
  - matplotlib / seaborn
  - scikit-learn
- Jupyter Notebook

---

## Project Structure

data/
    raw/
    interim/
    processed/

notebooks/
    01_data_collection.ipynb
    02_data_cleaning.ipynb
    03_analysis.ipynb
    04_modeling.ipynb

figures/
src/

---

## Current Status

✔ Data collection complete  
✔ Data cleaning complete  
🔄 Exploratory analysis underway  
🔄 Modeling & forecasting in progress  

---

## Why This Matters

San Jose is one of the most expensive housing markets in the United States. This project provides a data-driven framework for evaluating whether income growth has kept pace with housing cost inflation and offers insight into future affordability risks.