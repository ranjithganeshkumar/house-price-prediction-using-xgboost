# 🏠 House Price Prediction using XGBoost

## 📘 Overview
This project uses the **XGBoost Regressor** to predict house prices based on various housing features such as the average number of rooms, tax rate, distance to employment centers, and more.  
The dataset used is [`housing.csv`](./content/housing.csv).

---

## 🎯 Objective
To build a machine learning model that accurately predicts house prices using **XGBoost (Extreme Gradient Boosting)** — a high-performance and regularized regression algorithm.

---

## ⚙️ Technologies Used
- Python 🐍  
- Pandas & NumPy  
- Scikit-learn  
- XGBoost  
- Matplotlib / Seaborn  

---

## 📊 Dataset
**File:** `housing.csv`  
Each row represents housing data for a region, containing features like:

| Feature | Description |
|----------|--------------|
| CRIM | Per capita crime rate by town |
| ZN | Proportion of residential land zoned for lots |
| INDUS | Proportion of non-retail business acres |
| NOX | Nitric oxides concentration |
| RM | Average number of rooms per dwelling |
| AGE | Proportion of owner-occupied units built before 1940 |
| DIS | Distances to employment centers |
| RAD | Accessibility to radial highways |
| TAX | Property-tax rate |
| PTRATIO | Pupil-teacher ratio by town |
| LSTAT | Lower status population percentage |
| **price** | Target variable (house price) |

---

## 🧩 Model Used
**Algorithm:** `XGBRegressor` (Extreme Gradient Boosting Regressor)

**Why XGBoost?**
- High prediction accuracy  
- Built-in regularization to prevent overfitting  
- Handles missing values automatically  
- Fast training with parallel computation  

---

## 🧪 Model Performance

| Metric | Value |
|--------|--------|
| **Mean Absolute Error (MAE)** | 2.0749 |
| **Mean Squared Error (MSE)** | 7.9333 |
| **Root Mean Squared Error (RMSE)** | 2.8166 |
| **R² Score** | 0.9052 |

✅ **Interpretation:**  
- The model explains **~90.5% of the variance** in house prices.  
- The average prediction error is around **2.07 units**, showing excellent performance.

---

## 📈 Visualization

A scatter plot showing the relationship between actual and predicted house prices:

```python
plt.scatter(y_test, y_pred, color='blue')
plt.plot([y_test.min(), y_test.max()], [y_test.min(), y_test.max()], color='red', linewidth=2)
plt.xlabel('Actual Prices')
plt.ylabel('Predicted Prices')
plt.title('Actual vs Predicted Prices (XGBoost)')
plt.show()
