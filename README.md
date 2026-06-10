# 🧠 Machine Learning Notebooks — Udemy Course

A personal collection of Python notebooks created while completing a Machine Learning course on Udemy. Focused on **Supervised Learning** including regression and classification techniques.

---

## 👨‍🎓 About This Repo

This repository documents my learning journey through Machine Learning. Each notebook is self-contained with code, explanations, and outputs so I can revisit concepts easily and track my progress over time.

---

## 📁 Folder Structure

```
ML-Notebooks/
│
├── 00_datapreprocessing/
│   └── data_preprocessing_cm.ipynb 
│
├── 01_regression/
│   ├── simple_linear_regression_cm.ipynb
│   ├── multiple_linear_regression_cm.ipynb
│   ├── polynomial_regression_cm.ipynb
│   ├── decision_tree_regression_cm.ipynb
│   └── random_forest_regression_cm.ipynb
│
├── 02_classification/
│   ├── logistic_regression.ipynb
│   ├── decision_tree.ipynb
│   ├── random_forest.ipynb
│   ├── knn_classifier.ipynb
│   └── svm_classifier.ipynb
│
├── 03_model_evaluation/
│   ├── confusion_matrix.ipynb
│   ├── cross_validation.ipynb
│   └── bias_variance_tradeoff.ipynb
│
├── model_selection/
│   ├── regression/                         
│   │   ├── multiple_linear_regression.ipynb
│   │   ├── polynomial_regression.ipynb
│   │   ├── support_vector_regression.ipynb
│   │   ├── decision_tree_regression.ipynb
│   │   └── random_forest_regression.ipynb
│   │
│   └── classification/                     ← Coming soon
│
├── datasets/
│   └── Data.csv                            (used by SVR notebook)
│
└── README.md
```

---

## 📚 Topics Covered

### 📈 Regression
- Simple Linear Regression
- Multiple Linear Regression
- Polynomial Regression
- Support Vector Regression
- Decision Tree Regression
- Random Forest Regression

### 🔷 Classification
- Logistic Regression
- Decision Trees
- Random Forest
- K-Nearest Neighbors (KNN)
- Support Vector Machines (SVM)

### 📊 Model Evaluation
- Train/Test Split
- Cross Validation
- Confusion Matrix
- Accuracy, Precision, Recall, F1-Score
- Bias-Variance Tradeoff

---

## 🆕 Model Selection — Regression (R² Performance Comparison)

The `model_selection/regression/` folder contains notebooks that train and evaluate five regression models on the same pipeline, using **R² (Coefficient of Determination)** as the performance metric.

Each notebook follows the same structure:
1. Import libraries
2. Load dataset
3. Split into train/test sets (80/20, `random_state=0`)
4. Train the model
5. Predict on the test set
6. Evaluate using `r2_score` from `sklearn.metrics`

### 📓 Notebooks

| Notebook | Model | Key Detail | Feature Scaling |
|---|---|---|---|
| `multiple_linear_regression.ipynb` | Multiple Linear Regression | OLS via `LinearRegression()` | No |
| `polynomial_regression.ipynb` | Polynomial Regression | Degree 4, `PolynomialFeatures` + `LinearRegression` | No |
| `support_vector_regression.ipynb` | Support Vector Regression | RBF kernel, `SVR()` | ✅ Yes — `StandardScaler` on X and y |
| `decision_tree_regression.ipynb` | Decision Tree Regression | `DecisionTreeRegressor(random_state=0)` | No |
| `random_forest_regression.ipynb` | Random Forest Regression | 10 estimators, `random_state=0` | No |

### 📐 R² Score — What it measures

R² (Coefficient of Determination) measures the proportion of variance in the target variable explained by the model:

```
R² = 1 - (SSR / SST)
```

- **R² = 1.0** → perfect fit
- **R² = 0.0** → model no better than predicting the mean
- **R² < 0** → model worse than a flat mean prediction

> **Note on SVR:** Feature scaling is mandatory for SVR since it is distance-based. Both `X` and `y` are scaled using separate `StandardScaler` instances, and predictions are inverse-transformed before computing R².

### 📊 Known R² Result

| Model | R² Score |
|---|---|
| Support Vector Regression | **0.9481** (from notebook output) |
| Multiple Linear Regression | Run notebook to evaluate |
| Polynomial Regression | Run notebook to evaluate |
| Decision Tree Regression | Run notebook to evaluate |
| Random Forest Regression | Run notebook to evaluate |

> R² scores for remaining models will be populated as notebooks are run against a dataset.

### ⚙️ How to run

1. Place your dataset CSV in the `datasets/` folder
2. Update the `pd.read_csv(...)` line in each notebook to point to your file
3. Run all cells top to bottom

```python
# Update this line in each notebook
dataset = pd.read_csv('../datasets/Data.csv')
```

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| **Python 3.x** | Core language |
| **Jupyter Notebook** | Interactive coding environment |
| **NumPy** | Numerical computing |
| **Pandas** | Data manipulation |
| **Matplotlib / Seaborn** | Data visualization |
| **Scikit-learn** | ML algorithms & evaluation |

---

## ⚙️ Getting Started

### 1. Clone the Repo
```bash
git clone https://github.com/ChetanM-collab/ML-Notebooks.git
cd ML-Notebooks
```

### 2. Install Dependencies
```bash
pip install numpy pandas matplotlib seaborn scikit-learn jupyter
```

### 3. Launch Jupyter
```bash
jupyter notebook
```

---

## 📈 Progress Tracker

| Topic | Status |
|---|---|
| Data Pre-processing | ✅ Complete |
| Simple Linear Regression | ✅ Complete |
| Multiple Linear Regression | ✅ Complete |
| Polynomial Regression | ✅ Complete |
| Support Vector Regression | ✅ Complete |
| Decision Tree Regression | ✅ Complete |
| Random Forest Regression | ✅ Complete |
| Model Selection — Regression (R²) | ✅ Complete |
| Model Selection — Classification | ⏳ Upcoming |
| Logistic Regression | ⏳ Upcoming |
| Decision Trees | ⏳ Upcoming |
| Random Forest | ⏳ Upcoming |
| KNN | ⏳ Upcoming |
| SVM | ⏳ Upcoming |
| Model Evaluation | ⏳ Upcoming |

---

## 🎯 Goal

Complete the Udemy ML course, build a strong foundation in supervised learning, and apply these skills to real-world projects and freelance work.

---

## 📌 Notes

- Notebooks include markdown explanations alongside code
- Datasets are stored in the `/datasets` folder
- SVR notebook requires feature scaling — scalers are fit on training data only
- Progress tracker above is updated as topics are completed

---

## 🙋‍♂️ Author

**Your Name**
- GitHub: [@ChetanM-collab](https://github.com/ChetanM-collab)
- LinkedIn: [ChetanMMohite](https://www.linkedin.com/in/chetanmmohite/)

---

> 💡 *"The best way to learn machine learning is to build things."*
