
title: "Plotting in Python with Matplotlib"
teaching: 10
exercises: 5
questions:

"How do I create plots?"
"How do I use data sets to populate my plot?"
objectives:
"Understand how plots are formed syntactically using Matplotlib."
"Can create plots from data sets."
keypoints:

"Plotting is a useful tool for understanding our data; it is not just for result visualization."
Plotting our data is one of the best ways to intuitively explore it and understand the various relationships between variables. In Python, there are several libraries for creating plots. We'll be using Matplotlib, a versatile plotting library that provides a similar functionality to ggplot2 in R.

Data sets: These are the data that you provide.
Mapping aesthetics: This is how you connect the data to the graphics. It tells Matplotlib how to use your data to influence how the graph looks (e.g., changing what is plotted on the X or Y axis).
Layers: These are the actual graphical output from Matplotlib. Layers determine what kinds of plot are shown (scatter plot, histogram, etc.), the coordinate system used, and other important aspects of the plot.
Let’s use the iris data set to generate an example using Matplotlib. In your script panel make sure you have:

python
Copy code
import matplotlib.pyplot as plt
python
Copy code
plt.scatter(df_iris['PetalLengthCm'], df_iris['PetalWidthCm'])
plt.xlabel('Petal Length (cm)')
plt.ylabel('Petal Width (cm)')
plt.title('Scatter Plot of Petal Length vs. Petal Width')
plt.show()
Scatterplot in Spyder
Figure 1: Output plot that we have generated using Matplotlib

There is a fair amount to unpack here, so we will take it section by section:

plt.scatter(df_iris['PetalLengthCm'], df_iris['PetalWidthCm']): This line creates a scatter plot using the Petal Length and Petal Width columns from the iris dataset.
plt.xlabel('Petal Length (cm)') and plt.ylabel('Petal Width (cm)'): These lines label the x-axis and y-axis respectively.
plt.title('Scatter Plot of Petal Length vs. Petal Width'): This line sets the title of the plot.
Matplotlib offers a wide range of plot types. If you need a specific kind of plot, a good place to start is the official Matplotlib documentation or various online tutorials and resources.


