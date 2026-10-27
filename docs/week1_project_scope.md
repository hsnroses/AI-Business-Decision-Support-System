# Week 1 Project Scope — AI Business Decision Support System

## Project Name

**AI Business Decision Support System — Sales Analysis and Revenue Forecasting**

## Domain

Artificial Intelligence Engineering / Machine Learning / Data Analytics / Business Intelligence

## Problem Statement

Businesses collect sales data from different sources, but analysing the data and identifying useful business trends can be challenging. At a petrol station, sales come from multiple business segments, including Mogas (petrol), Diesel, and Kedai Mesra PETRONAS. Without a clear way to analyse these segments together, it may be difficult to understand sales patterns, compare performance, and estimate future revenue.

This project aims to develop an AI-powered business decision support system that analyses historical sales data, presents important business indicators, forecasts future sales revenue where the data supports reliable forecasting, and explains the results in simple language. The system is intended to help users understand business performance and make more informed planning decisions.

## Evidence of the Problem

- **Evidence 1: Microsoft Power BI**

  Power BI provides tools for creating dashboards, visualising business data, and monitoring key performance indicators. This demonstrates the importance of presenting business data in a form that supports analysis and decision-making.

  **Source:** Microsoft Power BI  
  https://www.microsoft.com/en-us/power-platform/products/power-bi

- **Evidence 2: Microsoft Excel**

  Excel provides spreadsheet tools for organising data, calculating values, and creating charts. However, users still need to build appropriate analyses and interpret the results for their specific business needs.

  **Source:** Microsoft Excel  
  https://www.microsoft.com/en-us/microsoft-365/excel

*Note: These sources demonstrate existing business analytics approaches. They do not independently prove the exact problems experienced by the selected petrol station. That should be confirmed by understanding its current sales reporting process and available data.*

## Initial Related Work / Existing Approaches

### 1. Business Intelligence Dashboards

**Example:** Microsoft Power BI

**Source:** https://www.microsoft.com/en-us/power-platform/products/power-bi

**What it already addresses:** Provides interactive dashboards, data visualisation, and reporting to help users understand business performance.

**Potential gap for this project:** The proposed system will focus specifically on analysing sales across Mogas, Diesel, and Kedai Mesra PETRONAS, with an emphasis on forecasting and explaining findings in simple language.

### 2. Spreadsheet-Based Sales Analysis

**Example:** Microsoft Excel

**Source:** https://www.microsoft.com/en-us/microsoft-365/excel

**What it already addresses:** Allows users to organise sales records, calculate totals, compare values, and create charts.

**Potential gap for this project:** Repeated analysis may require users to prepare calculations and interpret results manually. The proposed system aims to bring the key analyses and explanations into one workflow.

### 3. Time-Series Forecasting

**Example:** Statistical forecasting methods, including exponential smoothing.

**Source:** Hyndman and Athanasopoulos, *Forecasting: Principles and Practice*  
https://otexts.com/fpp3/

**What it already addresses:** Provides established methods for analysing historical observations and forecasting future values.

**Potential gap for this project:** Forecasting methods alone do not provide a complete business decision support workflow. This project will combine sales analysis, forecasting evaluation, visualisation, and plain-language explanations.

## Engineering Gap / Limitation

Existing tools support business reporting, spreadsheet analysis, and sales forecasting. However, the proposed project focuses on combining these capabilities into a single workflow tailored to the available petrol station sales data.

The system will aim to help users compare the performance of Mogas, Diesel, and Kedai Mesra PETRONAS, identify historical sales patterns, estimate future revenue when sufficient data is available, and understand the results through evidence-based explanations.

The actual engineering gap will be refined after examining the existing sales records and understanding how the business currently analyses its performance.

## Initial Project Objectives

- **O1:** To analyse historical sales records and identify sales trends and key business indicators for Mogas, Diesel, and Kedai Mesra PETRONAS.
- **O2:** To develop and evaluate a sales revenue forecasting approach using historical data and compare its performance against a simple baseline.
- **O3:** To develop a dashboard with clear, evidence-based explanations that help users understand sales performance and support business planning.

## Target Users

The intended users are the petrol station's owner, manager, or authorised staff who need to review sales performance and plan business activities.

## Data Sources

- **Source 1:** Historical Mogas sales records from the selected PETRONAS petrol station in Taman Yayasan, Segamat, Johor.
- **Source 2:** Historical Diesel sales records from the same station.
- **Source 3:** Historical Kedai Mesra PETRONAS sales records from the same station.

**Data availability and structure:** To be confirmed after inspecting the available records. The analysis will depend on the available dates, sales values, level of detail, and data quality. Access to and use of the records must be authorised.

## Initial Scope

### In Scope

- Importing and validating available historical sales data.
- Analysing sales trends and key indicators for the three business segments.
- Comparing sales performance across segments and time periods where the data permits.
- Forecasting future sales revenue if the dataset supports meaningful evaluation.
- Comparing forecast performance against a simple baseline.
- Displaying results through a dashboard.
- Providing plain-language explanations based on the calculated results and available evidence.

### Out of Scope

- Predicting exact future sales with a guarantee of accuracy.
- Calculating profit without reliable cost and expense data.
- Automatically changing fuel prices, inventory, staffing, or business operations.
- Replacing the station's existing accounting or point-of-sale systems.
- Making business decisions without human review.

## Initial Evaluation Focus

The system will be evaluated using the following areas:

1. **Data processing:** Whether valid sales records can be processed and invalid or missing data can be identified appropriately.
2. **Sales analysis:** Whether the system calculates sales totals and relevant indicators correctly.
3. **Forecasting performance:** Whether the forecasting approach performs better than, or provides useful value compared with, a simple baseline using suitable error metrics.
4. **Explanation quality:** Whether explanations are supported by the calculated results and do not introduce unsupported claims.
5. **Response time:** Whether common analysis and dashboard operations complete within a practical time.

Specific evaluation metrics and thresholds will be defined after the available data and system requirements have been examined.

## Weekly Progress

| Week | Focus | Deliverable | Status |
|---|---|---|---|
| W1 | Project framing and scoping | README and `docs/week1_project_scope.md` | In progress |

