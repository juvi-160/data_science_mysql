# SQL Practice — Course Work & Projects

A collection of SQL practice files I wrote while following an online SQL course. Everything here is me working through the lessons hands-on, plus a portfolio project where I applied the same techniques to clean and analyze a real-world layoffs dataset.
https://youtube.com/playlist?list=PLUaB-1hjhk8FE_XZ87vPPSfHqb6OcM0cF&si=FiGCloli6STDamKK

---

## 📚 What's Inside

The repo follows the course structure, from beginner to advanced. Each `.sql` file is a self-contained lesson with commented examples you can run yourself.

### 🟢 Beginner

| File | What you'll learn |
|------|-------------------|
| `Beginner - Select Statement.sql` | `SELECT`, `FROM`, aliases |
| `Beginner - Where Statement.sql` | Filtering with `WHERE`, comparison operators, `AND`/`OR`, `IN`, `LIKE` |
| `Beginner - Group By + Order By.sql` | `COUNT`, `SUM`, `AVG`, grouping, sorting |
| `Beginner - Having vs Where.sql` | Row-level vs group-level filtering |
| `Beginner - Limit and Aliasing.sql` | `LIMIT` and readable aliases |
| `Beginner - Parks_and_Rec_Create_db.sql` | Building a database and tables from scratch |

### 🟡 Intermediate

| File | What you'll learn |
|------|-------------------|
| `Intermediate - Joins.sql` | `INNER`, `LEFT`, `RIGHT`, `SELF` joins |
| `Intermediate - Unions.sql` | `UNION` vs `UNION ALL` |
| `Intermediate - Case Statements.sql` | Conditional logic with `CASE` |
| `Intermediate - Subqueries.sql` | Nested queries in `WHERE`, `FROM`, `SELECT` |
| `Intermediate - String Functions.sql` | `TRIM`, `REPLACE`, `SUBSTRING`, and more |
| `Intermediate - Window Functions.sql` | `ROW_NUMBER`, `RANK`, running totals |

### 🔴 Advanced

| File | What you'll learn |
|------|-------------------|
| `Advanced - CTEs.sql` | Common Table Expressions |
| `Advanced - Temp Tables.sql` | Temporary tables |
| `Advanced - Stored Procedures.sql` | Reusable query logic |
| `Advanced - Triggers and Events.sql` | Automated actions |

---

## 🚀 Project: Layoffs Data Cleaning & Analysis

For this project I applied the course techniques to a real dataset of tech-company layoffs:

- **Data Cleaning** — removed duplicates with window functions, standardized text (trimming, fixing `Crypto%` and country values), converted dates, and backfilled missing industry values by self-joining on company name.
- **EDA** — explored the cleaned data: biggest layoff events, totals by company/industry/country, trends over time, and rolling totals.

> 💡 **What this project taught me:** debugging real SQL. I spent a while tracking down why a backfill wasn't filling in — it turned out I was updating the wrong column in a `SELF JOIN`. Fixing that is where most of the real learning happened.

---

## 🛠️ Setup

1. Install **MySQL** (the work was done in MySQL Workbench).
2. Import `layoffs.csv` into a table named `layoffs`.
3. Run the **Data Cleaning** script first — it stages the data so the raw table stays untouched.
4. Then run the **EDA** script against the cleaned table.

> **Note:** The cleaning file uses a `layoffs_staging` table so the raw data stays protected.

