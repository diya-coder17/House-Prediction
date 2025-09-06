# 🏠 House Price Prediction - Boston Dataset  

## 📌 Project Overview  
This project predicts **house prices in Boston** using machine learning.  
We build a baseline **Linear Regression model** to understand how different features (e.g., crime rate, number of rooms, etc.) affect housing prices.  

---

## 📊 Dataset  
- **Name:** Boston Housing Dataset  
- **Rows:** 506  
- **Features:** 13 numeric + target (`MEDV` = Median value of homes)  
- **Target Variable:** House Price (in $1000s)  

---

## 🔎 Exploratory Data Analysis (EDA)  
Steps performed:  
- ✅ Checked dataset shape, info, summary statistics  
- ✅ Verified no missing or duplicate values  
- ✅ Visualized distributions of features & target  
- ✅ Correlation heatmap → identified most influential features (`RM`, `LSTAT`, `PTRATIO`)  
- ✅ Pairplots & scatterplots → observed linear relationships with target  

**Inference:**  
- 📈 Higher average rooms (`RM`) → higher house prices  
- 📉 Higher lower-income population (`LSTAT`) → lower house prices  
- ⚠️ Some skewed distributions (e.g., `CRIM`) may need transformation  

---

## 🤖 Model: Linear Regression  

### 🔨 Steps:  
1. Performed **train-test split** (80-20)  
2. Standardized features (important for regression stability)  
3. Trained a **Linear Regression** model  

```python
from sklearn.linear_model import LinearRegression

# Create and train model
model = LinearRegression()
model.fit(X_train, y_train)
````

---

## 📈 Model Performance

On **test data**:

* **Mean Squared Error (MSE):** 11.38
* **Root Mean Squared Error (RMSE):** 3.37
* **R² Score:** 0.78

**Interpretation:**

* ✅ Model explains \~78% of the variance in house prices
* ✅ Predictions are off by **\~\$3,370** on average

---

## ✅ Conclusion

* Linear Regression provides a **strong baseline** with decent accuracy
* Features like `RM`, `LSTAT`, and `PTRATIO` strongly influence house prices
* Can be improved further using **regularization (Ridge/Lasso)** or **tree-based models**

---

## 🛠️ Tech Stack

* **Python** → Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
* **Jupyter Notebook**

---

## ✨ Author

👩‍💻 **Diya Agarwal**
🔗 [LinkedIn](https://www.linkedin.com/in/diya-agarwal17/)

