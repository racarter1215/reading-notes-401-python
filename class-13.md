# How to run Linear regression in Python scikit-Learn

## Scikit-learn: a powerful Python module for machine learning. It contains function for regression, classification, clustering, model selection and dimensionality reduction.

### First, import the required Python libraries into Ipython Notebook. Example:
import sklearn

### Next, write:
from sklearn.datasets import load_boston
boston = load_boston()

boston.keys()
['data', 'feature_names', 'DESCR', 'target']

boston.data.shape
(506, 13)

### See example for printed dictionary

### List of import functions:
##### lm.fit() -> fits a linear model
##### lm.predict() -> Predict Y using the linear model with estimated coefficients
##### lm.score() -> Returns the coefficient of determination (R^2)

### You can also explore the functions inside lm object by pressing lm.<tab>
#### .coef_ gives the coefficients and .intercept_ gives the estimated intercepts.
  
### How to do train-test split
#### You have to divide your data sets randomly (scikit learn provides a function called train_test_split to do this)

