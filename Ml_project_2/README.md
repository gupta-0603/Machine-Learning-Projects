# Heart Disease Prediction & Exploratory Data Analysis

This repository contains an end-to-end Machine Learning and Exploratory Data Analysis (EDA) project designed to analyze clinical patient data and predict the likelihood of heart disease. The project explores key health indicators like cholesterol levels, resting blood pressure, chest pain type, and maximum heart rate to find patterns that strongly correlate with cardiovascular conditions.

## 📌 Project Overview
Cardiovascular diseases are a leading cause of mortality globally. Early detection through automated diagnostic tools can significantly improve patient care and treatment outcomes. This project implements data ingestion, aggressive data auditing/cleaning (addressing physically impossible values), visualizations, feature encoding, and dataset partitioning to lay a robust foundation for standard classification models.

## 📊 Dataset Features
The model operates on a clinical dataset (`heart.csv`) consisting of **918 records** and **12 feature columns**:

| Feature Name | Type | Description |
| :--- | :--- | :--- |
| **Age** | Numeric | Age of the patient [years] |
| **Sex** | Categorical | Patient gender [M: Male, F: Female] |
| **ChestPainType** | Categorical | [TA: Typical Angina, ATA: Atypical Angina, NAP: Non-Anginal Pain, ASY: Asymptomatic] |
| **RestingBP** | Numeric | Resting blood pressure [mm Hg] |
| **Cholesterol** | Numeric | Serum cholesterol [mm/dl] |
| **FastingBS** | Numeric | Fasting blood sugar [1: if FastingBS > 120 mg/dl, 0: otherwise] |
| **RestingECG** | Categorical | [Normal, ST: ST-T wave abnormality, LVH: Left ventricular hypertrophy] |
| **MaxHR** | Numeric | Maximum heart rate achieved [Numeric value between 60 and 202] |
| **ExerciseAngina** | Categorical | Exercise-induced angina [Y: Yes, N: No] |
| **Oldpeak** | Numeric | ST depression induced by exercise relative to rest |
| **ST_Slope** | Categorical | The slope of the peak exercise ST segment [Up, Flat, Down] |
| **HeartDisease** | Numeric (Target) | Output class [1: Heart Disease, 0: Normal] |

## 🛠️ Tech Stack & Libraries
- **Language:** Python 3
- **Data Manipulation:** `pandas`, `numpy`
- **Data Visualization:** `seaborn`, `matplotlib`
- **Machine Learning Environment:** `scikit-learn`
- **Notebook Environment:** Jupyter Notebook

## 🚀 Key Workflow & Implementation Steps

### 1. Exploratory Data Analysis (EDA) & Data Auditing
- Verified data dimensions ($918 \times 12$) and double-checked for exact duplicate entries (0 found).
- Calculated summary statistics to flag structural anomalies.
- Found out that columns like `RestingBP` and `Cholesterol` contained invalid values of `0` which are clinically impossible.

### 2. Advanced Data Cleaning & Imputation
- Rather than dropping columns or values blindly, the invalid `0` measurements inside the `Cholesterol` column were filtered out to find a clean clinical mean ($\approx 244.64$ mm/dl).
- Successfully replaced all impossible `0` entries with this calculated mean and rounded features uniformly to maintain statistical logic.

### 3. Deep Statistical Visualization
- Generated subplots containing data distribution density charts using `sns.histplot` with Kernel Density Estimations (KDE) to visualize skewness across `Age`, `RestingBP`, `Cholesterol`, and `MaxHR`.
- Created target feature balance counts to compare class differences between normal subjects and positive heart disease cases.

### 4. Categorical Feature Encoding
- Converted qualitative dimensions (`Sex`, `ChestPainType`, `RestingECG`, `ExerciseAngina`, `ST_Slope`) into modeling-ready numeric signals using multi-column one-hot encoding flags via Pandas to avoid hierarchical bias.

## 📈 Key Inferences from EDA
- **Outlier Anomalies:** While the patient population peaks within the 50-60 age bracket, statistical tails in serum cholesterol reach up to 600+ mm/dl, which highlights structural outliers.
- **Target Distribution:** The structural classes show a relatively uniform balance without extreme minority patterns, facilitating smooth classification accuracy calculations down the line.
