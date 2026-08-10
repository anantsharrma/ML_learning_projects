# Medical Insurance Cost Prediction – Data Preprocessing & Feature Engineering

## Overview

This project focuses on preparing a medical insurance dataset for machine learning. The goal is to clean the data, explore relationships between variables, engineer useful features, and perform statistical feature analysis before model training.

This project is part of my Machine Learning learning journey.

---

## Dataset

The dataset contains information about insurance customers, including:

- Age
- Sex
- BMI
- Number of Children
- Smoker Status
- Region
- Insurance Charges

Target Variable:

- **charges**

---

## Project Workflow

### 1. Exploratory Data Analysis (EDA)

Performed exploratory analysis to understand the dataset.

Included:

- Dataset overview
- Missing value inspection
- Data types
- Summary statistics
- Distribution plots
- Count plots
- Box plots
- Correlation heatmap
- Outlier inspection
- Data visualization

---

### 2. Data Cleaning

- Checked missing values
- Removed duplicates (if present)
- Verified data consistency

---

### 3. Feature Engineering

Created additional features such as:

- BMI Categories
- One-Hot Encoded categorical variables
- Dummy variables

Examples:

- is_female
- is_smoker
- region_northwest
- region_southeast
- bmi_category_normal
- bmi_category_overweight

---

### 4. Feature Scaling

Applied:

- StandardScaler

to normalize numerical features including:

- age
- bmi
- children

---

### 5. Statistical Feature Analysis

#### Pearson Correlation

Computed Pearson Correlation between numerical features and the target variable.

Purpose:

- Measure strength of linear relationships.
- Identify useful numerical predictors.

---

#### Chi-Square Test

Performed Chi-Square Test of Independence for categorical features.

Steps:

- Converted continuous target (`charges`) into quartiles using `pd.qcut()`.
- Built contingency tables using `pd.crosstab()`.
- Calculated Chi-Square statistic and p-values.
- Selected statistically significant categorical features.

---

## Libraries Used

- pandas
- numpy
- matplotlib
- seaborn
- scipy
- scikit-learn

---

## Skills Practiced

- Exploratory Data Analysis
- Data Cleaning
- Data Visualization
- Feature Engineering
- Feature Scaling
- One-Hot Encoding
- Pearson Correlation
- Chi-Square Test
- Statistical Feature Selection
- Pandas
- Scikit-Learn
- SciPy
  
## Project Structure

```
insurance-cost-prediction/
│
├── data/
│   └── insurance.csv
│
├── notebooks/
│   └── insurance_analysis.ipynb
│
├── README.md
└── requirements.txt
```

---

## Future Improvements

- Train multiple regression models
- Hyperparameter tuning
- Cross-validation
- Feature importance analysis
- Model deployment with Flask/FastAPI