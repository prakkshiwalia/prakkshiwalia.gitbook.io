# WHERE Clause

WHERE clause is used to filter records that fulfill a specified condition.&#x20;

Note: WHERE clause is not only used in SELECT but also used in UPDATE and DELETE.&#x20;

1. Text values would require single quotes whereas numeric field should not be enclosed in quotes like WHERE Country = 'Mexico', WHERE CustomerID =1

```
SELECT */ column1, column2
FROM table_name
WHERE condition; 
```

2. You can use operators in the WHERE clause like =, >, <, >=, <=, <> (Not equal), BETWEEN (Between a certain range), LIKE (Search for a pattern), IN (to specify multiple possible values for a column)

```
SELECT * 
FROM table_name
WHERE coilumn1 > 80;
```

3. The WHERE clause can contain one or more AND operators to filter records based on more than one condition and is considered  TRUE when all the conditions are TRUE&#x20;

```
SELECT *
FROM Customers
WHERE condition 1 AND condition 2...;

```

4. The OR operator is used to display records where any of the conditions are TRUE
5. The AND and OR operator can be combined. Parentheses in SQL are used to help SL control the order of operations while evaluating. They make sure certain conditions are grouped and evaluated together.

In Example 1, what SQL interprets is:

* First, it finds **customers from Spain whose names start with 'G'**.
* Then, it **adds ALL customers (from any country) whose names start with 'R'**.

Whereas,

In Example 2, what SQL interprets is:

* First, it finds customers from Spain&#x20;
* Then, it adds all customers (from Spain) whose names start with either G or R

**Key Takeaway**

* **Without parentheses**, `OR` applies to the whole condition, affecting records outside Spain.
* **With parentheses**, filtering applies correctly within Spain.

<pre><code>-- Example 1: Without Parentheses 
<strong>SELECT * 
</strong><strong>FROM Customers
</strong>WHERE Country = 'Spain' 
AND CustomerName LIKE 'G%'
OR CustomerName LIKE 'R%';

-- Example 2: With Parentheses 
SELECT * 
FROM Customers
WHERE Country = 'Spain' 
AND (CustomerName LIKE 'G%' OR CustomerName LIKE 'R%');
</code></pre>

6. When combining AND and OR in SQL , AND takes precedence over OR.
7. NOT can be used with AND and OR operator and change the logic completely.                                                                     &#x20;
