# 📅 75-Day T-SQL Plan with AdventureWorks2022 Practice Questions

## Week 1 (Days 1–7): SQL Foundations
- **Concepts:** `SELECT`, `WHERE`, `ORDER BY`, `DISTINCT`, `TOP`, `INSERT/UPDATE/DELETE`, operators.

### Practice:
1. Select first/last names of all employees.
2. Find employees hired in 2020.
3. Get distinct job titles.
4. List top 10 most expensive products.
5. Show products with `StandardCost` between 100 and 500.
6. Find products with `Color` IN (‘Red’, ‘Black’, ‘Silver’).
7. Show products where `SellEndDate` IS NULL.
8. Insert a new product into `Production.Product` (dummy values).
9. Update a product’s `ListPrice` by 10%.
10. Delete products with `SafetyStockLevel` < 5.

---

## Week 2 (Days 8–14): Joins & Relationships
- **Concepts:** `INNER`, `LEFT`, `RIGHT`, `FULL`, `CROSS`, `SELF JOIN`, `UNION`, `INTERSECT`, `EXCEPT`.

### Practice:
11. List employees with their department names.
12. List employees and their current manager (self-join).
13. Show customers and their orders (`JOIN Sales.Customer + Sales.SalesOrderHeader`).
14. Show customers with no orders (`LEFT JOIN + IS NULL`).
15. Show vendors and products they supply.
16. List products with category and subcategory.
17. Show employees in departments "Engineering" OR "Production".
18. Combine two queries with `UNION` (all red products + all black products).
19. Find customers that exist in both `Sales.Customer` and `Person.Person` (`INTERSECT`).
20. Find customers that exist in `Sales.Customer` but not in `Sales.Person` (`EXCEPT`).

---

## Week 3 (Days 15–21): Aggregation & Grouping
- **Concepts:** `GROUP BY`, `HAVING`, `ROLLUP`, `CUBE`.

### Practice:
21. Count employees per department.
22. Find avg salary per department.
23. Find departments with more than 10 employees.
24. Count products per subcategory.
25. Show max/min list price per category.
26. Total sales per year (`Sales.SalesOrderHeader`).
27. Sales per year/month using `ROLLUP`.
28. Sales per territory/year using `CUBE`.
29. Count customers per territory.
30. Avg days to ship (difference between `OrderDate` and `ShipDate`).

---

## Week 4 (Days 22–28): Subqueries & Constraints
- **Concepts:** subqueries, `IN`, `EXISTS`, correlated queries, constraints.

### Practice:
31. Find employees with salary > company average.
32. Find products with list price above category average.
33. Find employees in departments whose name starts with “E”.
34. Find customers who placed no orders (`NOT EXISTS`).
35. Find employees earning more than their manager.
36. Check if any products have `ReorderPoint` > `SafetyStockLevel`.
37. Find customers who ordered product `ProductID=707`.
38. List employees whose hire date is earlier than their manager’s (correlated).
39. Insert a product with default values (`DEFAULT` keyword).
40. Create a `CHECK` constraint to ensure list price > 0.

---

## Week 5 (Days 29–35): CTEs & Window Functions (Part 1)
- **Concepts:** CTEs, recursive CTEs, `OVER()`, partitioning, aggregates.

### Practice:
41. Use a CTE to list employees and their department names.
42. Recursive CTE: display org hierarchy from `HumanResources.Employee`.
43. Show each order’s total sales amount using `SUM() OVER`.
44. Show each employee’s salary vs department avg.
45. Show running total of sales by `OrderDate`.
46. Show % contribution of each order to total sales.
47. Rank territories by total sales using `SUM() OVER`.
48. Find avg line total per product per year.
49. Show cumulative count of customers by signup date.
50. Running balance of sales per territory.

---

## Week 6 (Days 36–42): Window Functions (Part 2)
- **Concepts:** `ROW_NUMBER`, `RANK`, `DENSE_RANK`, `NTILE`, `LAG`, `LEAD`, `FIRST_VALUE`, `LAST_VALUE`, frames.

