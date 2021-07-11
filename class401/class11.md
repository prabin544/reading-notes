## Data Analysis

### What is Jupyter Lab?

JupyterLab is a next-generation web-based user interface for Project Jupyter. JupyterLab enables you to work with documents and activities such as Jupyter notebooks, text editors, terminals, and custom components in a flexible, integrated, and extensible manner. You can arrange multiple documents and activities side by side in the work area using tabs and splitters. 
- Code Consoles 
- Kernel-backed documents 
- Notebook cell outputs can be mirrored into their own tab
- It is easy to have live preview of Markdown, Delimiter-separated Values, or Vega/Vega-Lite documents.

### Numpy Tutorial
NumPy is a commonly used Python data analysis package. By using NumPy, you can speed up your workflow, and interface with other packages in the Python ecosystem, like scikit-learn, that use NumPy under the hood. NumPy was originally developed in the mid 2000s, and arose from an even older package called Numeric. This longevity means that almost every data analysis or machine learning package for Python leverages NumPy in some way.

Lists Of Lists for CSV Data
```
import csv
with open('winequality-red.csv', 'r') as f:
    wines = list(csv.reader(f, delimiter=';'))
print(wines[:3])
[['fixed acidity', 'volatile acidity', 'citric acid', 'residual sugar', 'chlorides', 'free sulfur dioxide', 'total sulfur dioxide', 'density', 'pH', 'sulphates', 'alcohol', 'quality'], ['7.4', '0.7', '0', '1.9', '0.076', '11', '34', '0.9978', '3.51', '0.56', '9.4', '5'], ['7.8', '0.88', '0', '2.6', '0.098', '25', '67', '0.9968', '3.2', '0.68', '9.8', '5']]
```
Creating A NumPy Array
```
import csv
with open("winequality-red.csv", 'r') as f:
    wines = list(csv.reader(f, delimiter=";"))
import numpy as np
wines = np.array(wines[1:], dtype=np.float)
#If we display wines, we’ll now get a NumPy array:
wines
array([[ 7.4 , 0.7 , 0. , ..., 0.56 , 9.4 , 5. ],
[ 7.8 , 0.88 , 0. , ..., 0.68 , 9.8 , 5. ],
[ 7.8 , 0.76 , 0.04 , ..., 0.65 , 9.8 , 5. ],
...,
[ 6.3 , 0.51 , 0.13 , ..., 0.75 , 11. , 6. ],
[ 5.9 , 0.645, 0.12 , ..., 0.71 , 10.2 , 5. ],
[ 6. , 0.31 , 0.47 , ..., 0.66 , 11. , 6. ]])
```
Using NumPy To Read In Files
```
wines = np.genfromtxt("winequality-red.csv", delimiter=";", skip_header=1)
```
Slicing NumPy Arrays
```
wines[0:3,3]
array([ 1.9, 2.6, 2.3])
```
Assigning Values To NumPy Arrays
```
wines[1,5] = 10
wines[:,10] = 50
```
NumPy Data Types
- float — numeric floating point data.
- int — integer data.
- string — character data.
- object — Python objects.

