Car Price Prediction — EDA & Machine Learning
Overview

This project analyzes a used-car dataset and builds a Linear Regression model to predict car prices.

The project covers the complete workflow from exploratory data analysis (EDA) and data cleaning to preprocessing, feature selection, model training, and evaluation.

Dataset Features
Manufacturer
model
year
price — Target variable
mileage
tax
mpg
engineSize
transmission
fuelType
Project Workflow
1. Exploratory Data Analysis
Dataset structure and summary statistics
Missing-value analysis
Duplicate-value detection
Numerical feature distributions
Categorical feature distributions
Boxplots for identifying outliers
Correlation analysis
Correlation heatmap
Investigation of unusual values
2. Data Cleaning
Removed duplicate records
Handled missing values
Identified unusual mpg values
Treated mpg = 470.8 as an invalid value
Converted invalid engineSize = 0 values to NaN
Checked for constant features
3. Train-Test Split

The dataset was divided into:

80% training data
20% testing data

The test set was kept unseen during preprocessing and model training to prevent data leakage.

4. Preprocessing

A Scikit-learn preprocessing pipeline was used.

Numerical features:

Median imputation
Standard scaling

Categorical features:

One-hot encoding
handle_unknown="ignore" for unseen categories

ColumnTransformer was used to apply the appropriate preprocessing to each feature type.

5. Feature Engineering & Feature Selection

One-hot encoding expanded the original variables into 216 processed features.

Feature selection was then explored using:

Mutual Information
Feature importance analysis
Redundancy/constant-feature checks
6. Model

A Linear Regression model was trained using the processed features.

Baseline Results

Using all 216 processed features:

Metric	Score
Training R²	0.8614
Testing R²	0.8654

The small difference between training and testing R² indicates no obvious overfitting in the baseline model.

Technologies Used
Python
Pandas
NumPy
Matplotlib
Seaborn
Scikit-learn
Jupyter Notebook
Key Learning Outcomes
Performing structured EDA
Identifying and handling unusual data
Understanding data leakage
Separating numerical and categorical preprocessing
Using Pipeline and ColumnTransformer
One-hot encoding categorical variables
Feature selection for regression
Evaluating regression models using R²
Project Structure
Car-Price-Prediction/
│
├── car_price_prediction.ipynb
├── dataset.csv
└── README.md
Status

EDA → Data Cleaning → Preprocessing → Baseline Model → Feature Selection