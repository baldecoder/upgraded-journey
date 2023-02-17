# Plotly 


![](https://upload.wikimedia.org/wikipedia/commons/thumb/8/8a/Plotly-logo.png/1200px-Plotly-logo.png)


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
### **Installation**
**Plotly** does not come built-in with Python. To install it, type the below command in the terminal:


    pip install plotly
 This may take some time as it will install the dependencies as well.
 #### Package Structure of Plotly
There are three main modules in Plotly. They are:
-   **plotly.plotly**: _acts as the interface between the local machine and Plotly. It contains functions that require a response from Plotly’s server._
-   **plotly.graph.objects**: _module contains the objects (Figure, layout, data, and the definition of the plots like scatter plot, line chart) that are responsible for creating the plots._


        **Note:** _plotly.express module can create the entire Figure at once. It uses the graph_objects internally and returns the graph_objects.Figure instance._
-   **plotly.tools**: _contains various tools in the forms of the functions that can enhance the Plotly experience._
### Some Chart with plotly
With plotly we can create more than 40 charts and every plot can be created using the plotly.express and plotly.graph_objects class. Let’s see some commonly used charts with the help of Plotly.
1. **Line Chart**
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
**Example 2:**
```Python
import plotly.express as px
df = px.data.iris().head(20)
fig = px.line(df, x="sepal_width",y="sepal_length",
color="sepal_length")
fig.show()
```
Refer to the below article to get detailed information about the line charts.
- [Line Plot in plotly](https://www.geeksforgeeks.org/line-chart-using-plotly-in-python/?ref=lbp)
- [Line Plot official documentation ](https://plotly.com/python/line-charts/)