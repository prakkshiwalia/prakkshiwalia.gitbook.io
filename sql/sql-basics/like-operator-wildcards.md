# LIKE Operator, Wildcards

The LIKE operator is used in a WHERE clause to search for a specified pattern in a column. LIKE is used for pattern matching.&#x20;

A wildcard character is used to substitute one or more characters in a string.

It can be used to find email addresses with a specific domain like '%@xyz.com' . 4 kinds of wildcards often used with the LIKE operator:

1. % sign represents any number of characters, even zero characters

```
SELECT *
FROM employees
WHERE name LIKE 'a%' OR name LIKE 'c%' OR name LIKE '%o%';
```

* % at the end of a pattern matches string starting with a pattern/ character
* % at the beginning of a pattern/ character matches strings ending with a pattern
* % in the middle of the pattern/ characters matches the strings containing that pattern
* Only % matches everything&#x20;

2. \_ sign represents one, single character

<pre><code><strong>SELECT *
</strong>FROM employees
WHERE name LIKE 'C_ar___';
</code></pre>

Note: When to use one over the other in case of % and \_ :

✔ **Use `_`** when you want to match **only one** character.\
✔ **Use `%`** when you want to match **multiple characters** (zero or more).\
✔ `_` is more specific, while `%` is broader and more flexible.

Below query is searching for employee names where the second letter is "r", but the first letter can be anything, and there can be any number of characters after "r".

```
SELECT * 
FROM employees
WHERE name LIKE '_r%';
```

3. The \[] Wildcard  returns if any of the characters inside the square brackets is a match. Like in the example below, the query would show results of all the employees for whom the names are starting  with either e, f, g

```
SELECT *
FROM employees
WHERE name LIKE '[efg]%;
```

4. The - in \[] allows for a range of characters to be put inside the square characters

```
SELECT *
FROM employees
WHERE name LIKE '[e-j]%;
```
