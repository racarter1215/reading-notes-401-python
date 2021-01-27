# Matplotlib

### matplotlib: single most used Python package for 2D-graphics. 

### IPython: an enhanced interactive Python shell that has features including named inputs and outputs, access to shell commands, and improved debugging.

### pyplot: provides an interface to the matplotlib object-oriented plotting library. 
###### Mmodeled closely after Matlab(TM).

### Simple Plot Steps:

#### Step 1:
import numpy as np

X = np.linspace(-np.pi, np.pi, 256, endpoint=True)
C, S = np.cos(X), np.sin(X)

#### Run example:
$ python exercice_1.py

### Changing colors and line widths

#### Example:
...
plt.figure(figsize=(10,6), dpi=80)
plt.plot(X, C, color="blue", linewidth=2.5, linestyle="-")
plt.plot(X, S, color="red",  linewidth=2.5, linestyle="-")
...


