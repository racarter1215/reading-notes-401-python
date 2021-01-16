# JupyterLab

## JupyterLab: next-generation web-based user interface for Project Jupyter.

### One can arrange multiple documents and activities side by side in the work area using tabs and splitters

### Code Consoles: provide transient scratchpads for running code interactively, with full support for rich output.

### Kernel-backed documents: enable code in any text file to be run interactively in any Jupyter kernel.

### Notebook cell outputs: can be mirrored into their own tab, side by side with the notebook, enabling simple dashboards with interactive controls backed by a kernel.

### Multiple views: documents with different editors or viewers enable live editing of documents reflected in other viewers. For example, it is easy to have live preview of Markdown, Delimiter-separated Values, or Vega/Vega-Lite documents.

# Numpy

## Numpy: a commonly used Python data analysis package. 
###### speeds up your workflow, and interface with other packages in the Python ecosystem

## Tutorial code:
"fixed acidity";"volatile acidity";"citric acid";"residual sugar";"chlorides";"free sulfur dioxide";"total sulfur dioxide";"density";"pH";"sulphates";"alcohol";"quality"
7.4;0.7;0;1.9;0.076;11;34;0.9978;3.51;0.56;9.4;5
7.8;0.88;0;2.6;0.098;25;67;0.9968;3.2;0.68;9.8;5

### How to get started:
###### Import the csv library.
###### Open the winequality-red.csv file.
###### With the file open, create a new csv.reader object.
###### Pass in the keyword argument delimiter=";" to make sure that the records are split up on the semicolon character instead of the default comma character.
###### Call the list type to get all the rows from the file.
###### Assign the result to wines.

### import csv
with open('winequality-red.csv', 'r') as f:
    wines = list(csv.reader(f, delimiter=';'))
    

