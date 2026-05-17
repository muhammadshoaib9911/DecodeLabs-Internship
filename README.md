# DecodeLabs-Internship
==================================

This repository only contain DecodeLabs-internship tasks or projects

===================================

Data Cleaning & Preparation Project
=============================
----------
🚀 Overview
--------------

This project focuses on cleaning and preparing a raw e-commerce dataset to make it suitable for analysis. It was completed as part of my internship at DecodeLabs.

Raw data often contains missing values, duplicates, and inconsistencies. This project demonstrates how to handle such issues using Python.

==================
📂 Dataset Description
=================

The dataset contains 1200 records and 14 columns, including:

OrderID

Date

CustomerID

Product

Quantity

UnitPrice

TotalPrice

PaymentMethod

OrderStatus

CouponCode

==================
🎯 Project Objectives
====================

Identify and handle missing values

Remove duplicate records

Correct data formats (date, numeric, text)

Validate data consistency and accuracy

=====================
🛠️ Tools & Technologies
=====================

Python

Pandas

NumPy

Matplotlib

====================
🔧 Data Cleaning Steps
====================

1. Handling Missing Values

2. Found missing values in CouponCode
Replaced with "No Coupon"

3. Removing Duplicates
Checked for duplicate rows and removed them

4. Data Type Correction
Converted Date to datetime format
Ensured numeric columns were properly formatted

5. Text Cleaning
Removed extra spaces
Standardized text (lowercase)

6. Data Validation

Verified:
TotalPrice = Quantity × UnitPrice

Used numpy.isclose() to handle floating-point precision
📊 Data Analysis & Visualization

=======================================
Basic analysis was performed to understand the dataset:
=================================

Product distribution

Payment method trends

Sales by order status

Sales over time

===============
📈 Key Insights
===================

Dataset was mostly clean but required validation

No major calculation errors were found

Floating-point precision caused false mismatches

Product and payment trends provide useful insights

==============
# Project 03 SQL Data Analysis
=========

# E-Commerce Sales Analysis Using SQL
===========

## Project Overview

This project demonstrates how SQL queries can be used to analyze an e-commerce sales dataset. The analysis was performed inside a Jupyter Notebook using Python, Pandas, SQLite, and SQL queries in Visual Studio Code.

The main objective of the project is to extract useful business insights from the dataset by applying SQL fundamentals such as filtering, sorting, grouping, and aggregation.

---

# Objectives

The project focuses on:

* Writing SQL `SELECT` queries
* Filtering data using `WHERE`
* Sorting results using `ORDER BY`
* Grouping records using `GROUP BY`
* Performing aggregations using:

  * `COUNT()`
  * `SUM()`
  * `AVG()`

---

# Technologies Used

* Python
* Pandas
* SQLite
* Jupyter Notebook
* Visual Studio Code

---

# Dataset Information

The dataset contains 1200 e-commerce order records with 14 columns.

## Dataset Columns

| Column Name     | Description               |
| --------------- | ------------------------- |
| OrderID         | Unique order identifier   |
| Date            | Order date                |
| CustomerID      | Unique customer ID        |
| Product         | Product name              |
| Quantity        | Quantity purchased        |
| UnitPrice       | Price per unit            |
| ShippingAddress | Customer shipping address |
| PaymentMethod   | Payment method used       |
| OrderStatus     | Status of order           |
| TrackingNumber  | Shipment tracking number  |
| ItemsInCart     | Number of items in cart   |
| CouponCode      | Applied coupon code       |
| ReferralSource  | Marketing/referral source |
| TotalPrice      | Total order amount        |

---

# Project Workflow

## Step 1: Import Libraries

```python
import pandas as pd
import sqlite3
```

---

## Step 2: Load Dataset

```python
df = pd.read_csv("ecommerce.csv")
```

---

## Step 3: Create SQLite Database

```python
conn = sqlite3.connect("ecommerce.db")
df.to_sql("orders", conn, if_exists="replace", index=False)
```

---

# SQL Queries Used

## 1. Display All Records

```sql
SELECT * FROM orders;
```

---

## 2. Filter Delivered Orders

```sql
SELECT *
FROM orders
WHERE OrderStatus = 'Delivered';
```

---

## 3. Sort Orders by Highest Revenue

```sql
SELECT OrderID, Product, TotalPrice
FROM orders
ORDER BY TotalPrice DESC;
```

---

## 4. Count Total Orders

```sql
SELECT COUNT(*) AS TotalOrders
FROM orders;
```

---

## 5. Calculate Total Revenue

```sql
SELECT SUM(TotalPrice) AS TotalRevenue
FROM orders;
```

---

## 6. Calculate Average Order Value

```sql
SELECT AVG(TotalPrice) AS AvgOrderValue
FROM orders;
```

---

## 7. Group Sales by Product

```sql
SELECT Product,
       SUM(TotalPrice) AS TotalSales
FROM orders
GROUP BY Product;
```

---

## 8. Count Orders by Payment Method

```sql
SELECT PaymentMethod,
       COUNT(*) AS TotalOrders
FROM orders
GROUP BY PaymentMethod;
```

---

## 9. Analyze Orders by Status

```sql
SELECT OrderStatus,
       COUNT(*) AS TotalOrders
FROM orders
GROUP BY OrderStatus;
```

---

## 10. Revenue by Referral Source

```sql
SELECT ReferralSource,
       SUM(TotalPrice) AS Revenue
FROM orders
GROUP BY ReferralSource
ORDER BY Revenue DESC;
```

---

# Key Insights

* Identified the most popular payment methods.
* Analyzed total sales revenue.
* Determined top-selling products.
* Compared order statuses such as Delivered and Pending.
* Evaluated referral sources generating the highest revenue.
* Examined customer purchasing behavior.

---

# Conclusion

This project demonstrates the practical use of SQL for analyzing e-commerce sales data. Using SQL queries inside Jupyter Notebook helped extract meaningful insights from the dataset efficiently.

The project strengthened understanding of:

* SQL fundamentals
* Data filtering and sorting
* Aggregation functions
* Grouping and summarizing data
* Data analysis workflow using Python and SQL

---

# Future Improvements

Possible future enhancements include:

* Adding data visualizations using Matplotlib
* Creating interactive dashboards
* Using advanced SQL queries
* Performing customer segmentation analysis
* Building predictive sales models

---

# Author

Muhammad Shoaib

