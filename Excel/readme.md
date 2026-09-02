<h1 align="center">📊 Excel Notes & Cheat Sheet</h1>


## 📌 Overview
This repository contains a **comprehensive set of Excel notes and formulas** for quick reference.  
It covers essential functions, data analysis techniques, and productivity tips — perfect for interview prep, daily work, or study.

---

## 🗂️ Contents
- Math & Statistical Functions
- Date & Time Functions
- Text Functions
- Lookup & Reference Functions
- Logical Functions
- Financial Functions
- Information Functions
- Data Analysis Tools (Pivot Tables, Data Validation, Data Cleaning)

---

## 🔢 Math & Stats
| Function | Syntax | Example | Result |
|----------|--------|---------|--------|
| SUM | `=SUM(A1:A5)` | {2,4,6,8,10} | 30 |
| AVERAGE | `=AVERAGE(B1:B4)` | {5,10,15,20} | 12.5 |
| ROUND | `=ROUND(3.14159,2)` | — | 3.14 |
| RANDBETWEEN | `=RANDBETWEEN(1,100)` | — | Random (e.g., 57) |
| COUNTIF | `=COUNTIF(C1:C10,">50")` | {10,55,60,45} | 2 |

---

## ⏰ Date & Time
| Function | Syntax | Example | Result |
|----------|--------|---------|--------|
| TODAY | `=TODAY()` | — | Current Date |
| DATEDIF | `=DATEDIF("01-Jan-2020","01-Jan-2026","y")` | — | 6 |
| NETWORKDAYS | `=NETWORKDAYS("01-Jun-2026","15-Jun-2026")` | — | 11 |

---

## 🔤 Text Functions
| Function | Syntax | Example | Result |
|----------|--------|---------|--------|
| LEFT | `=LEFT("Microsoft",5)` | — | Micro |
| RIGHT | `=RIGHT("Excel",3)` | — | cel |
| LEN | `=LEN("Business Analyst")` | — | 16 |
| CONCAT | `=CONCAT("Hello ","World")` | — | Hello World |
| SUBSTITUTE | `=SUBSTITUTE("2026-06-16","-","/")` | — | 2026/06/16 |

---

## 🔎 Lookup & Reference
| Function | Syntax | Example | Result |
|----------|--------|---------|--------|
| VLOOKUP | `=VLOOKUP(101,A2:D10,3,FALSE)` | Row {101,"John","HR",5000} | HR |
| INDEX | `=INDEX(A1:C3,2,3)` | Value at row 2, col 3 | 45 |
| MATCH | `=MATCH(20,B1:B5,0)` | {10,20,30,40,50} | 2 |
| XLOOKUP | `=XLOOKUP(lookup_value, lookup_array, return_array, [if_not_found])` | Flexible search | — |

---

## ✅ Logical Functions
| Function | Syntax | Example | Result |
|----------|--------|---------|--------|
| IF | `=IF(A1>50,"Pass","Fail")` | A1=60 | Pass |
| AND | `=AND(A1>10,B1<100)` | A1=20, B1=80 | TRUE |
| OR | `=OR(A1=5,B1=10)` | A1=5 | TRUE |
| IFERROR | `=IFERROR(1/0,"Error Found")` | — | Error Found |

---

## 💰 Financial Functions
| Function | Syntax | Example | Result |
|----------|--------|---------|--------|
| PMT | `=PMT(5%/12,60,-20000)` | Loan 20k, 5% interest | 377.42 |
| FV | `=FV(6%/12,120,-200,-5000)` | Monthly deposits | ≈53,000 |

---

## ℹ️ Information Functions
| Function | Syntax | Example | Result |
|----------|--------|---------|--------|
| ISNUMBER | `=ISNUMBER(123)` | — | TRUE |
| ISTEXT | `=ISTEXT("Excel")` | — | TRUE |
| ISBLANK | `=ISBLANK(A1)` | A1 empty | TRUE |

---

## 📊 Data Analysis Tools
### Pivot Tables
- Summarize large datasets
- Group, filter, and aggregate data
- Useful for quick insights and reporting

### Data Validation
- Restrict data entry (dropdowns, ranges, limits)
- Maintain accuracy and consistency

### Data Cleaning
- Remove duplicates
- Handle missing values
- Standardize formats (dates, text, numbers)

---

## 📈 Usage
- Use this README as a **quick reference guide** while working in Excel.
- Ideal for **interview preparation** and **daily productivity**.
- Extend with your own formulas and case studies.

---

## 🤝 Contribution
Feel free to fork this repo, add new formulas, or enhance the notes with advanced Excel techniques (Power Query, Power Pivot, etc.).
