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

### **Table: NumPy Functions**

| **NumPy Function**  | **Purpose in A/B Testing**                  | **Example Use Case**                      |
| ------------------- | ------------------------------------------- | ----------------------------------------- |
| np.mean()           | Calculate the average of a numerical column | Find **average clicks per user**          |
| np.median()         | Get the middle value of sorted data         | Find **median clicks per user**           |
| np.std()            | Calculate standard deviation                | Check **variation in user clicks**        |
| np.var()            | Compute variance                            | Measure **spread of user engagement**     |
| np.percentile()     | Get percentile values (25th, 50th, 75th)    | Understand **user behavior distribution** |
| np.min() / np.max() | Get minimum and maximum values              | Identify **lowest and highest clicks**    |
| np.random.choice()  | Randomly select a value from an array       | Simulate **user interactions**            |

### Syntax references for NumPy functions are as below:

```
np.mean(array)  # Compute mean
np.median(array)  # Compute median
np.std(array)  # Compute standard deviation
np.var(array)  # Compute variance
np.min(array)  # Get minimum value
np.max(array)  # Get maximum value
np.percentile(array, 25)  # Get 25th percentile value
```
