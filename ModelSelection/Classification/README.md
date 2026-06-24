# Model Selection - Classification

This folder contains classification model-selection notebooks and matching Python scripts. The files use a shared workflow so classifiers can be compared with the same split and evaluation style.

## Workflow

1. Import libraries.
2. Load a dataset with `pd.read_csv(...)`.
3. Split features and target.
4. Create a 75/25 train/test split with `random_state=0`.
5. Apply feature scaling with `StandardScaler`.
6. Train one classifier.
7. Predict test-set labels.
8. Evaluate predictions with a confusion matrix and accuracy score.

## Files

| Notebook | Script | Model | Key configuration |
|---|---|---|---|
| `logistic_regression.ipynb` | `logistic_regression.py` | Logistic Regression | `LogisticRegression(random_state=0)` |
| `k_nearest_neighbors.ipynb` | `k_nearest_neighbors.py` | K-Nearest Neighbors | `KNeighborsClassifier(n_neighbors=5, metric='minkowski', p=2)` |
| `support_vector_machine.ipynb` | `support_vector_machine.py` | Support Vector Machine | `SVC(kernel='linear', random_state=0)` |
| `kernel_svm.ipynb` | `kernel_svm.py` | Kernel SVM | `SVC(kernel='rbf', random_state=0)` |
| `naive_bayes.ipynb` | `naive_bayes.py` | Naive Bayes | `GaussianNB()` |
| `decision_tree_classification.ipynb` | `decision_tree_classification.py` | Decision Tree Classification | `DecisionTreeClassifier(criterion='entropy', random_state=0)` |
| `random_forest_classification.ipynb` | `random_forest_classification.py` | Random Forest Classification | `RandomForestClassifier(n_estimators=10, criterion='entropy', random_state=0)` |

## Dataset

This folder includes `Data.csv`. Several notebooks and scripts currently use this placeholder line:

```python
dataset = pd.read_csv('ENTER_THE_NAME_OF_YOUR_DATASET_HERE.csv')
```

Replace the placeholder with the dataset you want to evaluate, for example:

```python
dataset = pd.read_csv('Data.csv')
```

## Evaluation Metrics

The classification notebooks use `confusion_matrix` and `accuracy_score` from `sklearn.metrics`.

| Metric | What it shows |
|---|---|
| Confusion matrix | Counts true positives, true negatives, false positives, and false negatives |
| Accuracy score | Overall share of correct predictions |

Accuracy is easy to compare across notebooks, but it can be misleading when classes are imbalanced. Review the confusion matrix alongside accuracy before deciding which classifier performed best.

## How To Run

1. Update the `pd.read_csv(...)` line to point at the dataset.
2. Confirm the final column is the target variable, or adjust the `X` and `y` slicing.
3. Run the notebook cells from top to bottom, or run the matching `.py` script.
