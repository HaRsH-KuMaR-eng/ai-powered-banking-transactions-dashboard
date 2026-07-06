# AI-Powered Banking Transactions & Customer Insights Dashboard

### Dashboard Link : https://app.powerbi.com/groups/me/reports/d0b6903b-ae1e-439b-a6da-ca2edf7e43d7/2d141a7ad995e2400633?experience=power-bi

---

# Problem Statement

This dashboard helps banking institutions analyse customer transactions, account balances, and financial activities through interactive Power BI reports. It provides valuable insights into customer behaviour, transaction trends, account performance, and operational metrics, enabling data-driven business decisions.

The project demonstrates an end-to-end Business Intelligence workflow by combining **Artificial Intelligence, SQL Server, Power BI, Power Query, and DAX**. AI was utilised to generate realistic banking data, design the SQL database, recommend KPIs, and assist in creating DAX measures for reporting.

The banking dataset contains approximately **10,000 synthetic transaction records** with intentionally introduced real-world data quality issues such as inconsistent date formats, missing values, duplicate records, invalid relationships, inconsistent text formatting, and outliers. These issues were cleaned using SQL Server and Power Query before creating an interactive Power BI dashboard.

The final dashboard enables stakeholders to monitor customer transactions, account balances, account types, demographic distribution, transaction trends, and customer insights through interactive visualisations and KPIs.

---

# Tech Stack

- Microsoft Power BI
- Microsoft SQL Server (T-SQL)
- Power Query
- DAX
- AI (Perplexity AI)
- Data Modelling
- Star Schema

---

# Database Design

The project uses **Microsoft SQL Server** as the primary data source.

Three relational tables were created:

- Customers
- Accounts
- Transactions

The tables were later combined into a single analytical table named:

```
CombinedBankingDataset
```

using SQL **LEFT JOIN** operations.

---

## Database Schema

### Customers

| Column |
|---------|
| CustomerID |
| Name |
| Gender |
| DateOfBirth |
| Address |
| Email |
| Phone |
| AccountID |

---

### Accounts

| Column |
|---------|
| AccountID |
| CustomerID |
| Type |
| OpenDate |
| Balance |

---

### Transactions

| Column |
|---------|
| TransactionID |
| AccountID |
| TransactionDate |
| Type |
| Amount |
| Description |
| Currency |

---

# Data Generation

A realistic banking database containing approximately **10,000 transaction records** was generated using AI-assisted SQL scripts.

The dataset intentionally contains several real-world data quality issues, including:

- Mixed date formats
- Missing values
- NULL values
- Duplicate records
- Invalid foreign key references
- Inconsistent capitalisation
- Negative transaction values
- Outlier balances
- Mixed currency formats

These issues were intentionally introduced to practice SQL data cleaning, ETL processes, and Power Query transformations.

---

# Steps Followed

- **Step 1:** Used Perplexity AI to generate a comprehensive banking dataset requirement prompt including realistic banking scenarios, 10,000 records, intentional data quality issues, KPI suggestions, chart recommendations, and required DAX measures.

- **Step 2:** Refined the generated AI prompt and regenerated it to improve dataset quality and business logic.

- **Step 3:** Generated SQL Server scripts using AI to:
  - Create database schema
  - Create banking tables
  - Insert approximately 10,000 records

- **Step 4:** Created SQL Server database:

```
Power_BI_PROJECT_AI
```

and executed all SQL scripts.

- **Step 5:** Performed SQL data cleaning by standardising date formats across the Customers, Accounts, and Transactions tables.

- **Step 6:** Combined all relational tables using SQL LEFT JOIN operations to create the final analytical dataset.

- **Step 7:** Imported the SQL Server database into Power BI Desktop.

- **Step 8:** Used AI to recommend KPIs, DAX measures, and visualisation ideas based on the available banking data.

- **Step 9:** Performed additional data cleaning in Power Query, including:
  - Handling missing values
  - Changing data types
  - Creating calculated columns
  - Removing inconsistencies

