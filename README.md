# task18-Select-Dataset-Columns-using-Pandas-loc-and-iloc

## Project Overview

This project demonstrates how to select specific rows and columns from a
dataset using the Pandas library in Python. The Iris dataset from
Scikit-learn is used for practice.

## Objective

Learn how to access specific parts of a Pandas DataFrame using: - `loc`
for label-based selection. - `iloc` for integer position-based
selection.

## Tools and Technologies

-   Python
-   Pandas
-   Scikit-learn
-   Jupyter Notebook

## Dataset

The project uses the built-in Iris dataset available through
`sklearn.datasets.load_iris()`.

The dataset contains four numerical features: - Sepal length (cm) -
Sepal width (cm) - Petal length (cm) - Petal width (cm)

## Installation

Install the required libraries if they are not already installed:

``` bash
pip install pandas scikit-learn jupyter
```

## How to Run

1.  Open Jupyter Notebook.
2.  Create a new Python 3 notebook.
3.  Copy the project code into notebook cells in the order given below.
4.  Run each cell using **Shift + Enter**.

## Code

### 1. Import libraries

``` python
import pandas as pd
from sklearn.datasets import load_iris
```

### 2. Load the dataset into a DataFrame

``` python
iris = load_iris()
df = pd.DataFrame(iris.data, columns=iris.feature_names)
print(df.head())
```

### 3. Select rows and columns using `loc`

``` python
# Select one row by its label
print(df.loc[0])

# Select rows 0 through 4 (both endpoints included)
print(df.loc[0:4])

# Select one column by its name
print(df.loc[:, 'sepal length (cm)'])

# Select rows 0 through 4 and two named columns
print(df.loc[0:4, ['sepal length (cm)', 'petal length (cm)']])
```

### 4. Select rows and columns using `iloc`

``` python
# Select the first row by position
print(df.iloc[0])

# Select the first five rows
print(df.iloc[0:5])

# Select the first column by position
print(df.iloc[:, 0])

# Select the first five rows and first two columns
print(df.iloc[0:5, 0:2])
```

### 5. Compare both methods

``` python
loc_result = df.loc[0:4, ['sepal length (cm)', 'sepal width (cm)']]
print("Selection using loc:")
print(loc_result)

iloc_result = df.iloc[0:5, 0:2]
print("\nSelection using iloc:")
print(iloc_result)
```

### 6. Display dataset information

``` python
print("Dataset shape:", df.shape)
print("Column names:")
print(df.columns)
print("\nDataset information:")
df.info()
```

## Difference Between `loc` and `iloc`

  `loc`                        `iloc`
  ---------------------------- ----------------------------------
  Label-based selection        Integer position-based selection
  Uses row and column labels   Uses row and column positions
  Slice endpoint is included   Slice endpoint is excluded

For example, `df.loc[0:4]` selects labels 0, 1, 2, 3, and 4.
`df.iloc[0:5]` selects positions 0, 1, 2, 3, and 4.

## Expected Deliverables

-   Examples using `loc`.
-   Examples using `iloc`.
-   Examples selecting both rows and columns.
-   Output displaying the selected records.

## Conclusion

This project demonstrates how to select specific rows and columns from a
dataset using Pandas. It explains the difference between label-based
selection with `loc` and position-based selection with `iloc`, using the
Iris dataset.

## Author

Add your name and course details here before submitting.
