<p align="center"><img src="" width=1000></p>

# EtchKay

[![PyPI][pypi_badge]][pypi_link] [![GitHub][github_badge]][github_link]

The concept is to have a personal moduel that contains all the handy functions that support efficient python workflows in the domain of data science and analytics.

🚩 v0.0.1 is now available with the initial concepts of the pathway to compress data science and analytics.

---

## Installation
To run the code successfully, all the dependencies can either be installed using **pip**:

```bash
pip install etchkay
```

## Features (Usage/Examples)

### A compressed module for Data Science & Analytics
*Available for use from v0.0.1*
```python
import etchkay
```

#### Limitations (in-scope features)
  - Data Cleaning concepts available 
```python
╔══════════════════════════════════════════════════════════════════════════╗
║                    How to use some available functions                   ║
╚══════════════════════════════════════════════════════════════════════════╝
>>> etchkay.clean_data(dataframe, drop_cols=None, fillna_cols=None, numeric_cols=None, date_cols=None, text_cols=None, regex_dict=None)
+------------------------------------------------------------+
|                returns cleaned dataframe                   |
+------------------------------------------------------------+

>>> etchkay.remove_outliers(dataframe, numeric_cols, threshold=3)
+------------------------------------------------------------+
|          returns dataframe with no outliers in it          |
+------------------------------------------------------------+

>>> etchkay.standardize_text(dataframe, text_cols)
+------------------------------------------------------------+
|         returns dataframe stopwords included in it         |
+------------------------------------------------------------+

>>> etchkay.encode_categorical(dataframe, cat_cols, encoding='one-hot')
+------------------------------------------------------------+
|      returns dataframe with encoded columns converted      |
|        from categorical columns (one-hot / label)          |
+------------------------------------------------------------+

>>> etchkay.handle_missing_values(dataframe, numeric_cols, cat_cols)
+------------------------------------------------------------+
|      returns dataframe filed with missing values           |
|                   using mean and mode                      |
+------------------------------------------------------------+

>>> etchkay.remove_duplicates(dataframe)
+------------------------------------------------------------+
|         returns dataframe with no duplicates in it         |
+------------------------------------------------------------+

>>> etchkay.normalize_data(dataframe, numeric_cols, scaling='min-max')
+------------------------------------------------------------+
|     Normalize your dataframe using min-max / z-score       |
+------------------------------------------------------------+

>>> etchkay.clean_text(dataframe, text_cols)
+------------------------------------------------------------+
|               clean your text attributes                   |
+------------------------------------------------------------+

>>> etchkay.handle_noisy_data(dataframe, column, window)
+------------------------------------------------------------+
|         Handle noisy data using rolling functions          |
+------------------------------------------------------------+
```
- Data Visualizations
```python
╔══════════════════════════════════════════════════════════════════════════╗
║                    How to use some available functions                   ║
╚══════════════════════════════════════════════════════════════════════════╝
>>> etchkay.generate_visualizations(dataframe)
+------------------------------------------------------------+
|       returns insightful visualizations which could be     |
|         possibly generated on the dataset provided         |
+------------------------------------------------------------+
```

- Machine Learning
```python
╔══════════════════════════════════════════════════════════════════════════╗
║                    How to use some available functions                   ║
╚══════════════════════════════════════════════════════════════════════════╝
>>> model = etchkay.perform_regression(dataframe, target_column, feature_columns, regression_type='linear', test_size=0.2, random_state=42)
+------------------------------------------------------------------------------------------------------------------+
|     Perform regression on a given dataset and return the trained model object.                                   |
|                                                                                                                  |
|     Parameters:                                                                                                  |
|        df (pandas.DataFrame): The input dataset.                                                                 |
|        target_column (str): The name of the target column.                                                       |
|        feature_columns (list): A list of column names to use as features.                                        |
|        regression_type (str): The type of regression to perform. Must be one of ['linear', 'ridge', 'lasso',     |
|            'elastic_net', 'decision_tree', 'random_forest', 'gradient_boosting']. Default is 'linear'.           |
|        test_size (float): The proportion of the data to use for testing. Default is 0.2.                         |
|       random_state (int): The random seed to use for reproducibility. Default is 42.                             |
|                                                                                                                  |
|    Returns:                                                                                                      |
|        A trained regression model object.                                                                        |
+------------------------------------------------------------------------------------------------------------------+

>>> best_model = etchkay.get_best_regression(dataframe)
+------------------------------------------------------------------------------------------------------------------+
|     Identify the best regression model for a given dataset and return the trained model object.                  |
|                                                                                                                  |
|          Parameters:                                                                                             |
|              df (pandas.DataFrame): The input dataset.                                                           |
|                                                                                                                  |
|           Returns:                                                                                               |
|               A trained regression model object.                                                                 |
+------------------------------------------------------------------------------------------------------------------+

>>> results = etchkay.perform_clustering(dataframe)
+------------------------------------------------------------------------------------------------------------------+
|       Performs various clustering models on a given dataframe and returns the resulting labels                   |
|        and inertia values for each model.                                                                        |
|                                                                                                                  |
|          Parameters:                                                                                             |
|            df (pd.DataFrame): Dataframe to be clustered                                                          |
|                                                                                                                  |
|          Returns:                                                                                                |
|            results (dict): A dictionary containing the resulting labels                                          |
|              and inertia values for each clustering model                                                        |
+------------------------------------------------------------------------------------------------------------------+

>>> model, accuracy, precision, recall, f1 = etchkay.apply_classification(dataset, target_column, classification_technique="decision_tree")
+------------------------------------------------------------------------------------------------------------------+
|       Performs classification model on a given dataframe (classification techniques: descision_tree,             |
|                                            random_forest, logistic_regression, svm, naive_bayes)                 |
|        and inertia values for each model.                                                                        |
|                                                                                                                  |
|          Parameters:                                                                                             |
|            df (pd.DataFrame): Dataframe to perform classification on                                             |
|            target_column: Label / Target column to perform classification on                                     |                                                          |            classification_technique: Technique to perform                                                        |
|                                                                                                                  |
|          Returns:                                                                                                |
|            results : model, accuracy, precision, recall, f1                                                      |
+------------------------------------------------------------------------------------------------------------------+

>>> model, best_technique, accuracy, precision, recall, f1 = etchkay.find_best_classification(dataframe, target_column)
+------------------------------------------------------------------------------------------------------------------+
|         Performs and returns best classification model returning model, best technique, accuracy,                |
|                              precision, recall, f1                                                               |
|                                                                                                                  |
|          Parameters:                                                                                             |
|            df (pd.DataFrame): Dataframe to perform classification on                                             |
|            target_column: Label / Target column to perform classification on                                     |                                                         
|                                                                                                                  |
|          Returns:                                                                                                |
|            results : model, best_technique, accuracy, precision, recall, f1                                      |
+------------------------------------------------------------------------------------------------------------------+
```

## Changelog

v0.0.1
- Minor release that supports the compressed module with initial techniques in the data science and analytics domain
- `import etchkay` 

## Authors

- [Hamza Khalid](https://www.linkedin.com/in/hamzaakhalid/)

[github_badge]: https://badgen.net/badge/icon/GitHub?icon=github&color=47b778&label
[github_link]: https://github.com/hamzaa-khalid/etchkay

[pypi_badge]: https://badgen.net/pypi/v/etchkay?icon=pypi&color=47b778&labelColor=090422
[pypi_link]: https://pypi.org/project/etchkay/
