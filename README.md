# Health Insurance Data Analysis

![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange)
![Python](https://img.shields.io/badge/Python-3.7%2B-blue)
![Pandas](https://img.shields.io/badge/Pandas-1.3.0-blue)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.4.3-blue)

A Jupyter Notebook for exploratory data analysis (EDA) of health insurance cost data.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/m1d0e1/HealthInsurance/blob/main/HealthInsurance.ipynb)

## Overview

This repository contains an analysis of health insurance data to understand relationships between:
- Demographic factors (age, sex, region)
- Health metrics (BMI)
- Lifestyle factors (smoking status)
- Insurance charges

Key features:
- Data cleaning and preprocessing
- Statistical summaries
- Distribution visualizations
- Missing value handling

## Dataset

The `insurance.xlsx` dataset contains 1,338 records with columns:
- `age`: Age of primary beneficiary
- `sex`: Gender (male/female)
- `bmi`: Body mass index
- `children`: Number of dependents
- `smoker`: Smoking status (yes/no)
- `region`: Geographic region
- `charges`: Individual medical costs billed by insurance

## Analysis Steps

1. **Data Loading & Inspection**
   ```python
   df = pd.read_excel('insurance.xlsx')
   df.head()
   ```

2. **Data Cleaning**
   - Check for missing values: `df.isnull().sum()`
   - Remove duplicates: `df.drop_duplicates()`

3. **Statistical Analysis**
   - Summary statistics: `df.describe()`

4. **Visualizations**
   - Distribution plots for:
     - Insurance charges
     - Age distribution
     - BMI distribution
     - Number of children

## Key Findings

1. **Charge Distribution**
   - Right-skewed distribution showing most charges below $20,000
   - Long tail indicating high-cost cases

2. **Age Distribution**
   - Peak in young adults (18-25 years)
   - Normal distribution across other age groups

3. **BMI Distribution**
   - Normal distribution centered around 25-35

4. **Children**
   - Most insured have 0-2 children
   - Right-skewed distribution

## Requirements

```bash
pandas==1.3.0
numpy==1.21.0
matplotlib==3.4.3
seaborn==0.11.2
```
