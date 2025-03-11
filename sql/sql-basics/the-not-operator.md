# The NOT Operator

The `NOT` operator is used in combination with other operators to give the opposite result, also called the negative result.

```
SELECT column1, column2, ...
FROM table_name
WHERE NOT condition;
```

1. The NOT LIKE&#x20;

```
SELECT * FROM Customers
WHERE CustomerName NOT LIKE 'A%';
```

2. NOT BETWEEN

```
SELECT * FROM Customers
WHERE CustomerID NOT BETWEEN 10 AND 60;
```

3. NOT IN&#x20;

```
SELECT * FROM Customers
WHERE City NOT IN ('Paris', 'London');
```

4. NOT Greater Than&#x20;

```
SELECT * FROM Customers
WHERE NOT CustomerID > 50;
```

5. NOT Less Than&#x20;

```
SELECT * FROM Customers
WHERE NOT CustomerId < 50;
```
