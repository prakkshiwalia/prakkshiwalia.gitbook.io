# ALIASES

SQL aliases are used to give a table, or a column in a table, a temporary name. Aliases are often used to make column names more readable. It only exists for the duration of that query and is created with the `AS` keyword.

* The table\_name can also be changed using this as shown in the second code of the below example.
* If you want to name aliases in more than one character and with spaces, square bracket is used or double quotes " "to name it in query&#x20;

```
SELECT employee_Id AS ID/ employee_number/ [employee number]
FROM employees;

SELECT employee_id
FROM employees AS workforce 
```

### Concatenate Columns

Concatenating columns in SQL is used to **combine** multiple column values into a single column value. This is useful for formatting output, creating full names from first and last names, merging address components, or generating unique identifiers.

```
Example: SELECT CustomerName, CONCAT(Address,', ',PostalCode,', ',City,', ',Country) AS Address
FROM Customers;
```
