# Medical Insurance Cost Prediction

## Overview

This project uses machine learning to predict medical insurance charges based on customer information.

The project covers the complete workflow of a regression problem, including exploratory data analysis, data preprocessing, feature engineering, feature selection, model training, and evaluation.

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

### Target Variable

- **charges**

---

## Project Workflow

### 1. Exploratory Data Analysis (EDA)

Performed exploratory analysis to understand the dataset and relationships between variables.

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

- Checked for missing values
- Checked for duplicate records
- Verified data types and data consistency

---

### 3. Feature Engineering

Created additional features to improve the representation of the data.

Included:

- BMI categorization
- One-Hot Encoding of categorical variables
- Creation of dummy variables

Examples:

- `is_female`
- `is_smoker`
- `region_northwest`
- `region_southeast`
- `bmi_category_normal`
- `bmi_category_overweight`

---

### 4. Feature Scaling

Applied `StandardScaler` to numerical features where appropriate.

Features included:

- Age
- BMI
- Children

---

### 5. Statistical Feature Analysis

#### Pearson Correlation

Calculated Pearson correlation between numerical features and the target variable.

Purpose:

- Measure the strength and direction of linear relationships
- Identify potentially useful numerical predictors

#### Chi-Square Test

Performed Chi-Square Test of Independence for categorical features.

Steps:

- Converted continuous `charges` into quartile-based categories using `pd.qcut()`
- Created contingency tables using `pd.crosstab()`
- Calculated Chi-Square statistics and p-values
- Used statistical significance to help evaluate categorical features

---

### 6. Feature Selection

Evaluated the engineered and processed features to determine which variables were useful for the regression model.

Feature selection was based on:

- Correlation analysis
- Statistical significance
- Feature relevance
- Model performance

---

### 7. Train-Test Split

Split the dataset into training and testing sets to evaluate how well the model generalizes to unseen data.

---

### 8. Model Training

Used **Linear Regression** as the prediction model.

The model was trained to predict medical insurance charges based on the selected features.

---

### 9. Model Evaluation

Evaluated the model using:

- **R² Score**
- **Adjusted R² Score**
- Training vs. testing performance

#### R² Score

Measures the proportion of variance in insurance charges explained by the model.

#### Adjusted R² Score

Adjusts the R² score based on the number of predictors in the model and is useful when comparing models with different numbers of features.

---

### 10. Underfitting & Overfitting Analysis

Compared training and testing performance to determine whether the model was:

- Underfitting
- Overfitting
- Generalizing reasonably well

---

## Model

**Algorithm:** Linear Regression

The model predicts insurance charges using demographic, lifestyle, and other relevant customer features.

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
- One-Hot Encoding
- Feature Scaling
- Pearson Correlation
- Chi-Square Test
- Feature Selection
- Train-Test Split
- Linear Regression
- R² Score
- Adjusted R² Score
- Underfitting & Overfitting Analysis
- Pandas
- NumPy
- Scikit-Learn
- SciPy

---

## Project Structure

```text
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