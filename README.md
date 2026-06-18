# Machine Learning Projects

This repository contains machine learning projects developed using Python, Pandas, NumPy, Scikit-Learn, Matplotlib, and Seaborn.

## Ml_project_1

# Medical Insurance Charges Analysis and Preprocessing

## Project Overview

This project focuses on performing **Exploratory Data Analysis (EDA)** and **Data Preprocessing** on a medical insurance dataset to understand the factors affecting insurance charges and prepare the data for machine learning model development.

The dataset contains information about individuals, including age, gender, BMI, number of children, smoking habits, region, and medical insurance charges. Through detailed analysis and visualization, the project identifies key relationships between these features and insurance costs.

---

## Objective

The primary objectives of this project are:

* Understand the structure and characteristics of the insurance dataset.
* Identify important factors influencing medical insurance charges.
* Detect patterns, trends, and correlations among variables.
* Handle categorical variables through encoding techniques.
* Perform feature engineering to improve data representation.
* Scale numerical features for machine learning readiness.
* Create a clean and processed dataset suitable for predictive modeling.

---

## Dataset Description

The dataset contains the following features:

| Feature  | Description                  |
| -------- | ---------------------------- |
| age      | Age of the insured person    |
| sex      | Gender of the individual     |
| bmi      | Body Mass Index              |
| children | Number of dependent children |
| smoker   | Smoking status               |
| region   | Residential region           |
| charges  | Medical insurance charges    |

---

## Exploratory Data Analysis (EDA)

Several visualization and analysis techniques were used to gain insights from the dataset:

### Data Inspection

* Dataset shape analysis
* Data type verification
* Missing value detection
* Statistical summary generation

### Univariate Analysis

* Distribution of age
* Distribution of BMI
* Distribution of insurance charges
* Frequency analysis of categorical variables

### Bivariate Analysis

* Impact of smoking on insurance charges
* Relationship between age and charges
* BMI versus charges analysis
* Regional comparison of insurance costs

### Correlation Analysis

* Correlation heatmap generation
* Identification of highly influential features
* Understanding relationships among numerical variables

---

## Data Preprocessing

To prepare the dataset for machine learning, multiple preprocessing steps were performed:

### Label Encoding

Categorical binary variables were converted into numerical format:

* Sex
* Smoker

### One-Hot Encoding

The region feature was transformed into multiple binary columns to avoid introducing ordinal relationships.

### Feature Engineering

A new BMI category feature was created to classify individuals into:

* Underweight
* Normal Weight
* Overweight
* Obese

This helps capture health-related patterns more effectively.

### Feature Scaling

Numerical features were standardized using StandardScaler to ensure consistent feature ranges and improve model performance.

---

## Key Insights

### Smoking Status

Smoking emerged as the most influential factor affecting medical insurance charges. Smokers incur significantly higher insurance costs compared to non-smokers.

### Age

Insurance charges generally increase with age, indicating higher medical risk among older individuals.

### BMI

Higher BMI values are associated with increased medical expenses, showing the impact of obesity on healthcare costs.

### Region

Regional differences exist but have a relatively smaller effect on charges compared to smoking and BMI.

---

## Technologies Used

* Python
* Jupyter Notebook
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn

---

## Skills Demonstrated

* Data Cleaning
* Exploratory Data Analysis (EDA)
* Statistical Analysis
* Data Visualization
* Feature Engineering
* Feature Encoding
* Data Preprocessing
* Machine Learning Pipeline Preparation

---

## Future Scope

The processed dataset can be used to build predictive machine learning models such as:

* Linear Regression
* Ridge Regression
* Lasso Regression
* Random Forest Regressor
* XGBoost Regressor

to accurately predict medical insurance charges based on customer information.

---

This description is detailed enough for GitHub, internships, resume projects, and portfolio showcases.
