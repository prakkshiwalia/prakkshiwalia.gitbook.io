---
description: Data analysis and manipulation
---

# Panda lib

Use case: Analyze user behavior, product metrics and financial data. This is used to help clean data, manipulate and analyze large datasets quickly.&#x20;

Breaking down the below code:

* import pandas as pd - This imports the pandas library which is used for working with tables,  datasets and spreadsheets in python. as pd gives pandas a short name (pd)
* df = pd.read\_csv("user\_data.csv") - .read\_csv() is a pandas function that reads a csv file and ocnvert s it into a data frame. this reads csv file named user\_data.csv. df =.... stores the data from the CSV file to the variable called df(stands for DataFrame) which is like a table (similar to excel spreadsheet) that organizes data in rows and columns.
* print(df.head()) - df.head() is a pandas function that returns the first 5 rows of the dataframe and print outputs on the screen. example print(df.head(10)) to show first 10 rows&#x20;

<pre><code><strong>import pandas as pd  # Load user engagement data
</strong>
df = pd.read_csv("user_data.csv")  # Read the CSV file into a DataFrame

print(df.head())  # View the first few rows of the dataset
</code></pre>

