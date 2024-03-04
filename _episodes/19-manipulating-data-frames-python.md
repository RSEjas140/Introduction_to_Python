
title: "Manipulating data frames"
teaching: 20
exercises: 10
questions:
- "How do I access the data stored in data frames?"
objectives:
- "Understand the fundamentals of addressing data frames."
keypoints:
- "The complexity of the process is related to the complexity of the conditions for retrieving the data you want."
---

## Datasets

In Python, the pandas library provides functionality similar to R's data frames. Let's start by exploring the iris dataset.

```python
import pandas as pd

# Load iris dataset
iris = pd.read_csv('https://raw.githubusercontent.com/mwaskom/seaborn-data/master/iris.csv')

# Display the first few rows
print(iris.head())
{: .language-python}

Copy code
   sepal_length  sepal_width  petal_length  petal_width species
0           5.1          3.5           1.4          0.2  setosa
1           4.9          3.0           1.4          0.2  setosa
2           4.7          3.2           1.3          0.2  setosa
3           4.6          3.1           1.5          0.2  setosa
4           5.0          3.6           1.4          0.2  setosa
{: .output}

We can use various methods to examine and manipulate this dataset.

Accessing Data Frames
python
Copy code
# Display basic information about the dataset
print(iris.info())

# Display summary statistics
print(iris.describe())
{: .language-python}

The info() method provides information about the dataframe's structure, and the describe() method gives summary statistics for numerical columns.

Adding and Removing Columns and Rows
python
Copy code
# Add a new column 'num_petals'
iris['num_petals'] = 4

# Remove the 'num_petals' column
iris = iris.drop(columns=['num_petals'])

# Add a new row
new_row = {'sepal_length': 5.4, 'sepal_width': 3.2, 'petal_length': 4.9, 'petal_width': 1.9, 'species': 'setosa'}
iris = iris.append(new_row, ignore_index=True)

# Remove a row
iris = iris.drop(iris.index[-1])
{: .language-python}

Subsetting Data Frames
python
Copy code
# Select specific columns
print(iris[['sepal_length', 'sepal_width']])

# Select rows by index
print(iris.iloc[[1, 2, 3]])

# Select rows and columns using slices
print(iris.iloc[1:4, 1:3])

# Select rows based on condition
print(iris[iris['sepal_length'] > 5.0])
{: .language-python}

Additional Options
Pandas provides many more options for data manipulation, similar to those available in R. For more advanced operations, you can explore pandas documentation or other libraries like NumPy for array manipulation.

css
Copy code

This converted content should work in a Python environment like Spyder, allowing users to manipulate and analyze data frames using pandas.