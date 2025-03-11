# ORDER BY Clause

1. The ORDER BY keyword is used to sort the result-set in AESC or DESC order. The result-set will have records presented in ascending order by default. They can also be ordered alphabetically using the same syntax.&#x20;

```
SELECT column1, column2, ...
FROM table_name
ORDER BY column1, column2, ... ASC|DESC;
```

2. The following SQL statement selects all the columns from the table, sorted by column1 and the column2 which means that it orders by column1, but if some rows have the same values in column1, it orders them by column2 values.

Note: In the example below, The records are ordered by Country, but if some rows have the     same Country, it orders them by CustomerName. Furthermore, can be used to reorder them in non-deafault vales like Example 2.&#x20;

```
SELECT * 
FROM table_name 
ORDER BY Column1, Column2;

Example: 
SELECT * 
FROM Customers
ORDER BY Country, CustomerName;

Example 2:
SELECT * 
FROM Customers
ORDER BY Country ASC, CustomerName DESC;
```

