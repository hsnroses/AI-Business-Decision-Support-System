# Week 2: Project Framing and Requirements
## AI Business Decision Support System

# Section 0 — Project Framing and Application Scope

## 0.1 Project Name

**AI Business Decision Support System — Sales Analysis and Revenue Forecasting**

## 0.2 Problem Statement

Businesses collect sales records but may find it challenging to turn the data into useful information for business planning. A petrol station has different sales segments, including Mogas, Diesel, and Kedai Mesra PETRONAS. Understanding the performance of each segment requires accurate calculations, comparisons, and interpretation of historical sales patterns.

This project aims to develop an AI-powered decision support system that analyses historical sales data, presents key business indicators, forecasts future sales revenue where the available data supports it, and explains the findings in simple language.

## 0.3 Evidence of the Problem

**Evidence 1: Microsoft Power BI**

Microsoft Power BI provides business intelligence tools for data visualisation, reporting, and monitoring key performance indicators. This demonstrates the practical use of dashboards to help users understand business data.

Source: https://www.microsoft.com/en-us/power-platform/products/power-bi

**Evidence 2: Microsoft Excel**

Microsoft Excel provides spreadsheet functions for calculations, data organisation, and chart creation. Users can use these features to analyse sales records, although the analysis and interpretation still depend on how the spreadsheet is prepared and used.

Source: https://www.microsoft.com/en-us/microsoft-365/excel

These sources demonstrate existing approaches to business analysis. They do not independently confirm the specific difficulties experienced by the selected petrol station. The current reporting process and business needs should be confirmed when the available data is examined.

## 0.4 Existing Approaches

### 1. Business Intelligence Dashboards

**Example:** Microsoft Power BI  
**Source:** https://www.microsoft.com/en-us/power-platform/products/power-bi

Power BI supports interactive dashboards, data visualisation, and business reporting.

**Potential gap for this project:** The proposed system will focus on the specific sales segments of Mogas, Diesel, and Kedai Mesra PETRONAS and combine their analysis with revenue forecasting and evidence-based explanations.

### 2. Spreadsheet-Based Analysis

**Example:** Microsoft Excel  
**Source:** https://www.microsoft.com/en-us/microsoft-365/excel

Excel supports data organisation, calculations, comparisons, and charts.

**Potential gap for this project:** Repeated analysis may require users to prepare calculations and interpret the results manually. The proposed system aims to provide a more consistent workflow for sales analysis and interpretation.

### 3. Time-Series Forecasting

**Example:** Statistical forecasting methods, including exponential smoothing.  
**Source:** *Forecasting: Principles and Practice*  
https://otexts.com/fpp3/

Time-series forecasting methods use historical observations to estimate future values and evaluate forecasting errors.

**Potential gap for this project:** Forecasting alone does not provide a complete decision support workflow. This project combines forecasting with historical sales analysis, visualisation, and plain-language explanations.

## 0.5 Engineering Gap

Existing tools already support business reporting, spreadsheet analysis, and forecasting. This project focuses on integrating these capabilities into one workflow tailored to the available petrol station sales records.

The system will help users review sales performance across the three business segments, identify trends, assess future revenue estimates, and understand the results through explanations based on calculated evidence.

The exact engineering gap will be refined after the available dataset and current business reporting process have been examined. The project does not claim that these existing tools cannot perform similar functions.

## 0.6 Project Objectives

- **O1:** To analyse historical sales records and identify sales trends and key business indicators for Mogas, Diesel, and Kedai Mesra PETRONAS.
- **O2:** To develop and evaluate a sales revenue forecasting approach using historical data and compare its performance against a simple baseline.
- **O3:** To develop a dashboard with clear, evidence-based explanations that help users understand sales performance and support business planning.

## 0.7 Application Scope

### Intended Users

The intended users are the owner, manager, or authorised staff of the selected PETRONAS petrol station in Taman Yayasan, Segamat, Johor.

### Supported Tasks

The system is intended to support the following tasks:

1. Import and validate available historical sales records.
2. Calculate sales totals and key business indicators.
3. Compare sales performance across Mogas, Diesel, and Kedai Mesra PETRONAS.
4. Display sales trends using charts and summaries.
5. Forecast future sales revenue when sufficient suitable historical data is available.
6. Compare forecasting performance against a simple baseline.
7. Explain sales trends and forecasting results using available evidence.

### Information and Knowledge Domain

The system focuses on historical sales information, sales performance indicators, time-based sales trends, revenue forecasting, and business planning.

### Operating Context

The system is intended to operate as a decision support application for authorised users reviewing historical sales data. The initial version will use available records supplied with appropriate permission. The data format, update frequency, and level of detail are to be confirmed.

### Important Constraints

- The completeness and quality of historical sales records may limit the analysis.
- Forecasting depends on the amount and consistency of historical data.
- Revenue does not represent profit unless reliable cost and expense information is available.
- Confidential business information must be protected.
- Forecasts are estimates and may not reflect unexpected changes in business conditions.
- The system provides decision support and does not guarantee successful business decisions.

### Out-of-Scope Tasks

- Automatically changing fuel prices or business operations.
- Replacing existing accounting or point-of-sale systems.
- Predicting future sales with guaranteed accuracy.
- Calculating profit without reliable cost and expense data.
- Making business decisions without human review.
- Integrating live sales systems unless access and project requirements justify it.

## 0.8 Evaluation Focus

The evaluation will determine whether the system:

1. Calculates sales indicators correctly.
2. Handles invalid or incomplete sales records appropriately.
3. Produces useful revenue forecasts compared with a simple baseline.
4. Generates explanations supported by calculated results and available evidence.
5. Protects confidential business information.
6. Responds within a practical time for common analysis tasks.

