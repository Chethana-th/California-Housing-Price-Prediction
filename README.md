# 🏠 California Housing Price Prediction

This project explores various regression techniques to predict house prices using the **California Housing dataset**. The goal is to compare the performance of Linear, Ridge, and Lasso regression models and understand how regularization affects model performance.

---

## 🛠️ Preprocessing Steps

- **Missing Value Handling**:
  - The dataset contained 207 missing values in the `total_bedrooms` column.
  - These were imputed using the **median**, as it is **robust against outliers**, which were present in the feature.

- **Outlier Detection**:
  - Outliers were detected using the **IQR method** and visualized with boxplots.
  - Median imputation helped ensure the model is not biased by extreme values.

- **Categorical Variable Handling**:
  - The `ocean_proximity` column is categorical.
  - Applied **OneHotEncoding** to convert this into a numerical format suitable for regression models.

---

## 📈 Model Comparison

| Model              | R² Score | RMSE           |
|-------------------|----------|----------------|
| Linear Regression | 0.6254   | 70,060.52      |
| Ridge Regression  | 0.6253   | 70,070.20      |
| Lasso Regression  | 0.6254   | 70,060.68      |

All three models performed similarly, indicating that regularization was not critical in this case.

---

## 💡 Key Learnings

- Median imputation is effective when outliers are present.
- One-hot encoding is essential for converting non-numeric data for regression.
- Ridge and Lasso are useful tools, especially for more complex or noisy datasets.

