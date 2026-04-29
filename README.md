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
