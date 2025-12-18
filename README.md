# AIRBNB-PRICE-PREDICTION-MACHINE-LEARNING
Machine Learning models for predicting Airbnb weekday prices in London
# Airbnb Weekday Price Prediction using Machine Learning

## Module Information
- **Module:** LDS7003M – Artificial Intelligence and Machine Learning  
- **Level:** 7 (MSc)
- **Assessment Component:** Group Presentation (Component 2)
- **Institution:** York St John University (London Campus)

---

## Project Overview
This project applies machine learning techniques to predict **weekday Airbnb prices in London** using structured listing data. The aim is to explore, preprocess, model, and evaluate multiple regression algorithms and critically analyse their performance in a real-world pricing context.

The project focuses on predicting a **continuous numerical outcome** (Airbnb price) based on property characteristics, location information, and guest-related features.

---

## Dataset
The dataset used is the **Airbnb London Weekday Prices dataset**, provided via the module Moodle page.

### Target Variable
- `realSum` – Weekday Airbnb listing price

### Features Include
- Room type
- Property capacity
- Guest satisfaction score
- Cleanliness rating
- Distance to metro stations
- Geographic coordinates (latitude, longitude)
- Host-related attributes

---

## Methodology

### 1. Data Exploration & Preprocessing
- Exploratory Data Analysis (EDA) using summary statistics and visualisations
- Handling of missing values
- Feature encoding and engineering
- Outlier inspection during EDA
- No scaling applied as all models are tree-based and scale-invariant

---

### 2. Model Development
Three tree-based ensemble regression models were implemented:

- **Random Forest Regressor**  
  Used as a baseline model due to robustness and minimal preprocessing requirements.

- **Gradient Boosting Regressor**  
  Applied to improve predictive performance by learning from residual errors.

- **XGBoost Regressor**  
  Used as the final optimised model due to regularisation and superior generalisation ability.

---

### 3. Model Evaluation & Optimisation
- Train–test split and cross-validation
- Evaluation metrics:
  - R²
  - RMSE
  - MAE
- Hyperparameter tuning performed using **GridSearchCV**
- Best-performing model selected based on generalisation performance

---

## Results
The tuned **XGBoost Regressor** achieved the strongest performance, explaining approximately **76% of the variance** in weekday Airbnb prices on the test data.

---

## Ethical Considerations
- The dataset is publicly available; however, care was taken to avoid re-identification of hosts or properties
- Outliers were retained as they represent valid premium listings
- Model predictions are intended to support decision-making, not replace human judgement
- Potential bias related to location and socio-economic factors is acknowledged

---

## How to Run This Project

### Requirements
- Python 3.9+
- Jupyter Notebook

### Required Libraries
```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost
