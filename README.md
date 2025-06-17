# 🏡 Melbourne Property Price Prediction (Python)

This project analyses housing data from Melbourne to predict property prices using machine learning techniques. It includes data cleaning, exploratory analysis, feature engineering, and model building with scikit-learn.

---

## 🎯 Project Objective

To build a machine learning model that predicts property prices in Melbourne based on key features like location, building type, number of rooms, and land size.

---

## 🧰 Tools & Technologies

- **Python**  
- **Pandas, NumPy** – data manipulation and cleaning  
- **Matplotlib, Seaborn** – data visualisation  
- **Scikit-learn** – model training and evaluation  
- **Jupyter Notebook**

---

## 🗂️ Dataset Overview

The dataset includes property sale records in Melbourne with the following key features:

- `Suburb`, `Address`, `Rooms`, `Type`, `Price`, `Method`, `SellerG`, `Date`
- `Distance` to city center, `Bedroom2`, `Bathroom`, `Car`, `Landsize`, `BuildingArea`
- `CouncilArea`, `Regionname`, `Propertycount`

---

## 🧼 Data Cleaning Steps

- Dropped columns with excessive missing values  
- Handled missing numerical values using **median**  
- Filled missing categorical values using **mode**  
- Converted `Date` to datetime format  
- One-hot encoded categorical variables (`Type`, `Regionname`, etc.)

---

## 📊 Exploratory Data Analysis

Key findings:
- Properties with more rooms and larger land sizes tend to have higher prices  
- Region plays a significant role in property value  
- Suburbs closer to the city center generally have higher average prices  
- Outliers exist in land size and building area

---

## 🧠 Model Building

Models trained and evaluated:
- **Linear Regression**  
- **Decision Tree Regressor**  
- **Random Forest Regressor**

**Performance Metric:** R² score and RMSE on test set

```python
from sklearn.metrics import r2_score, mean_squared_error
r2_score(y_test, y_pred)
