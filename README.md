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

## Evaluation Results

- MAE: 970043.4039201637
- MSE: 1754318687330.6633
- RMSE: 1324506.9600914384
- R² Score: 0.6529242642153185

---

## Coefficient Interpretation (Sample)

| Feature                           | Coefficient | Interpretation                                                           |
| --------------------------------- | ----------- | ------------------------------------------------------------------------ |
| `area`                            | 235.97      | For each additional square foot, price increases by approx ₹236          |
| `bedrooms`                        | 76,778      | Each additional bedroom adds about ₹76,778 to the price                  |
| `bathrooms`                       | 1,094,445   | Each additional bathroom increases price by over ₹1 million              |
| `stories`                         | 407,477     | Each additional story/floor adds ₹4.07 lakh to the price                 |
| `mainroad`                        | 367,920     | If the house is on a main road, price increases by approx ₹3.68 lakh     |
| `guestroom`                       | 231,610     | Having a guest room adds ₹2.31 lakh                                      |
| `basement`                        | 390,251     | Having a basement increases the price by ₹3.9 lakh                       |
| `hotwaterheating`                 | 684,650     | Presence of hot water heating increases price by approx ₹6.85 lakh       |
| `airconditioning`                 | 791,427     | Air conditioning adds about ₹7.91 lakh to the price                      |
| `parking`                         | 224,842     | Each additional parking space adds ₹2.25 lakh                            |
| `prefarea`                        | 629,891     | Preferred area increases price by ₹6.3 lakh                              |
| `furnishingstatus_semi-furnished` | -126,882    | Semi-furnished houses are approx ₹1.27 lakh cheaper than fully furnished |
| `furnishingstatus_unfurnished`    | -413,645    | Unfurnished houses are approx ₹4.13 lakh cheaper than fully furnished    |


---


## File Structure

```

Task-3/
├── Housing.csv
├── task3.ipynb
├── README.md

```

---

## How to Run the Project

1. Clone or download this repository.
2. Install dependencies:
```

pip install pandas numpy matplotlib seaborn scikit-learn

```
3. Open `tes3.ipynb` in Jupyter Notebook or Google Colab.
4. Upload housing.csv
5. Run all cells step by step.

---

