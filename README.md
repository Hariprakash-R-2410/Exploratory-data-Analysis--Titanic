# 🚢 Titanic Survival Prediction (EDA + Logistic Regression)

## 📌 Overview
This project analyzes the Titanic dataset to understand the factors that influenced passenger survival and builds a **Logistic Regression model** to predict survival outcomes.

The workflow includes **Exploratory Data Analysis (EDA), data preprocessing, feature engineering, and machine learning model building**.

---

## 🎯 Problem Statement
The objective is to predict whether a passenger survived the Titanic disaster based on features such as age, gender, passenger class, fare, and family relations.

This is a **binary classification problem**:
- `1` → Survived  
- `0` → Did not survive  

---

## 📊 Dataset
The dataset contains information about Titanic passengers.

### Key Features:
- PassengerId
- Pclass (Ticket class)
- Sex
- Age
- SibSp (Siblings/Spouses aboard)
- Parch (Parents/Children aboard)
- Fare
- Embarked
- Survived (Target variable)

---

## 🔍 Exploratory Data Analysis (EDA)

The following steps were performed:

- Checked missing values using heatmaps
- Visualized survival distribution using count plots
- Analyzed survival based on gender and passenger class
- Studied age distribution across passenger classes
- Identified important relationships between features

### Key Insights:
- Females had a higher survival rate compared to males
- First-class passengers had higher survival chances
- Passenger class strongly influenced survival probability
- Age and fare also showed noticeable patterns

---

## 🧹 Data Preprocessing

- Handled missing values in the Age column using imputation based on passenger class
- Converted categorical variables into numerical format using **One-Hot Encoding**
  - `Sex → male`
  - `Embarked → Q, S`
- Used `drop_first=True` to avoid the dummy variable trap
- Dropped irrelevant columns:
  - PassengerId
  - Name
  - Ticket
  - Cabin

---

## ⚙️ Feature Engineering

- Converted categorical features into numerical format
- Created dummy variables for categorical columns
- Ensured dataset was fully numeric for model training

---

## 🤖 Model Building

- Algorithm Used: **Logistic Regression**
- Split data into:
  - Training set (70%)
  - Testing set (30%)
- Used `train_test_split` with `random_state=101` for reproducibility

### Training Process:
The model learns relationships between input features and survival outcome.

---

## 📈 Model Evaluation

### Accuracy Score:
- Achieved Accuracy: **~78%**

### Confusion Matrix:
