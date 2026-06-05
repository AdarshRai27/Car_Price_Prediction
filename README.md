# Car Price Prediction using Linear Regression

## Overview

This project builds a machine learning model to predict car prices based on vehicle characteristics such as make, model, year, engine size, mileage, fuel type, and transmission.

The dataset was cleaned, preprocessed, and transformed using one-hot encoding for categorical features before training a Linear Regression model.

## Features Used

* Year
* Engine Size
* Mileage
* Make
* Model
* Fuel Type
* Transmission

## Data Preprocessing

### Handling Categorical Variables

The following categorical features were converted into numerical format using One-Hot Encoding:

* Make
* Model
* Fuel Type
* Transmission

Example:

| Make  | Make_BMW | Make_Ford | Make_Honda | Make_Toyota |
| ----- | -------- | --------- | ---------- | ----------- |
| BMW   | 1        | 0         | 0          | 0           |
| Honda | 0        | 0         | 1          | 0           |

### Feature Selection

Target Variable:

```python
Price
```

Input Features:

```python
Year
Engine Size
Mileage
Make
Model
Fuel Type
Transmission
```

## Model

The project uses:

```python
LinearRegression()
```

from Scikit-Learn.

## Train-Test Split

```python
train_test_split(
    test_size=0.2,
    random_state=42
)
```

* Training Data: 80%
* Testing Data: 20%

## Results

### Performance Metrics

| Metric      | Score   |
| ----------- | ------- |
| R² Score    | 0.8171  |
| Adjusted R² | 0.8033  |
| MAE         | 1810.55 |
| RMSE        | 2237.29 |
| Train R²    | 0.8458  |
| Test R²     | 0.8171  |

### Interpretation

* The model explains approximately 81.7% of the variance in car prices.
* The small gap between training and testing scores indicates good generalization.
* The average prediction error is approximately $1,811.
* No significant overfitting was observed.

## Visualization

### Actual vs Predicted Prices

The scatter plot below compares actual car prices with model predictions.

* Points close to the diagonal represent accurate predictions.
* The model shows a strong positive correlation between actual and predicted values.
* Prediction accuracy remains consistent across most price ranges.

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-Learn
* Jupyter Notebook

## Project Structure

```text
Car-Price-Prediction/
│
├── Car_Price_LR.ipynb
├── dataset.csv
├── README.md
└── requirements.txt
```

## Installation

Clone the repository:

```bash
git clone https://github.com/your-username/car-price-prediction.git
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run the notebook:

```bash
jupyter notebook
```

## Future Improvements

* Ridge Regression
* Lasso Regression
* Random Forest Regressor
* XGBoost Regressor
* Hyperparameter Tuning
* Feature Importance Analysis

## Author

Developed as a machine learning project for car price prediction using Linear Regression.
