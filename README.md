# Sales Tracker – Veda Technology Task 8

## Project Overview

This project is a sales tracking system created using Google Sheets as part of the Veda Technology internship Task 8.

The objective of the project is to organize sales data and automatically calculate daily, weekly, and monthly sales totals using spreadsheet formulas and data validation.

## Tools Used

* Google Sheets
* Microsoft Excel (.xlsx)
* GitHub

## Workbook Structure

The workbook contains two main sheets:

### 1. Raw Data

The Raw Data sheet contains the individual sales transactions with the following fields:

* Date
* Product
* Category
* Quantity
* Unit Price
* Total Sales

The Total Sales column is calculated automatically using:

`Quantity × Unit Price`

Product and Category fields use dropdown-based data validation to reduce incorrect entries.

### 2. Summary

The Summary sheet provides automatic sales aggregation at different levels:

* Overall Sales
* Daily Sales
* Weekly Sales
* Monthly Sales

The summary uses spreadsheet formulas to calculate sales totals from the Raw Data sheet.

## Key Features

* Separate Raw Data and Summary sheets
* Automatic Total Sales calculation
* Product dropdown validation
* Category dropdown validation
* Daily sales aggregation
* Weekly sales aggregation
* Monthly sales aggregation
* Currency formatting
* Formula-based calculations
* Manual verification of calculated totals

## Sample Results

Using the sample sales data entered in the workbook:

| Summary                       |    Sales |
| ----------------------------- | -------: |
| Overall Sales                 | ₹249,000 |
| Week 1 (01 Aug – 07 Aug 2026) | ₹208,000 |
| Week 2 (08 Aug – 14 Aug 2026) |  ₹41,000 |
| August 2026                   | ₹249,000 |

The weekly totals were manually verified:

**₹208,000 + ₹41,000 = ₹249,000**

The daily sales totals also reconcile with the overall sales total.

## Formulas Used

### Total Sales

```excel
=D2*E2
```

### Daily Sales

```excel
=SUMIFS('Raw Data'!$F$2:$F$100,'Raw Data'!$A$2:$A$100,A8)
```

### Weekly Sales

The weekly calculation uses date-range based aggregation to calculate sales between the selected week start and week end dates.

### Monthly Sales

The monthly total is calculated from the daily sales summary to provide the total sales for the selected month.

## Outcome

The completed sales tracker provides a structured and easy-to-use way to record sales transactions and monitor sales performance across daily, weekly, and monthly periods.

This project demonstrates practical skills in:

* Spreadsheet data management
* Data validation
* Formula-based calculations
* Sales aggregation
* Data organization
* Basic reporting and analysis

## Project File

The completed Excel workbook is available in this repository as:

`sales-tracker-task-8.xlsx`
