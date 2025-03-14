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

### Table of Pandas Functions generally used and Real-Life case scenarios

| **Pandas Function**                                              | **Purpose in This Code**                                     | **Other Real-Life Use Cases**                                                         |
| ---------------------------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------------------------------- |
| pd.read\_csv("file.csv")                                         | Load the A/B testing dataset                                 | Reading sales reports, customer databases, or stock market data.                      |
| df.info()                                                        | Show dataset structure (columns, data types, missing values) | Checking data quality in survey responses or product inventory.                       |
| df.describe()                                                    | Summary statistics for numerical data                        | Analyzing website traffic, marketing campaign performance, or test scores.            |
| df\["group"].value\_counts()                                     | Count users in A/B test groups                               | Counting product categories in e-commerce, tracking survey responses.                 |
| df.groupby("group").agg({"clicks": "mean", "converted": "mean"}) | Calculate average clicks and conversion rates                | Finding average customer spending per region, analyzing user engagement per platform. |
| df.index = df.index + 1                                          | Shift DataFrame index to start from 1                        | Reindexing rows after filtering or merging datasets (e.g., employee records).         |
| df.to\_csv("cleaned\_data.csv", index=False)                     | Save cleaned dataset for further analysis                    | Exporting processed data for reporting, saving filtered customer lists.               |
