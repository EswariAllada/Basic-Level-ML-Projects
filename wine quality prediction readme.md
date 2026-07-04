# 🍷 Wine Quality Prediction using Random Forest Classification

## 📌 Project Overview

This project predicts whether a wine is **Good Quality** or **Not Good Quality** based on its physicochemical properties using a **Random Forest Classifier**.

The original dataset contains wine quality scores ranging from **3 to 8**. Since the dataset is highly imbalanced across these quality levels, the problem was transformed into a **binary classification** task:

* **0 → Not Good Quality Wine** (Quality Score: 3–6)
* **1 → Good Quality Wine** (Quality Score: 7–8)

This approach helps improve model performance while making the classification problem more practical.

---

## 🎯 Problem Statement

Wine quality depends on several chemical properties such as acidity, alcohol content, pH, sulphates, and density. Predicting wine quality can help manufacturers maintain product standards and support quality control.

The objective of this project is to build a machine learning model that predicts whether a wine belongs to the **Good Quality** or **Not Good Quality** category based on its chemical characteristics.

---

## 📂 Dataset

**Dataset:** WineQT Dataset

### Features

* Fixed Acidity
* Volatile Acidity
* Citric Acid
* Residual Sugar
* Chlorides
* Free Sulfur Dioxide
* Total Sulfur Dioxide
* Density
* pH
* Sulphates
* Alcohol

### Target Variable

The original **quality** column was converted into a binary target:

| Original Quality | Label                |
| ---------------- | -------------------- |
| 3–6              | 0 (Not Good Quality) |
| 7–8              | 1 (Good Quality)     |

The **Id** column was removed because it does not contribute to prediction.

---

## 🛠 Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn

---

## 🔍 Project Workflow

1. Import required libraries
2. Load the dataset
3. Perform data exploration
4. Check for missing values and duplicates
5. Create a binary target variable (Good Quality)
6. Split the dataset into training and testing sets
7. Train a Random Forest Classifier
8. Predict wine quality
9. Evaluate model performance
10. Visualize dataset relationships using a correlation heatmap
11. Visualize the distribution of wine quality classes

---

## 🤖 Machine Learning Model

**Algorithm Used:**

* Random Forest Classifier

### Model Parameters

* n_estimators = 500
* class_weight = "balanced"
* random_state = 42

The **class_weight='balanced'** parameter helps improve learning for the minority class (Good Quality wines).

---

## 📊 Model Performance

* **Accuracy:** **93.89%**

### Classification Report

| Class                | Precision | Recall | F1-Score |
| -------------------- | --------: | -----: | -------: |
| Not Good Quality (0) |      0.95 |   0.99 |     0.97 |
| Good Quality (1)     |      0.85 |   0.61 |     0.71 |

The model performs very well in identifying not-good-quality wines while achieving good precision for identifying good-quality wines.

---

## 📈 Visualizations

The project includes:

* Correlation Heatmap
* Wine Quality Distribution Bar Chart

These visualizations help understand feature relationships and class distribution within the dataset.

---

## 📌 Conclusion

This project demonstrates an end-to-end machine learning workflow for solving a binary classification problem. By transforming the original multiclass quality ratings into two categories, the model effectively handles class imbalance and achieves high prediction accuracy.

The project highlights essential machine learning concepts such as data preprocessing, feature selection, class balancing, model training, evaluation, and data visualization using Random Forest Classification.
