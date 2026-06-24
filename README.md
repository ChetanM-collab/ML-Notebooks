# Machine Learning Notebooks - Udemy Course

A personal collection of Python and Jupyter notebooks created while completing a Machine Learning course on Udemy. The repo currently focuses on supervised learning workflows, including data preprocessing, regression, classification, and model selection.

## About This Repo

This repository documents my machine learning learning journey. Each notebook is intended to be self-contained enough to revisit concepts, rerun examples, and compare how different algorithms behave on similar datasets.

## Folder Structure

```text
ML-Notebooks/
|-- 00_datapreprocessing/
|   `-- data_preprocessing.ipynb
|
|-- 01_Regression/
|   |-- simple_linear_regression_cm.ipynb
|   |-- multiple_linear_regression_cm.ipynb
|   |-- polynomial_regression_cm.ipynb
|   |-- support_vector_regression_cm.ipynb
|   |-- decision_tree_regression_cm.ipynb
|   `-- random_forest_regression_cm.ipynb
|
|-- 02_Classification/
|   |-- logistic_regression_cm.ipynb
|   |-- k_nearest_neighbors_cm.ipynb
|   |-- support_vector_machine_cm.ipynb
|   |-- kernel_svm.ipynb
|   |-- naive_bayes.ipynb
|   |-- decision_tree_classification.ipynb
|   `-- random_forest_classification.ipynb
|
|-- ModelSelection/
|   |-- Regression/
|   |   |-- README.md
|   |   |-- multiple_linear_regression.ipynb
|   |   |-- polynomial_regression.ipynb
|   |   |-- support_vector_regression.ipynb
|   |   |-- decision_tree_regression.ipynb
|   |   `-- random_forest_regression.ipynb
|   |
|   `-- Classification/
|       |-- README.md
|       |-- Data.csv
|       |-- logistic_regression.ipynb
|       |-- k_nearest_neighbors.ipynb
|       |-- support_vector_machine.ipynb
|       |-- kernel_svm.ipynb
|       |-- naive_bayes.ipynb
|       |-- decision_tree_classification.ipynb
|       |-- random_forest_classification.ipynb
|       `-- matching .py scripts for each classifier
|
|-- datasets/
|   |-- Data.csv
|   |-- Data1.csv
|   |-- Position_Salaries.csv
|   |-- Salary_Data.csv
|   `-- Social_Network_Ads.csv
|
`-- README.md
```

## Topics Covered

### Data Preprocessing

- Importing libraries and datasets
- Handling missing data
- Encoding categorical variables
- Splitting data into training and test sets
- Feature scaling

### Regression

- Simple Linear Regression
- Multiple Linear Regression
- Polynomial Regression
- Support Vector Regression
- Decision Tree Regression
- Random Forest Regression

### Classification

- Logistic Regression
- K-Nearest Neighbors
- Support Vector Machine
- Kernel SVM
- Naive Bayes
- Decision Tree Classification
- Random Forest Classification

### Model Selection

Detailed model-selection notes now live inside the model-selection subfolders:

- [Model Selection - Regression](ModelSelection/Regression/README.md)
- [Model Selection - Classification](ModelSelection/Classification/README.md)

These folders focus on comparing models with consistent train/test splits and common evaluation metrics.

## Tech Stack

| Tool | Purpose |
|---|---|
| Python 3.x | Core language |
| Jupyter Notebook | Interactive coding environment |
| NumPy | Numerical computing |
| Pandas | Data manipulation |
| Matplotlib / Seaborn | Data visualization |
| Scikit-learn | ML algorithms and evaluation |

## Getting Started

### 1. Clone the repo

```bash
git clone https://github.com/ChetanM-collab/ML-Notebooks.git
cd ML-Notebooks
```

### 2. Install dependencies

```bash
pip install numpy pandas matplotlib seaborn scikit-learn jupyter
```

### 3. Launch Jupyter

```bash
jupyter notebook
```

## Progress Tracker

| Topic | Status |
|---|---|
| Data preprocessing | Complete |
| Simple Linear Regression | Complete |
| Multiple Linear Regression | Complete |
| Polynomial Regression | Complete |
| Support Vector Regression | Complete |
| Decision Tree Regression | Complete |
| Random Forest Regression | Complete |
| Logistic Regression | Complete |
| K-Nearest Neighbors | Complete |
| Support Vector Machine | Complete |
| Kernel SVM | Complete |
| Naive Bayes | Complete |
| Decision Tree Classification | Complete |
| Random Forest Classification | Complete |
| Model Selection - Regression | Complete |
| Model Selection - Classification | Complete |

## Notes

- Datasets are stored in the root `datasets/` folder, with an additional `Data.csv` inside `ModelSelection/Classification/`.
- Model-selection notebooks use placeholder dataset names in some files. Update `pd.read_csv(...)` before running those notebooks against a specific dataset.
- Classification model-selection notebooks evaluate predictions with a confusion matrix and accuracy score.
- Regression model-selection notebooks evaluate predictions with R2 score.
- Distance-based models such as SVR, SVM, Kernel SVM, and KNN require feature scaling.

## Goal

Complete the Udemy ML course, build a strong foundation in supervised learning, and apply these skills to real-world projects and freelance work.

## Author

**Chetan Mohite**

- GitHub: [@ChetanM-collab](https://github.com/ChetanM-collab)
- LinkedIn: [ChetanMMohite](https://www.linkedin.com/in/chetanmmohite/)

> "The best way to learn machine learning is to build things."
