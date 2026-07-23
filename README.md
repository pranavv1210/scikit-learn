# Scikit-Learn Practice Projects

This repository contains machine learning practice notebooks, datasets, saved models, and a small Flask-based house price prediction project.

## Folder Structure

1. **Bagging** - Bagging classifier examples with the diabetes dataset.
2. **Decision Tree** - Decision tree examples using salary and Titanic datasets.
3. **One Hot Encoding** - One-hot encoding and dummy variable examples.
4. **Hyperparameter Tuning** - Model tuning examples.
5. **K-Means Clustering** - K-Means clustering examples for income and Iris datasets.
6. **K-Fold Cross Validation** - K-Fold and cross-validation examples.
7. **K-Nearest Neighbor Classification** - KNN classification notebook.
8. **Linear Regression** - Linear regression notebooks, sample CSV files, and saved models.
9. **Logistic Regression** - Binary and multiclass logistic regression notebooks.
10. **Multivariate Regression** - Multivariate regression examples.
11. **Naive Bayes** - Naive Bayes examples for Titanic, wine, and spam classification.
12. **Principal Component Analysis** - PCA example notebook.
13. **Projects** - Bangalore house price prediction project with notebook, model, client, and Flask server.
14. **Random Forest** - Random forest notebook.
15. **Regularization** - Regularization notebook and housing dataset.
16. **Support Vector Machine** - SVM notebook.
17. **Train And Test Split** - Train/test split notebook and data.
18. **Miscellaneous Files** - Additional compiled class files.

## Requirements

The notebooks use common Python data science packages:

- Python
- Jupyter Notebook
- numpy
- pandas
- matplotlib
- scikit-learn
- flask and flask-cors for the house price prediction server

Install the main dependencies with:

```bash
pip install numpy pandas matplotlib scikit-learn flask flask-cors notebook
```

## Running Notebooks

Start Jupyter from the repository root:

```bash
jupyter notebook
```

Then open any notebook from the numbered topic folders.

## House Price Prediction Project

The project is under `13. Projects`.

To run the Flask server:

```bash
cd "13. Projects/server"
python server.py
```

Then open `13. Projects/client/app.html` in a browser. The client expects the API at `http://127.0.0.1:5000`.

## Notes

- Folder names have been numbered and capitalized for a cleaner learning sequence.
- Generated Python cache files and Jupyter checkpoint folders are ignored by git.
