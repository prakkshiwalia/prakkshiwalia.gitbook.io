# Join Clauses

Imagine you have two toy boxes:\
🟦 **One box has LEGO people** (names & ages).\
🟥 **Another box has their favorite toys** (name & toy).

But you want to know **which person likes which toy**!

A **JOIN** in SQL helps you **combine** these two boxes based on something **common**—like the **person’s name**. So, a `JOIN` clause is used to combine rows from two or more tables, based on a related column between them. A JOIN is also considered an inner join by default.&#x20;

#### **Example**

**Two Tables:**

🔹 **People Table:**

| Name    | Age |
| ------- | --- |
| Alice   | 5   |
| Bob     | 6   |
| Charlie | 4   |

🔹 **Toys Table:**

| Name  | Favorite Toy |
| ----- | ------------ |
| Alice | Teddy Bear   |
| Bob   | Toy Car      |

**Using JOIN to Connect the Two**

```sql
SELECT People.Name, People.Age, Toys.Favorite_Toy
FROM People
JOIN Toys ON People.Name = Toys.Name;
```

**Result:**

| Name  | Age | Favorite Toy |
| ----- | --- | ------------ |
| Alice | 5   | Teddy Bear   |
| Bob   | 6   | Toy Car      |

Now we can **see who loves which toy!**&#x20;

#### **Types of JOINs with the same analogy**

1️⃣ **INNER JOIN** - Only keeps matching names from both boxes\
2️⃣ **LEFT JOIN** - Keeps everyone from **People**, even if they don’t have a toy\
3️⃣ **RIGHT JOIN** - Keeps all toys, even if no person is found\
4️⃣ **FULL JOIN** - Keeps **everything**, even if they don’t match)

