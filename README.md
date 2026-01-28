# 🛍️ E-Commerce Linear Regression Analysis

## 📌 Project Description
This project applies **Multiple Linear Regression** to analyze customer behavior data from an online clothing store.  
The objective is to **predict yearly customer spending** and provide a data-driven recommendation on whether the company should focus on improving its **mobile application** or **website**.

The analysis is fully implemented in a Jupyter Notebook using Python and standard data science libraries.

---

## 📂 Dataset Overview

The dataset contains customer information collected after personalized in-store styling sessions. Customers later place orders through either a **mobile app** or a **website**.

### 🔢 Features
- **Avg. Session Length** – Average duration of in-store styling sessions  
- **Time on App** – Time spent using the mobile application  
- **Time on Website** – Time spent using the website  
- **Length of Membership** – Duration of customer membership  

### 🎯 Target Variable
- **Yearly Amount Spent** – Total annual spending per customer  

### 📊 Dataset Characteristics
- Samples: **500**
- Features: **4 numerical**
- Missing values: **None**
- Target type: Continuous

---

## 🔍 Exploratory Data Analysis (EDA)

The notebook includes:
- Dataset inspection using `info()` and `describe()`
- Identification of numerical vs categorical variables
- Visualization of feature distributions
- Correlation analysis between features and the target variable

### 📈 Correlation with Target
| Feature | Correlation |
|-------|-------------|
| Length of Membership | 0.809 |
| Time on App | 0.499 |
| Avg. Session Length | 0.355 |
| Time on Website | -0.003 |

These results guided feature interpretation but **no feature was removed** during training.

---

## 🤖 Model Development

- Model: **Multiple Linear Regression**
- Library: `scikit-learn`
- Train/Test split: **80% / 20%**
- All numerical features were used without scaling

### 📐 Model Equation
y_hat = β0 
        + 25.72 * Avg. Session Length
        + 38.60 * Time on App
        + 0.46 * Time on Website
        + 61.67 * Length of Membership


---

## 📊 Model Performance

| Metric | Value |
|------|------|
| R² (Training) | 0.9854 |
| R² (Testing) | 0.9809 |
| Mean Squared Error (MSE) | 103.92 |
| Root Mean Squared Error (RMSE) | ≈ 10.19 |

✔️ The small difference between training and testing R² scores confirms that the model **generalizes well** and does **not suffer from overfitting**.

---

## 📌 Coefficient Interpretation

| Feature | Coefficient | Interpretation |
|------|------------|---------------|
| Avg. Session Length | 25.72 | Moderate positive impact |
| Time on App | 38.60 | Strong positive impact |
| Time on Website | 0.46 | Negligible impact |
| Length of Membership | 61.67 | Strongest impact |

---

## 🎯 Business Insight

- Customers who spend more time on the **mobile app** tend to spend significantly more money annually.
- **Length of membership** is the strongest predictor of customer spending.
- Time spent on the website has almost no effect on yearly spending.

### ✅ Recommendation
The company should prioritize improving the **mobile app experience** rather than focusing on the website.

---

## 🛠️ Tools & Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---
