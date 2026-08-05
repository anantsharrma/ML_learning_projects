This project focuses on performing Exploratory Data Analysis (EDA) and data preprocessing on the Heart Disease dataset to prepare it for machine learning classification models.

Objectives
Understand the dataset and feature distributions
Analyze relationships between features and the target variable
Detect missing values, duplicates, and outliers
Encode categorical features
Scale numerical features
Perform feature selection using statistical methods
Produce a clean dataset ready for classification
Dataset

The dataset contains patient health information such as:

Age
Sex
Chest Pain Type
Resting Blood Pressure
Cholesterol
Fasting Blood Sugar
Resting ECG
Maximum Heart Rate
Exercise-Induced Angina
Oldpeak
ST Slope
Heart Disease (Target)

Target Variable: HeartDisease

0 → No Heart Disease
1 → Heart Disease
Exploratory Data Analysis
Dataset overview
Missing value analysis
Duplicate check
Univariate analysis
Target class distribution
Correlation heatmap
Feature vs target analysis
Outlier detection
Data Preprocessing
One-Hot Encoding
Label Encoding (where applicable)
Feature Scaling using StandardScaler
Chi-Square test for categorical feature selection
Clean feature matrix generation
Libraries Used
Pandas
NumPy
Matplotlib
Seaborn
Scikit-learn
SciPy
Outcome-
A cleaned and preprocessed dataset suitable for training machine learning models for binary classification.