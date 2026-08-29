# 📈 Power BI Interview Questions & Answers — Fresher to Experienced

> 🚀 Complete Power BI interview preparation guide for Data Analysts, BI Analysts, Power BI Developers, and experienced professionals.

---

## 📚 Table of Contents

### 🟢 Fresher Level
- [1. Power BI Basics](#-1-power-bi-basics)
- [2. Data Sources](#-2-data-sources)
- [3. Power Query](#-3-power-query)
- [4. Data Modeling](#-4-data-modeling)
- [5. Visualizations](#-5-visualizations)

### 🟡 Intermediate Level
- [6. DAX](#-6-dax)
- [7. Advanced DAX](#-7-advanced-dax)
- [8. Power Query Advanced](#-8-power-query-advanced)
- [9. Data Modeling Advanced](#-9-data-modeling-advanced)
- [10. Power BI Service](#-10-power-bi-service)
- [11. Dashboard Development](#-11-dashboard-development)

### 🔴 Experienced Level
- [12. Performance Optimization](#-12-performance-optimization)
- [13. Row-Level Security](#-13-row-level-security)
- [14. Incremental Refresh](#-14-incremental-refresh)
- [15. Advanced Scenarios](#-15-advanced-scenarios)
- [16. Real Project Questions](#-16-real-project-questions)

### 🎯 Scenario Based
- [17. Scenario-Based Interview Questions](#-17-scenario-based-interview-questions)

---

# 🟢 1. Power BI Basics

## 1. What is Power BI?

**Answer:**

Power BI is Microsoft's Business Intelligence and data visualization platform. It allows users to connect to different data sources, transform data, create data models, build interactive reports and dashboards, and share insights with users.

### Main Power BI components:

- Power BI Desktop
- Power BI Service
- Power BI Mobile
- Power Query
- DAX
- On-premises Data Gateway
- Power BI Report Server

---

## 2. What is Power BI Desktop?

**Answer:**

Power BI Desktop is a Windows application used to:

- Connect to data sources
- Transform data
- Create relationships
- Build data models
- Create DAX calculations
- Design reports
- Publish reports to Power BI Service

---

## 3. What is Power BI Service?

**Answer:**

Power BI Service is the cloud-based platform where users can:

- Publish reports
- Create dashboards
- Share reports
- Create workspaces
- Configure scheduled refresh
- Implement security
- Manage semantic models
- Collaborate with users

---

## 4. What is Power BI Mobile?

**Answer:**

Power BI Mobile allows users to access and interact with Power BI reports and dashboards from mobile devices.

---

## 5. What is a Power BI Report?

**Answer:**

A report is a collection of interactive pages containing visuals such as:

- Charts
- Tables
- Cards
- Maps
- Slicers
- KPIs

A report is generally connected to a semantic model.

---

## 6. What is a Power BI Dashboard?

**Answer:**

A dashboard is a **single-page canvas in Power BI Service** containing tiles pinned from reports or other content.

### Report vs Dashboard

| Report | Dashboard |
|---|---|
| Can have multiple pages | Single page |
| Created primarily in Desktop | Created in Service |
| Many visual types | Tile-based |
| Supports detailed analysis | High-level monitoring |

---

## 7. What is a visual?

**Answer:**

A visual is a graphical representation of data.

Examples:

- Bar chart
- Line chart
- Pie chart
- Matrix
- Table
- Card
- KPI
- Map
- Scatter chart

---

## 8. What is a slicer?

**Answer:**

A slicer is an interactive visual used to filter report data.

### Example:

A Region slicer can allow users to select:

```text
North
South
East
West
```

---

## 9. What is drill-down?

**Answer:**

Drill-down allows users to navigate through different levels of a hierarchy.

Example:

```text
Year
 ↓
Quarter
 ↓
Month
 ↓
Day
```

---

## 10. What is drill-through?

**Answer:**

Drill-through allows users to navigate from a summary page to a detailed page filtered for the selected item.

### Example:

From:

```text
Sales Dashboard
```

User selects:

```text
Customer = John
```

Then navigates to:

```text
Customer Details
```

showing only John's transactions.

---

# 🟢 2. Data Sources

## 11. What data sources can Power BI connect to?

**Answer:**

Power BI supports many sources including:

- SQL Server
- MySQL
- PostgreSQL
- Oracle
- Excel
- CSV
- SharePoint
- Web APIs
- Azure
- Snowflake
- Dataverse
- Salesforce
- Google BigQuery

---

## 12. What is Import Mode?

**Answer:**

Import mode loads data into Power BI's in-memory storage engine.

### Advantages:

- Fast report performance
- Powerful DAX analysis
- Data compression
- Rich modeling capabilities

---

## 13. What is DirectQuery?

**Answer:**

DirectQuery does not import the entire dataset into Power BI. Instead, Power BI sends queries to the underlying data source when users interact with the report.

### Advantages:

- Useful for large datasets
- Near-real-time scenarios
- Data remains in the source

### Disadvantages:

- Depends on source performance
- Some modeling/calculation limitations
- Can be slower than Import

---

## 14. Import vs DirectQuery

| Import | DirectQuery |
|---|---|
| Data loaded into Power BI | Data remains in source |
| Usually faster | Depends on source |
| Strong modeling flexibility | More limitations |
| Requires refresh | Queries source |
| Uses in-memory storage | Uses source database |

---

## 15. What is a Live Connection?

**Answer:**

A live connection connects Power BI to an existing semantic model or Analysis Services model instead of importing the underlying data into the report.

---

## 16. What is a Composite Model?

**Answer:**

A composite model allows a Power BI model to use multiple storage modes, such as Import and DirectQuery.

---

# 🟢 3. Power Query

## 17. What is Power Query?

**Answer:**

Power Query is Power BI's data extraction and transformation technology.

It is mainly used for:

- Cleaning data
- Removing duplicates
- Handling nulls
- Changing data types
- Merging tables
- Appending tables
- Creating calculated columns
- Connecting to data sources

Power Query uses the **M language**.

---

## 18. What is ETL?

**Answer:**

ETL stands for:

```text
Extract
Transform
Load
```

### Extract

Get data from sources.

### Transform

Clean and prepare the data.

### Load

Load the transformed data into the semantic model.

---

## 19. What is Query Folding?

**Answer:**

Query folding means Power Query translates supported transformations into source-system queries so that the source performs the processing.

### Example:

If SQL Server can perform a filter, Power Query may push that filter to SQL Server.

### Benefits:

- Better performance
- Less data transferred
- Reduced Power BI processing

---

## 20. Why is Query Folding important?

**Answer:**

Query folding can significantly improve refresh performance because transformations are pushed to the source whenever supported.

---

## 21. Merge vs Append

### Merge

Merge combines columns from two tables based on matching keys.

It is similar to:

```sql
JOIN
```

### Append

Append combines rows from multiple tables.

It is similar to:

```sql
UNION ALL
```

---

## 22. What is Remove Duplicates?

**Answer:**

It removes duplicate records based on selected columns.

---

## 23. How do you handle null values?

**Answer:**

Depending on business requirements, I can:

- Replace null values
- Remove rows
- Fill values
- Keep nulls
- Use conditional logic

I always verify the business meaning before modifying missing values.

---

## 24. How do you change a data type?

**Answer:**

In Power Query:

```text
Select Column
→ Data Type
→ Select Required Type
```

Common data types:

- Text
- Whole Number
- Decimal Number
- Date
- Date/Time
- Boolean

---

## 25. What are Applied Steps?

**Answer:**

Applied Steps display the sequence of transformations performed in Power Query.

Example:

```text
Source
↓
Promoted Headers
↓
Changed Type
↓
Removed Columns
↓
Filtered Rows
↓
Merged Queries
```

---

## 26. What is a Custom Column?

**Answer:**

A Custom Column is a new column created using an M expression.

Example:

```text
[Sales] - [Cost]
```

---

## 27. What is Conditional Column?

**Answer:**

A conditional column creates values based on business rules.

Example:

```text
If Sales > 100000
Then "High"
Else "Low"
```

---

# 🟢 4. Data Modeling

## 28. What is Data Modeling?

**Answer:**

Data modeling is the process of organizing tables, relationships, columns, and measures so that data can be analyzed efficiently.

---

## 29. What is a Fact Table?

**Answer:**

A fact table contains measurable business events.

Example:

```text
Sales
Orders
Transactions
Invoices
```

Typical columns:

```text
OrderID
CustomerID
ProductID
DateID
Quantity
SalesAmount
Cost
```

---

## 30. What is a Dimension Table?

**Answer:**

Dimension tables contain descriptive information.

Examples:

```text
Customer
Product
Date
Employee
Region
```

---

## 31. What is a Star Schema?

**Answer:**

A star schema contains a central fact table connected to dimension tables.

Example:

```text
             Customer
                 |
                 |
Product ---- Sales ---- Date
                 |
                 |
              Region
```

---

## 32. Why is Star Schema preferred?

**Answer:**

Star schema provides:

- Simpler relationships
- Better performance
- Easier DAX
- Better usability
- Reduced ambiguity

---

## 33. What is Cardinality?

**Answer:**

Cardinality defines how records in two tables relate.

Common types:

- One-to-one
- One-to-many
- Many-to-one
- Many-to-many

---

## 34. What is a One-to-Many relationship?

**Answer:**

One record in the dimension table can relate to many records in the fact table.

Example:

```text
Customer
CustomerID = 101
```

can have:

```text
Order 1
Order 2
Order 3
```

---

## 35. What is Many-to-Many?

**Answer:**

Many-to-many occurs when multiple records on both sides can match each other.

It should be used carefully because it can create ambiguity and unexpected filtering.

---

## 36. What is a Date Table?

**Answer:**

A Date table is a dedicated calendar table containing continuous dates and useful attributes such as:

```text
Date
Year
Quarter
Month
Month Number
Week
Day
```

It is important for time-intelligence calculations.

---

# 🟡 5. Visualizations

## 37. Which chart is best for trends?

**Answer:**

A line chart is generally best for showing trends over time.

---

## 38. Which chart is best for category comparison?

**Answer:**

Bar charts and column charts are commonly used.

---

## 39. When would you use a Pie Chart?

**Answer:**

Pie charts can be used for simple part-to-whole comparisons with a small number of categories. For many categories, bar charts are usually easier to read.

---

## 40. What is Conditional Formatting?

**Answer:**

Conditional formatting changes visual appearance based on values or rules.

Example:

```text
Profit > 0 → Positive indicator
Profit < 0 → Negative indicator
```

---

## 41. What is a KPI?

**Answer:**

A KPI is a Key Performance Indicator used to track business performance against a target.

Example:

```text
Actual Sales = ₹10M
Target Sales = ₹12M
Achievement = 83.3%
```

---

## 42. What is a Tooltip?

**Answer:**

A tooltip displays additional information when the user hovers over a visual.

---

## 43. What is a Bookmark?

**Answer:**

A bookmark captures the current state of a report page, including visibility, filters, and visual states, and can be used for navigation or storytelling.

---

# 🟡 6. DAX

## 44. What is DAX?

**Answer:**

DAX stands for **Data Analysis Expressions**.

It is used to create:

- Measures
- Calculated columns
- Calculated tables

---

## 45. Measure vs Calculated Column

| Measure | Calculated Column |
|---|---|
| Calculated at query time | Calculated during refresh |
| Responds to filter context | Stored in model |
| Usually better for aggregations | Useful for row-level logic |
| Doesn't increase rows | Adds a column to table |

---

## 46. What is CALCULATE?

**Answer:**

`CALCULATE()` evaluates an expression after modifying the filter context.

Example:

```DAX
Total Sales = SUM(Sales[SalesAmount])
```

Sales for 2025:

```DAX
Sales 2025 =
CALCULATE(
    [Total Sales],
    'Date'[Year] = 2025
)
```

---

## 47. What is Filter Context?

**Answer:**

Filter context is the set of filters applied to a DAX calculation.

It can come from:

- Slicers
- Visuals
- Page filters
- Report filters
- Relationships
- DAX expressions

---

## 48. What is Row Context?

**Answer:**

Row context refers to the current row being evaluated, commonly in calculated columns and iterator functions.

---

## 49. What is Context Transition?

**Answer:**

Context transition occurs when `CALCULATE()` converts row context into filter context.

---

## 50. SUM vs SUMX

### SUM

Adds values from a column.

```DAX
Total Sales =
SUM(Sales[SalesAmount])
```

### SUMX

Iterates through a table and evaluates an expression for each row.

```DAX
Total Revenue =
SUMX(
    Sales,
    Sales[Quantity] * Sales[UnitPrice]
)
```

---

## 51. COUNT vs COUNTROWS

### COUNT

Counts nonblank numeric values in a column.

```DAX
COUNT(Sales[OrderID])
```

### COUNTROWS

Counts rows in a table.

```DAX
COUNTROWS(Sales)
```

---

## 52. What is DISTINCTCOUNT?

**Answer:**

It counts unique values.

```DAX
Unique Customers =
DISTINCTCOUNT(Sales[CustomerID])
```

---

## 53. What is DIVIDE?

**Answer:**

`DIVIDE()` safely handles division and can return an alternate result for zero or blank denominators.

```DAX
Profit Margin =
DIVIDE(
    [Profit],
    [Total Sales],
    0
)
```

---

## 54. What is ALL?

**Answer:**

`ALL()` removes filters from specified tables or columns.

Example:

```DAX
Total Sales All Regions =
CALCULATE(
    [Total Sales],
    ALL(Region)
)
```

---

## 55. What is REMOVEFILTERS?

**Answer:**

`REMOVEFILTERS()` explicitly removes filters from specified tables or columns.

```DAX
Total Sales =
CALCULATE(
    [Total Sales],
    REMOVEFILTERS(Region)
)
```

---

## 56. What is FILTER?

**Answer:**

`FILTER()` returns a filtered table based on a condition.

Example:

```DAX
High Value Sales =
CALCULATE(
    [Total Sales],
    FILTER(
        Sales,
        Sales[SalesAmount] > 10000
    )
)
```

---

## 57. What is RELATED?

**Answer:**

`RELATED()` retrieves a value from a related table, commonly in calculated columns.

```DAX
Product Category =
RELATED(Product[Category])
```

---

## 58. What is RELATEDTABLE?

**Answer:**

`RELATEDTABLE()` returns the related rows from another table.

---

# 🟡 7. Advanced DAX

## 59. What is Time Intelligence?

**Answer:**

Time intelligence allows analysis across dates and periods.

Examples:

- YTD
- MTD
- QTD
- Previous Year
- Previous Month
- Year-over-Year Growth

---

## 60. YTD Sales

```DAX
Sales YTD =
TOTALYTD(
    [Total Sales],
    'Date'[Date]
)
```

---

## 61. Previous Year Sales

```DAX
Sales PY =
CALCULATE(
    [Total Sales],
    SAMEPERIODLASTYEAR('Date'[Date])
)
```

---

## 62. YoY Growth

```DAX
YoY Growth % =
DIVIDE(
    [Total Sales] - [Sales PY],
    [Sales PY],
    0
)
```

---

## 63. What is SELECTEDVALUE?

**Answer:**

`SELECTEDVALUE()` returns the selected value when exactly one distinct value is in context.

```DAX
Selected Region =
SELECTEDVALUE(
    Region[Region],
    "All Regions"
)
```

---

## 64. What is HASONEVALUE?

**Answer:**

It checks whether a column has exactly one distinct value in the current filter context.

```DAX
HASONEVALUE(Product[Category])
```

---

## 65. What is ISFILTERED?

**Answer:**

`ISFILTERED()` checks whether a column or table is directly filtered.

---

## 66. What is RANKX?

**Answer:**

`RANKX()` ranks values based on an expression.

Example:

```DAX
Product Rank =
RANKX(
    ALL(Product[ProductName]),
    [Total Sales],
    ,
    DESC
)
```

---

## 67. What is TOPN?

**Answer:**

`TOPN()` returns the top N rows from a table based on an expression.

---

## 68. What is a Variable in DAX?

**Answer:**

Variables store intermediate results.

Example:

```DAX
Profit Margin =
VAR ProfitValue = [Profit]
VAR SalesValue = [Total Sales]
RETURN
DIVIDE(
    ProfitValue,
    SalesValue,
    0
)
```

### Benefits:

- Improves readability
- Avoids repeated calculations
- Can improve maintainability
- Makes debugging easier

---

# 🟡 8. Power Query Advanced

## 69. What is the M Language?

**Answer:**

M is the functional language used by Power Query to perform data extraction and transformation.

---

## 70. Merge vs Append in Power Query

```text
Merge = Add Columns
Append = Add Rows
```

Example:

```text
Customer + Customer Details
        ↓
      Merge
```

```text
Sales 2025
Sales 2026
     ↓
   Append
```

---

## 71. What is a Reference Query?

**Answer:**

A reference query creates a new query based on an existing query while maintaining a dependency on the original.

---

## 72. What is a Duplicate Query?

**Answer:**

A duplicate query creates an independent copy of the original query steps.

---

## 73. Reference vs Duplicate

| Reference | Duplicate |
|---|---|
| Depends on original | Independent copy |
| Changes can flow from source query | Changes are separate |
| Useful for reusable transformations | Useful for independent branches |

---

## 74. How do you optimize Power Query?

**Answer:**

I would:

1. Filter rows early.
2. Remove unnecessary columns.
3. Preserve query folding.
4. Avoid unnecessary transformations.
5. Perform transformations at the source when appropriate.
6. Use correct data types.
7. Reduce repeated operations.

---

# 🟡 9. Data Modeling Advanced

## 75. What is a Snowflake Schema?

**Answer:**

A snowflake schema normalizes dimension tables into additional related tables.

Example:

```text
Sales
 |
Product
 |
Category
 |
Department
```

---

## 76. Star Schema vs Snowflake Schema

| Star | Snowflake |
|---|---|
| Simpler | More complex |
| Fewer joins | More relationships |
| Easier DAX | More complicated |
| Often preferred in Power BI | Useful for some normalized structures |

---

## 77. Why should dimension keys be unique?

**Answer:**

The dimension side of a one-to-many relationship should generally contain unique keys. Duplicate keys can cause incorrect filtering and relationship problems.

---

## 78. Why avoid unnecessary bidirectional relationships?

**Answer:**

Bidirectional filtering can create:

- Ambiguous filter paths
- Unexpected results
- Performance issues

Single-direction relationships are usually preferred unless there is a clear requirement.

---

## 79. What is a Bridge Table?

**Answer:**

A bridge table is an intermediate table used to resolve many-to-many relationships.

Example:

```text
Customer
   |
Bridge
   |
Account
```

---

# 🟡 10. Power BI Service

## 80. What is a Workspace?

**Answer:**

A workspace is a collaborative environment where Power BI content is managed.

It can contain:

- Reports
- Semantic models
- Dashboards
- Dataflows
- Apps

---

## 81. What is a Power BI App?

**Answer:**

A Power BI App packages selected workspace content for business users.

---

## 82. What is Scheduled Refresh?

**Answer:**

Scheduled refresh automatically refreshes a semantic model according to a defined schedule.

---

## 83. What is an On-Premises Data Gateway?

**Answer:**

The gateway enables Power BI Service to securely connect to supported on-premises data sources.

Example:

```text
Power BI Service
       ↓
   Gateway
       ↓
SQL Server
```

---

## 84. Gateway types?

**Answer:**

Common gateway options include:

- Standard/Enterprise gateway
- Personal mode gateway

The standard gateway is generally used for organizational workloads and shared data sources.

---

## 85. What is a Workspace Role?

**Answer:**

Power BI workspaces support roles such as:

- Admin
- Member
- Contributor
- Viewer

Each role has different permissions.

---

## 86. What is Deployment Pipeline?

**Answer:**

Deployment pipelines help move Power BI content through environments such as:

```text
Development
      ↓
Test
      ↓
Production
```

---

# 🔐 11. Row-Level Security

## 87. What is Row-Level Security?

**Answer:**

Row-Level Security, or RLS, restricts which rows a user can access.

Example:

```text
User A → North Region
User B → South Region
User C → West Region
```

---

## 88. Static RLS

**Answer:**

Static RLS uses fixed filters.

Example:

```text
Region = "North"
```

---

## 89. Dynamic RLS

**Answer:**

Dynamic RLS determines access based on the logged-in user.

A common function is:

```DAX
USERPRINCIPALNAME()
```

---

## 90. Example Dynamic RLS

Security table:

| Email | Region |
|---|---|
| user1@company.com | North |
| user2@company.com | South |

RLS logic can use the current user's identity and relationships to filter the allowed region.

---

## 91. What is USERPRINCIPALNAME()?

**Answer:**

`USERPRINCIPALNAME()` returns the current user's principal name and is commonly used in dynamic security designs.

---

# ⚡ 12. Performance Optimization

## 92. How do you improve Power BI performance?

**Answer:**

I would focus on:

- Star schema
- Removing unnecessary columns
- Reducing unnecessary rows
- Optimizing DAX
- Preserving query folding
- Reducing visual count
- Avoiding unnecessary bidirectional relationships
- Choosing appropriate storage modes
- Optimizing source queries

---

## 93. What is Performance Analyzer?

**Answer:**

Performance Analyzer is a Power BI Desktop feature that helps identify which visuals are taking the most time to load.

It helps analyze:

- DAX query time
- Visual display time
- Other processing time

---

## 94. What is VertiPaq?

**Answer:**

VertiPaq is Power BI's columnar in-memory storage engine used by Import-mode semantic models.

It provides high compression and fast analytical queries.

---

## 95. How can you reduce model size?

**Answer:**

I would:

- Remove unused columns
- Remove unnecessary rows
- Use appropriate data types
- Reduce high-cardinality columns where possible
- Avoid storing unnecessary calculated columns
- Aggregate data when detailed data is not required

---

## 96. What is High Cardinality?

**Answer:**

A high-cardinality column contains a large number of unique values.

Examples:

```text
Transaction ID
GUID
Timestamp
```

High-cardinality columns can increase model size.

---

# 🔄 13. Incremental Refresh

## 97. What is Incremental Refresh?

**Answer:**

Incremental refresh refreshes only the required portion of data instead of refreshing the entire dataset every time.

---

## 98. Why use Incremental Refresh?

**Answer:**

It is useful for large datasets because it can:

- Reduce refresh time
- Reduce source load
- Process only recent data
- Improve scalability

---

## 99. Example Incremental Refresh Strategy

Suppose a sales table contains:

```text
10 years of data
```

Business requirement:

```text
Keep 10 years
Refresh last 7 days
```

Incremental refresh can process the recent period while retaining historical partitions.

---

# 🔴 14. Advanced Scenarios

## 100. What is a Composite Model?

**Answer:**

A composite model combines different storage modes, such as Import and DirectQuery, within a semantic model.

---

## 101. What is a Disconnected Table?

**Answer:**

A disconnected table does not have a physical relationship with other tables.

It can be used for:

- Parameters
- Scenario analysis
- Dynamic selections
- What-if analysis

---

## 102. What is a What-If Parameter?

**Answer:**

A What-If parameter allows users to dynamically change a numeric value and analyze its impact.

Example:

```text
Discount = 0% to 30%
```

Users can select a discount and see its impact on revenue or profit.

---

## 103. What are Field Parameters?

**Answer:**

Field parameters allow users to dynamically switch between fields or measures in visuals.

Example:

```text
Sales
Profit
Quantity
```

A user can select the metric to display.

---

## 104. What is a Calculation Group?

**Answer:**

Calculation groups allow reusable calculation logic to be applied across multiple measures.

They are useful for patterns such as:

```text
Current Year
Previous Year
YTD
YoY %
```

---

# 💼 15. Real Project Questions

## 105. Explain your Power BI project.

### Sample Answer:

> I worked on an end-to-end Power BI reporting solution where I connected Power BI to multiple data sources, performed data cleaning and transformation using Power Query, designed a star-schema data model, created DAX measures, and developed interactive dashboards.
>
> I implemented KPIs, slicers, drill-downs, drill-through pages, and business-specific calculations. I also configured refresh and security requirements and worked with stakeholders during requirement gathering, validation, UAT, and report deployment.
>
> I focused on report usability, data accuracy, and performance optimization.

---

## 106. How do you gather Power BI requirements?

**Answer:**

I follow a structured approach:

1. Understand the business objective.
2. Identify stakeholders.
3. Identify KPIs.
4. Understand required dimensions and filters.
5. Identify data sources.
6. Understand refresh requirements.
7. Understand security requirements.
8. Prepare wireframes.
9. Develop the report.
10. Conduct UAT.
11. Deploy to production.

---

## 107. How do you validate report data?

**Answer:**

I compare Power BI results against the source system.

I check:

- Row counts
- Total sales
- Record counts
- Distinct customers
- Null values
- Duplicate records
- Date ranges
- KPI calculations

---

## 108. What do you do if business users say the report numbers are incorrect?

**Answer:**

I would not immediately change the DAX.

I would first:

1. Understand the expected number.
2. Check source data.
3. Check filters.
4. Check relationships.
5. Check data granularity.
6. Validate DAX.
7. Check duplicate records.
8. Compare with source SQL.
9. Document the root cause.
10. Fix and retest.

---

## 109. How do you handle changing requirements?

**Answer:**

I first clarify the new requirement and assess its impact on:

- Data source
- Power Query
- Data model
- DAX
- Visuals
- Security
- Performance

Then I implement the change, test it, obtain stakeholder validation, and deploy it through the appropriate process.

---

## 110. How do you work with stakeholders?

**Answer:**

I work closely with business stakeholders to understand requirements, clarify KPI definitions, validate data, review dashboard designs, conduct UAT, and incorporate feedback.

---

# 🎯 16. Scenario-Based Interview Questions

## 111. Your Power BI report is very slow. What will you do?

**Answer:**

I would troubleshoot systematically:

```text
Performance Analyzer
        ↓
Visual Performance
        ↓
DAX Performance
        ↓
Data Model
        ↓
Relationships
        ↓
Power Query
        ↓
Source Query
```

I would also check:

- Number of visuals
- High-cardinality columns
- Complex DAX
- Bidirectional relationships
- Query folding
- Storage mode

---

## 112. Your Power BI model has 50 million rows. How would you optimize it?

**Answer:**

I would:

- Use a star schema.
- Remove unnecessary columns.
- Remove unnecessary historical data if permitted.
- Optimize source queries.
- Preserve query folding.
- Consider incremental refresh.
- Review Import vs DirectQuery.
- Use aggregations where appropriate.
- Optimize DAX.

---

## 113. Sales numbers are duplicated. What could be the reason?

**Answer:**

Possible reasons include:

- Duplicate keys
- Incorrect relationships
- Many-to-many relationship
- Incorrect joins
- Wrong granularity
- Duplicate fact records

I would validate the grain and relationships first.

---

## 114. A relationship is showing Many-to-Many. What will you do?

**Answer:**

I would investigate whether the many-to-many relationship is actually required.

If possible, I would redesign the model using:

```text
Dimension
   ↓
Bridge
   ↓
Fact
```

or create a proper dimension with unique keys.

---

## 115. A DAX measure works correctly in a card but incorrectly in a table. Why?

**Answer:**

The calculation may behave differently because the table introduces additional filter context or row context.

I would investigate:

- Filter context
- Row context
- Context transition
- Relationships
- Aggregation level
- Iterator behavior

---

## 116. Why is a calculated column not recommended for every calculation?

**Answer:**

Calculated columns are stored in the model and increase model size.

For dynamic aggregations, measures are generally preferred because they are calculated at query time based on filter context.

---

## 117. Users should see only their region. What would you implement?

**Answer:**

I would implement Dynamic Row-Level Security using a user-to-region mapping table and the logged-in user's identity.

---

## 118. The business wants the dashboard refreshed every morning. What will you configure?

**Answer:**

I would configure Scheduled Refresh in Power BI Service and verify:

- Data source credentials
- Gateway, if required
- Refresh frequency
- Time zone
- Refresh history
- Failure notifications

---

## 119. Power BI cannot connect to an on-premises SQL Server. What do you check?

**Answer:**

I would check:

1. Gateway installation.
2. Gateway service status.
3. Data source configuration.
4. Server/database name.
5. Credentials.
6. Network connectivity.
7. Gateway mapping.
8. Refresh error details.

---

## 120. How would you implement a Top 10 Customer dashboard?

**Answer:**

I would:

1. Create Total Sales measure.
2. Create Customer dimension.
3. Create a bar chart.
4. Apply Top N filtering.
5. Sort by Sales descending.
6. Add supporting KPIs.
7. Add slicers such as Date and Region.

---

## 121. Business wants Top N to be dynamically selected. What would you use?

**Answer:**

I would use a What-If parameter or a suitable field parameter/design depending on the requirement.

---

## 122. Business wants users to switch between Sales, Profit, and Quantity. What would you use?

**Answer:**

I would use Field Parameters or a parameter-driven measure-selection approach.

---

## 123. How would you show Actual vs Target?

**Answer:**

I would create measures such as:

```DAX
Actual = SUM(Sales[SalesAmount])

Target = SUM(Target[TargetAmount])

Achievement % =
DIVIDE(
    [Actual],
    [Target],
    0
)
```

Then use KPI, gauge, card, or appropriate comparison visuals.

---

## 124. How would you calculate Profit Margin?

```DAX
Profit =
[Total Sales] - [Total Cost]

Profit Margin =
DIVIDE(
    [Profit],
    [Total Sales],
    0
)
```

---

## 125. How would you calculate Year-over-Year Growth?

```DAX
Sales PY =
CALCULATE(
    [Total Sales],
    SAMEPERIODLASTYEAR('Date'[Date])
)

YoY Growth % =
DIVIDE(
    [Total Sales] - [Sales PY],
    [Sales PY],
    0
)
```

---

# 🔴 17. Experienced-Level Interview Questions

## 126. How do you design a Power BI solution from scratch?

**Answer:**

I follow an end-to-end process:

```text
Business Requirement
        ↓
Source Identification
        ↓
Data Profiling
        ↓
Data Transformation
        ↓
Data Modeling
        ↓
DAX Development
        ↓
Report Development
        ↓
Security
        ↓
Performance Testing
        ↓
UAT
        ↓
Deployment
        ↓
Monitoring
```

---

## 127. How do you choose between Import and DirectQuery?

**Answer:**

I evaluate:

- Data volume
- Refresh requirements
- Source performance
- Near-real-time requirements
- Concurrency
- Transformation requirements
- Security
- Infrastructure

If the dataset can be efficiently imported and refreshed within requirements, Import is often preferred for performance.

---

## 128. How do you optimize a large enterprise model?

**Answer:**

I would:

1. Use a star schema.
2. Define proper table grain.
3. Remove unused columns.
4. Optimize data types.
5. Reduce cardinality where practical.
6. Optimize DAX.
7. Use incremental refresh.
8. Review storage modes.
9. Optimize source queries.
10. Monitor performance continuously.

---

## 129. How do you handle production issues?

**Answer:**

I first identify the issue and its business impact.

Then:

```text
Identify
   ↓
Reproduce
   ↓
Analyze
   ↓
Find Root Cause
   ↓
Fix
   ↓
Test
   ↓
Deploy
   ↓
Monitor
```

I also document the root cause and resolution.

---

## 130. How do you ensure data quality?

**Answer:**

I implement validation checks such as:

- Row count validation
- Duplicate detection
- Null validation
- Data type validation
- Key validation
- Source-to-report reconciliation
- KPI validation
- Date validation

---

## 131. How do you handle large amounts of historical data?

**Answer:**

Depending on requirements, I would consider:

- Incremental refresh
- Partitioning
- Aggregations
- Data reduction
- Archiving
- Source-side optimization
- Appropriate storage mode

---

## 132. How do you troubleshoot incorrect DAX results?

**Answer:**

I break the calculation into smaller measures and validate each component.

For example:

```text
Total Sales
     ↓
Previous Year Sales
     ↓
Difference
     ↓
Growth %
```

I then check:

- Filter context
- Relationships
- Date table
- Granularity
- DAX functions
- Source data

---

## 133. What is your approach to dashboard design?

**Answer:**

I follow a business-first approach.

### Page structure:

```text
Page 1 → Executive Summary
Page 2 → Sales Analysis
Page 3 → Customer Analysis
Page 4 → Product Analysis
Page 5 → Detailed Transactions
```

I focus on:

- KPI hierarchy
- Simple navigation
- Consistent formatting
- Limited visual clutter
- Interactive filtering
- Business actions

---

## 134. What is UAT?

**Answer:**

UAT stands for **User Acceptance Testing**.

Business users validate whether the report meets the agreed requirements and produces expected results.

---

## 135. What should be included in Power BI documentation?

**Answer:**

Documentation should include:

- Business requirements
- Data sources
- Data model
- Table descriptions
- Column definitions
- KPI definitions
- DAX measures
- Power Query transformations
- Refresh schedule
- Gateway information
- Security
- Deployment process
- Known limitations

---

# 🧠 Rapid-Fire Power BI Questions

## 136. What does DAX stand for?

**Answer:** Data Analysis Expressions.

## 137. What does ETL stand for?

**Answer:** Extract, Transform, Load.

## 138. What language does Power Query use?

**Answer:** M.

## 139. What is used for calculations in Power BI?

**Answer:** DAX.

## 140. What is the preferred schema for Power BI?

**Answer:** Star schema.

## 141. What is RLS?

**Answer:** Row-Level Security.

## 142. What is KPI?

**Answer:** Key Performance Indicator.

## 143. What is UAT?

**Answer:** User Acceptance Testing.

## 144. What is a semantic model?

**Answer:** The modeled analytical layer containing tables, relationships, measures, columns, and metadata used by reports.

## 145. What is Query Folding?

**Answer:** Pushing supported Power Query transformations back to the source.

## 146. What is Incremental Refresh?

**Answer:** Refreshing only the required portion of data rather than processing the entire dataset.

## 147. What is CALCULATE?

**Answer:** A DAX function that evaluates an expression in a modified filter context.

## 148. What is SUMX?

**Answer:** An iterator that evaluates an expression row by row and then aggregates the results.

## 149. What is a measure?

**Answer:** A DAX calculation evaluated dynamically according to filter context.

## 150. What is a calculated column?

**Answer:** A column calculated during model refresh and stored in the model.

---

# ⭐ Top 20 Questions to Prepare First

If you have limited interview preparation time, focus on these:

1. What is Power BI?
2. Power BI Desktop vs Service
3. Import vs DirectQuery
4. Power Query
5. Query Folding
6. Merge vs Append
7. Fact vs Dimension
8. Star Schema
9. Relationships and Cardinality
10. Measure vs Calculated Column
11. CALCULATE
12. SUM vs SUMX
13. Filter Context vs Row Context
14. Time Intelligence
15. RLS
16. Gateway
17. Scheduled Refresh
18. Incremental Refresh
19. Performance Optimization
20. Explain your Power BI project

---

# 💼 How to Answer "Tell Me About Your Power BI Experience"

### Fresher Version

> I have hands-on knowledge of Power BI, including data connection, Power Query transformations, data modeling, DAX, and dashboard development. I have practiced creating interactive reports using slicers, filters, KPIs, drill-downs, and drill-throughs. I am also familiar with Power BI Service, scheduled refresh, and Row-Level Security.

### Experienced Version

> I have experience working on end-to-end Power BI solutions, starting from requirement gathering and data-source analysis through Power Query transformation, data modeling, DAX development, dashboard creation, testing, and deployment. I have worked with star-schema models, KPI development, time-intelligence calculations, dynamic filtering, Row-Level Security, refresh configuration, and performance optimization. I also collaborate with stakeholders during requirement discussions, UAT, and production support.

---

# 🎯 How to Explain a Power BI Project in an Interview

Use this structure:

```text
1. Project Name
2. Business Problem
3. Business Objective
4. Data Sources
5. Data Volume
6. Power Query Transformations
7. Data Model
8. DAX Measures
9. Dashboard Pages
10. KPIs
11. Security
12. Refresh Strategy
13. Performance Optimization
14. UAT
15. Business Impact
```

### Example

> The project was a Sales Performance Dashboard designed to help management monitor revenue, profit, customer performance, and regional trends.
>
> Data came from SQL Server and Excel sources. I used Power Query for cleaning, data type conversion, filtering, merging, and transformation. I created a star-schema model with Sales as the fact table and Customer, Product, Date, and Region as dimensions.
>
> I created DAX measures for Total Sales, Total Cost, Profit, Profit Margin, YTD Sales, Previous Year Sales, and YoY Growth. The dashboard included KPI cards, trend analysis, regional performance, Top Customers, Top Products, slicers, drill-down, and drill-through.
>
> I validated the report against source data and supported UAT. For performance, I reduced unnecessary columns, optimized DAX, reviewed relationships, and used appropriate refresh strategies.
>
> The final dashboard provided management with a centralized view of sales performance and helped them identify trends and underperforming areas.

---

# 🏆 Final Interview Tips

### For Fresher Interviews

Focus on:

```text
Power BI Basics
↓
Power Query
↓
Data Modeling
↓
Basic DAX
↓
Visualizations
↓
Power BI Service
```

### For 2–4 Years Experience

Focus on:

```text
Advanced DAX
↓
Data Modeling
↓
Power Query
↓
RLS
↓
Performance
↓
Power BI Service
↓
Real Project Scenarios
```

### For 4–8 Years Experience

Focus on:

```text
Enterprise Modeling
↓
Advanced DAX
↓
Performance Optimization
↓
Security
↓
Incremental Refresh
↓
Deployment
↓
Governance
↓
Architecture
↓
Production Troubleshooting
```

---

# 📌 Quick Power BI Cheat Sheet

| Topic | Key Point |
|---|---|
| Power BI | Business Intelligence Platform |
| Desktop | Report Development |
| Service | Cloud Sharing & Management |
| Power Query | Data Transformation |
| M | Power Query Language |
| DAX | Analytical Calculation Language |
| Fact Table | Business Events |
| Dimension | Descriptive Data |
| Star Schema | Preferred Analytical Model |
| Measure | Dynamic Calculation |
| Calculated Column | Stored Row-Level Calculation |
| Import | In-Memory Data |
| DirectQuery | Query Source Directly |
| RLS | Restrict Rows by User |
| Gateway | Connect Service to On-Premises Sources |
| Query Folding | Push Transformations to Source |
| Incremental Refresh | Refresh Required Data Only |
| UAT | User Acceptance Testing |
| KPI | Key Performance Indicator |
| CALCULATE | Modify Filter Context |

---

# 🚀 Conclusion

Power BI interviews are not only about remembering definitions. For experienced roles, interviewers generally want to understand **how you solve business problems using data**.

Always explain your answers using:

```text
Business Requirement
        ↓
Data
        ↓
Transformation
        ↓
Data Model
        ↓
DAX
        ↓
Visualization
        ↓
Validation
        ↓
Security
        ↓
Performance
        ↓
Business Impact
```

> ⭐ **Interview Tip:** When answering an experienced-level question, use a real project example whenever possible. Explain **what the requirement was, what you implemented, why you chose that approach, how you validated it, and what business impact it created.**

---

**📚 Power BI Interview Preparation — Fresher to Experienced**

*Keep practicing. Keep building dashboards. Keep improving your DAX. 🚀*