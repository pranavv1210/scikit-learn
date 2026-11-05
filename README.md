# scikit-learn — Practical Machine Learning Examples

This repository is a hands-on collection of Python and scikit-learn notebooks. It covers core estimators, preprocessing, model selection, evaluation, model persistence and a complete Bengaluru house-price prediction project.

The original notebooks, datasets, model files and client/server project files are retained. Some examples originate from older tutorial workflows; read the explanations added around them and pay attention to any compatibility notes before running older cells with a newer scikit-learn release.

## Learning path

| Stage | Existing folders | Key skills |
|---|---|---|
| Ensembles and trees | 01–02, 14 | Bagging, decision trees, random forests |
| Categorical data | 03 | Encoding and dummy variables |
| Model selection | 04, 06, 17 | Hyperparameter search, cross-validation, train/test split |
| Clustering and neighbors | 05, 07 | K-Means, KNN |
| Regression and classification | 08–11 | Linear/logistic regression, multivariate regression, Naive Bayes |
| Dimensionality and generalization | 12, 15–16 | PCA, regularization, SVM |
| Applied project | 13 | Bengaluru house-price workflow and prediction service |

## Folder guide

1. Bagging
2. Decision Tree
3. One Hot Encoding
4. Hyperparameter Tuning
5. K-Means Clustering
6. K-Fold Cross Validation
7. K-Nearest Neighbor Classification
8. Linear Regression
9. Logistic Regression
10. Multivariate Regression
11. Naive Bayes
12. Principal Component Analysis
13. Projects — Bengaluru house prices
14. Random Forest
15. Regularization
16. Support Vector Machine
17. Train And Test Split
18. Miscellaneous Files

## How to study

- Read the explanation before running each code cell.
- Identify what each variable represents and inspect its shape.
- Understand which columns are features and which column is the target.
- Understand whether the task is regression, classification or clustering.
- Check how training and test data are separated.
- Interpret metrics instead of simply trying to maximize a score.
- When a model is saved, understand which preprocessing steps and feature order it expects.

## Setup

```bash
python -m venv .venv
# Windows PowerShell:
.venv\Scripts\Activate.ps1
# macOS / Linux:
source .venv/bin/activate
python -m pip install --upgrade pip
pip install numpy pandas matplotlib seaborn scikit-learn jupyter joblib
jupyter notebook
```

Older notebooks may use APIs or prediction formats that generate warnings in recent releases. The correct long-term pattern is to keep feature names and column order consistent between fit and predict, and to use Pipelines for preprocessing plus the estimator.

## Important terminology

- **Estimator:** a scikit-learn object that learns from data through `fit`.
- **Transformer:** an object that learns a data transformation and applies it through `transform`.
- **Predictor:** an estimator that can produce predictions using `predict`.
- **Pipeline:** a sequence of transformers and a final estimator treated as one workflow.
- **Hyperparameter:** a setting chosen outside the model's learned coefficients, such as `max_depth`.
- **Cross-validation:** repeated train/validation splits used to estimate how a model may generalize.
- **Feature encoding:** converting categories such as city names into numeric representations a model can process.

## Project: Bengaluru house prices

The project demonstrates loading and cleaning real-estate data, engineering features such as BHK and price per square foot, handling location categories, training a regression model, tuning alternatives, saving a model and exposing prediction logic through a small server/client example.

The dataset is historical and the resulting model is an educational example. Its predictions must not be treated as current property valuations or financial advice.

## Further reading

- [scikit-learn User Guide](https://scikit-learn.org/stable/user_guide.html)
- [scikit-learn API reference](https://scikit-learn.org/stable/modules/classes.html)
- [GeeksforGeeks scikit-learn tutorials](https://www.geeksforgeeks.org/machine-learning/)
- [Pandas documentation](https://pandas.pydata.org/docs/)
- [Matplotlib documentation](https://matplotlib.org/stable/)

Open `study-tracker.html` to track your study progress.
