# HAVING Clause

The `HAVING` clause was added to SQL because the `WHERE` keyword cannot be used after aggregate functions to group the result-set.&#x20;

```
SELECT column_name(s)
FROM table_name
WHERE condition
GROUP BY column_name(s)
HAVING condition
ORDER BY column_name(s);
```

Difference between ORDER BY, GROUP BY, and HAVING CLAUSE\


<table><thead><tr><th>Clause</th><th>Purpose</th><th width="66">Aggregate Functions Allowed?</th><th>Execution Order</th><th>Example Use Case</th></tr></thead><tbody><tr><td><code>WHERE</code></td><td>Filters individual rows before aggregation</td><td>❌ No</td><td>Before <code>GROUP BY</code></td><td>Find employees with salary > 50,000</td></tr><tr><td><code>GROUP BY</code></td><td>Groups rows and applies aggregate functions</td><td>✅ Yes</td><td>After <code>WHERE</code>, before <code>HAVING</code></td><td>Find the highest salary per department</td></tr><tr><td><code>HAVING</code></td><td>Filters aggregated results after <code>GROUP BY</code></td><td>✅ Yes</td><td>After <code>GROUP BY</code></td><td>Find departments where max salary > 80,000</td></tr></tbody></table>
