<h1 align="center"> 🗄️ SQL Notes & Cheat Sheet </h1>

## 📌 Overview
This repository contains a **comprehensive set of SQL notes** ranging from beginner queries to advanced concepts.  
It is designed for learners, professionals, and interview preparation.

---

## 🗂️ Contents
- Introduction to SQL
- Basic Queries
- Filtering & Sorting
- Joins
- Aggregations
- Subqueries
- Advanced SQL Concepts
- Window Functions
- Performance Optimization
- Best Practices

---

## 🟢 1. Introduction
- **SQL (Structured Query Language)** is used to manage and query relational databases.
- Common databases: MySQL, PostgreSQL, SQL Server, Oracle.
- Basic operations: `SELECT`, `INSERT`, `UPDATE`, `DELETE`.

---

## 🔤 2. Basic Queries
-- Select all columns
SELECT * FROM Customers;

-- Select specific columns
SELECT CustomerName, City FROM Customers;

-- Insert data
INSERT INTO Customers (CustomerName, City) VALUES ('John Doe', 'London');

-- Update data
UPDATE Customers SET City = 'Paris' WHERE CustomerID = 1;

-- Delete data
DELETE FROM Customers WHERE CustomerID = 1;

---
## 🔎 3. Filtering & Sorting
-- WHERE clause
SELECT * FROM Orders WHERE OrderDate > '2026-01-01';

-- LIKE operator
SELECT * FROM Customers WHERE CustomerName LIKE 'A%';

-- ORDER BY
SELECT * FROM Products ORDER BY Price DESC;

-- BETWEEN
SELECT * FROM Orders WHERE OrderDate BETWEEN '2026-01-01' AND '2026-06-30';

---
## 🔗 4. Joins
-- INNER JOIN
SELECT Customers.CustomerName, Orders.OrderID
FROM Customers
INNER JOIN Orders ON Customers.CustomerID = Orders.CustomerID;

-- LEFT JOIN
SELECT Customers.CustomerName, Orders.OrderID
FROM Customers
LEFT JOIN Orders ON Customers.CustomerID = Orders.CustomerID;

-- RIGHT JOIN
SELECT Customers.CustomerName, Orders.OrderID
FROM Customers
RIGHT JOIN Orders ON Customers.CustomerID = Orders.CustomerID;

-- FULL OUTER JOIN (if supported)
SELECT Customers.CustomerName, Orders.OrderID
FROM Customers
FULL OUTER JOIN Orders ON Customers.CustomerID = Orders.CustomerID;

---
## 📊 5. Aggregations
-- COUNT, SUM, AVG, MIN, MAX
SELECT COUNT(*) FROM Orders;
SELECT SUM(Amount) FROM Payments;
SELECT AVG(Price) FROM Products;
SELECT MIN(Price), MAX(Price) FROM Products;

-- GROUP BY
SELECT CustomerID, COUNT(OrderID) AS TotalOrders
FROM Orders
GROUP BY CustomerID;

-- HAVING
SELECT CustomerID, COUNT(OrderID) AS TotalOrders
FROM Orders
GROUP BY CustomerID
HAVING COUNT(OrderID) > 5;

---

## 📑 6. Subqueries
-- Simple subquery
SELECT CustomerName
FROM Customers
WHERE CustomerID IN (SELECT CustomerID FROM Orders WHERE Amount > 1000);

-- Correlated subquery
SELECT CustomerName
FROM Customers c
WHERE EXISTS (SELECT 1 FROM Orders o WHERE o.CustomerID = c.CustomerID);

---

## 🧮 7. Advanced SQL Concepts
Constraints: PRIMARY KEY, FOREIGN KEY, UNIQUE, CHECK

Indexes: Improve query performance

Views: Virtual tables

Stored Procedures: Encapsulate logic

Triggers: Automate actions on events

---

## 📈 8. Window Functions
-- ROW_NUMBER
SELECT CustomerID, OrderID,
       ROW_NUMBER() OVER (PARTITION BY CustomerID ORDER BY OrderDate) AS RowNum
FROM Orders;

-- RANK & DENSE_RANK
SELECT ProductID, Price,
       RANK() OVER (ORDER BY Price DESC) AS Rank,
       DENSE_RANK() OVER (ORDER BY Price DESC) AS DenseRank
FROM Products;

-- SUM with OVER
SELECT CustomerID, SUM(Amount) OVER (PARTITION BY CustomerID) AS TotalSpent
FROM Payments;

---

## ⚡ 9. Performance Optimization
Use indexes on frequently queried columns

Avoid SELECT * in production queries

Normalize data but denormalize for reporting when needed

Use EXPLAIN to analyze query execution plans

Optimize joins and subqueries

---

## 🏆 10. Best Practices
Always use aliases for readability

Prefer INNER JOIN over subqueries when possible

Use transactions for critical operations

Document schema and queries

Apply security practices (least privilege, parameterized queries)

--- 

## 📥 Usage
Use this README as a quick reference guide while working with SQL.

Ideal for interview preparation and project documentation.

Extend with your own queries and case studies.

---

## 🤝 Contribution
Contributions are welcome! Fork the repo, add new SQL notes, or enhance with advanced techniques (CTEs, recursive queries, optimization tips).
  
