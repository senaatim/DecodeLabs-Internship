# DecodeLabs-Internship
# Walmart Weekly Sales Analytics Project — DecodeLabs

## Project Overview
This repository contains a comprehensive data analytics project utilizing a historical Walmart Weekly Sales dataset sourced from Kaggle. The workflow covers initial dataset profiling, robust data cleaning pipelines via Power Query, exploratory data analysis using DAX, and executive-level dashboard creation in Power BI.

---

## Project Architecture & File Formats
Data/Walmart_Sales.csv.xlsx — The original, untamed historical retail transaction data from Kaggle.
Dashboard/Walmart_Weekly_sales_sheet.pbix — The complete analytical powerhouse containing our Power Query data cleaning transformations, internal relational schema, DAX calculations, and interactive visualizations.
Dashboard/dashboard_screenshot.png — A high-resolution static preview of the finished reporting canvas for rapid review.

---

## Task 1 — Data Collection & Dataset Understanding

### Dataset Profile
The source engine consists of historical retail transaction logs capturing operational timelines between **2010 and 2012**. 

### Feature Schema & Data Types
The data model explicitly defines 8 structural columns across precise native data footprints:
Store (Integer) — Unique numerical identifier for individual physical Walmart branch locations.
Date (Date Format) — Weekly calendar marker tracking specific business periods.
Weekly_Sales (Decimal/Currency) — Total revenue performance figures recorded for the designated store week.
Holiday_Flag (Integer/Boolean) — Binary indicator tracking whether a given week contains a major holiday event ($1$ = Holiday, $0$ = Non-Holiday).
Temperature (Decimal) — Regional atmospheric temperature tracking on the day of sales tracking.
Fuel_Price (Decimal) — Prevailing regional cost of fuel per gallon during the transaction cycle.
CPI (Decimal) — Consumer Price Index evaluation metric tracking inflationary impacts.
Unemployment (Decimal) — Local localized unemployment rates active during the reporting period.

---

## Task 2 — Data Cleaning & Preprocessing

The source dataset was processed through a rigorous **Power Query Editor** validation pipeline:

Data Type Realignment: The critical "Date" feature was transformed from a loose "Any" data format into an explicit native "Date" format
Granular Deduplication: Duplicate transactional rows were tracked and eliminated by implementing a strict composite primary key using "Store" + "Date" as the unique combination.
Data Quality Audit: Executed a comprehensive column-quality sweep confirming a 0% missing/null data rate across all 8 native columns, ensuring completely unbiased metrics.

---

## Task 3 — Exploratory Data Analysis (EDA)

Advanced analytical layers were established within the Power BI layer by engineering custom **DAX (Data Analysis Expressions)** measures. The core retail performance footprint is anchored by these dynamic evaluations:

Total Revenue Pool: Summation of all sales streams.
Operational Averages: Evaluation of standard baseline weekly sales performance.
Bound Limits: Dynamic calculation of maximum and minimum sales thresholds.

### Key Data Insights
By grouping sales footprints into **Holiday vs. Non-Holiday matrices**, the DAX models surfaced a distinct, quantifiable upward shift in average sales velocity during holiday calendar weeks. This confirms significant, predictable seasonal buying patterns that Walmart can exploit for strategic inventory staging.

---

## Task 4 — Data Visualization & Storytelling

The output of this project is a fully dynamic, highly scannable Power BI Dashboard engineered to deliver executive business intelligence at a glance. 

### Core Interface Components:
1. The Executive KPI Panel: Implements high-impact Power BI Card visuals summarizing Total Revenue, Average Weekly Sales, and Global Peak Volatility records based on our DAX measures.
2. Seasonality Analysis (Line Chart): Tracks historical "Weekly_Sales" against a rolling "Date" timeline, providing immediate visual confirmation of Q4 shopping velocity spikes.
3. Macroeconomic Impact Layer: Features interactive filtering matrices that allow users to instantly view how fluctuations in "Fuel_Price", "CPI", and "Unemployment" correlate with high-performing retail hubs.
4. Dynamic Context Slicers: Includes an active "Store" and "Holiday_Flag" selection system on the canvas margins, empowering stakeholders to drill down into specific regional subsets instantly.
