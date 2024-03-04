---
title: "Plotting in Python with Matplotlib"
teaching: 10
exercises: 5
questions:
- "How do I create plots?"
- "How do I use data sets to populate my plot?"
objectives:
- "Understand how plots are formed syntactically in Matplotlib."
- "Can create plots from data sets."
keypoints:
- "Plotting is a useful tool for understanding our data; it is not just for results visualization."
---

## Plotting

Plotting our data is one of the best ways to intuitively explore it, and the various relationships between variables. While there are several libraries available for plotting in Python, we'll be using Matplotlib because it is versatile and widely used.

Matplotlib is a comprehensive library for creating static, animated, and interactive visualizations in Python.

Let's start by exploring a simple example using Matplotlib in Python. Make sure you have Matplotlib installed in your Python environment:

```
import matplotlib.pyplot as plt
```
{: .language-python}

# Sample data
x = [1, 2, 3, 4, 5]
y = [2, 3, 5, 7, 11]

# Create a basic scatter plot
plt.scatter(x, y)
plt.xlabel('X-axis Label')
plt.ylabel('Y-axis Label')
plt.title('Simple Scatter Plot')
plt.show()
The example above demonstrates a basic scatter plot using Matplotlib in Python. Here's a breakdown of the key components:

plt.scatter(x, y): This function creates a scatter plot using the given x and y coordinates.
plt.xlabel('X-axis Label') and plt.ylabel('Y-axis Label'): These functions set the labels for the x-axis and y-axis, respectively.
plt.title('Simple Scatter Plot'): This function sets the title of the plot.
plt.show(): This function displays the plot.
Matplotlib offers a wide range of customization options for creating various types of plots, including line plots, bar plots, histograms, and more. For more advanced plotting techniques and customization options, refer to the official Matplotlib documentation: Matplotlib Documentation.


