---
description: Numerical Computations
---

# NumPy

Use cases: Perform numerical calculations on large datasets like sales trends. This is used for efficiently handling numerical data for forecasting and product insights.&#x20;

Breakdown of the below code is as follows:

* np .array(\[...]) in which np calls the library and .array(\[...]) converts a python list into a NumPy array like \[1000, 1200, 900, 1500] is a list of revenue values and the revenue stores the array in the variable.&#x20;
* A NumPy array is a special type if list that: Stores numbers more efficiently than a regular Python list and allows for fast mathematical operations.&#x20;
* .mean() calculates the average of all numbers in the revenue array&#x20;

```
import numpy as np

revenue = np.array([1000, 1200, 900, 1500])
avg_revenue = np.mean(revenue)  # Calculate average revenue
print(avg_revenue)
```
