#                                       🗄️ SQL Interview Questions & Answers
### Complete SQL Interview Preparation — Fresher to Experienced

![SQL](https://img.shields.io/badge/SQL-Interview%20Preparation-blue?style=for-the-badge)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Beginner](https://img.shields.io/badge/Level-Fresher-orange?style=for-the-badge)
![Advanced](https://img.shields.io/badge/Level-Experienced-red?style=for-the-badge)

> A complete collection of **SQL interview questions and answers** for Freshers, Data Analysts, Business Analysts, BI Analysts, SQL Developers, and experienced professionals.

---

# 📚 Table of Contents

1. [SQL Basics](#-1-sql-basics)
2. [Database Concepts](#-2-database-concepts)
3. [SQL Commands](#-3-sql-commands)
4. [Constraints](#-4-constraints)
5. [Operators](#-5-operators)
6. [Aggregate Functions](#-6-aggregate-functions)
7. [GROUP BY & HAVING](#-7-group-by--having)
8. [WHERE vs HAVING](#-8-where-vs-having)
9. [Joins](#-9-joins)
10. [Subqueries](#-10-subqueries)
11. [CTEs](#-11-ctes)
12. [CASE Statement](#-12-case-statement)
13. [String Functions](#-13-string-functions)
14. [Date Functions](#-14-date-functions)
15. [NULL Handling](#-15-null-handling)
16. [Window Functions](#-16-window-functions)
17. [ROW_NUMBER, RANK & DENSE_RANK](#-17-row_number-rank--dense_rank)
18. [LEAD & LAG](#-18-lead--lag)
19. [UNION & UNION ALL](#-19-union--union-all)
20. [Views](#-20-views)
21. [Indexes](#-21-indexes)
22. [Normalization](#-22-normalization)
23. [Transactions](#-23-transactions)
24. [DELETE vs TRUNCATE vs DROP](#-24-delete-vs-truncate-vs-drop)
25. [Stored Procedures](#-25-stored-procedures)
26. [Functions](#-26-functions)
27. [Keys](#-27-keys)
28. [Data Cleaning](#-28-data-cleaning)
29. [Data Analyst SQL Questions](#-29-data-analyst-sql-questions)
30. [Fresher Interview Questions](#-30-fresher-interview-questions)
31. [Experienced Interview Questions](#-31-experienced-interview-questions)
32. [Scenario-Based Questions](#-32-scenario-based-questions)
33. [Practical SQL Queries](#-33-practical-sql-queries)
34. [Advanced SQL Questions](#-34-advanced-sql-questions)
35. [SQL Performance Optimization](#-35-sql-performance-optimization)
36. [Top 30 Must-Know Questions](#-36-top-30-must-know-sql-questions)
37. [SQL Cheat Sheet](#-37-sql-cheat-sheet)

---

# 🟢 1. SQL Basics

## 1. What is SQL?

SQL stands for:

**Structured Query Language**

It is used to communicate with relational databases.

SQL can be used to:

- Create databases
- Create tables
- Insert data
- Update data
- Delete data
- Retrieve data
- Filter data
- Aggregate data
- Join tables
- Analyze business data

---

## 2. What is a database?

A database is an organized collection of data.

Example:

```text
Sales Database
│
├── Customers
├── Orders
├── Products
├── Employees
└── Payments
```

---

## 3. What is a DBMS?

DBMS stands for:

**Database Management System**

It is software used to manage databases.

Examples:

- MySQL
- PostgreSQL
- Oracle
- SQL Server
- SQLite

---

## 4. What is an RDBMS?

RDBMS stands for:

**Relational Database Management System**

It stores data in tables consisting of rows and columns.

Examples:

```text
MySQL
PostgreSQL
Oracle
SQL Server
```

---

## 5. What is a table?

A table stores data in rows and columns.

Example:

```text
Customers

Customer_ID | Name   | City
------------|--------|---------
101         | Rahul  | Bangalore
102         | Amit   | Mumbai
103         | Priya  | Delhi
```

---

## 6. What is a record?

A record is a single row in a table.

---

## 7. What is a column?

A column represents a specific attribute.

Example:

```text
Customer_ID
Customer_Name
City
Age
```

---

# 🟢 2. Database Concepts

## 8. What is a schema?

A schema defines the structure of database objects such as:

- Tables
- Views
- Procedures
- Functions
- Relationships

---

## 9. What is a primary key?

A primary key uniquely identifies each row.

Example:

```sql
CREATE TABLE Customers (
    Customer_ID INT PRIMARY KEY,
    Customer_Name VARCHAR(100)
);
```

Properties:

- Unique
- Cannot contain NULL
- One primary key constraint per table

---

## 10. What is a foreign key?

A foreign key creates a relationship between two tables.

```sql
CREATE TABLE Orders (
    Order_ID INT PRIMARY KEY,
    Customer_ID INT,
    FOREIGN KEY (Customer_ID)
    REFERENCES Customers(Customer_ID)
);
```

---

## 11. Primary Key vs Foreign Key

| Primary Key | Foreign Key |
|---|---|
| Uniquely identifies row | References another table |
| Cannot be NULL | Can generally contain NULL |
| Unique | Can contain duplicates |
| Identifies entity | Establishes relationship |

---

# 🟢 3. SQL Commands

SQL commands are commonly categorized into:

```text
DDL
DML
DQL
DCL
TCL
```

---

## 12. What is DDL?

DDL = **Data Definition Language**

Commands:

```sql
CREATE
ALTER
DROP
TRUNCATE
```

Example:

```sql
CREATE TABLE Employees (
    Employee_ID INT,
    Employee_Name VARCHAR(100)
);
```

---

## 13. What is DML?

DML = **Data Manipulation Language**

Commands:

```sql
INSERT
UPDATE
DELETE
```

Example:

```sql
INSERT INTO Employees
VALUES (101, 'Rahul');
```

---

## 14. What is DQL?

DQL = **Data Query Language**

Main command:

```sql
SELECT
```

Example:

```sql
SELECT *
FROM Employees;
```

---

## 15. What is DCL?

DCL = **Data Control Language**

Commands:

```sql
GRANT
REVOKE
```

---

## 16. What is TCL?

TCL = **Transaction Control Language**

Commands:

```sql
COMMIT
ROLLBACK
SAVEPOINT
```

---

# 🟢 4. Constraints

## 17. What are constraints?

Constraints enforce rules on table data.

Common constraints:

```text
PRIMARY KEY
FOREIGN KEY
UNIQUE
NOT NULL
CHECK
DEFAULT
```

---

## 18. What is UNIQUE?

Ensures values are unique.

```sql
CREATE TABLE Employees (
    Employee_ID INT UNIQUE
);
```

---

## 19. What is NOT NULL?

Ensures a column cannot contain NULL.

```sql
Employee_Name VARCHAR(100) NOT NULL
```

---

## 20. What is CHECK?

Restricts values based on a condition.

```sql
CHECK (Salary > 0)
```

---

## 21. What is DEFAULT?

Provides a default value.

```sql
Status VARCHAR(20) DEFAULT 'Active'
```

---

# 🟢 5. Operators

Common SQL operators:

### Comparison

```text
=
<>
!=
>
<
>=
<=
```

### Logical

```text
AND
OR
NOT
```

### Special

```text
IN
BETWEEN
LIKE
IS NULL
IS NOT NULL
```

---

## 22. What is BETWEEN?

```sql
SELECT *
FROM Employees
WHERE Salary BETWEEN 30000 AND 70000;
```

---

## 23. What is IN?

```sql
SELECT *
FROM Customers
WHERE City IN ('Bangalore', 'Mumbai', 'Delhi');
```

---

## 24. What is LIKE?

Used for pattern matching.

```sql
SELECT *
FROM Customers
WHERE Customer_Name LIKE 'A%';
```

`A%` means the name starts with A.

---

# 🟢 6. Aggregate Functions

Common aggregate functions:

```text
COUNT()
SUM()
AVG()
MIN()
MAX()
```

---

## 25. COUNT()

```sql
SELECT COUNT(*)
FROM Employees;
```

---

## 26. SUM()

```sql
SELECT SUM(Salary)
FROM Employees;
```

---

## 27. AVG()

```sql
SELECT AVG(Salary)
FROM Employees;
```

---

## 28. MIN() and MAX()

```sql
SELECT
    MIN(Salary) AS Min_Salary,
    MAX(Salary) AS Max_Salary
FROM Employees;
```

---

# 🟢 7. GROUP BY & HAVING

## 29. What is GROUP BY?

GROUP BY groups records based on one or more columns.

Example:

```sql
SELECT
    Department,
    COUNT(*) AS Employee_Count
FROM Employees
GROUP BY Department;
```

---

## 30. What is HAVING?

HAVING filters grouped results.

```sql
SELECT
    Department,
    COUNT(*) AS Employee_Count
FROM Employees
GROUP BY Department
HAVING COUNT(*) > 10;
```

---

# 🟡 8. WHERE vs HAVING

| WHERE | HAVING |
|---|---|
| Filters rows | Filters groups |
| Before GROUP BY | After GROUP BY |
| Cannot normally use aggregate result directly | Commonly used with aggregates |

Example:

```sql
SELECT
    Department,
    SUM(Salary) AS Total_Salary
FROM Employees
WHERE Status = 'Active'
GROUP BY Department
HAVING SUM(Salary) > 500000;
```

---

# 🔵 9. Joins

Joins combine data from multiple tables.

Types:

```text
INNER JOIN
LEFT JOIN
RIGHT JOIN
FULL OUTER JOIN
CROSS JOIN
SELF JOIN
```

---

## 31. What is INNER JOIN?

Returns matching records from both tables.

```sql
SELECT
    c.Customer_ID,
    c.Customer_Name,
    o.Order_ID
FROM Customers c
INNER JOIN Orders o
    ON c.Customer_ID = o.Customer_ID;
```

---

## 32. What is LEFT JOIN?

Returns all records from the left table and matching records from the right table.

```sql
SELECT
    c.Customer_ID,
    c.Customer_Name,
    o.Order_ID
FROM Customers c
LEFT JOIN Orders o
    ON c.Customer_ID = o.Customer_ID;
```

---

## 33. Find customers who have not placed orders.

```sql
SELECT
    c.Customer_ID,
    c.Customer_Name
FROM Customers c
LEFT JOIN Orders o
    ON c.Customer_ID = o.Customer_ID
WHERE o.Customer_ID IS NULL;
```

---

## 34. What is RIGHT JOIN?

Returns all rows from the right table and matching rows from the left table.

---

## 35. What is FULL OUTER JOIN?

Returns matching and non-matching rows from both tables.

---

## 36. What is CROSS JOIN?

Returns every possible combination of rows.

If:

```text
Table A = 5 rows
Table B = 4 rows
```

CROSS JOIN produces:

```text
5 × 4 = 20 rows
```

---

## 37. What is SELF JOIN?

A table joins with itself.

Example: Employee-manager relationship.

```sql
SELECT
    e.Employee_Name,
    m.Employee_Name AS Manager_Name
FROM Employees e
LEFT JOIN Employees m
    ON e.Manager_ID = m.Employee_ID;
```

---

# 🔵 10. Subqueries

## 38. What is a subquery?

A query inside another query.

Example:

```sql
SELECT *
FROM Employees
WHERE Salary > (
    SELECT AVG(Salary)
    FROM Employees
);
```

This returns employees earning above average salary.

---

## 39. What is a correlated subquery?

A correlated subquery depends on the outer query.

Example:

```sql
SELECT e1.Employee_ID,
       e1.Employee_Name,
       e1.Salary
FROM Employees e1
WHERE e1.Salary > (
    SELECT AVG(e2.Salary)
    FROM Employees e2
    WHERE e2.Department = e1.Department
);
```

---

# 🔵 11. CTEs

## 40. What is a CTE?

CTE stands for:

**Common Table Expression**

Syntax:

```sql
WITH SalesData AS (
    SELECT
        Customer_ID,
        SUM(Amount) AS Total_Sales
    FROM Orders
    GROUP BY Customer_ID
)
SELECT *
FROM SalesData;
```

---

## 41. Advantages of CTEs

CTEs improve:

- Readability
- Maintainability
- Complex query structure
- Reusability within a statement

They are also useful for recursive queries in systems that support recursive CTEs.

---

## 42. CTE vs Subquery

| CTE | Subquery |
|---|---|
| More readable for complex queries | Can be concise |
| Defined using WITH | Nested inside query |
| Useful for multi-step logic | Useful for smaller logic |
| Can improve organization | Can become difficult to read when deeply nested |

---

# 🟡 12. CASE Statement

## 43. What is CASE?

CASE implements conditional logic.

```sql
SELECT
    Employee_Name,
    Salary,
    CASE
        WHEN Salary >= 100000 THEN 'High'
        WHEN Salary >= 50000 THEN 'Medium'
        ELSE 'Low'
    END AS Salary_Category
FROM Employees;
```

---

## 44. How do you calculate customer segments?

```sql
SELECT
    Customer_ID,
    Total_Sales,
    CASE
        WHEN Total_Sales >= 100000 THEN 'Premium'
        WHEN Total_Sales >= 50000 THEN 'Gold'
        ELSE 'Standard'
    END AS Customer_Segment
FROM Customer_Sales;
```

---

# 🟢 13. String Functions

Common functions:

```text
UPPER()
LOWER()
LENGTH()
TRIM()
CONCAT()
SUBSTRING()
REPLACE()
LEFT()
RIGHT()
```

Example:

```sql
SELECT UPPER(Customer_Name)
FROM Customers;
```

---

## 45. Find customers whose name starts with A.

```sql
SELECT *
FROM Customers
WHERE Customer_Name LIKE 'A%';
```

---

## 46. Remove extra spaces.

```sql
SELECT TRIM(Customer_Name)
FROM Customers;
```

---

# 🟢 14. Date Functions

Common functions vary by database.

Examples:

```text
CURRENT_DATE
CURRENT_TIMESTAMP
YEAR
MONTH
DAY
DATEADD
DATEDIFF
EXTRACT
```

---

## 47. Find orders from 2026.

MySQL example:

```sql
SELECT *
FROM Orders
WHERE YEAR(Order_Date) = 2026;
```

For large tables, a date range can often be more index-friendly:

```sql
SELECT *
FROM Orders
WHERE Order_Date >= '2026-01-01'
  AND Order_Date < '2027-01-01';
```

---

## 48. Calculate days between two dates.

```sql
SELECT
    DATEDIFF(Delivery_Date, Order_Date) AS Delivery_Days
FROM Orders;
```

> Syntax differs across SQL databases.

---

# 🟢 15. NULL Handling

## 49. What is NULL?

NULL represents a missing or unknown value.

It is not the same as:

```text
0
''
'NULL'
```

---

## 50. How do you check NULL?

Correct:

```sql
WHERE Salary IS NULL
```

Incorrect:

```sql
WHERE Salary = NULL
```

---

## 51. What is COALESCE?

COALESCE returns the first non-NULL value.

```sql
SELECT
    COALESCE(Phone, 'Not Available')
FROM Customers;
```

---

# 🔵 16. Window Functions

Window functions perform calculations across related rows without collapsing them into one row per group.

Common functions:

```text
ROW_NUMBER()
RANK()
DENSE_RANK()
LAG()
LEAD()
SUM() OVER()
AVG() OVER()
COUNT() OVER()
```

---

## 52. What is ROW_NUMBER()?

Assigns a unique sequential number.

```sql
SELECT
    Employee_ID,
    Employee_Name,
    Salary,
    ROW_NUMBER() OVER (
        ORDER BY Salary DESC
    ) AS Row_Num
FROM Employees;
```

---

## 53. What is PARTITION BY?

PARTITION BY divides data into groups for a window calculation.

```sql
SELECT
    Employee_ID,
    Department,
    Salary,
    ROW_NUMBER() OVER (
        PARTITION BY Department
        ORDER BY Salary DESC
    ) AS Rank_No
FROM Employees;
```

---

# 🔵 17. ROW_NUMBER, RANK & DENSE_RANK

## 54. Difference between ROW_NUMBER, RANK and DENSE_RANK

Suppose salaries are:

```text
100000
100000
90000
80000
```

Results:

| Salary | ROW_NUMBER | RANK | DENSE_RANK |
|---:|---:|---:|---:|
| 100000 | 1 | 1 | 1 |
| 100000 | 2 | 1 | 1 |
| 90000 | 3 | 3 | 2 |
| 80000 | 4 | 4 | 3 |

### ROW_NUMBER

Always generates unique sequential numbers.

### RANK

Produces gaps after ties.

### DENSE_RANK

Does not produce gaps after ties.

---

## 55. Find the second-highest salary.

Using DENSE_RANK:

```sql
WITH RankedEmployees AS (
    SELECT
        Employee_ID,
        Employee_Name,
        Salary,
        DENSE_RANK() OVER (
            ORDER BY Salary DESC
        ) AS Salary_Rank
    FROM Employees
)
SELECT *
FROM RankedEmployees
WHERE Salary_Rank = 2;
```

---

## 56. Find the highest-paid employee in each department.

```sql
WITH RankedEmployees AS (
    SELECT
        Employee_ID,
        Employee_Name,
        Department,
        Salary,
        ROW_NUMBER() OVER (
            PARTITION BY Department
            ORDER BY Salary DESC
        ) AS rn
    FROM Employees
)
SELECT *
FROM RankedEmployees
WHERE rn = 1;
```

---

# 🔵 18. LEAD & LAG

## 57. What is LAG?

LAG retrieves a value from a previous row.

```sql
SELECT
    Month,
    Sales,
    LAG(Sales) OVER (
        ORDER BY Month
    ) AS Previous_Month_Sales
FROM Monthly_Sales;
```

---

## 58. What is LEAD?

LEAD retrieves a value from a following row.

```sql
SELECT
    Month,
    Sales,
    LEAD(Sales) OVER (
        ORDER BY Month
    ) AS Next_Month_Sales
FROM Monthly_Sales;
```

---

## 59. Calculate month-over-month growth.

```sql
WITH MonthlySales AS (
    SELECT
        YEAR(Order_Date) AS Sales_Year,
        MONTH(Order_Date) AS Sales_Month,
        SUM(Amount) AS Sales
    FROM Orders
    GROUP BY
        YEAR(Order_Date),
        MONTH(Order_Date)
)
SELECT
    Sales_Year,
    Sales_Month,
    Sales,
    LAG(Sales) OVER (
        ORDER BY Sales_Year, Sales_Month
    ) AS Previous_Sales
FROM MonthlySales;
```

---

# 🟢 19. UNION & UNION ALL

## 60. UNION vs UNION ALL

| UNION | UNION ALL |
|---|---|
| Removes duplicates | Keeps duplicates |
| Usually more processing | Usually faster |
| Combines result sets | Combines result sets |

Example:

```sql
SELECT Customer_ID FROM Customers_2025
UNION
SELECT Customer_ID FROM Customers_2026;
```

---

```sql
SELECT Customer_ID FROM Customers_2025
UNION ALL
SELECT Customer_ID FROM Customers_2026;
```

---

# 🔵 20. Views

## 61. What is a View?

A View is a virtual table based on a query.

```sql
CREATE VIEW Active_Customers AS
SELECT *
FROM Customers
WHERE Status = 'Active';
```

Query:

```sql
SELECT *
FROM Active_Customers;
```

---

## 62. Advantages of Views

- Simplifies complex queries
- Provides abstraction
- Can restrict access to underlying data
- Reusable query logic

---

# 🔵 21. Indexes

## 63. What is an index?

An index helps the database locate rows more efficiently.

Example:

```sql
CREATE INDEX idx_customer_id
ON Orders(Customer_ID);
```

---

## 64. Advantages of indexes

- Faster data retrieval
- Helpful for filtering
- Helpful for joins
- Helpful for sorting in suitable cases

---

## 65. Disadvantages of indexes

- Require storage
- Can slow INSERT/UPDATE/DELETE operations
- Need maintenance

---

## 66. Clustered vs Non-Clustered Index

The exact behavior depends on the database engine.

Generally:

**Clustered index**
- Determines the physical/logical organization of table rows in systems that support clustered storage.
- Typically one per table in systems such as SQL Server.

**Non-clustered index**
- Separate index structure pointing to table rows.
- Multiple can generally exist.

---

# 🔵 22. Normalization

## 67. What is normalization?

Normalization organizes data to reduce:

- Redundancy
- Data duplication
- Update anomalies
- Insert anomalies
- Delete anomalies

---

## 68. What is 1NF?

First Normal Form requires atomic values and no repeating groups.

---

## 69. What is 2NF?

2NF requires:

- 1NF
- No partial dependency on part of a composite key

---

## 70. What is 3NF?

3NF requires:

- 2NF
- No transitive dependency for non-key attributes

---

## 71. What is denormalization?

Denormalization intentionally introduces redundancy to improve read performance or simplify analytical queries.

Common in reporting and data warehousing scenarios.

---

# 🔵 23. Transactions

## 72. What is a transaction?

A transaction is a logical unit of work.

Example:

```sql
START TRANSACTION;

UPDATE Accounts
SET Balance = Balance - 1000
WHERE Account_ID = 101;

UPDATE Accounts
SET Balance = Balance + 1000
WHERE Account_ID = 102;

COMMIT;
```

---

## 73. What is ACID?

ACID stands for:

```text
A → Atomicity
C → Consistency
I → Isolation
D → Durability
```

---

## 74. What is COMMIT?

Permanently saves a transaction.

```sql
COMMIT;
```

---

## 75. What is ROLLBACK?

Reverts uncommitted transaction changes.

```sql
ROLLBACK;
```

---

# 🔴 24. DELETE vs TRUNCATE vs DROP

| DELETE | TRUNCATE | DROP |
|---|---|---|
| Removes rows | Removes all rows | Removes object |
| Can use WHERE | Typically no WHERE | Removes table structure |
| DML | DDL in many systems | DDL |
| Can be transactional depending on DB | Behavior varies by DB | Behavior varies by DB |
| Table remains | Table remains | Table removed |

### DELETE

```sql
DELETE FROM Employees
WHERE Employee_ID = 101;
```

### TRUNCATE

```sql
TRUNCATE TABLE Employees;
```

### DROP

```sql
DROP TABLE Employees;
```

---

# 🔵 25. Stored Procedures

## 76. What is a Stored Procedure?

A stored procedure is a named collection of SQL statements stored in the database.

Example syntax varies by database.

Conceptually:

```sql
CREATE PROCEDURE Get_Employees()
BEGIN
    SELECT *
    FROM Employees;
END;
```

---

## 77. Advantages of Stored Procedures

- Reusable logic
- Centralized processing
- Can improve maintainability
- Can enforce database-side logic
- Can reduce repeated application-side SQL

---

# 🔵 26. Functions

## 78. What is a SQL function?

A function performs a calculation and returns a value or table, depending on database support.

Examples:

```text
COUNT()
SUM()
AVG()
MAX()
MIN()
```

User-defined functions are also supported by many database systems.

---

# 🟢 27. Keys

## 79. What is a candidate key?

A candidate key is a column or combination of columns that can uniquely identify rows.

---

## 80. What is a super key?

A super key is any set of columns that uniquely identifies a row.

---

## 81. What is a composite key?

A composite key consists of multiple columns.

Example:

```sql
PRIMARY KEY (Order_ID, Product_ID)
```

---

# 🔵 28. Data Cleaning

## 82. Find duplicate customer records.

```sql
SELECT
    Customer_ID,
    COUNT(*) AS Record_Count
FROM Customers
GROUP BY Customer_ID
HAVING COUNT(*) > 1;
```

---

## 83. Find duplicate emails.

```sql
SELECT
    Email,
    COUNT(*) AS Count_Email
FROM Customers
GROUP BY Email
HAVING COUNT(*) > 1;
```

---

## 84. Find NULL values.

```sql
SELECT *
FROM Customers
WHERE Email IS NULL;
```

---

## 85. Replace NULL values.

```sql
SELECT
    COALESCE(Phone, 'Not Available') AS Phone
FROM Customers;
```

---

# 📊 29. Data Analyst SQL Questions

## 86. Find total sales.

```sql
SELECT SUM(Amount) AS Total_Sales
FROM Orders;
```

---

## 87. Find total sales by region.

```sql
SELECT
    Region,
    SUM(Amount) AS Total_Sales
FROM Orders
GROUP BY Region;
```

---

## 88. Find top 5 customers by sales.

```sql
SELECT
    Customer_ID,
    SUM(Amount) AS Total_Sales
FROM Orders
GROUP BY Customer_ID
ORDER BY Total_Sales DESC
LIMIT 5;
```

> `LIMIT` syntax varies by database.

---

## 89. Find monthly sales.

```sql
SELECT
    YEAR(Order_Date) AS Year,
    MONTH(Order_Date) AS Month,
    SUM(Amount) AS Total_Sales
FROM Orders
GROUP BY
    YEAR(Order_Date),
    MONTH(Order_Date)
ORDER BY
    Year,
    Month;
```

---

## 90. Find average order value.

```sql
SELECT
    AVG(Amount) AS Average_Order_Value
FROM Orders;
```

---

## 91. Find customers with more than 5 orders.

```sql
SELECT
    Customer_ID,
    COUNT(*) AS Order_Count
FROM Orders
GROUP BY Customer_ID
HAVING COUNT(*) > 5;
```

---

## 92. Find the top-selling product.

```sql
SELECT
    Product_ID,
    SUM(Quantity) AS Total_Quantity
FROM Order_Details
GROUP BY Product_ID
ORDER BY Total_Quantity DESC
LIMIT 1;
```

---

# 🟢 30. Fresher Interview Questions

### 93. What is SQL?

Structured Query Language used to work with relational databases.

### 94. What is a primary key?

A unique identifier for each row.

### 95. What is a foreign key?

A column that references a key in another table.

### 96. What is a JOIN?

A mechanism for combining data from multiple tables.

### 97. What is GROUP BY?

Used to group rows for aggregate calculations.

### 98. What is HAVING?

Used to filter grouped results.

### 99. What is NULL?

Represents a missing or unknown value.

### 100. What is a subquery?

A query nested inside another query.

### 101. What is a view?

A virtual table based on a query.

### 102. What is an index?

A database structure used to improve query performance.

---

# 🔴 31. Experienced Interview Questions

## 103. How do you optimize a slow SQL query?

I would:

1. Examine the execution plan.
2. Check indexes.
3. Verify join conditions.
4. Reduce unnecessary columns.
5. Filter data early where appropriate.
6. Avoid unnecessary subqueries.
7. Review aggregation logic.
8. Check for functions applied to indexed columns.
9. Check table statistics where applicable.
10. Measure performance before and after changes.

---

## 104. CTE vs Temporary Table?

### CTE

Useful for organizing a single statement.

### Temporary Table

Useful when intermediate results need to be stored and reused across multiple statements within a session/transaction, depending on the database.

---

## 105. WHERE vs HAVING?

```text
WHERE  → Filters rows
HAVING → Filters groups
```

---

## 106. UNION vs UNION ALL?

```text
UNION     → Removes duplicates
UNION ALL → Keeps duplicates
```

---

## 107. RANK vs DENSE_RANK?

```text
RANK       → Gaps after ties
DENSE_RANK → No gaps after ties
```

---

## 108. DELETE vs TRUNCATE?

DELETE can remove selected rows using a condition.

TRUNCATE removes all rows from a table in systems that support it.

---

## 109. What is an execution plan?

An execution plan shows how the database intends to execute a query.

It can reveal:

- Table scans
- Index scans
- Index seeks
- Join strategies
- Sort operations
- Aggregations
- Estimated costs

---

# 🔴 32. Scenario-Based Questions

## 110. Sales dropped 20%. How would you investigate using SQL?

I would break the analysis into:

```text
Total Sales
     ↓
Year-over-Year
     ↓
Month
     ↓
Region
     ↓
Product
     ↓
Customer
     ↓
Order Volume
     ↓
Average Order Value
```

Then compare each dimension against the previous period.

---

## 111. Find customers who never ordered.

```sql
SELECT
    c.Customer_ID,
    c.Customer_Name
FROM Customers c
LEFT JOIN Orders o
    ON c.Customer_ID = o.Customer_ID
WHERE o.Order_ID IS NULL;
```

---

## 112. Find the second-highest salary.

```sql
SELECT MAX(Salary) AS Second_Highest
FROM Employees
WHERE Salary < (
    SELECT MAX(Salary)
    FROM Employees
);
```

Alternative using DENSE_RANK:

```sql
WITH Ranked AS (
    SELECT
        *,
        DENSE_RANK() OVER (
            ORDER BY Salary DESC
        ) AS rnk
    FROM Employees
)
SELECT *
FROM Ranked
WHERE rnk = 2;
```

---

## 113. Find the highest salary by department.

```sql
WITH Ranked AS (
    SELECT
        *,
        DENSE_RANK() OVER (
            PARTITION BY Department
            ORDER BY Salary DESC
        ) AS rnk
    FROM Employees
)
SELECT *
FROM Ranked
WHERE rnk = 1;
```

---

## 114. Find employees earning above their department average.

```sql
SELECT
    e.Employee_ID,
    e.Employee_Name,
    e.Department,
    e.Salary
FROM Employees e
JOIN (
    SELECT
        Department,
        AVG(Salary) AS Avg_Salary
    FROM Employees
    GROUP BY Department
) d
    ON e.Department = d.Department
WHERE e.Salary > d.Avg_Salary;
```

---

## 115. Find the third-highest salary.

```sql
WITH Ranked AS (
    SELECT
        *,
        DENSE_RANK() OVER (
            ORDER BY Salary DESC
        ) AS rnk
    FROM Employees
)
SELECT *
FROM Ranked
WHERE rnk = 3;
```

---

# 🔴 33. Practical SQL Queries

## Query 1: Select all records

```sql
SELECT *
FROM Employees;
```

---

## Query 2: Select specific columns

```sql
SELECT
    Employee_ID,
    Employee_Name,
    Salary
FROM Employees;
```

---

## Query 3: Filter employees

```sql
SELECT *
FROM Employees
WHERE Department = 'IT';
```

---

## Query 4: Sort employees by salary

```sql
SELECT *
FROM Employees
ORDER BY Salary DESC;
```

---

## Query 5: Count employees

```sql
SELECT COUNT(*) AS Employee_Count
FROM Employees;
```

---

## Query 6: Department-wise employee count

```sql
SELECT
    Department,
    COUNT(*) AS Employee_Count
FROM Employees
GROUP BY Department;
```

---

## Query 7: Department-wise average salary

```sql
SELECT
    Department,
    AVG(Salary) AS Average_Salary
FROM Employees
GROUP BY Department;
```

---

## Query 8: Departments with average salary above 50000

```sql
SELECT
    Department,
    AVG(Salary) AS Average_Salary
FROM Employees
GROUP BY Department
HAVING AVG(Salary) > 50000;
```

---

## Query 9: Employees hired after 2025

```sql
SELECT *
FROM Employees
WHERE Hire_Date >= '2026-01-01';
```

---

## Query 10: Top 10 salaries

```sql
SELECT *
FROM Employees
ORDER BY Salary DESC
LIMIT 10;
```

---

# 🔴 34. Advanced SQL Questions

## 116. Find duplicate records but keep one record.

Using ROW_NUMBER:

```sql
WITH Duplicates AS (
    SELECT
        *,
        ROW_NUMBER() OVER (
            PARTITION BY Email
            ORDER BY Employee_ID
        ) AS rn
    FROM Employees
)
SELECT *
FROM Duplicates
WHERE rn > 1;
```

---

## 117. Find consecutive login days.

A common approach is to use `LAG()` and date differences.

Conceptually:

```text
Login Date
    ↓
LAG(Login Date)
    ↓
Calculate Date Difference
    ↓
Identify consecutive records
    ↓
Group streaks
```

---

## 118. Find the first order for every customer.

```sql
WITH RankedOrders AS (
    SELECT
        *,
        ROW_NUMBER() OVER (
            PARTITION BY Customer_ID
            ORDER BY Order_Date
        ) AS rn
    FROM Orders
)
SELECT *
FROM RankedOrders
WHERE rn = 1;
```

---

## 119. Find the latest order for every customer.

```sql
WITH RankedOrders AS (
    SELECT
        *,
        ROW_NUMBER() OVER (
            PARTITION BY Customer_ID
            ORDER BY Order_Date DESC
        ) AS rn
    FROM Orders
)
SELECT *
FROM RankedOrders
WHERE rn = 1;
```

---

## 120. Calculate running total.

```sql
SELECT
    Order_Date,
    Amount,
    SUM(Amount) OVER (
        ORDER BY Order_Date
    ) AS Running_Total
FROM Orders;
```

---

## 121. Calculate cumulative sales by customer.

```sql
SELECT
    Customer_ID,
    Order_Date,
    Amount,
    SUM(Amount) OVER (
        PARTITION BY Customer_ID
        ORDER BY Order_Date
    ) AS Cumulative_Sales
FROM Orders;
```

---

## 122. Find percentage contribution of each product.

```sql
SELECT
    Product_ID,
    SUM(Amount) AS Product_Sales,
    SUM(Amount) * 100.0 /
        SUM(SUM(Amount)) OVER () AS Sales_Percentage
FROM Orders
GROUP BY Product_ID;
```

---

# 🚀 35. SQL Performance Optimization

## 123. How can you improve SQL query performance?

### 1. Select only required columns

Avoid:

```sql
SELECT *
FROM Orders;
```

Prefer:

```sql
SELECT
    Order_ID,
    Customer_ID,
    Amount
FROM Orders;
```

---

### 2. Use appropriate indexes

```sql
CREATE INDEX idx_orders_customer
ON Orders(Customer_ID);
```

---

### 3. Avoid unnecessary functions on indexed columns

Instead of:

```sql
WHERE YEAR(Order_Date) = 2026
```

a range predicate may allow better index usage:

```sql
WHERE Order_Date >= '2026-01-01'
  AND Order_Date < '2027-01-01'
```

---

### 4. Check execution plans

Examples vary by database:

```sql
EXPLAIN
SELECT *
FROM Orders
WHERE Customer_ID = 101;
```

---

### 5. Avoid unnecessary joins

Only join tables required for the analysis.

---

### 6. Filter early where appropriate

Reduce the number of rows processed by later operations.

---

# ⭐ 36. Top 30 Must-Know SQL Questions

1. What is SQL?
2. What is DBMS?
3. What is RDBMS?
4. Primary Key vs Foreign Key?
5. What are constraints?
6. What is NULL?
7. WHERE vs HAVING?
8. GROUP BY?
9. INNER JOIN?
10. LEFT JOIN?
11. RIGHT JOIN?
12. FULL OUTER JOIN?
13. UNION vs UNION ALL?
14. DELETE vs TRUNCATE vs DROP?
15. What is a subquery?
16. What is a correlated subquery?
17. What is a CTE?
18. What is a View?
19. What is an Index?
20. What is normalization?
21. What is denormalization?
22. What are window functions?
23. ROW_NUMBER vs RANK vs DENSE_RANK?
24. LEAD vs LAG?
25. What is CASE?
26. What is COALESCE?
27. What is a transaction?
28. What is ACID?
29. How do you find the second-highest salary?
30. How do you optimize a slow query?

---

# 📌 SQL Cheat Sheet

## Basic Query

```sql
SELECT column1, column2
FROM table_name
WHERE condition
ORDER BY column1;
```

---

## Aggregation

```sql
SELECT
    Department,
    COUNT(*) AS Employee_Count,
    AVG(Salary) AS Average_Salary
FROM Employees
GROUP BY Department;
```

---

## HAVING

```sql
SELECT
    Department,
    AVG(Salary) AS Average_Salary
FROM Employees
GROUP BY Department
HAVING AVG(Salary) > 50000;
```

---

## JOIN

```sql
SELECT
    a.ID,
    a.Name,
    b.Amount
FROM TableA a
JOIN TableB b
    ON a.ID = b.ID;
```

---

## CTE

```sql
WITH Data AS (
    SELECT *
    FROM Orders
)
SELECT *
FROM Data;
```

---

## ROW_NUMBER

```sql
ROW_NUMBER() OVER (
    PARTITION BY Customer_ID
    ORDER BY Order_Date DESC
)
```

---

## RANK

```sql
RANK() OVER (
    ORDER BY Salary DESC
)
```

---

## DENSE_RANK

```sql
DENSE_RANK() OVER (
    ORDER BY Salary DESC
)
```

---

## LAG

```sql
LAG(Sales) OVER (
    ORDER BY Month
)
```

---

## LEAD

```sql
LEAD(Sales) OVER (
    ORDER BY Month
)
```

---

# 🎯 SQL Learning Roadmap

## 🟢 Fresher

```text
SQL Basics
     ↓
SELECT
     ↓
WHERE
     ↓
ORDER BY
     ↓
GROUP BY
     ↓
HAVING
     ↓
Aggregate Functions
     ↓
JOINS
     ↓
Subqueries
     ↓
CASE
```

---

## 🟡 1–3 Years

```text
Advanced JOINs
     ↓
CTEs
     ↓
Window Functions
     ↓
ROW_NUMBER
     ↓
RANK
     ↓
DENSE_RANK
     ↓
LEAD / LAG
     ↓
Views
     ↓
Indexes
     ↓
Data Cleaning
```

---

## 🔴 3–5+ Years

```text
Advanced SQL
     ↓
Complex CTEs
     ↓
Window Functions
     ↓
Performance Tuning
     ↓
Execution Plans
     ↓
Index Optimization
     ↓
Transactions
     ↓
Stored Procedures
     ↓
Data Modeling
     ↓
Business Problem Solving
```

---

# 📊 SQL for Data Analysts

For a Data Analyst interview, prioritize these topics:

```text
⭐⭐⭐⭐⭐ SELECT
⭐⭐⭐⭐⭐ WHERE
⭐⭐⭐⭐⭐ GROUP BY
⭐⭐⭐⭐⭐ HAVING
⭐⭐⭐⭐⭐ JOINS
⭐⭐⭐⭐⭐ CASE
⭐⭐⭐⭐⭐ CTE
⭐⭐⭐⭐⭐ Window Functions
⭐⭐⭐⭐⭐ ROW_NUMBER
⭐⭐⭐⭐⭐ RANK
⭐⭐⭐⭐⭐ DENSE_RANK
⭐⭐⭐⭐⭐ LAG / LEAD
⭐⭐⭐⭐⭐ Aggregate Functions
⭐⭐⭐⭐⭐ Date Functions
⭐⭐⭐⭐⭐ Subqueries
⭐⭐⭐⭐  Data Cleaning
⭐⭐⭐⭐  Query Optimization
⭐⭐⭐⭐  Business Scenarios
```

---

# 💼 Business Scenarios to Practice

### Sales

- Total sales
- Monthly sales
- Year-over-year growth
- Top products
- Top customers
- Regional performance
- Average order value

### Customer

- New customers
- Repeat customers
- Inactive customers
- Customers without orders
- Customer retention
- Customer lifetime value

### Employee

- Highest salary
- Second-highest salary
- Department salary
- Employee count
- Employee-manager hierarchy
- Employees above department average

### Finance

- Revenue
- Expenses
- Profit
- Profit margin
- Monthly growth
- Budget vs actual

### E-commerce

- Orders
- Revenue
- Average order value
- Conversion metrics
- Repeat customers
- Product performance

---

# 🏆 Interview Answer Framework

When answering an SQL interview question, use:

```text
1. Definition
2. Syntax
3. Example
4. Business Use Case
5. Alternative Approach
6. Performance Consideration
```

### Example

**Question: What is a CTE?**

**Answer:**

> A CTE, or Common Table Expression, is a temporary named result set defined using the `WITH` clause. It helps organize complex SQL queries into readable steps.

Example:

```sql
WITH CustomerSales AS (
    SELECT
        Customer_ID,
        SUM(Amount) AS Total_Sales
    FROM Orders
    GROUP BY Customer_ID
)
SELECT *
FROM CustomerSales
WHERE Total_Sales > 100000;
```

---

# 🔥 Final SQL Interview Preparation Checklist

### Fresher

- [ ] SQL basics
- [ ] SELECT
- [ ] WHERE
- [ ] ORDER BY
- [ ] GROUP BY
- [ ] HAVING
- [ ] Aggregate functions
- [ ] Joins
- [ ] Subqueries
- [ ] CASE
- [ ] NULL handling

### Intermediate

- [ ] CTEs
- [ ] Window functions
- [ ] ROW_NUMBER
- [ ] RANK
- [ ] DENSE_RANK
- [ ] LEAD
- [ ] LAG
- [ ] Views
- [ ] Indexes
- [ ] Data cleaning

### Advanced

- [ ] Query optimization
- [ ] Execution plans
- [ ] Index optimization
- [ ] Transactions
- [ ] ACID
- [ ] Stored procedures
- [ ] Advanced joins
- [ ] Complex CTEs
- [ ] Data modeling
- [ ] Business case studies

---

# 🚀 Recommended Data Analyst Skill Stack

```text
             DATA ANALYST
                  │
       ┌──────────┼──────────┐
       │          │          │
      SQL       Excel     Power BI
       │          │          │
       └──────────┼──────────┘
                  │
              Tableau
                  │
               Python
                  │
              Statistics
                  │
            Data Analysis
```

> **SQL + Excel + Power BI + Tableau + Python + Statistics = Strong Data Analyst Profile**

---

## ⭐ Keep Practicing

The best way to prepare for SQL interviews is to solve **real business problems**, not just memorize syntax.

Practice with datasets such as:

- Sales
- Customers
- Orders
- Employees
- Banking
- Finance
- Healthcare
- Retail
- E-commerce

**Happy Learning & Good Luck! 🚀**
