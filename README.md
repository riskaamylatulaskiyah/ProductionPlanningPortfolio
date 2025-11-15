# ProductionPlanningPortfolio
Production Planning
Production Material Accuracy & Component Tracking Dashboard
(Manufacturing – Footwear Industry)
Production Planning (MES) Portfolio by Riska Amylatul Askiyah


📘 Background

This portfolio presents a data analysis and tracking system designed for the footwear manufacturing environment. In mass-production plants, material accuracy is a critical factor that directly impacts production efficiency, cost control, and inventory integrity. Variances between SAP records (planned consumption) and MES records (actual consumption) often occur due to real-world operational dynamics, scanning errors, scrap, or process deviations.

This file demonstrates an end-to-end approach to identifying, cleaning, analyzing, and visualizing material consumption data across production lines and processes (Cutting, Sewing, StockFitting, Assembling). It showcases applied analytical understanding relevant to roles such as Data Analyst, Production Planner, Industrial Engineer, Process Analyst, and Supply Chain Analyst in the footwear sector.


🎯 Purpose of This File

To demonstrate the ability to analyze manufacturing production data using Excel.

To evaluate material usage accuracy by comparing SAP Qty (planned) and MES Qty (actual).

To provide insights on production behavior across lines, shifts, and processes.

To calculate key metrics such as total scans, shortages, overs, variances, and accuracy rate.

To build an automated system using formulas (VLOOKUP, HLOOKUP, SUMIFS, COUNTIFS).

To create a forecasting sheet (Target & Actual) for daily and operational performance monitoring.

To showcase a real manufacturing workflow understanding relevant to footwear operations.


🏭 Industry Process Understanding

The footwear manufacturing workflow involves multiple production stages:

1. Cutting – Raw materials are cut into required shapes.

2. Sewing – Upper components are stitched and assembled.

3. StockFitting – Components are prepared and matched with semi-finished goods.

4. Assembling – Upper and outsole are combined into the final product.

Throughout these processes, each material is identified by:

ComponentCode – Internal material identifier.

Description – Material name (Upper, Outsole, Accessory, etc.).

UnitWeight_kg – Reference for physical consumption validation.

Data flows through:

SAP → planning, BOM, and theoretical material usage

MES → real-time scanning and actual consumption

Analysis File → compares theory vs reality to identify operational variances

This analysis enables process improvement, cost reduction, and production accuracy monitoring.


📊 Contents of this File

1. RawData

Detailed production records per date, shift, line, process, component, SAP Qty, MES Qty, and differences.

2. ComponentsMaster

Reference table for ComponentCode, Description, and UnitWeight_kg.

3. Summary Dashboard (Pivot Tables)

Line-level performance

Process-level consumption

Total overs, shorts, matches

MES vs SAP variance

4. Forecast – Target & Actual

Contains:

Daily Targets

Actual MES Qty per day

HLOOKUP-based target retrieval

Variance & performance tags

Simple forecast trend indicator

5. Automated Formula Sheet

Includes formulas such as:

=VLOOKUP(A2, RawData!$A:$I, 9, FALSE)
=SUMIFS(RawData!$I:$I, RawData!$A:$A, A2)
=VLOOKUP(B2, Forecast!$A$1:$F$2, 2, FALSE)


🔍 Insights & Findings

Overs occurred more frequently than shorts (44 overs vs 31 shorts).

Certain lines (Line-4 Sewing, Line-5 StockFitting) show negative variances, indicating under-scanning or missing records.

Cutting and Sewing generally maintain closer alignment between SAP and MES.

Variance patterns can be used to set priority improvement areas.


🌟 Opportunities & Improvements

Integrate barcode validation to reduce over-scanning.

Introduce real-time variance alerts.

Improve operator training for scanning discipline.

Apply predictive analysis for material usage forecasting.

Build a full Power BI version of the dashboard.


🔧 Notes for Users / Instruksi Pengguna

Input new daily data in RawData only.

All summaries, dashboards, and forecasts update automatically.

Do not edit formulas in colored cells.
