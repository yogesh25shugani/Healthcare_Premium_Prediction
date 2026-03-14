# Insurance Premium Prediction

## Project Overview

This project predicts the **insurance premium amount** for a customer based on demographic, lifestyle, and medical attributes.

The model analyzes factors such as:

- Age
- Income
- Number of Dependants
- BMI Category
- Smoking Status
- Employment Status
- Region
- Medical History
- Genetic Risk

The project demonstrates a **complete end-to-end Machine Learning pipeline**, including:

- Data Cleaning
- Exploratory Data Analysis (EDA)
- Feature Engineering
- Model Training
- Hyperparameter Tuning
- Model Export for Deployment

---

# Dataset

The dataset contains customer information and their corresponding insurance premium.

Key features in the dataset:

| Feature | Description |
|------|------|
| Age | Age of the customer |
| Gender | Male / Female |
| Region | Residential region |
| Number_of_dependants | Number of dependants |
| Income_lakhs | Annual income in lakhs |
| Insurance_plan | Bronze / Silver / Gold |
| Marital_status | Married / Unmarried |
| BMI_category | Underweight / Normal / Overweight / Obesity |
| Smoking_status | Non-smoker / Occasional / Regular |
| Employment_status | Salaried / Self-employed |
| Medical_history | Existing diseases |
| Genetical_risk | Family genetic risk |
| Premium_amount | Target variable |

---

# Feature Engineering

## 1. Medical Risk Score

Medical history is converted into a **numerical risk score**.

Example mapping:

| Disease | Risk Score |
|------|------|
| Heart Disease | 8 |
| Diabetes | 6 |
| High Blood Pressure | 6 |
| Thyroid | 5 |
| No Disease | 0 |

The score is normalized between **0 and 1**.
normalized_risk_score = (total_risk_score - min_score) / (max_score - min_score)

---

# Model Strategy

The dataset is split into two groups:

### Young Population
Age ≤ 25


### Rest Population

## Project Structure
Age > 25


Two separate models were trained because risk behavior differs significantly across age groups.

---

# Algorithms Used

The following algorithms were tested:

- Linear Regression
- Ridge Regression

Hyperparameter tuning was performed using:
RandomizedSearchCV


---

# Data Preprocessing

The preprocessing pipeline includes:

### Handling Missing Values
Rows with missing values were removed.

### Removing Duplicates
Duplicate records were removed.

### One-Hot Encoding
Categorical variables were converted into dummy variables.


## Installation

Clone the repository:

```bash
git clone https://github.com/yogesh25shugani/Healthcare_Premium_Prediction.git
cd Healthcare_Premium_Prediction