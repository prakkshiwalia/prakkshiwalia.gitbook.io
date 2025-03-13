---
description: Data Visualization
---

# Matplotlib

Use case: Create charts for user engagement trends and A/B test results. PMs use this to turn raw data into visual insights for presentations.&#x20;

* Matplotlib is a large library for creating different types of plots. .pyplot is a specific module inside matplotlib that provides a simple interface to create plots quickly. Think of it as matplotlib is like a toolbox for creating visualizations, and .pyplot is like a small set of tools inside that toolbox making it easier to create basic plots.&#x20;
* Plotting in matplotlib.pyplot refers to the process of visually representing data in different types of graphs, such as line charts, bar charts, scatter plots and more.&#x20;
* Pandas and NumPy are single-purpose libraries which are used for  data processing, whereas matplotlib is a big library with many submodules and since we don't need the whole matplotlib package every time, we import only .pyplot
* Different pyplot plotting functions and what it does are given below:



| `plt.plot(x, y)`     | Creates a **line graph**.      |
| -------------------- | ------------------------------ |
| `plt.bar(x, y)`      | Creates a **bar chart**.       |
| `plt.scatter(x, y)`  | Creates a **scatter plot**.    |
| `plt.title("Title")` | Adds a **title** to the graph. |
| `plt.show()`         | **Displays** the graph.        |

* In the below example, it will give an error because plotting function inside the pyplot module and not the main matplotlib package.&#x20;

```
import matplotlib
matplotlib.plot([1, 2, 3, 4])  # This will NOT work!
```

#### Breakdown of the below code is as follows:

* import matplotlib.pyplot imports the pyplot module from the matplotlib.&#x20;
* plt.plot(...) creates a line chart in which months is used as the values for x-axis and sales as the y-axis values as python automatically assumes first argument as to be the x-axis and second to be the y-axis.&#x20;

```
import matplotlib.pyplot as plt

months = ["Jan", "Feb", "Mar", "Apr"]
sales = [5000, 7000, 8000, 6500]

plt.plot(months, sales)
plt.title("Monthly Sales Trend")
plt.show()
```