- **Step 10:** Created relationships using a Star Schema data model.

- **Step 11:** Developed DAX measures for various KPIs.

- **Step 12:** Designed a two-page interactive Power BI dashboard using cards, line charts, pie charts, bar charts, treemaps, slicers, and area charts.

- **Step 13:** Published the report to Microsoft Power BI Service.

---

# KPIs Used

## Dashboard 1

### Transactions by Type

**Description**

Displays the distribution of Credit and Debit transactions.

**Visual**

Pie Chart

---

### Monthly Transaction Amount

**Description**

Shows monthly transaction amount trends throughout the year.

**Visual**

Area Chart

---

### Total Balance by Account Type

**Description**

Compares balances across Savings and Current accounts.

**Visual**

Clustered Column Chart

---

### Top Customers by Transaction Amount

**Description**

Displays customers with the highest transaction amounts.

**Visual**

Bar Chart

---

### Inactive Accounts

**Description**

Shows inactive accounts based on transaction activity.

**Visual**

Line Chart

---

## Dashboard 2

### Customer Gender Distribution

**Description**

Displays the distribution of customers by gender.

**Visual**

Donut Chart

---

### Customers by Age Group

**Description**

Categorises customers into different age groups.

**Visual**

Column Chart

---

### Accounts by Account Type

**Description**

Displays the number of Current and Savings accounts.

**Visual**

Treemap

---

### Monthly Transaction Balance Trend

**Description**

Displays monthly balance trends to monitor financial performance.

**Visual**

Area Chart

---

# Data Cleaning

Several SQL update queries were executed before importing the dataset into Power BI.

Cleaning operations included:

- Standardised all dates into MM/DD/YYYY format
- Corrected inconsistent date formats
- Cleaned customer birth dates
- Standardised account opening dates
- Standardised transaction dates
- Corrected inconsistent data values
- Prepared dataset for ETL

---

# Data Modelling

The project follows a relational data model.

```
Customers
      │
      ▼
Accounts
      │
      ▼
Transactions
      │
      ▼
CombinedBankingDataset
      │
      ▼
Power BI Dashboard
```

---

# Dashboard Snapshot (Page 1)

![Dashboard 1](https://github.com/HaRsH-KuMaR-eng/ai-powered-banking-transactions-dashboard/blob/43379121c046161c7ebe9ea328abee659c880a73/DashBoard1.png)

---

# Dashboard Snapshot (Page 2)


![Dashboard 2](https://github.com/HaRsH-KuMaR-eng/ai-powered-banking-transactions-dashboard/blob/41e672930764cd73af2ae5058eef13f2ae2dd1e0/dashboard2.png)

---

# Insights

### Transaction Analysis

- Debit and Credit transactions are almost equally distributed.
- Monthly transaction amounts fluctuate throughout the year with noticeable peaks.
- Some customers contribute significantly higher transaction values than others.

### Customer Insights

- Customer demographics are evenly distributed between male and female customers.
- Most customers belong to the 36–50 and 51+ age groups.
- Savings and Current account distributions are balanced.

### Account Analysis

- Current accounts hold a significantly higher total balance.
- Several inactive accounts were identified through transaction history.
- Monthly balance trends help monitor customer account performance.

---

# SQL Scripts

The repository includes SQL scripts for:

- Database Creation
- Table Creation
- Synthetic Data Generation
- SQL Data Cleaning
- Table Joins
- Combined Dataset Creation

---

# Project Features

- AI-assisted dataset generation
- SQL Server relational database
- ETL using SQL and Power Query
- Star Schema Data Modelling
- Interactive Power BI Dashboards
- DAX Measures
- Business KPIs
- Customer Insights
- Transaction Analysis
- Account Performance Analysis

---

# Future Improvements

- Real-time SQL Server integration
- Live Banking API
- Fraud Detection Dashboard
- Loan Analytics Dashboard
- Credit Risk Prediction
- Machine Learning Integration
- Customer Segmentation using AI

---

# Author

**Harsh Kumar**

Data Analyst | Power BI Developer


---
