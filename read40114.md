# Readings: Data Visualization Summary :
## Data Visualization
* Data visualization is the discipline of trying to understand data by placing it in a visual context so that patterns, trends and correlations that might not otherwise be detected can be exposed.
* ![image](https://cdn-images-1.medium.com/max/800/1*JxbqIQmD_E3M3I7Tjo0OqA.jpeg)

## Matplotlib :low level, provides lots of freedom
* **Matplotlib** is probably the single most used Python package for 2D-graphics. It provides both a very quick way to visualize data from Python and publication-quality figures in many formats.
* Matplotlib is specifically good for creating basic graphs like line charts, bar charts, histograms and many more. It can be imported by typing: **import matplotlib.pyplot as plt**
* To create a scatter plot in Matplotlib we can use the scatter method. We will also create a figure and an axis using plt.subplots so we can give our plot a title and labels.
* We can give the graph more meaning by coloring in each data-point by its class. This can be done by creating a dictionary which maps from class to color and then scattering each point on its own using a for-loop and passing the respective color.

* **IPython** is an enhanced interactive Python shell that has lots of interesting features including named inputs and outputs, access to shell commands, improved debugging and much more. When we start it with the command line argument **-pylab** (--pylab since IPython version 0.12), it allows interactive **matplotlib** sessions that have Matlab/Mathematica-like functionality.
* **pyplot** provides a convenient interface to the **matplotlib object-oriented plotting library**. It is modeled closely after Matlab(TM). Therefore, the majority of plotting commands in pyplot have Matlab(TM) analogs with similar arguments. Important commands are explained with interactive examples.
* **Matplotlib** comes with a set of default settings that allow customizing all kinds of properties. You can control the defaults of almost every property in matplotlib: figure size and dpi, line width, color and style, axes, axis and grid properties, text and font properties and so on. While matplotlib defaults are rather good in most cases, you may want to modify some properties for specific cases.
## Seaborn : high-level interface, great default styles
* The Python visualization library **Seaborn** is based on matplotlib and provides a high-level interface for drawing attractive statistical graphics.
* The basic steps to creating plots with Seaborn are:
 1. Prepare some data
 2. Control figure aesthetics
 3. Plot with Seaborn
 4. Further customize your plot

