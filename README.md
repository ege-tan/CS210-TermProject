# 📈 CS 210 - Predicting Tesla Stock Prices Using Brent Oil Prices

This repository contains my **CS 210: Data Analysis & Machine Learning Project**, where I analyze the relationship between **Brent crude oil prices and Tesla's stock prices (2019-2022)**. Through **statistical analysis, hypothesis testing, and machine learning models**, this project aims to **predict Tesla stock prices based on historical trends in oil prices**.

---

## 📌 Project Overview
The project is divided into multiple phases:
1. **Phase I: Exploratory Data Analysis (EDA) & Hypothesis Testing**
2. **Phase II: Statistical Correlation & Regression Analysis**
3. **Phase III: Machine Learning Models (KNN & Random Forest)**
4. **Final Phase: Model Optimization & Performance Comparison**

---

## 🔹 Phase I: Data Collection & Exploratory Data Analysis (EDA)
- **Datasets Used:**
  - Tesla stock prices (2019-2022)
  - Brent crude oil prices (2019-2022)
- **Data Preprocessing:**
  - Removed unnecessary columns.
  - Handled missing values using **backfill (bfill)**.
  - Merged datasets based on **date** for time-series analysis.
- **Descriptive Statistics & Visualizations:**
  - **Time series plots** of Tesla stock price & Brent oil price.
  - **Histograms** showing price distributions.
  - **Scatter plots** to examine initial trends.

---

## 🔹 Phase II: Statistical Correlation & Hypothesis Testing
- **Formulated Hypothesis:**
  - **H₀ (Null Hypothesis):** No relationship between Brent oil prices & Tesla stock prices.
  - **Hₐ (Alternative Hypothesis):** A positive relationship exists.
- **Pearson Correlation Analysis:**
  - **Result: r = 0.578 (p < 0.05)**
  - **Interpretation:** Moderate **positive correlation**—higher oil prices are linked with higher Tesla stock prices.
- **Simple Linear Regression:**
  - **R² = 0.3351** → 33.5% of Tesla stock price variance explained by oil price fluctuations.
  - **MSE = 9188.32, RMSE = 95.88**.
  - **Conclusion:** Oil prices **influence** Tesla’s valuation, but **other factors** (e.g., market sentiment, production capacity) play a role.

---

## 🔹 Phase III: Machine Learning Models for Prediction
In this phase, two **regression models** were implemented:
### **1️⃣ K-Nearest Neighbors (KNN) Regression**
- **Steps:**
  - Selected **k = 8** after hyperparameter tuning.
  - Predicted Tesla stock prices based on nearest neighbors.
- **Performance Metrics:**
  - **MSE = 8061.72, RMSE = 89.78**.
  - **Scatter plots** visualized actual vs. predicted values.

### **2️⃣ Random Forest Regression**
- **Steps:**
  - Implemented **n_estimators = 750** and **max_depth = 5** after tuning.
  - Used an ensemble of decision trees to predict stock prices.
- **Performance Metrics:**
  - **MSE = 7504.92, RMSE = 86.63**.
  - **Scatter plots & time-series comparisons** showed Random Forest outperformed KNN.

### **🔍 Model Comparison**
| Model            | MSE      | RMSE   |
|-----------------|---------|--------|
| K-Nearest Neighbors | 8061.72 | 89.78  |
| Random Forest    | **7504.92** | **86.63**  |

- **Random Forest outperformed KNN**, demonstrating **lower error & better generalization**.
- **Ensemble learning** (Random Forest) captured complex data patterns better than KNN.

---

## 📌 Key Takeaways
- **Oil Prices & Tesla Valuation:** Statistical analysis confirms **a moderate positive correlation**.
- **Machine Learning Predictability:** 
  - **Random Forest (RMSE: 86.63) is the best model** for Tesla stock price prediction.
  - **KNN struggled with capturing complex relationships** but still provided insights.
