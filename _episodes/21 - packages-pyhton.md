title: "Packages in Python"
teaching: 5
exercises: 0
questions:

"How do I install packages?"
"How do I get help with packages?"
objectives:
"Can install and load packages."
"Understands how to find help with packages."
keypoints:
"There are many packages with a wide range of features; becoming adept at utilizing packages is key to getting the most out of Python."
Packages extend the functionality of base Python by providing additional functions, datasets, and tools for specific tasks or domains. It is important to be aware that different versions of Python and package versions may be required to use multiple packages simultaneously (version compatibility). It is recommended to keep packages up to date wherever possible, as new versions normally include bug fixes, performance improvements, and new features. We should have already installed all the packages that we need for this course based on the pre-worksheet. However, as a reminder:

python
Copy code
!pip install package_name
Installation only needs to be done once, no matter how many projects you start. To use the package in Spyder, you need to ensure that you import it at the beginning of your script:

python
Copy code
import package_name
Note:
This import statement will need to be added to the beginning of every script that needs this package.

Help with packages
Many packages come with documentation and tutorials. You can usually find help by referring to the official documentation or using Python's built-in help function. For example:

python
Copy code
help(package_name)
or

python
Copy code
package_name?