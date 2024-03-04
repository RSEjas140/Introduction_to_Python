---
title: "Lists and Arrays in Python"
teaching: 10
exercises: 0
questions:
- "What other data structures are there?"
objectives:
- "Understand the use of lists and arrays in Python."
keypoints:
- "Arrays are more efficient for numerical computations compared to lists."
- "Lists are more flexible and can hold different data types, unlike arrays."
---

### Lists

We will take a brief look at lists in Python. At first glance, lists may seem very similar to arrays, but we are going to cover some key differences. 
1. Lists can hold different data types; they are not restricted to a single data type like arrays.
2. Lists can hold various elements such as integers, strings, and even other lists, allowing them to have more complicated and hierarchical structures compared to arrays.  

Try out: 

list_example = [1, "hello", True] 

array_example = numpy.array([1, 2, 3])

If we output both structures via the console:

list_example

[1, "hello", True]

array_example

array([1, 2, 3])

> ## What is different about the 'array_example' and the 'list_example'?  
> Arrays are more efficient for numerical computations compared to lists. They are fixed in size and homogeneous, meaning all elements must be of the same data type. Lists, on the other hand, are more flexible and can hold elements of different data types.

### Accessing elements

To access a specific element in a list, you use single brackets (e.g., "list_example[0]"). Arrays are accessed in a similar way.

list_example[0]

1

array_example[0]

1

### Arrays in Python

Arrays in Python are typically represented using NumPy arrays. NumPy is a powerful library for numerical computing in Python. Arrays are more efficient for numerical computations compared to lists, especially when dealing with large datasets or performing mathematical operations.

NumPy arrays are homogeneous, meaning all elements must be of the same data type. They are also fixed in size, unlike lists which can dynamically resize.

```python
import numpy as np

array_example = np.array([1, 2, 3])
Conclusion
In Python, both lists and arrays have their advantages and use cases. Lists are more flexible and versatile, suitable for general-purpose programming and handling heterogeneous data. Arrays, on the other hand, are more efficient for numerical computations and large datasets, making them ideal for scientific computing and data analysis tasks.