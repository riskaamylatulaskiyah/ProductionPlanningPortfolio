Production Material Accuracy & Component Tracking Dashboard
(Manufacturing – Footwear Industry)
Production Planning (MES) Portfolio by Riska Amylatul Askiyah
to download this file in xlxs format please check this link: github

📘 Background

This portfolio presents a practical data-tracking and analysis system built for the footwear manufacturing industry.

Material accuracy is an essential component of production performance. Differences between SAP Qty (planned consumption) and MES Qty (actual scanned consumption) commonly occur due to real operational variations such as scrap, scanning mistakes, missing scans, rework, or deviations in process behavior.

This file demonstrates an end-to-end workflow:

extracting production scan data,

referencing component master data,

validating quantity accuracy,

analyzing variances,

summarizing trends,

forecasting values, and

visualizing manufacturing performance using Excel.

The structure and analysis fully align with the responsibilities of a Production Planner, Manufacturing Analyst, Industrial Engineer, Supply Chain Analyst, or Data Analyst within the footwear sector.


🎯 Purpose of This File

This portfolio is designed to demonstrate:

Ability to perform manufacturing data analysis using Excel.

Comparison of SAP Qty (theoretical consumption) vs MES Qty (actual usage).

Monitoring of production behavior across lines, shifts, and processes.

Calculation of key operational metrics:

total scans

overs

shorts

matches

total variance (465 units)

Use of Excel formulas (VLOOKUP, HLOOKUP, SUMIFS, COUNTIFS, Moving Average).

Construction of a forecast sheet for monitoring target vs actual performance.

Understanding of manufacturing workflow in footwear production.


🏭 Industry Process Understanding

Footwear Production Flow

1. Cutting – Raw materials (upper, lining, outsole sheet) are cut into required parts.

2. Sewing – Upper components are stitched, reinforced, and assembled.

3. StockFitting – Components are prepared and combined with semi-finished parts.

4. Assembling – Upper and outsole join to form the finished product.

System Understanding

ComponentCode → Unique material identification

Description → Material name

UnitWeight_kg → Material’s reference weight (used for consumption validation)

Data Flow Structure

SAP System
→ Holds BOM, routing, and planned material usage

MES System
→ Captures actual barcode scans and real-time consumption

This Analysis File
→ Compares planned vs actual, identifies accuracy gaps, and highlights improvement opportunities


📊 Contents of This File

1. RawData Sheet

Contains:

Date, Shift, Line, Process

MES_Code

ComponentCode & Component Description

SAP Qty (planned)

MES Qty (actual scanned)

Difference (variance)

Status (Over/Short/Match)
This is the primary operational dataset derived from factory MES scanning.


2. ComponentsMaster Sheet

Reference master table containing:

ComponentCode

Description

UnitWeight_kg
Used for data validation and material identification.


3. Pivot Table Sheet

Contains multiple pivot tables analyzing:

Line-level performance

Process-level variance

Overs vs Shorts

Total variance (465 units)

Scanning behavior patterns

Pivot filters include Line, Process, Component, and Status.


4. Forecast Target & Actual Sheet

Includes:

Daily target values (via VLOOKUP)

Actual MES_Qty aggregated per day

Variance & performance indicators

3-Day Moving Average Forecast
Formula sample:
=AVERAGE(B2:B4)


5. Summary_Calculations Sheet

Contains automated metrics using COUNTIF, SUMIFS, and reference checks, such as:

Total scans

Total overs, shorts, matches

Total SAP Qty

Total MES Qty


6. Balance_Check Sheet

Uses SUMIFS to confirm data consistency and ensure total calculations match pivot results.


🔍 Insights & Findings

Total variance of 465 units indicates deviation between theoretical and actual usage.

Overs (44) occur more frequently than shorts (31), suggesting scanning redundancy in some areas.

Negative variances appear in processes such as Line-4 Sewing and Line-5 StockFitting, indicating under-scanning or missing records.

Cutting and Sewing maintain closer MES–SAP alignment than other processes.

Variance patterns can be used to prioritize process improvements and operator training.


🌟 Improvement Opportunities

Implement barcode validation or double-scan prevention to reduce over-scanning.

Add real-time MES variance alerting.

Improve operator training on scanning discipline.

Enhance material handling accuracy during shift transitions.

Expand forecasting into error-measured predictive modeling (MAPE-based).

Build a Power BI version for interactive real-time visibility.
![Uploading image.png…]()
