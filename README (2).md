# Online Learning SQL Analytics: Database Schema & Business Reporting

## Project Overview

This project demonstrates how SQL can be used to design a relational
database and transform online-learning data into meaningful business
reports.

The project uses **MySQL 8** and contains four connected tables:

-   **students** -- learner information
-   **courses** -- course catalogue and course details
-   **enrollments** -- student-course enrollment, status, progress and
    completion
-   **assessments** -- quiz, assignment and final-exam results

The database schema uses primary keys, foreign keys, unique constraints,
`CHECK` constraints, appropriate data types and indexes to maintain data
integrity and support efficient querying.

## Objectives

The project focuses on:

1.  Designing a normalized relational database for an online-learning
    platform.
2.  Creating tables and inserting sample data.
3.  Connecting related tables using primary and foreign keys.
4.  Building SQL reports to answer practical business questions.
5.  Applying aggregation, joins, conditional logic, CTEs, date functions
    and window functions.
6.  Converting raw learner data into actionable KPIs and performance
    insights.

## Database Structure

``` text
students
   |
   | 1 : N
   v
enrollments
   ^       |
   |       | 1 : N
   |       v
courses  assessments
```

The `enrollments` table resolves the many-to-many relationship between
students and courses.

## SQL Reports

The project includes ten analytical reports:

  -----------------------------------------------------------------------
  Report                  Business Question       Main SQL Technique
  ----------------------- ----------------------- -----------------------
  3.1 Executive KPI       What are the headline   Subqueries + Aggregates
  Summary                 platform metrics?       

  3.2 Course Scorecard    How does each course    JOIN + Weighted Average
                          perform?                

  3.3 Category            Which categories        Conditional Aggregation
  Performance             attract learners and    
                          revenue?                

  3.4 Monthly Enrollment  How do enrollments      CTE + Window Functions
  Trend                   change over time?       

  3.5 Time to Complete vs How long do learners    Date Arithmetic
  Course Length           take to complete        
                          courses?                

  3.6 Learner Leaderboard Who has the highest     `RANK()`
                          assessment performance? 

  3.7 Best Course per     Which course has the    `ROW_NUMBER()` +
  Category                highest completion rate `PARTITION BY`
                          in each category?       

  3.8 Final Exam          How are final-exam      `CASE` Bucketing
  Distribution            scores distributed?     

  3.9 Completion by       How does completion     `HAVING` Threshold
  Country                 vary by country?        

  3.10 Stalled Learners   Which learners have     `COALESCE()` +
                          been inactive for 30+   `DATEDIFF()`
                          days?                   
  -----------------------------------------------------------------------

## Key SQL Concepts Demonstrated

-   `CREATE DATABASE`
-   `CREATE TABLE`
-   `INSERT INTO`
-   Primary and foreign keys
-   `UNIQUE` and `CHECK` constraints
-   `JOIN` and `LEFT JOIN`
-   `GROUP BY`
-   `HAVING`
-   `COUNT`, `SUM`, `AVG`, `MAX`
-   `CASE WHEN`
-   Common Table Expressions (CTEs)
-   Window functions
-   `RANK()`
-   `ROW_NUMBER()`
-   `PARTITION BY`
-   `LAG()`
-   `DATE_FORMAT()`
-   `DATEDIFF()`
-   `COALESCE()`
-   Subqueries
-   Weighted averages

## Executive KPIs from the Project

The presentation reports the following platform-level metrics:

-   **60** total students
-   **8** courses
-   **190** enrollments
-   **64.2%** completion rate
-   **26.3%** dropout rate
-   **9.5%** in-progress rate
-   **79.4%** average enrollment progress
-   **74.6%** overall assessment score

## Example Business Insights

The analysis highlights several patterns in the sample dataset:

-   SQL Fundamentals has a reported **75.0% completion rate**.
-   Advanced SQL has a reported **33.3% completion rate** and **58.3%
    dropout rate**.
-   Data & Analytics has **77 enrollments** across three courses in the
    report.
-   The monthly enrollment analysis uses a running total and
    month-over-month growth.
-   The learner leaderboard applies a minimum of three assessments
    before ranking learners.
-   Country-level completion analysis applies a minimum threshold of 10
    enrollments.
-   The stalled-learner report identifies learners who are in progress,
    below 90% completion, and inactive for at least 30 days.

## Files in This Repository

``` text
SQL-online-Coaching.sql
README.md
Online_Learning_Schema_and_Reporting.pdf
```

## How to Run

1.  Install **MySQL 8.0** or a compatible MySQL environment.
2.  Open MySQL Workbench, command line, or another MySQL client.
3.  Run the SQL script.
4.  The script creates the `online_learning` database and its tables.
5.  Load the sample data.
6.  Run the analytical SQL reports individually to reproduce the
    results.

## Project Value

This project demonstrates practical SQL skills for **Data Analyst /
Business Analyst** roles by combining database design with
business-oriented reporting. It shows how relational data can be
structured, queried and analyzed to answer questions about learner
engagement, course performance, assessment results and completion
behavior.

## Tools & Technologies

-   MySQL 8
-   SQL
-   Relational Database Design
-   Data Analysis
-   Business Reporting
-   Window Functions
-   CTEs

## Author

**Jaya Shanker**

Agricultural Economics \| Data Analytics \| Data Science
