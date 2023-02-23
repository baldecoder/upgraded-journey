# Plotly 

![](https://upload.wikimedia.org/wikipedia/commons/thumb/8/8a/Plotly-logo.png/1200px-Plotly-logo.png)

# Table of contents
**[Plotly]()**  
**[Why to use it?]()**  
**[Is Plotly for Python Free?]()**  
**[Can I use Plotly for Python without signing up to any service?]()**  
**[Can I use Plotly for Python offline, without being connected to the internet?]()**  
**[Does Plotly also make commercial software?]()**
1. **[Installation](#installation)**  
   - [Package Structure](#PackageStructure)
2. [Some Chart with plotly](#Some_Chart_with_plotly)
   1. [Line chart](#subparagraph1)
   2. [Bar chart](#subparagraph1)
   3. [Histogramm](#subparagraph1)
   4. [Scatter Plot and Bubble charts](#subparagraph1)
   5. [Pie Charts](#subparagraph1)
   6. [Box Plots](#subparagraph1)
   7. [Violin plot](#subparagraph1)
   8. [Gantt Charts](#subparagraph1)
   9. [3D Line Plots](#subparagraph1)
   10. [3D Scatter Plot](#subparagraph1)
   11. [3D Surface Plots](#subparagraph1)
3. [Interacting with the Plots](#paragraph2)
   4. [Creating Dropdown Menu in Plotly](#paragraph2)
   5. [Adding Buttons to the Plot](#paragraph2)
   6. [Creating Sliders and Selectors to the Plot](#paragraph2)
4. [More Plots using Plotly](#paragraph2)
5. [More Topics on Plotly](#paragraph2)
6. [More Topics on Python Data scientist libraries](#paragraph2)


#### What is it? 
Python Plotly is a high-level and open-source data visualization package that allows you to create interactive plots with very little code. It supports over 40 unique chart types covering a wide range of statistical, financial, geographic, scientific,...
#### Why to use it?
We use plotly for many different reasons:
-   Plotly has hover tool capabilities that allow us to detect any outliers or anomalies in a large number of data points.
    
-   It is visually attractive and can be accepted by a wide range of audiences.
    
-   It allows us for the endless customization of our graphs that makes our plot more meaningful and understandable for others.
    
-   considerably reduces the size of the code to achieve very advanced things
#### Is Plotly for Python Free?

**Yes.**  Plotly for Python is free and open-source software,  [licensed under the  **MIT license**](https://github.com/plotly/plotly.py/blob/master/LICENSE.txt). It costs nothing to  [install and use](https://plotly.com/python/getting-started). You can view the source, report issues or contribute using  [our Github repository](https://github.com/plotly/plotly.py).

#### Can I use Plotly for Python without signing up to any service?

**Yes.**  You can use Plotly for Python to make, view, and distribute charts and maps without registering for any service, obtaining any token, or creating any account. The one exception is that to view tile maps which use tiles from the Mapbox service (which is optional, as  [you can use other tile servers](https://plotly.com/python/mapbox-layers)), you will need to have a Mapbox token.

#### Can I use Plotly for Python offline, without being connected to the internet?

**Yes.**  You can use Plotly for Python to make, view, and distribute graphics totally offline. The one exception is that to view tile maps which use tiles from a cloud-hosted service, such as Open Street Maps or Mapbox, you will need a connection to that service. You can view tile maps totally offline if you run your own local tile server and  [use its tiles](https://plotly.com/python/mapbox-layers).

#### Does Plotly also make commercial software?

**Yes.**  Plotly has commercial offerings such as  [Dash Enterprise](https://plotly.com/dash)  and  [Chart Studio Enterprise](https://plotly.com/online-chart-maker/).

---
### **Installation** <a name="installation"></a>
**Plotly** does not come built-in with Python. To install it, type the below command in the terminal:

    pip install plotly
 This may take some time as it will install the dependencies as well.
 #### Package Structure of Plotly <a name="PackageStructure"></a>
There are three main modules in Plotly. They are:
-   **plotly.plotly**: _acts as the interface between the local machine and Plotly. It contains functions that require a response from Plotly’s server._
-   **plotly.graph.objects**: _module contains the objects (Figure, layout, data, and the definition of the plots like scatter plot, line chart) that are responsible for creating the plots._

	**Note:** _plotly.express module can create the entire Figure at once. It uses the graph_objects internally and returns the graph_objects.Figure instance._
-   **plotly.tools**: _contains various tools in the forms of the functions that can enhance the Plotly experience._
### Some Chart with plotly <a name="Some_Chart_with_plotly"></a>
With plotly we can create more than 40 charts and every plot can be created using the plotly.express and plotly.graph_objects class. Let’s see some commonly used charts with the help of Plotly.
1.  **Line Chart**

**Line plot** in Plotly is much accessible and illustrious annexation to plotly which manage a variety of types of data and assemble easy-to-style statistic. With **px.line** each data position is represented as a vertex (which location is given by the x and y columns) of a polyline mark in 2D space.

**Example 1:**
```Python
    import plotly.express as px
    # using the iris dataset (it is a dataset that exists by default on plotly)
    df = px.data.iris()
    # plotting the line chart
	fig = px.line(df, x="species", y="petal_width")
	# showing the plot
	fig.show()
```
![](https://github.com/baldecoder/upgraded-journey/blob/master/img/LinePlot.PNG)

**Example 2:**
```Python
import plotly.express as px

df = px.data.iris().head(20)

fig = px.line(df, x="sepal_width",y="sepal_length",color="sepal_length")

fig.show()
```
![](https://github.com/baldecoder/upgraded-journey/blob/master/img/LinePlot2.png)
Refer to the below article to get detailed information about the line charts.
- [Line Plot in plotly](https://www.geeksforgeeks.org/line-chart-using-plotly-in-python/?ref=lbp)
- [Line Plot official documentation ](https://plotly.com/python/line-charts/)
---
2. **Bar Chart**  
A **bar chart** is a pictorial representation of data that presents categorical data with rectangular bars with heights or lengths proportional to the values that they represent. In other words, it is the pictorial representation of dataset. These data sets contain the numerical values of variables that represent the length or height.
**Example:**
```Python
import plotly.express as px

# using the iris dataset
df = px.data.iris()

# plotting the bar chart
fig = px.bar(df, x="sepal_width", y="sepal_length")

# showing the plot
fig.show()
```
![](https://github.com/baldecoder/upgraded-journey/blob/master/img/BarChart.png)
Refer to the below articles to get detailed information about the bar chart.

-   [How to create Stacked bar chart in Python-Plotly?](https://www.geeksforgeeks.org/how-to-create-stacked-bar-chart-in-python-plotly/)
-   [Bar chart Official Doc](https://plotly.com/python/bar-charts/)
---
3. **Histograms**  
A **histogram** contains a rectangular area to display the statistical information which is proportional to the frequency of a variable and its width in successive numerical intervals. A graphical representation that manages a group of data points into different specified ranges. It has a special feature that shows no gaps between the bars and similar to a vertical bar graph.
**Example:**
```Python
import plotly.express as px
# using the iris dataset
df = px.data.iris()

# plotting the histogram
fig = px.histogram(df, x="sepal_length", y="petal_width")

# showing the plot
fig.show()
```
![](https://github.com/baldecoder/upgraded-journey/blob/master/img/Histogram.png)
Refer to the below articles to get detailed information about the histograms.

-   [Histogram using Plotly in Python](https://www.geeksforgeeks.org/histogram-using-plotly-in-python/)
-   [Histograms in Plotly using graph_objects class](https://www.geeksforgeeks.org/histograms-in-plotly-using-graph_objects-class/)
-   [How to create a Cumulative Histogram in Plotly?](https://www.geeksforgeeks.org/how-to-create-a-cumulative-histogram-in-plotly/)
-   [Documentation](https://plotly.com/python/histograms/)
---
4. **Scatter Plot and Bubble charts**  
A  **scatter plot**  is a set of dotted points to represent individual pieces of data in the horizontal and vertical axis. A graph in which the values of two variables are plotted along X-axis and Y-axis, the pattern of the resulting points reveals a correlation between them.  
A **bubble plot**  is a scatter plot with bubbles (color-filled circles). Bubbles have various sizes dependent on another variable in the data. It can be created using the scatter() method of plotly.express.

**Example 1:** Scatter Plot
```Python
import plotly.express as px

# using the iris dataset
df = px.data.iris()

# plotting the scatter chart
fig = px.scatter(df, x="species", y="petal_width")

# showing the plot
fig.show()
```
![](https://github.com/baldecoder/upgraded-journey/blob/master/img/Scatter.png)
**Example 2:** Bubble Plot
```Python
import plotly.express as px

# using the iris dataset
df = px.data.iris()

# plotting the bubble chart
fig = px.scatter(df, x="species", y="petal_width",size="petal_length", color="species")

# showing the plot
fig.show()
```
![](https://github.com/baldecoder/upgraded-journey/blob/master/img/Bubble.png)
Refer to the below articles to get detailed information about the scatter plots and bubble plots.

-   [plotly.express.scatter() function in Python](https://www.geeksforgeeks.org/plotly-express-scatter-function-in-python/)
-   [Documentation](https://plotly.com/python/line-and-scatter/)
-   [Scatter plot using Plotly in Python](https://www.geeksforgeeks.org/scatter-plot-using-plotly-in-python/)
-   [Bubble chart using Plotly in Python](https://www.geeksforgeeks.org/bubble-chart-using-plotly-in-python/)
---
5. **Pie Charts**  
A **pie chart** is a circular statistical graphic, which is divided into slices to illustrate numerical proportions. It depicts a special chart that uses “pie slices”, where each sector shows the relative sizes of data. A circular chart cuts in a form of radii into segments describing relative frequencies or magnitude also known as circle graph.

**Example:**
```Python
import plotly.express as px

# using the tips dataset
df = px.data.tips()

# plotting the pie chart
fig = px.pie(df, values="total_bill", names="day")

# showing the plot
fig.show()
```
![](https://github.com/baldecoder/upgraded-journey/blob/master/img/Pie.png)
Refer to the below articles to get detailed information about the pie charts.

-   [Pie plot using Plotly in Python](https://www.geeksforgeeks.org/pie-plot-using-plotly-in-python/)
-   [Documentation](https://plotly.com/python/pie-charts/)
---
6. **Box Plots**  
A **Box Plot**  is also known as Whisker plot is created to display the summary of the set of data values having properties like minimum, first quartile, median, third quartile and maximum. In the box plot, a box is created from the first quartile to the third quartile, a vertical line is also there which goes through the box at the median. Here x-axis denotes the data to be plotted while the y-axis shows the frequency distribution.

**Example:**
```Python
import plotly.express as px

# using the tips dataset
df = px.data.tips()

# plotting the box chart
fig = px.box(df, x="day", y="total_bill")

# showing the plot
fig.show()
```
![](https://github.com/baldecoder/upgraded-journey/blob/master/img/Box.png)
Refer to the below articles to get detailed information about box plots.

-   [Box Plot using Plotly in Python](https://www.geeksforgeeks.org/box-plot-using-plotly-in-python/)
-   [Documentation](https://plotly.com/python/box-plots/)
-   [How to create Grouped box plot in Plotly?](https://www.geeksforgeeks.org/how-to-create-grouped-box-plot-in-plotly/)
---
7. **Violin plots**  
**Violin Plot**  is a method to visualize the distribution of numerical data of different variables. It is similar to Box Plot but with a rotated plot on each side, giving more information about the density estimate on the y-axis. The density is mirrored and flipped over and the resulting shape is filled in, creating an image resembling a violin. The advantage of a violin plot is that it can show nuances in the distribution that aren’t perceptible in a boxplot. On the other hand, the boxplot more clearly shows the outliers in the data.

**Example:**
```Python
import plotly.express as px

# using the tips dataset
df = px.data.tips()

# plotting the violin chart
fig = px.violin(df, x="day", y="total_bill")

# showing the plot
fig.show()
```
![](https://github.com/baldecoder/upgraded-journey/blob/master/img/Violin.png)
Refer to the below articles to get detailed information about the violin plots.

-   [Violin Plots using Plotly](https://plotly.com/python/violin/)
---
8. **Gantt Charts**  
**Generalized Activity Normalization Time Table (GANTT) chart**  is type of chart in which series of horizontal lines are present that show the amount of work done or production completed in given period of time in relation to amount planned for those projects.

**Example:**
```Python
import plotly.figure_factory as ff

# Data to be plotted
df = [dict(Task="A", Start='2020-01-01', Finish='2009-02-02'),
	  dict(Task="Job B", Start='2020-03-01', Finish='2020-11-11'),
	  dict(Task="Job C", Start='2020-08-06', Finish='2020-09-21')]

# Creating the plot
fig = ff.create_gantt(df)
fig.show()
```
![](https://github.com/baldecoder/upgraded-journey/blob/master/img/Gantt.png)
Refer to the below articles to get detailed information about the Gantt Charts.
-   [Gantt Chart in Plotly](https://www.geeksforgeeks.org/gantt-chart-in-plotly/)
-   [Documentation](https://plotly.com/python/gantt/)
---
9. **3D Line Plots**  
Line plot in plotly is much accessible and illustrious annexation to plotly which manage a variety of types of data and assemble easy-to-style statistic. With  **px.line_3d** each data position is represented as a vertex (which location is given by the x, y and z columns) of a polyline mark in 3D space.

**Example:**
```Python
import plotly.express as px

# data to be plotted
df = px.data.tips()

# plotting the figure
fig = px.line_3d(df, x="sex", y="day",z="time", color="sex")

fig.show()
``` 
![](https://github.com/baldecoder/upgraded-journey/blob/master/img/Line3D.png)
Refer to the below articles to get detailed information about the 3D line charts.

-   [Documentation](https://plotly.com/python/3d-line-plots/)
-   [3D Line Plots using Plotly in Python](https://www.geeksforgeeks.org/3d-line-plots-using-plotly-in-python/)
---
10. **3D Scatter Plot Plotly**  
**3D Scatter Plot**  can plot two-dimensional graphics that can be enhanced by mapping up to three additional variables while using the semantics of hue, size, and style parameters. All the parameter control visual semantic which are used to identify the different subsets. Using redundant semantics can be helpful for making graphics more accessible. It can be created using the scatter_3d function of plotly.express class.
**Example:**
```Python
import plotly.express as px
# Data to be plotted
df = px.data.iris()
# Plotting the figure
fig = px.scatter_3d(df, x = 'sepal_width',y = 'sepal_length',z = 'petal_width',color = 'species')
fig.show()
```
![](https://github.com/baldecoder/upgraded-journey/blob/master/img/Scatter3D.png)
Refer to the below articles to get detailed information about the 3D scatter plot.

-   [3D scatter plot using Plotly in Python](https://www.geeksforgeeks.org/3d-surface-plots-using-plotly-in-python/)
-   [Documentation](https://plotly.com/python/3d-scatter-plots/)
-   [3D Bubble chart using Plotly in Python](https://www.geeksforgeeks.org/3d-bubble-chart-using-plotly-in-python/)
---
11. **3D Surface Plots**  
**Surface plot**  is those plot which has three-dimensions data which is X, Y, and Z. Rather than showing individual data points, the surface plot has a functional relationship between dependent variable Y and have two independent variables X and Z. This plot is used to distinguish between dependent and independent variables.
**Example:**
```Python
import plotly.graph_objects as go
import numpy as np

# Data to be plotted
x = np.outer(np.linspace(-2, 2, 30), np.ones(30))
y = x.copy().T
z = np.cos(x ** 2 + y ** 2)

# plotting the figure
fig = go.Figure(data=[go.Surface(x=x, y=y, z=z)])

fig.show()
```
![](https://github.com/baldecoder/upgraded-journey/blob/master/img/3DSurfacePlot.png)
Refer to the below articles to get detailed information about the 3D Surface plot.
-   [Documentation](https://plotly.com/python/3d-surface-plots/)
---
## Interacting with the Plots  
Plotly provides various tools for interacting with the plots such as adding dropdowns, buttons, sliders, etc. These can be created using the update menu attribute of the plot layout. Let’s see how to do all such things in detail.

### Creating Dropdown Menu in Plotly

A  [**drop-down menu**](https://www.geeksforgeeks.org/how-to-make-dropdown-menus-in-plotly/)  is a part of the menu-button which is displayed on a screen all the time. Every menu button is associated with a Menu widget that can display the choices for that menu button when clicked on it. In plotly, there are 4 possible methods to modify the charts by using update menu method.

-   **restyle:** modify data or data attributes
-   **relayout:**  modify layout attributes
-   **update:**  modify data and layout attributes
-   **animate:**  start or pause an animation

**Example:**
```Python
import plotly.graph_objects as px
import numpy as np


# creating random data through randomint
# function of numpy.random
np.random.seed(42)

# Data to be Plotted
random_x = np.random.randint(1, 101, 100)
random_y = np.random.randint(1, 101, 100)

plot = px.Figure(data=[px.Scatter(x=random_x,y=random_y,mode='markers',)])

# Add dropdown
plot.update_layout(
	updatemenus=[
		dict(
			buttons=list([
				dict(
					args=["type", "scatter"],
					label="Scatter Plot",
					method="restyle"
				),
				dict(
					args=["type", "bar"],
					label="Bar Chart",
					method="restyle"
				)
			]),
			direction="down",
		),
	]
)

plot.show()
```
![](https://github.com/baldecoder/upgraded-journey/blob/master/img/Dropdown.png)

In the above example we have created two graphs for the same data. These plots are accessible using the dropdown menu.

Refer to the below articles to get detailed information about the dropdown menu.
-   [Documentation](https://plotly.com/python/dropdowns/)
---
### Adding Buttons to the Plot

In plotly, [**actions custom Buttons**](https://www.geeksforgeeks.org/how-to-make-custom-buttons-in-plotly/)  are used to quickly make actions directly from a record. Custom Buttons can be added to page layouts in CRM, Marketing, and Custom Apps. There are also 4 possible methods that can be applied in custom buttons:

-   **restyle:**  modify data or data attributes
-   **relayout:**  modify layout attributes
-   **update:**  modify data and layout attributes
-   **animate:**  start or pause an animation

Refer to the below articles to get detailed information about the dropdown menu.
-   [Documentation](https://plotly.com/python/custom-buttons/)

### Creating Sliders and Selectors to the Plot

In plotly, the **range slider** is a custom range-type input control. It allows selecting a value or a range of values between a specified minimum and maximum range. And the range selector is a tool for selecting ranges to display within the chart. It provides buttons to select pre-configured ranges in the chart. It also provides input boxes where the minimum and maximum dates can be manually input.
[**Learn More here**](https://www.geeksforgeeks.org/how-to-make-range-slider-and-selector-in-plotly/)

## More Plots using Plotly

-   [plotly.express.scatter_geo() function in Python](https://www.geeksforgeeks.org/plotly-express-scatter_geo-function-in-python/)
-   [plotly.express.scatter_polar() function in Python](https://www.geeksforgeeks.org/plotly-express-scatter_polar-function-in-python/)
-   [plotly.express.scatter_ternary() function in Python](https://www.geeksforgeeks.org/plotly-express-scatter_ternary-function-in-python/)
-   [plotly.express.line_ternary() function in Python](https://www.geeksforgeeks.org/plotly-express-line_ternary-function-in-python/)
-   [Filled area chart using plotly in Python](https://www.geeksforgeeks.org/filled-area-chart-using-plotly-in-python/)
-   [How to Create Stacked area plot using Plotly in Python?](https://www.geeksforgeeks.org/how-to-create-stacked-area-plot-using-plotly-in-python/)
-   [Sunburst Plot using Plotly in Python](https://www.geeksforgeeks.org/sunburst-plot-using-plotly-in-python/)
-   [Sunburst Plot using graph_objects class in plotly](https://www.geeksforgeeks.org/sunburst-plot-using-graph_objects-class-in-plotly/)
-   [plotly.figure_factory.create_annotated_heatmap() function in Python](https://www.geeksforgeeks.org/plotly-figure_factory-create_annotated_heatmap-function-in-python/)
-   [plotly.figure_factory.create_2d_density() function in Python](https://www.geeksforgeeks.org/plotly-figure_factory-create_2d_density-function-in-python/)
-   [Ternary contours Plot using Plotly in Python](https://www.geeksforgeeks.org/ternary-contours-plot-using-plotly-in-python/)
-   [How to make Log Plots in Plotly – Python?](https://www.geeksforgeeks.org/how-to-make-log-plots-in-plotly-python/)
-   [Polar Charts using Plotly in Python](https://www.geeksforgeeks.org/polar-charts-using-plotly-in-python/)
-   [Carpet Contour Plot using Plotly in Python](https://www.geeksforgeeks.org/carpet-contour-plot-using-plotly-in-python/)
-   [Ternary Plots in Plotly](https://www.geeksforgeeks.org/ternary-plots-in-plotly/)
-   [How to create a Ternary Overlay using Plotly?](https://www.geeksforgeeks.org/how-to-create-a-ternary-overlay-using-plotly/)
-   [Parallel Coordinates Plot using Plotly in Python](https://www.geeksforgeeks.org/parallel-coordinates-plot-using-plotly-in-python/)
-   [Carpet Plots using Plotly in Python](https://www.geeksforgeeks.org/carpet-plots-using-plotly-in-python/)
-   [3D Cone Plots using Plotly in Python](https://www.geeksforgeeks.org/3d-cone-plots-using-plotly-in-python/)
-   [3D Volume Plots using Plotly in Python](https://www.geeksforgeeks.org/3d-volume-plots-using-plotly-in-python/)
-   [3D Streamtube Plots using Plotly in Python](https://www.geeksforgeeks.org/3d-streamtube-plots-using-plotly-in-python/)
-   [3D Mesh Plots using Plotly in Python](https://www.geeksforgeeks.org/3d-mesh-plots-using-plotly-in-python/)
-   [How to create Tables using Plotly in Python?](https://www.geeksforgeeks.org/how-to-create-tables-using-plotly-in-python/)
-   [plotly.figure_factory.create_dendrogram() function in Python](https://www.geeksforgeeks.org/plotly-figure_factory-create_dendrogram-function-in-python/)
-   [Define Node position in Sankey Diagram in plotly](https://www.geeksforgeeks.org/define-node-position-in-sankey-diagram-in-plotly/)
-   [Sankey Diagram using Plotly in Python](https://www.geeksforgeeks.org/sankey-diagram-using-plotly-in-python/)
-   [Quiver Plots using Plotly in Python](https://www.geeksforgeeks.org/quiver-plots-using-plotly-in-python/)
-   [Treemap using Plotly in Python](https://www.geeksforgeeks.org/treemap-using-plotly-in-python/)
-   [Treemap using graph_objects class in plotly](https://www.geeksforgeeks.org/treemap-using-graph_objects-class-in-plotly/)
-   [plotly.figure_factory.create_candlestick() function in Python](https://www.geeksforgeeks.org/plotly-figure_factory-create_candlestick-function-in-python/)
-   [plotly.figure_factory.create_choropleth() function in Python](https://www.geeksforgeeks.org/plotly-figure_factory-create_choropleth-function-in-python/)
-   [plotly.figure_factory.create_bullet() in Python](https://www.geeksforgeeks.org/plotly-figure_factory-create_bullet-in-python/)
-   [Streamline Plots in Plotly using Python](https://www.geeksforgeeks.org/streamline-plots-in-plotly-using-python/)
-   [How to make Wind Rose and Polar Bar Charts in Plotly – Python?](https://www.geeksforgeeks.org/how-to-make-wind-rose-and-polar-bar-charts-in-plotly-python/)

## More Topics on Plotly

-   [Title alignment in Plotly](https://www.geeksforgeeks.org/title-alignment-in-plotly/)
-   [Change marker border color in Plotly – Python](https://www.geeksforgeeks.org/change-marker-border-color-in-plotly-python/)
-   [Plot Live Graphs using Python Dash and Plotly](https://www.geeksforgeeks.org/plot-live-graphs-using-python-dash-and-plotly/)
-   [Animated Data Visualization using Plotly Express](https://www.geeksforgeeks.org/animated-data-visualization-using-plotly-express/)
-   [Introduction to Plotly-online using Python](https://www.geeksforgeeks.org/introduction-to-plotly-online-using-python/)
-   [How to display image using Plotly?](https://www.geeksforgeeks.org/how-to-display-image-using-plotly/)

## More Topics on Python Data scientist libraries
-   [GeoPandas](https://geopandas.org/en/stable/)
-   [Polar](https://www.pola.rs/)
