# 🟡 Gold Price Prediction using KNN Regression

## 📌 Project Overview

This project focuses on **predicting Gold closing prices** using historical financial market data. The notebook demonstrates a **complete machine learning workflow** with emphasis on **data analysis, preprocessing, and K-Nearest Neighbors (KNN) regression**.

Unlike typical regression projects, this notebook **does NOT use Linear, Ridge, Lasso, or ElasticNet models**. The final prediction model is built **only using KNN Regressor** after proper feature scaling.

---

## 📂 Dataset Description

* **File used**: `financial_regression.csv`
* **Data type**: Tabular financial time-series–like data
* **Target variable**: `gold close`

### Features include:

* Stock indices (S&P 500, NASDAQ)
* Commodity prices (Crude oil, Palladium, etc.)
* Open, High, Low, Close, Volume values
* Date-based information

All features are **numerical**, making the dataset suitable for regression.

---

## 🔍 Exploratory Data Analysis (EDA)

The notebook performs extensive EDA, including:

* Viewing data using `head()` and `tail()`
* Statistical summary using `describe()`
* Dataset structure with `info()`
* Checking missing values and duplicates
* Correlation analysis using `df.corr()`
* Large correlation heatmap visualization

📌 **Observation**: Some numerical columns contain missing values, but no duplicate rows were found.

---

## 🧹 Data Cleaning & Feature Engineering

Steps performed:

* Converted `date` column to datetime format
* Extracted **year** feature from date
* Filled missing numerical values using **mean imputation**
* Selected numerical columns for modeling

---

## ✂️ Train–Test Split

* Target (`y`) → `gold close`
* Features (`X`) → remaining numerical columns
* Data split into **80% training** and **20% testing** using `train_test_split`

---

## ⚙️ Feature Scaling

Since KNN is **distance-based**, feature scaling is mandatory.

* Used **StandardScaler** inside a **ColumnTransformer**
* Applied scaling to all numerical features
* Converted scaled arrays back into DataFrames for clarity

---

## 🤖 Model Used

### 🔹 K-Nearest Neighbors Regressor (KNN)

* Model: `KNeighborsRegressor`
* Distance-based regression model
* Predicts gold price based on similarity to nearest data points

The model is trained on scaled training data and evaluated on scaled test data.

---

## 📊 Model Evaluation

Evaluation metrics used:

* **Mean Squared Error (MSE)**
* **R² Score (Train)**

These metrics help measure prediction accuracy and model fit.

---

## 🧠 Key Learnings

* Financial datasets often contain correlated features
* Feature scaling is **critical** for KNN models
* KNN can work well for regression when data is well-prepared
* Simple models can still give meaningful insights with proper preprocessing

---

## 🛠️ Libraries Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn

---

## 🚀 How to Run

```bash
pip install pandas numpy matplotlib scikit-learn
jupyter notebook Gold_price_prediction.ipynb
```

---

## 🔮 Future Improvements

* Hyperparameter tuning for `k`
* Compare KNN with linear models
* Add lag-based features for time-series behavior
* Cross-validation for better generalization

---

## 👤 Author

**Devendra Kushwah**
B.Tech CSE (AI & ML)
Aspiring Machine Learning Engineer

---

⭐ If you found this project useful, feel free to star the repository!
