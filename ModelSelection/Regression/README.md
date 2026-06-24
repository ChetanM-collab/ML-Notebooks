# Model Selection - Regression

This folder contains regression model-selection notebooks. Each notebook follows the same general workflow so model performance can be compared more consistently.

## Workflow

1. Import libraries.
2. Load a dataset with `pd.read_csv(...)`.
3. Split features and target.
4. Create an 80/20 train/test split with `random_state=0`.
5. Train one regression model.
6. Predict test-set values.
7. Evaluate performance with `r2_score`.

## Notebooks

| Notebook | Model | Key configuration | Feature scaling |
|---|---|---|---|
| `multiple_linear_regression.ipynb` | Multiple Linear Regression | `LinearRegression()` | No |
| `polynomial_regression.ipynb` | Polynomial Regression | `PolynomialFeatures(degree=4)` with `LinearRegression()` | No |
| `support_vector_regression.ipynb` | Support Vector Regression | `SVR(kernel='rbf')` | Yes, scales both `X` and `y` |
| `decision_tree_regression.ipynb` | Decision Tree Regression | `DecisionTreeRegressor(random_state=0)` | No |
| `random_forest_regression.ipynb` | Random Forest Regression | `RandomForestRegressor(n_estimators=10, random_state=0)` | No |

## Evaluation Metric

The notebooks use R2 score, also known as the coefficient of determination.

```text
R2 = 1 - (SSR / SST)
```

| R2 value | Meaning |
|---|---|
| `1.0` | Perfect fit |
| `0.0` | No better than predicting the mean |
| Less than `0.0` | Worse than predicting the mean |

## Notes

- Most notebooks currently use `ENTER_THE_NAME_OF_YOUR_DATASET_HERE.csv` as a placeholder. Replace that value before running.
- `support_vector_regression.ipynb` currently reads `Data.csv` directly.
- SVR uses separate `StandardScaler` instances for features and target values, then inverse-transforms predictions before evaluation.
- Keep the same dataset and split settings when comparing R2 scores across models.

## How To Run

1. Place the target CSV in this folder or update the notebook path to point to the correct dataset.
2. Confirm the final column is the target variable, or adjust the `X` and `y` slicing.
3. Run all notebook cells from top to bottom.

```python
dataset = pd.read_csv('ENTER_THE_NAME_OF_YOUR_DATASET_HERE.csv')
```
