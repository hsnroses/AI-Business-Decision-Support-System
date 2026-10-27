# AI Business Decision Support System — Week 2: Architecture Decisions

## 1. Architecture Overview

The AI Business Decision Support System is designed to help users understand sales performance at a PETRONAS petrol station in Taman Yayasan, Segamat, Johor.

The system processes historical sales data from three business segments: Mogas, Diesel, and Kedai Mesra PETRONAS. It validates the available records, analyses sales trends and key business indicators, and forecasts future sales revenue if the dataset contains sufficient suitable historical information.

The results are presented through a dashboard containing summaries, charts, and relevant business indicators. An AI explanation component helps users understand the results in simple language. Its explanations should be based on calculated values and available evidence rather than unsupported assumptions.

The initial architecture focuses on the main system capabilities without committing to specific technologies or models before the requirements and dataset have been fully examined.

## 2. Architecture Decision Records (ADRs)

| ADR ID | Decision | Reason | Trade-off / Limitation |
|---|---|---|---|
| ADR1 | Use historical sales records from Mogas, Diesel, and Kedai Mesra PETRONAS as the primary data source. | The system needs actual business data to analyse sales performance and identify trends. | Data quality, completeness, and availability may limit the analysis. The data structure must be confirmed before implementation. |
| ADR2 | Separate data validation, sales analysis, forecasting, and explanation into distinct components. | Each component has a clear responsibility, making the system easier to test, maintain, and improve. | A modular design requires additional work to define how the components exchange data. |
| ADR3 | Compare the forecasting approach against a simple baseline before presenting its results as useful predictions. | This helps determine whether the forecasting approach provides value beyond a basic prediction method. | Forecasting may not be reliable if the dataset is too small, inconsistent, or affected by changing business conditions. |
| ADR4 | Generate business explanations using calculated results and supporting evidence. | Users should be able to understand why sales changed without relying on unsupported AI-generated claims. | Explanations depend on the accuracy of the calculations and the information available to the system. |
| ADR5 | Present findings through a dashboard while keeping business decisions under human control. | Users can review sales indicators and forecasts before deciding on business actions. | The dashboard provides decision support but cannot guarantee that the resulting business decisions will be successful. |

## 3. Requirements Traceability Matrix

| Objective / Requirement | Evaluation Criteria | Architecture Component | Evidence of Implementation |
|---|---|---|---|
| O1: Analyse historical sales records and identify trends and key business indicators. | EC1: Data processing and sales calculation correctness. | Data Input, Data Validation, and Sales Analysis | Test results show that sales totals and selected indicators match independently calculated values. |
| O2 / FR4: Develop and evaluate a sales revenue forecasting approach. | EC2: Forecasting error compared with a simple baseline. | Forecasting Component and Evaluation Process | Evaluation results report suitable forecasting metrics and baseline comparisons using held-out historical data. |
| O3 / FR5: Present clear, evidence-based explanations of business results. | EC3: Explanation accuracy and evidence support. | AI Explanation Component and Evidence Retrieval | Tested explanations agree with the relevant calculations and do not introduce unsupported numerical claims. |
| FR1 / FR2: Import and validate available historical sales records. | EC1: Data validation effectiveness. | Data Input and Data Validation | Tests identify invalid records and handle missing or inconsistent values according to defined rules. |
| NFR1: Complete common analysis and dashboard operations within a practical response time. | EC4: Response time. | Analysis, Forecasting, and Dashboard Components | Response times are recorded for a defined set of representative operations. |
| RAI1 / RAI2: Protect confidential sales data and ensure explanations are supported by evidence. | EC3 and EC5: Explanation grounding and data protection. | Data Access Controls and AI Explanation Component | Access checks and explanation tests provide evidence that the defined controls are working. |

## 4. Design Considerations and Limitations

The initial architecture focuses on the essential capabilities required for sales analysis, forecasting, and business decision support. It avoids choosing a specific programming framework, forecasting model, database, or language model before the dataset and requirements are confirmed.

The system depends on the availability and quality of historical sales records. Missing dates, inconsistent records, or insufficient historical information may affect the accuracy of the analysis and forecasting results.

Forecasts will be evaluated against a simple baseline using historical data that was not used to fit the forecasting approach. If the forecasting approach does not provide useful results, the system should communicate the limitation rather than present the forecasts as reliable predictions.

AI-generated explanations must be supported by calculated results and relevant evidence. The system should distinguish observed historical performance from estimated future performance. Revenue analysis must not be described as profit analysis unless reliable cost and expense data are also available.

The architecture may be refined after implementation and testing. Any additional components should be justified by specific requirements, evaluation findings, or technical constraints.

## 5. Reflection

The most important trade-off is between providing useful AI-generated explanations and ensuring that the explanations remain accurate and evidence-based.

A general-purpose AI model may produce explanations that sound convincing but are not supported by the sales records. To reduce this risk, the architecture separates numerical analysis from explanation generation and requires explanations to use the calculated results as evidence.

This approach may limit the range of questions the assistant can answer, but it improves the ability to verify its explanations and makes the system more suitable for supporting business decisions.