### Practice:
51. Number employees by hire date (`ROW_NUMBER`).
52. Rank employees by salary per department (`RANK`).
53. Dense rank customers by total sales.
54. Split sales into quartiles by amount (`NTILE(4)`).
55. Show difference between current and previous sales (`LAG`).
56. Show next order date for each customer (`LEAD`).
57. First order date per customer (`FIRST_VALUE`).
58. Last order date per customer (`LAST_VALUE`).
59. Running average sales per month using frame clause.
60. Show sales growth rate from previous year.

---

## Week 7 (Days 43–49): Programmability (Part 1)
- **Concepts:** variables, `CASE`, `IF`, `WHILE`, stored procedures.

### Practice:
61. Declare a variable for average list price and print it.
62. Use `CASE` to label products “Cheap/Moderate/Expensive”.
63. Write `IF` to check if a department exists before inserting.
64. Loop with `WHILE`: insert 10 dummy records.
65. Stored procedure: input department ID → return employees.
66. Stored procedure: input product ID → return order history.
67. Stored procedure: update salary with raise % as parameter.
68. Stored procedure: return top N products by sales.
69. Stored procedure: return employees hired in given date range.
70. Stored procedure: return YOY sales growth.

---

## Week 8 (Days 50–56): Programmability (Part 2)
- **Concepts:** UDFs, Views, Triggers.

### Practice:
71. Scalar function: age of employee from DOB.
72. Inline TVF: products above given price.
73. Multi-statement TVF: employees in given department.
74. View: customer name + order total.
75. Indexed view: product inventory by location.
76. Trigger: log deletes from `SalesOrderDetail`.
77. Trigger: prevent update of `BirthDate`.
78. Trigger: insert audit record on `UPDATE`.
79. Trigger: prevent order total < 0.
80. Trigger: auto-update modified date column.

---

## Week 9 (Days 57–63): Transactions & Performance
- **Concepts:** ACID, isolation, `TRY/CATCH`, indexes, execution plans.

### Practice:
81. Transaction: update salaries, rollback if >200,000.
82. Transaction: transfer stock from one location to another.
83. `TRY/CATCH`: handle insert errors gracefully.
84. Demonstrate dirty read with `READ UNCOMMITTED`.
85. Compare `COUNT(*)` with and without index.
86. Add nonclustered index on `OrderDate`, test performance.
87. Execution plan: scan vs seek on `SalesOrderDetail`.
88. Create covering index for frequently queried columns.
89. Drop/rebuild index and compare query times.
90. Test deadlock by running conflicting transactions.

---

## Week 10 (Days 64–70): Advanced SQL
- **Concepts:** temp tables, table vars, `MERGE`, `OUTPUT`, dynamic SQL.

### Practice:
91. Create temp table with top 10 products.
92. Table variable with employees hired after 2020.
93. Merge staging table into Products.
94. Merge order data from staging into `SalesOrderHeader`.
95. Use `OUTPUT` to capture inserted IDs.
96. `OUTPUT` old vs new salary during update.
97. Dynamic SQL: return row count of given table.
98. Dynamic SQL: select top N from a given table.
99. Dynamic SQL: build filter query based on parameters.
100. Dynamic SQL: drop and recreate a given index.

---

## Week 11 (Days 71–75): Special Topics + Revision
- **Concepts:** Sequences, JSON, XML, row-level security, final projects.

### Practice:
101. Create sequence (start=1000, step=10), insert into test table.
102. Use sequence for `OrderID` generation.
103. Convert products to JSON using `FOR JSON AUTO`.
104. Parse JSON with `OPENJSON`.
105. Extract product description from XML.
106. Use `CROSS APPLY` with XML nodes.
107. Implement row-level security: salesperson only sees their territory.
108. Mask sensitive data (partial SSN, phone).
109. Final project: top 3 customers per year by purchase amount.
110. Final project: stored proc → sales growth YOY by territory.
111. Final project: CTE + window functions → employee salary vs dept avg + rank.
112. Final project: dynamic SQL → flexible reporting query (customer, product, or territory filter).