The dataset must be inspected before finalising the forecasting approach and confirming the suitability of the proposed thresholds.

---

# Section 1 — Functional Requirements (FR)

Functional requirements describe what the system must do. Each requirement must be observable and testable.

| ID | Functional Requirement | Measurement Method | Metric | Initial Threshold |
|---|---|---|---|---|
| FR1 | The system shall import supported historical sales records containing the available sales dates, business segments, and sales values. | Test importing valid sample files and check whether records are loaded correctly. | Successful valid-file import rate | 100% of predefined valid-file test cases |
| FR2 | The system shall identify and report predefined data-quality issues, including missing dates, invalid sales values, duplicate records, and inconsistent formats where applicable. | Test records containing known data-quality issues and compare the results with expected validation outcomes. | Correct validation and handling rate | 100% of predefined data-quality test cases |
| FR3 | The system shall calculate sales totals and selected business indicators for Mogas, Diesel, and Kedai Mesra PETRONAS using the available records. | Compare the system's calculations against independently calculated expected values. | Calculation correctness rate | 100% of predefined valid-data calculation tests, allowing documented rounding differences |
| FR4 | The system shall generate future sales revenue forecasts when the available historical data is suitable for forecasting. | Evaluate forecasts against a held-out historical period and compare them with a simple baseline. | MAE and percentage improvement over baseline MAE | Target at least 5% lower MAE than the baseline, where meaningful and feasible |
| FR5 | The system shall provide plain-language explanations of sales trends and forecasting results based on available calculated values and evidence. | Check generated factual claims against the underlying calculations and sales records. | Evidence-supported factual claim rate | At least 95%; important numerical claims must match the underlying calculations |

**Notes:**

- The forecasting target is an initial goal, not a guarantee. If the data is insufficient or the forecasting approach does not outperform the baseline, the result and limitation must be reported honestly.
- The supported file formats and actual data fields will be confirmed after inspecting the dataset.

---

# Section 2 — Non-Functional Requirements (NFR)

Non-functional requirements describe how well the system should perform and how it should be maintained or used.

| ID | Quality Attribute | Requirement | Measurement Method | Metric | Initial Threshold |
|---|---|---|---|---|---|
| NFR1 | Performance | The system shall complete common sales summary and analysis queries within an acceptable response time under the documented test environment. | Measure response times across a representative set of test queries. | 95th-percentile response time (P95) | At most 3 seconds for common summary and analysis queries, excluding long-running forecasting jobs |
| NFR2 | Reliability | The system shall handle predefined invalid inputs and recoverable processing errors without an unhandled application crash. | Execute valid and invalid input tests and monitor application errors. | Test cases completed without an unhandled crash | 100% of predefined reliability test cases |
| NFR3 | Maintainability | The system shall allow sales analysis, forecasting, and explanation components to be tested and updated independently where their interfaces permit. | Review the component structure and perform a controlled component update. | Number of unrelated components requiring changes during the test | No unrelated component changes required for a routine isolated update |
| NFR4 | Usability | The system shall present key sales indicators, charts, and explanations in a form that intended users can understand. | Ask representative users to complete predefined tasks and provide feedback. | Task completion rate | At least 80% of test tasks completed successfully by participating users |

The proposed thresholds will be reviewed during implementation and testing. Usability results will depend on the number and characteristics of participating users.

---

# Section 3 — Responsible AI Requirements (RAI)

Responsible AI requirements define controls to reduce risks involving confidential data, unsupported explanations, and misleading forecasts.

| ID | Responsible AI Risk | Requirement | Measurement Method | Metric | Initial Threshold |
|---|---|---|---|---|---|
| RAI1 | Privacy and confidentiality | The system shall restrict access to confidential sales records to authorised users and shall not expose the records to unauthorised users or destinations. | Test access restrictions and inspect relevant data flows and outputs. | Access-control test pass rate; number of unauthorised disclosures observed | 100% of predefined access-control tests pass; zero unauthorised disclosures observed in testing |
| RAI2 | Unsupported AI-generated claims | The system shall base factual explanations on available calculated results and supporting sales evidence, and shall communicate when sufficient evidence is unavailable. | Review a test set of generated explanations and verify their factual claims against the underlying records. | Evidence-supported factual claim rate | At least 95% of factual claims are supported; important numerical claims must be correct |
| RAI3 | Misleading forecasts and automation risk | The system shall identify forecasts as estimates, communicate relevant limitations, and leave final business decisions to human users. | Test forecast displays and explanations, including cases with insufficient data or poor forecasting performance. | Correct forecast-label and limitation-disclosure rate; number of unauthorised automated business actions | 100% of predefined forecast-transparency tests pass; zero automated business actions |

## Reflection: Most Difficult Responsible AI Requirement

RAI2, which focuses on ensuring that AI-generated explanations are supported by evidence, may be the most difficult requirement to measure and enforce technically.

An explanation may sound reasonable while still making a claim that is not supported by the sales records. To evaluate this requirement, factual claims must be compared with the actual calculations and available evidence. Some business trends may also have several possible explanations, and the sales data alone may not establish the cause.

The system should therefore distinguish observed patterns from possible interpretations and avoid claiming that a particular factor caused a sales change unless sufficient evidence supports that conclusion.

---

## Requirement Review

Before implementation, the following checks should be completed:

- Confirm that all three project objectives are supported by relevant requirements.
- Inspect the available dataset and confirm its structure and quality.
- Confirm that each requirement has a measurable test method and initial threshold.
- Ensure the evaluation criteria use the same requirement IDs as this document.
- Review confidentiality, evidence-grounding, and forecast-transparency controls.
- Refine the requirements if the available data or implementation constraints make a target unsuitable.
