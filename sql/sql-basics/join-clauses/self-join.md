# Self Join

A self join is a regular join, but the table is joined with itself. It is used when a table contains hierarchical or relational data, and we need to compare or relate rows within the same table using the different joins discussed above.&#x20;

Note: Since the same table is used twice, but treated as different versions separately for SQL to interpret. it is necessary to use aliases to avoid further confusion. The results returned are based on what columns are needed based on what is put in the SELECT statement after interpreting of what is self-joined for easy comparison for decision-making.&#x20;

```
SELECT column_name(s)
FROM table1 T1, table1 T2
WHERE condition;
```

**When Do We Use SELF JOIN?**

* Hierarchical Data (e.g., Employee-Manager Relationships)
* Comparing Values Within the Same Table
* Finding Duplicate Records
* Finding Related Items in the Same Category

**Explanation of SELF JOIN**

* We use two copies of the same table:
  * `e1` represents the employees.
  * `e2` represents their managers (who are also employees).
* The JOIN condition matches `e1.manager_id` with `e2.employee_id` to find each employee’s manager.
* `NULL` means the employee has no manager (Like Alice, who is the CEO).

```
SELECT e.name AS employee, m.name AS manager
FROM employees e
LEFT JOIN employees m ON e.manager_id = m.employee_id;
```

How does the above query work in SQL's mind if it was a person?

Step 1: You want to get data from the employees table. Since, you are using this table twice, so you gave it aliases: e (employees as employees),`m` (employees who are also managers). This way in this SELF JOIN, we are using the same table twice, but treating each version differently, where first version says look at its employees and second version says look at their managers. SQL doesn't let us use different versions of the same table without aliases to avoid further confusion.&#x20;

Step 2: You want to match the manager\_id in `e` (employees) with the employee\_id in `m` (managers). So, for each employee in `e`, I’ll look into `m` and try to find the corresponding manager.

Step 3: Based on LEFT JOIN rules, I should keep all employees from `e`, even if they don’t have a manager. If there’s no match in `m`, I’ll just put `NULL` for the manager’s name.

Step 4: You don’t want to see IDs, just the names. I’ll show the employee’s name from `e` and the manager’s name from `m`.

Step 5: When SQL starts matching, the following happens:

For Alice (101) → No manager (`NULL` appears).

For Bob (102) → Manager is Alice (101).

For Charlie (103) → Manager is Alice (101).

For David (104) → Manager is Bob (102).

