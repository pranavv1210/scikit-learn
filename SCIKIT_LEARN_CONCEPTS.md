# scikit-learn Concepts Explained

## The estimator pattern

Most scikit-learn models follow a predictable interface:

```python
model = SomeEstimator(parameters)
model.fit(X_train, y_train)
predictions = model.predict(X_test)
```

- **Estimator:** the object that learns patterns from examples.
- **X:** a table of input features. Conventionally rows are observations and columns are features.
- **y:** the target values corresponding to rows in X.
- **fit:** learns internal model parameters from the training data.
- **predict:** applies the learned model to new feature rows.

For unsupervised algorithms, `fit(X)` may not need a target. Some estimators also provide `transform`, `predict_proba` or `decision_function`.

## Transformers

A transformer changes the representation of data. For example, StandardScaler learns a training-set mean and standard deviation, then scales each feature.

```python
from sklearn.preprocessing import StandardScaler

scaler = StandardScaler()
X_train_scaled = scaler.fit_transform(X_train)
X_test_scaled = scaler.transform(X_test)
```

Notice the difference: fit the scaler on training data only. Calling `fit_transform` on the test set would allow information from the test distribution to influence preprocessing.

## Pipelines

A Pipeline connects transformations and a final model:

```python
from sklearn.pipeline import make_pipeline
from sklearn.preprocessing import StandardScaler
from sklearn.linear_model import LogisticRegression

model = make_pipeline(StandardScaler(), LogisticRegression())
model.fit(X_train, y_train)
predictions = model.predict(X_test)
```

This is safer and easier to cross-validate because the scaler is refit inside each training fold.

## Train/test split

A training set is used to fit the model. A test set is held back to estimate performance on unseen examples. Repeatedly selecting models based on the test score turns the test set into a validation set and makes the final estimate optimistic.

Use validation data or cross-validation to choose models and hyperparameters. Keep the test set for final evaluation.

## Classification vs regression

- Regression predicts a numeric quantity, such as a house price.
- Classification predicts a category, such as spam vs not spam.

The metric must match the task and the cost of errors. Accuracy alone can be misleading when the class distribution is uneven.

## Hyperparameters

Learned parameters are determined from training data. Hyperparameters are configuration choices supplied by the practitioner, such as tree depth, number of neighbors or regularization strength. Search them using cross-validation rather than tuning against the final test set.

## Feature names and warnings

When a model is fitted using a Pandas DataFrame, scikit-learn may remember feature names. Passing a plain list or NumPy array to predict can trigger a feature-name warning. Prefer a DataFrame with the same named columns and order used during training.

## Common terms

- **Overfitting:** fitting noise or training-specific detail, resulting in weaker generalization.
- **Underfitting:** a model is too simple to capture the important pattern.
- **Regularization:** a penalty or constraint that discourages overly complex models.
- **Stratification:** preserving approximate class proportions across splits.
- **Leakage:** allowing information unavailable at prediction time to influence training.
- **Baseline:** a simple reference model used to judge whether a more complex approach adds value.
