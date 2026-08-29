# 📊 Power BI Notes & Cheat Sheet

## 📌 Overview
This repository contains a **comprehensive set of Power BI notes** ranging from beginner concepts to advanced techniques.  
It is designed for learners, professionals, and interview preparation.

---

## 🗂️ Contents
- Introduction to Power BI
- Data Sources & Power Query
- Data Modeling
- DAX (Data Analysis Expressions)
- Visualizations
- Publishing & Sharing
- Advanced Features
- Best Practices

---

## 🟢 1. Introduction
- **Power BI** is Microsoft’s business intelligence tool for data visualization and reporting.
- Components:
  - **Power BI Desktop** – Create reports locally
  - **Power BI Service** – Publish & share online
  - **Power BI Mobile** – View reports on mobile

---

## 🔗 2. Data Sources & Power Query
- Connect to: SQL Server, Excel, CSV, JSON, Web APIs
- **Power Query**: Used for data cleaning and transformation
  - Remove duplicates
  - Split columns
  - Merge queries
  - Change data types

---

## 🗄️ 3. Data Modeling
- Relationships: One-to-Many, Many-to-Many
- **Star Schema** (preferred) vs **Snowflake Schema**
- Example:
  - **Fact Table**: Sales (Revenue, Quantity)
  - **Dimension Table**: Customers, Products, Dates

---

## 🧮 4. DAX (Data Analysis Expressions)
- **Measures**: Calculations evaluated at query time
- **Calculated Columns**: Stored in the model
- Common Functions:
  - `SUM(Sales[Revenue])`
  - `CALCULATE(SUM(Sales[Revenue]), FILTER(Products, Products[Category]="Electronics"))`
  - `IF([Revenue]>100000,"High","Low")`
- Advanced DAX:
  - Time Intelligence: `TOTALYTD()`, `SAMEPERIODLASTYEAR()`
  - LOD-style calculations: `ALL()`, `ALLEXCEPT()`

---

## 📊 5. Visualizations
- Charts: Bar, Line, Pie, Map, TreeMap
- **Slicers & Filters**: Interactive filtering
- **Drill-through**: Navigate to detailed pages
- **Bookmarks**: Save report states
- **KPI Cards**: Show performance indicators

---

## 🌐 6. Publishing & Sharing
- Publish reports to **Power BI Service**
- Create **Dashboards** by pinning visuals
- Share via **Workspaces** and **Apps**
- Apply **Row-Level Security (RLS)** for restricted access

---

## 🚀 7. Advanced Features
- **DAX Studio**: Performance tuning
- **Composite Models**: Combine DirectQuery & Import
- **Paginated Reports**: Pixel-perfect reporting
- **Power BI Embedded**: Integrate into applications
- **AI Visuals**: Key Influencers, Decomposition Tree

---

## 🏆 8. Best Practices
- Use **Measures** instead of calculated columns
- Optimize data models (remove unused columns)
- Keep visuals simple and avoid clutter
- Apply **RLS** for secure access
- Document KPIs and calculations

---

## 📈 Usage
- Use this README as a **quick reference guide** while working in Power BI.
- Ideal for **interview preparation** and **project documentation**.
- Extend with your own dashboards and case studies.

---

## 🤝 Contribution
Contributions are welcome! Fork the repo, add new notes, or enhance with advanced Power BI techniques (Power Query, DAX, AI visuals).
