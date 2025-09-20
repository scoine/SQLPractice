# 📅 T-SQL 75-Day Mastery Plan

## 👉 Assumptions:
- You can dedicate 2–3 hours per day on weekdays + 4–5 hours on weekends.
- You’ll practice daily (not just read/watch).

## Week 1 (Days 1–7): SQL Foundations
- **Database objects:** Database, Schema, Table, View.
- **Data types:** `int`, `varchar`, `datetime`, `money`, etc.
- **SELECT basics:** `SELECT`, `FROM`, `WHERE`, `DISTINCT`, `ORDER BY`, `TOP`.
- **Operators:** `=`, `<>`, `BETWEEN`, `IN`, `LIKE`, `IS NULL`.
- **INSERT, UPDATE, DELETE.**

### Practice:
- Write 20+ queries: filtering, sorting, inserting.
  - E.g., Find all employees hired after 2020, sort by name.

---

## Week 2 (Days 8–14): Joins & Relationships
- **Keys:** PK, FK.
- **JOIN types:** 
  - `INNER JOIN`, `LEFT JOIN`, `RIGHT JOIN`
  - `FULL OUTER JOIN`, `CROSS JOIN`, `SELF JOIN`
- **Set operations:** `UNION`, `INTERSECT`, `EXCEPT`

### Practice:
- Join Employees with Departments.
- List employees with no manager (`LEFT JOIN` + NULL check).
- Write queries using `UNION` vs `UNION ALL`.

---

## Week 3 (Days 15–21): Aggregation & Grouping
- **GROUP BY, HAVING.**
- **Aggregates:** `SUM`, `AVG`, `MIN`, `MAX`, `COUNT`.
- **GROUPING SETS, ROLLUP, CUBE.**

### Practice:
- Department-wise salary totals.
- Top 3 departments by headcount.
- Write queries with `CUBE/ROLLUP` for multi-level summaries.

---

## Week 4 (Days 22–28): Subqueries & Constraints
- **Subqueries:** scalar, table, correlated.
- **Operators:** `IN`, `EXISTS`, `NOT EXISTS`.
- **Constraints:** PK, FK, UNIQUE, CHECK, DEFAULT, Identity.

### Practice:
- Employees earning above dept avg (correlated subquery).
- Check constraint for salary > 1000.
- Default constraint for hire date = `GETDATE()`.

---

## Week 5 (Days 29–35): CTEs & Window Functions (Part 1)
- **CTE basics.**
- **Recursive CTEs** (hierarchies).
- **Window function intro:** `OVER()` clause.
- **Aggregates with window functions:** `SUM() OVER`, `AVG() OVER`.

### Practice:
- Find each employee’s salary vs dept average.
- Use recursive CTE to expand an org hierarchy.

---

## Week 6 (Days 36–42): Window Functions (Part 2)
- **Ranking functions:** `ROW_NUMBER`, `RANK`, `DENSE_RANK`, `NTILE`.
- **Offset functions:** `LAG`, `LEAD`.
- **First/Last value:** `FIRST_VALUE`, `LAST_VALUE`.
- **Window frames:** `ROWS BETWEEN`.

### Practice:
- Top 3 earners per department.
- Salary difference from previous employee (`LAG`).
- Running total with `ROWS BETWEEN`.

---

## Week 7 (Days 43–49): Programmability (Part 1)
- **Variables:** `DECLARE`, `SET`.
- **Control flow:** `IF`, `CASE`, `WHILE`.
- **Stored procedures:** create, execute, parameters.

### Practice:
- Write a stored procedure: input = department, output = avg salary.
- Use `CASE` to classify employees by salary range.

---

## Week 8 (Days 50–56): Programmability (Part 2)
- **User Defined Functions (UDF):** scalar, table-valued.
- **Views:** standard, indexed.
- **Triggers:** `AFTER`, `INSTEAD OF`.

### Practice:
- UDF for age from DOB.
- View showing only active employees.
- Trigger to log all DELETEs.

---

## Week 9 (Days 57–63): Transactions & Performance
- **Transactions:** `BEGIN`, `COMMIT`, `ROLLBACK`.
- **Error handling:** `TRY…CATCH`.
- **Isolation levels:** `READ COMMITTED`, `SERIALIZABLE`, etc.
- **Locks, blocking basics.**
- **Indexes:** clustered, non-clustered, covering.
- **Execution plans intro.**

### Practice:
- Wrap salary update in transaction with rollback.
- Compare query speed with/without index.

---

## Week 10 (Days 64–70): Advanced SQL
- **Temp tables:** `#temp`, table variables (`@table`).
- **MERGE statement:** UPSERT.
- **OUTPUT clause.**
- **Dynamic SQL:** `EXEC`, `sp_executesql`.

### Practice:
- Store intermediate results in temp tables.
- Merge new employees into Employees table.
- Use `OUTPUT` to capture inserted IDs.

---

## Week 11 (Days 71–75): Special Topics + Revision
- **Sequences.**
