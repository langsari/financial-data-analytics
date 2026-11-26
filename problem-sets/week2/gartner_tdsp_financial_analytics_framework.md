# Reconstructed Financial Data Analytics Framework: Gartner Analytics Ascendancy Model + TDSP

## Overview

Combining **Gartner’s Analytics Ascendancy Model** (Descriptive, Diagnostic, Predictive, and Prescriptive analytics) with Microsoft’s **Team Data Science Process (TDSP)** establishes an end-to-end, value-driven architecture for financial data. In this reconstructed framework, TDSP provides the engineering and governance lifecycle while Gartner’s model defines the analytical maturity progression. Each stage is enhanced with an explicit **Input → Processing → Output (IPO)** structure so that the output of one phase seamlessly feeds the input of the next.

---

## Framework Process Map Diagram

~~~mermaid
flowchart LR
    subgraph S1["1. Descriptive Analytics (What Happened?)"]
        direction TB
        T1["TDSP: Business Understanding & Data Acquisition"]
        I1["INPUT: Raw ledgers, transactions, Basel III / IFRS 9 rules"]
        P1["PROCESSING: ETL/ELT pipelines, cleansing, KPI aggregation, EDA"]
        O1["OUTPUT: Validated data warehouse, P&L & baseline dashboards"]
        T1 --> I1 --> P1 --> O1
    end

    subgraph S2["2. Diagnostic Analytics (Why Did It Happen?)"]
        direction TB
        T2["TDSP: Data Understanding & Deep Analysis"]
        I2["INPUT: Clean data, flagged variances, macro & bureau feeds"]
        P2["PROCESSING: Drill-downs, correlation, variance & root-cause analysis"]
        O2["OUTPUT: Root-cause reports, forensic dashboards, risk drivers"]
        T2 --> I2 --> P2 --> O2
    end

    subgraph S3["3. Predictive Analytics (What Will Happen?)"]
        direction TB
        T3["TDSP: Feature Engineering & Modeling"]
        I3["INPUT: Enriched datasets, risk drivers, target variables"]
        P3["PROCESSING: Feature engineering, ML/econometric training, stress-testing"]
        O3["OUTPUT: Validated models, default/fraud forecasts, SHAP reports"]
        T3 --> I3 --> P3 --> O3
    end

    subgraph S4["4. Prescriptive Analytics (How Can We Make It Happen?)"]
        direction TB
        T4["TDSP: Deployment & Customer Acceptance"]
        I4["INPUT: Predictive scores, live streams, risk & optimization rules"]
        P4["PROCESSING: MLOps API deployment, decision engines, audit validation"]
        O4["OUTPUT: Automated financial actions, live APIs, audit & ROI sign-off"]
        T4 --> I4 --> P4 --> O4
    end

    O1 --> I2
    O2 --> I3
    O3 --> I4
    O4 -. "Continuous Feedback Loop: Realized Outcomes, Retraining & Regulatory Audit" .-> I1
~~~

---

## Stage-by-Stage IPO Breakdown

### 1. Descriptive Analytics (*"What happened?"*)
**Enhanced TDSP Phase:** *Business Understanding & Data Acquisition*

* **Input:**
  * Raw financial data sources: general ledgers, core banking transactions, SWIFT/payment logs, and historical financial statements.
  * Business objectives and regulatory frameworks (e.g., Basel III, IFRS 9, AML/KYC reporting mandates).
  * Historical KPI definitions and compliance thresholds.
* **Processing (TDSP Enhancement):**
  * Translate financial goals into measurable historical reporting questions and target schemas.
  * Execute automated ETL/ELT ingestion, currency/timezone normalization, deduplication, and data-quality validation.
  * Perform Exploratory Data Analysis (EDA) and baseline aggregations (P&L, cash flow, default rates, liquidity ratios).
* **Output:**
  * Validated, audit-ready financial data warehouse and Data Quality Report.
  * Baseline descriptive BI dashboards (balance sheets, historical revenue, delinquency trends).
  * Project Charter and flagged anomalies handed off to Stage 2.

---

### 2. Diagnostic Analytics (*"Why did it happen?"*)
**Enhanced TDSP Phase:** *Data Acquisition & Understanding (Deep Analysis)*

* **Input:**
  * Validated financial datasets and flagged variances/anomalies from Stage 1.
  * External contextual data: macroeconomic indicators (interest rates, inflation, GDP), credit bureau histories, and market feeds.
  * Domain hypotheses from risk, treasury, or audit teams.
