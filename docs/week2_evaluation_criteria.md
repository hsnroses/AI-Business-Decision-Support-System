# Week 2: Evaluation Criteria — AI Business Decision Support System

## 1. Purpose

The purpose of this evaluation is to determine whether the AI Business Decision Support System can analyse sales data correctly, produce useful revenue forecasts, and explain business results clearly.

The evaluation criteria are linked to the project objectives and requirements. The thresholds below are initial targets and will be reviewed after the dataset and system capabilities are confirmed.

## 2. Evaluation Criteria Table

| Requirement ID / Objective | Evaluation Criterion | Capability Bucket | Measurement Method | Metric | Initial Threshold | Expected User / Business Outcome |
|---|---|---|---|---|---|---|
| FR3 / O1 | Correctness of sales calculations | Domain-specific capability | Compare system-generated sales totals and key indicators against independently calculated results from a test dataset. | Calculation correctness rate | 100% for predefined test cases with valid input data | Users can trust the reported sales totals and indicators. |
| FR4 / O2 | Revenue forecasting performance | Domain-specific capability | Evaluate forecasts on a held-out historical test period and compare them with a simple baseline, such as the previous period's sales value. | Mean Absolute Error (MAE) and percentage improvement over baseline MAE | Target at least 5% lower MAE than the baseline, if the data supports meaningful forecasting | Users receive forecasts that provide measurable value beyond a simple baseline. |
| FR5 / O3 | Accuracy and evidence support of AI-generated explanations | Generation capability | Prepare test questions about known sales trends and compare generated explanations with independently verified calculations and source data. | Evidence-supported claim rate | At least 95% of factual claims are supported by the available evidence | Users can understand sales changes without being misled by unsupported explanations. |
| FR2 / O1 | Handling of missing or invalid sales records | Domain-specific capability | Test the system with records containing missing dates, invalid sales values, duplicates, and inconsistent formats. | Correct validation and handling rate | 100% of predefined invalid-data test cases are handled according to the documented validation rules | Users are informed about data quality issues before relying on the analysis. |
| RAI1 / O3 | Protection of confidential business data | Instruction-following capability | Review access-control behaviour and inspect data flows to check that unauthorised users cannot access restricted sales records. | Successful access-control test rate; number of unauthorised disclosures | 100% of predefined access-control tests pass; zero unauthorised disclosures in testing | The business can use its sales information with appropriate confidentiality controls. |
| NFR1 / O3 | Response time for common dashboard operations | Cost and latency | Measure the time required to load sales summaries and return answers for a defined set of representative test queries. | 95th-percentile response time (P95) | At most 3 seconds for common sales summaries and analysis queries, excluding long-running forecasting jobs | Users can explore business performance without excessive waiting. |

## 3. Evaluation Details

### EC1: Sales Calculation Correctness

The system will be tested using a small dataset with known sales values. Expected totals and indicators will be calculated independently and compared with the system's results.

**Metric:**

Calculation correctness rate = Number of correct predefined calculations / Total predefined calculations × 100%

**Target:** 100% of predefined calculations must match the expected results, allowing only documented rounding differences.

### EC2: Revenue Forecasting Performance

The dataset will be divided chronologically into training and test periods to avoid using future information when building forecasts. The forecasting approach will be compared against a simple baseline on the same test period.

**Metric 1 — Mean Absolute Error (MAE):**

MAE measures the average absolute difference between actual and predicted sales values.

**Metric 2 — Improvement over baseline:**

Improvement (%) = (Baseline MAE − Model MAE) / Baseline MAE × 100%

**Target:** Aim for at least 5% lower MAE than the baseline. If the baseline MAE is zero, percentage improvement will not be used. If the dataset is insufficient or the forecasting approach does not outperform the baseline, the limitation will be documented rather than claiming that the forecast is better.

### EC3: Explanation Quality and Evidence Support

A set of test questions will be prepared using known sales results. Each factual claim in the generated explanations will be checked against the calculated indicators or available sales records.

**Metric:**

Evidence-supported claim rate = Number of factual claims supported by evidence / Total factual claims evaluated × 100%

**Target:** At least 95% of factual claims must be supported by the available evidence. Important numerical claims must match the underlying calculations.

### EC4: Data Validation

Test records will be created to represent common data-quality issues, including missing dates, invalid numerical values, duplicate records, and inconsistent formats.

**Metric:** Percentage of predefined invalid-data test cases handled according to the validation rules.

**Target:** 100% of the predefined test cases must be handled correctly. This does not mean that every real-world data issue will automatically be detected.

### EC5: Confidentiality and Access Control

Testing will check whether access restrictions work as intended and whether confidential sales records are exposed to unauthorised users or destinations.

**Metric:** Access-control test pass rate and number of unauthorised disclosures observed during testing.

**Target:** All predefined access-control tests must pass, with zero unauthorised disclosures observed during testing.

### EC6: Response Time

Response times will be measured using representative sales-analysis queries and dashboard operations under a documented test environment.

**Metric:** 95th-percentile response time (P95), which indicates the time within which 95% of measured requests complete.

**Target:** P95 of no more than 3 seconds for common summaries and analysis queries. Forecasting jobs will be measured separately because their processing time may be different.

## 4. Evaluation Limitations

The evaluation depends on the quality, completeness, and duration of the available sales records. Forecasting may not be meaningful if the dataset contains insufficient historical observations or inconsistent time periods.

The proposed thresholds are initial engineering targets, not achieved results. They may be revised after inspecting the dataset, defining the test cases, and measuring the performance of the initial system.

Revenue forecasts will be evaluated as estimates of sales revenue, not profit. Profit analysis requires reliable cost and expense information.

## 5. Reflection

The most important evaluation criterion is revenue forecasting performance compared with a simple baseline. This is important because one of the main goals of the system is to help the business estimate future sales and plan its activities.

If the forecasting approach cannot provide better or otherwise useful results than a simple baseline, it may not provide enough value to justify its additional complexity. However, forecasting accuracy alone is not sufficient. The system must also calculate sales correctly, protect confidential information, and provide explanations that users can verify.
