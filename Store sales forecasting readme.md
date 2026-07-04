# 🛒 Retail Store Sales Forecasting using Random Forest Regression

## 📌 Project Overview

This project predicts daily retail store sales using historical sales data from 10 different stores. The objective is to forecast future sales based on previous sales trends, promotions, holidays, and date-related features. Accurate sales forecasting helps businesses make informed decisions about inventory management, staffing, marketing campaigns, and overall business planning.

The model is built using **Random Forest Regressor**, a powerful ensemble machine learning algorithm capable of learning complex relationships between multiple features.

---

## 📂 Dataset

The dataset contains daily sales records for **10 retail stores** from **January 1, 2022** to **December 31, 2023**.

### Dataset Features

| Feature | Description                                               |
| ------- | --------------------------------------------------------- |
| date    | Date of the sales record                                  |
| store   | Store ID (1–10)                                           |
| sales   | Daily sales amount (Target Variable)                      |
| promo   | Promotion status (1 = Promotion Active, 0 = No Promotion) |
| holiday | Holiday indicator (1 = Holiday, 0 = Normal Day)           |

---

## 🎯 Project Objective

The primary goal of this project is to:

* Forecast future daily sales for retail stores.
* Analyze the impact of promotions and holidays on sales.
* Capture historical sales patterns using lag features.
* Build a machine learning model capable of making accurate sales predictions.

---

## 🛠 Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn

---

## 📊 Project Workflow

### 1. Data Loading

* Loaded the dataset using Pandas.
* Displayed dataset information and checked its structure.

### 2. Data Exploration

Performed:

* Missing value analysis
* Duplicate value detection
* Dataset shape inspection
* Statistical summary

### 3. Date Processing

Converted the `date` column into datetime format and extracted useful date-related features:

* Year
* Month
* Day
* Weekday

These features help the model learn seasonal and weekly sales patterns.

### 4. Feature Engineering

Created lag features to provide historical sales information to the model.

* **lag_1** → Previous day's sales
* **lag_7** → Sales from one week earlier

These features significantly improve forecasting performance by allowing the model to learn temporal dependencies.

### 5. Data Preparation

Selected the following input features:

* Store
* Promotion
* Holiday
* Year
* Month
* Day
* Weekday
* Lag 1
* Lag 7

Target variable:

* Sales

### 6. Time-Based Train-Test Split

Instead of randomly splitting the dataset, the data was divided chronologically:

* First 80% → Training
* Remaining 20% → Testing

This approach better simulates real-world forecasting where future sales are predicted using historical data.

### 7. Model Building

A **Random Forest Regressor** with 100 decision trees was trained to predict daily sales.

### 8. Model Evaluation

The model was evaluated using:

* Mean Absolute Error (MAE)
* Root Mean Squared Error (RMSE)
* R² Score

### 9. Visualization

Generated:

* Actual vs Predicted Sales plot
* Feature Importance plot

These visualizations help evaluate prediction quality and identify the most influential features.

---

## 📈 Model Performance

| Metric   | Value      |
| -------- | ---------- |
| MAE      | **9.78**   |
| RMSE     | **11.70**  |
| R² Score | **0.8323** |

The model successfully explains approximately **83% of the variation in daily sales**, demonstrating strong forecasting performance.

---


## 📚 Key Learning Outcomes

Through this project, I learned:

* Time Series Forecasting fundamentals
* Date-based Feature Engineering
* Lag Feature Creation
* Time-based Train-Test Splitting
* Random Forest Regression
* Regression Model Evaluation
* Business-oriented Sales Forecasting
* Data Visualization and Model Interpretation

---

## 📌 Conclusion

This project demonstrates how machine learning can be applied to forecast retail store sales using historical sales data and engineered time-based features. By incorporating promotions, holidays, and lag features, the Random Forest model effectively captures sales patterns and provides reliable predictions that can support better business decision-making.