* **Processing (TDSP Enhancement):**
  * Run multi-dimensional drill-downs, cohort segmentation, and statistical variance analysis.
  * Execute correlation, causality, and forensic pattern analysis to isolate drivers behind financial shifts (e.g., why SME loan defaults spiked in a specific region or sector).
  * Validate candidate explanatory variables and refine data definitions.
* **Output:**
  * Diagnostic root-cause investigation reports and interactive forensic dashboards.
  * Verified list of financial risk drivers and hypothesis logs.
  * Enriched, context-aware datasets ready for feature engineering in Stage 3.

---

### 3. Predictive Analytics (*"What will happen?"*)
**Enhanced TDSP Phase:** *Feature Engineering & Modeling*

* **Input:**
  * Enriched historical datasets and verified risk drivers from Stage 2.
  * Defined target variables (e.g., 12-month Probability of Default, fraud flag, cash-flow shortfall, customer churn).
  * Domain-specific feature specifications (e.g., debt-to-income ratios, rolling volatility, transaction velocity).
* **Processing (TDSP Enhancement):**
  * Engineer financial features and resolve class imbalance (e.g., rare fraud or default events).
  * Train, tune, and benchmark machine learning and econometric models (e.g., gradient boosting for credit scoring, time-series forecasting for liquidity, anomaly detection for AML).
  * Conduct out-of-time backtesting, cross-validation, macroeconomic stress-testing, and model explainability analysis.
* **Output:**
  * Validated predictive models with documented performance metrics (AUC-ROC, KS statistic, RMSE).
  * Forward-looking risk scores, default probabilities, and financial forecasts.
  * Explainability artifacts (e.g., SHAP values) and model risk validation packages for regulatory review.

---

### 4. Prescriptive Analytics (*"How can we make it happen?"*)
**Enhanced TDSP Phase:** *Deployment & Customer Acceptance*

* **Input:**
  * Validated predictive models and forward-looking scores from Stage 3.
  * Real-time financial transaction streams and live operational systems.
  * Institutional business rules, risk appetite thresholds, capital constraints, and optimization objectives.
* **Processing (TDSP Enhancement):**
  * Containerize and deploy models into production APIs or batch pipelines with CI/CD and MLOps drift monitoring.
  * Connect predictive outputs to optimization and automated decision engines (e.g., dynamic credit-limit adjustments, real-time fraud blocking, automated portfolio rebalancing).
  * Validate realized business ROI, conduct regulatory compliance audits, and route actual financial outcomes back into Stage 1 for continuous retraining.
* **Output:**
  * Live production scoring APIs and automated prescriptive financial actions (approve/decline, block, hedge, rebalance).
  * Signed-off Financial Governance, Compliance, and ROI Acceptance Reports.
  * Closed-loop feedback pipeline feeding realized outcomes back into Descriptive and Diagnostic monitoring.

---

## Quick-Reference IPO Matrix

| Gartner Stage | Enhanced TDSP Phase | Key Input | Core Processing | Primary Output |
| :--- | :--- | :--- | :--- | :--- |
| **1. Descriptive** | Business Understanding & Data Acquisition | Raw ledgers, transactions, Basel III / IFRS 9 rules | ETL, cleansing, KPI aggregation, EDA | Clean financial data, baseline P&L/KPI dashboards |
| **2. Diagnostic** | Data Understanding & Deep Analysis | Clean data, flagged variances, macro feeds | Drill-downs, correlation, root-cause & variance analysis | Root-cause reports, forensic dashboards, risk drivers |
| **3. Predictive** | Feature Engineering & Modeling | Enriched datasets, risk drivers, target variables | Feature engineering, ML/econometric training, stress-testing | Validated models, default/fraud forecasts, SHAP reports |
| **4. Prescriptive** | Deployment & Customer Acceptance | Predictive scores, live streams, risk rules | MLOps API deployment, optimization & decision engines | Automated financial actions, live APIs, audit & ROI sign-off |

---

## Continuous Feedback & Governance Loop

To maintain regulatory compliance and analytical accuracy in dynamic financial markets, realized outcomes from **Stage 4 (Prescriptive)**—such as actual default rates, prevented fraud losses, and portfolio returns—are continuously fed back into **Stage 1 (Descriptive)** and **Stage 2 (Diagnostic)**. This closes the TDSP lifecycle, enabling automated drift detection, model recalibration, and ongoing regulatory auditability.