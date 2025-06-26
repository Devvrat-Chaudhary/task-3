# Task 3: Linear Regression – Housing Price Prediction

## Objective

The goal of this task is to understand and implement both simple and multiple linear regression using a real-world dataset. The model should be able to predict house prices based on various input features.

---

## Tools and Libraries Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

## Dataset Description

Source: Kaggle – Housing Price Prediction  
Target Variable: `price`

Features include:
- `area`: Size in square feet
- `bedrooms`, `bathrooms`, `stories`: House dimensions
- `mainroad`, `guestroom`, `basement`, `hotwaterheating`, `airconditioning`, `prefarea`: Categorical features (yes/no)
- `parking`: Number of parking spaces
- `furnishingstatus`: Categorical (unfurnished, semi-furnished, furnished)

---

## Workflow

### 1. Data Preprocessing
- Converted all categorical variables to numerical.
- Checked for and confirmed no missing values.
- Used one-hot encoding for `furnishingstatus`.

### 2. Train-Test Split
- Split the data into training (80%) and testing (20%) using `train_test_split`.

### 3. Model Building
- Used `LinearRegression` from `sklearn.linear_model`.
- Trained the model using the training data.

### 4. Model Evaluation
- Evaluated using:
  - Mean Absolute Error (MAE)
  - Mean Squared Error (MSE)
  - Root Mean Squared Error (RMSE)
  - R² Score (coefficient of determination)

### 5. Model Interpretation
- Extracted and printed coefficients for all input features to understand their impact on price.

---

## Example Evaluation Results

- MAE: Around 430000
- MSE: Around 3.2e+11
- RMSE: Around 565000
- R² Score: ~0.89 (89% of the variance is explained by the model)

---

## Coefficient Interpretation (Sample)

Each coefficient shows the impact of a 1-unit increase in that feature on the house price:

Example:
- `area`: 120.5 → Each additional sq.ft increases price by ₹120.5
- `bedrooms`: 25000 → Each bedroom adds ₹25,000 to the price

---

## Interview Question Summaries

1. **Linear Regression Assumptions**: Linearity, Independence, Homoscedasticity, Normality of residuals, No multicollinearity.
2. **Coefficient Interpretation**: Change in target variable per unit change in feature.
3. **R² Score**: Proportion of variance explained by the model.
4. **MSE vs MAE**: MSE penalizes larger errors more; MAE is more robust to outliers.
5. **Detecting Multicollinearity**: Use correlation matrix or Variance Inflation Factor (VIF).
6. **Simple vs Multiple Regression**: One feature vs multiple features.
7. **Can Linear Regression be used for classification?** No; use logistic regression instead.
8. **What if assumptions are violated?** The model may give biased or misleading results.

---

## File Structure

```

Task-3-Linear-Regression/
├── Housing.csv
├── linear\_regression.ipynb
├── README.md

```

---

## How to Run the Project

1. Clone or download this repository.
2. Install dependencies:
```

pip install pandas numpy matplotlib seaborn scikit-learn

```
3. Open `linear_regression.ipynb` in Jupyter Notebook or Google Colab.
4. Run all cells step by step.

---

