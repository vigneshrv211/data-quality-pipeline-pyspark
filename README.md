Data Quality Monitoring Pipeline (PySpark)
🔍 Overview

End-to-end data quality monitoring system built using PySpark and a Bronze–Silver–Gold architecture.
This project validates data, detects issues, and provides a Power BI dashboard to monitor data health and quality score.

🏗️ Architecture
📥 Bronze Layer (Raw Data)
        ↓
🧹 Silver Layer (Data Quality Checks)
        ↓
📊 Gold Layer (Aggregated Metrics)
        ↓
📈 Power BI Dashboard
⚙️ Tech Stack
PySpark – Data processing & transformations
Python – Validation logic
Delta Lake / Data Lake – Layered architecture
Power BI – Dashboard & visualization
📁 Project Structure
📁 notebooks/
   ├── 01_Bronze_Raw_Ingestion.ipynb
   ├── 02_Silver_Quality_Checks.ipynb
   ├── 03_Gold_Metrics_Table.ipynb

📁 dashboard/
   ├── dashboard.png
✅ Data Quality Checks Implemented
Check Type	Description
NULL_CHECK	Detect missing values
DUPLICATE_CHECK	Identify duplicate records
STRING_LENGTH_CHECK	Validate min/max length
FUTURE_DATE	Detect invalid future dates
INVALID_STATUS	Validate categorical values
NEGATIVE_VALUE	Detect incorrect negative values
REFERENTIAL_INTEGRITY	Foreign key validation
⚡ Workflow
🟤 Bronze Layer – Raw Ingestion
Load raw dataset into data lake
No transformations applied
⚪ Silver Layer – Data Quality Checks
Apply validation rules on each column
Generate:
Issue Count
Issue %
Severity
🟡 Gold Layer – Metrics Table
Aggregate all results
Compute:
Table-level quality score
Issue distribution
Severity classification
📊 Dashboard Features
📌 Tables Monitored
📌 Total Rows Processed
📌 Total Issues Found
📌 Overall Quality Score
📈 Visual Insights
Quality Score by Table
Issue Count by Check Type
Column-level issue breakdown
📊 Sample Output
Tables monitored: 6
Rows processed: 291K
Issues found: 24K
Quality score: 92.95%
📌 Severity Logic
Issue %	Severity
0–5%	Low
5–20%	Medium
>20%	High
📷 Dashboard Preview

(Upload your image and keep this line)

<img width="1323" height="742" alt="image" src="https://github.com/user-attachments/assets/d73fb34b-ce73-493a-b9d8-3ba490b7415c" />
