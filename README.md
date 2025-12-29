# Manufacturing-Data-Integration-AI-Literacy-Program
Integrated procurement, shipment, forecasting, and stock data into analysis-ready tables for AI readiness in a manufacturing environment. Built a material forecasting view linking Finished Goods part numbers to Material Codes via BoM, enabling automated stock status and recommendations.

**Note (Confidentiality):** This repository uses **mock data** to demonstrate the structure and logic. The original project was built for a manufacturing company and is confidential.
---

## Overview
Manufacturing operations often rely on multiple Excel files with different formats across procurement, logistics, and planning. This fragmentation reduces visibility and slows decision-making, increasing the risk of **overstock** (cash tied up in inventory) and **shortages** (delayed production and delivery). The case study demonstrates how Excel-based integration and automation can improve data readiness and enable AI-supported workflows.

---
## Results 
- **201 operational files consolidated** into a structured monitoring workbook 
- **AI literacy improved by +1.34** average score (pre–post assessment)
- **Program satisfaction: 4.93/5** average scor
- Reporting and reconciliation processes that previously took **hours** could be reduced to **minutes** after integration (qualitative outcome from implementation).

---
## What This System Does
### Inputs
- Forecast data (material-level demand)
- Procurement order reference
- ETA / shipment tracking
- Delivery actuals
- Stock snapshot (inventory)
- BoM mapping (Finished Goods Part Number → Material Code)

### Outputs
- **Balance** (available stock vs requirement)
- **Stock Ratio** (coverage ratio)
- **Status:** Leaking / Overstock / OK
- **Issue** and **Recommendation** to support procurement and planning actions
---

## Excel Sheet Map (Public Replica)
`Data Mockup FIX.xlsx` contains the mock input tables:
- `Mock_Forecast`
- `Procurement_Order`
- `ETA_Material`
- `BoM`
---

## Methodology (Aligned with the Case Study)
This project follows the integration approach described in the case study: **data input → data cleaning → data integration → analysis & automation**.

### 1) Data Input
Operational datasets were collected from multiple sources, including procurement orders, ETA tracking, forecasting, stock snapshots, and delivery actuals. The implementation consolidated inputs from many Excel files into a structured dataset for analysis.

### 2) Data Cleaning
Before integration, data was standardized to ensure consistency across files:
- Normalized material identifiers and text formats
- Standardized date formats
- Removed duplicates and handled missing values
- Aligned quantity units to avoid inconsistent calculations

### 3) Data Integration
The system links tables using material-level keys and BoM mapping:
- Connected procurement, ETA/shipment, and delivery data to each material code
- Added linkage between **Finished Goods Part Number** and **Material Code** using **BoM**
- Produced a unified base table enabling complete visibility (PO → delivery → stock → forecast)

### 4) Analysis & Automation (Excel-based)
The workbook calculates key indicators and produces automated output fields:
- **Balance** and **Stock Ratio** calculations
- Automated **Status** assignment (Leaking / Overstock / OK)
- Generated **Issue** and **Recommendation** fields to support decision-making

The implementation uses Excel formulas and logic functions such as:
`SUMIF`, `COUNTIF`, `IF`, `VLOOKUP`, `INDEX-MATCH`, `IFERROR`, and logical operators.

---
## Logic Rules (Simplified)
- **Leaking:** Balance < 0  
- **Overstock:** Stock Ratio > threshold  
- **OK:** within acceptable range  

> Threshold values are configurable and were company-defined in the original implementation
---

## Disclaimer
This repository is a **public replica** created for portfolio purposes. It contains **no proprietary company data**. Any resemblance to real operational datasets is coincidental.
