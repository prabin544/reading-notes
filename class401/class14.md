## Matplotlib Tutorial
Matplotlib is a low level graph plotting library in python that serves as a visualization utility.  
  
Matplotlib was created by John D. Hunter. 

Matplotlib is open source and we can use it freely.  

Matplotlib is mostly written in python, a few segments are written in C, Objective-C and Javascript for Platform compatibility. 

Most of the Matplotlib utilities lies under the pyplot submodule, and are usually imported under the plt alias:
```
import matplotlib.pyplot as plt
```
Example
Draw a line in a diagram from position (0,0) to position (6,250):
```
import matplotlib.pyplot as plt
import numpy as np

xpoints = np.array([0, 6])
ypoints = np.array([0, 250])

plt.plot(xpoints, ypoints)
plt.show()
```
### Plotting x and y points

The plot() function is used to draw points (markers) in a diagram.

By default, the plot() function draws a line from point to point.

The function takes parameters for specifying points in the diagram.

Parameter 1 is an array containing the points on the x-axis.

Parameter 2 is an array containing the points on the y-axis.

If we need to plot a line from (1, 3) to (8, 10), we have to pass two arrays [1, 8] and [3, 10] to the plot function.
```
import matplotlib.pyplot as plt
import numpy as np

xpoints = np.array([1, 8])
ypoints = np.array([3, 10])

plt.plot(xpoints, ypoints)
plt.show()
```
### Markers
You can use the keyword argument marker to emphasize each point with a specified marker:

Mark each point with a circle:
```
import matplotlib.pyplot as plt
import numpy as np

ypoints = np.array([3, 8, 1, 10])

plt.plot(ypoints, marker = 'o')
plt.show()
```
### Create Labels for a Plot
With Pyplot, you can use the xlabel() and ylabel() functions to set a label for the x- and y-axis.

Add labels to the x- and y-axis:
```
import numpy as np
import matplotlib.pyplot as plt

x = np.array([80, 85, 90, 95, 100, 105, 110, 115, 120, 125])
y = np.array([240, 250, 260, 270, 280, 290, 300, 310, 320, 330])

plt.plot(x, y)

plt.xlabel("Average Pulse")
plt.ylabel("Calorie Burnage")

plt.show()
```
### Creating Bars
With Pyplot, you can use the bar() function to draw bar graphs:

Draw 4 bars:
```
import matplotlib.pyplot as plt
import numpy as np

x = np.array(["A", "B", "C", "D"])
y = np.array([3, 8, 1, 10])

plt.bar(x,y)
plt.show()
```
