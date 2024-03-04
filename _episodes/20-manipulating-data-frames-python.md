---
title: "Pandas and manipulating data frames"
teaching: 20
exercises: 10
questions:
- "How do I organise tabular data efficiently?"
objectives:
- "Understand how Pandas can be used to store, manipulate and subset tabular data."
keypoints:
- "Pandas provides powerful data structures like Series and DataFrame for easy manipulation and analysis of structured data."
- "It offers extensive functionality for data cleaning, selection, transformation, and integration with other libraries like NumPy and Matplotlib."
- "With Pandas, you can efficiently handle data tasks such as handling missing values, merging datasets, and preparing data for machine learning models."
---

## Inspecting Datasets
Pandas is a Python library for data manipulation and analysis, providing powerful data structures like DataFrame and Series along with a wide range of functions for tasks such as data cleaning, preparation, and exploration. It is widely used in data science and machine learning workflows for its ease of use and flexibility.

We can now explore the Iris dataset to gain insights into its structure and contents.

### Inspecting a Dataset
To understand the structure of the Iris dataset, we can use various methods provided by Pandas:

```
print(iris_df.head())
```
{: .language-python}

```
print(iris_df.info())
```
{: .language-python}

```
print(iris_df.describe())
```
{: .language-python}

Understanding the contents and data types of a data set is important for accurate analysis.

### Manipulating DataFrames
Pandas provides powerful functionalities to manipulate DataFrames. Here are some examples:

Adding and Removing Columns

Adding:
```
iris_df['sepal_ratio'] = iris_df['sepal_length'] / iris_df['sepal_width']
```
{: .language-python}

Removing:
```
iris_df.drop('species', axis=1, inplace=True)
```
{: .language-python}

Adding and removing rows

Adding:
```
new_row = {'sepal_length': 5.1, 'sepal_width': 3.5, 'petal_length': 1.4, 'petal_width': 0.2, 'species': 'setosa'}
iris_df = iris_df.append(new_row, ignore_index=True)
```
{: .language-python}

Removing:
```
iris_df.drop(0, inplace=True)
```
{: .language-python}


### Subsetting Data

Subsetting allows us to select specific rows or columns based on conditions:

```
# Select rows where petal_length is greater than 5
subset_df = iris_df[iris_df['petal_length'] > 5]
```
{: .language-python}

```
# Select rows where species is 'setosa' and petal_length is less than 1.5
subset_df = iris_df[(iris_df['species'] == 'setosa') & (iris_df['petal_length'] < 1.5)]
```
{: .language-python}

```
# Select rows where sepal_length is greater than 5 and species is either 'setosa' or 'versicolor'
subset_df = iris_df[(iris_df['sepal_length'] > 5) & (iris_df['species'].isin(['setosa', 'versicolor']))]
```
{: .language-python}

```
# Select rows where species is 'setosa' or 'versicolor' and petal_length is not equal to 1.5
subset_df = iris_df[(iris_df['species'].isin(['setosa', 'versicolor'])) & (iris_df['petal_length'] != 1.5)]
```
{: .language-python}


### Applying a function

To apply a function to a DataFrame column in Pandas, you can use the .apply() method.

```
# Define a custom function
def square_value(x):
    return x ** 2
```
{: .language-python}

```
iris_df['petal_length_squared'] = df['petal_length'].apply(square_value)
```
{: .language-python}

