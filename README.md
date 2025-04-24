# 🏠 California Housing Price Prediction

This project explores various regression techniques to predict house prices using the **California Housing dataset**. The goal is to compare the performance of Linear, Ridge, and Lasso regression models and understand how regularization affects model performance.

---
#About this file
#The dataset link https://www.kaggle.com/datasets/camnugent/california-housing-prices

Columns
1. longitude: A measure of how far west a house is; a higher value is farther west
2. latitude: A measure of how far north a house is; a higher value is farther north
3. housingMedianAge: Median age of a house within a block; a lower number is a newer building
4. totalRooms: Total number of rooms within a block
5. totalBedrooms: Total number of bedrooms within a block
6. population: Total number of people residing within a block
7. households: Total number of households, a group of people residing within a home unit, for a block
8. medianIncome: Median income for households within a block of houses (measured in tens of thousands of US Dollars)
9. medianHouseValue: Median house value for households within a block (measured in US Dollars)
10. oceanProximity: Location of the house w.r.t ocean/sea

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

