
# Car-sale-analysis
# Tata Car Sales Analysis

![Pivot Table](https://img.shields.io/badge/Pivot%20Table-4CAF50?style=for-the-badge&logo=microsoftexcel&logoColor=white)
![Charts](https://img.shields.io/badge/Charts-2196F3?style=for-the-badge&logo=googlecharts&logoColor=white)
![Bar Graph](https://img.shields.io/badge/Bar%20Graph-FF9800?style=for-the-badge&logo=chartdotjs&logoColor=white)
![Dashboard](https://img.shields.io/badge/Dashboard-9C27B0?style=for-the-badge&logo=dashlane&logoColor=white)
![Data Collection](https://img.shields.io/badge/Data%20Collection-009688?style=for-the-badge&logo=databricks&logoColor=white)
![Data Validation](https://img.shields.io/badge/Data%20Validation-F44336?style=for-the-badge&logo=checkmarx&logoColor=white)
![Conditional Formatting](https://img.shields.io/badge/Conditional%20Formatting-3F51B5?style=for-the-badge&logo=formstack&logoColor=white)

An Excel-based sales analytics workbook for Tata Motors vehicle sales, featuring an interactive dashboard, pivot tables, and city/model-level breakdowns built from a 51-record transaction dataset.

## Overview

This workbook tracks car sales across Tata's model lineup, capturing product cost, taxes, delivery cost, final on-road price, delivery status, and city category (Metro / Tier 1 / Tier 2) for each unit sold. It rolls the raw transaction log up into a dashboard and a set of pivot-table analyses for quick business insights.

---

## Dashboard Preview

**KPI Tracker — model selector, revenue, cost, and P&L summary**

![TATA Sales Revenue Dashboard with KPI Tracker]<img width="1841" height="657" alt="dashboard-charts" src="https://github.com/user-attachments/assets/99709702-41ed-4a1d-9d39-b91d7924d5d9" />

**Revenue by City Category & Model-wise Sales Breakdown**

![Dashboard charts — revenue by city and model]<img width="1840" height="543" alt="model-sale-report" src="https://github.com/user-attachments/assets/1413cb4c-318d-4784-83a2-2e776bf04678" />

**Model-wise Sale Report & Product Cost vs. Tax/Delivery Cost**

![Model wise sale report and product cost chart]<img width="1871" height="549" alt="city-sale-insights" src="https://github.com/user-attachments/assets/76ea8e91-70af-49e2-83c3-d4b23a72c1d2" />

**City-wise Sale Report, Sale Insights & Delivery Status by Model**

![City wise sale report and sale insights]<img width="1869" height="686" alt="dashboard-overview" src="https://github.com/user-attachments/assets/f89eab6a-14aa-46b9-a666-882b614e1a10" />

---

## Workbook Structure

| Sheet | Description |
|---|---|
| `Data_Sheet` | Raw transaction log — one row per unit (Product ID, city category, batch, model, delivery status, cost, tax & delivery cost, final cost, on-road price) |
| `Dashboard` | Interactive summary — model selector with units sold, revenue, avg. sale price, cost, and P&L totals |
| `Sale_analysis` | Count of units by product status (e.g. In Transit) |
| `City_category` | Pivot: product cost by model, broken down by city category |
| `Model wise Analysis` | Delivered / Pending / In Transit counts per model |
| `city_wise_analysis` | Cars sold, total sales, and average sale price by city category |
| `Delivered pivot` | Count of delivered units per model |
| `Sale_Report_Delivered` | Filtered report of delivered units, plus a cars-sold-by-city summary |
| `Sheet1` | Product cost and tax/delivery cost summary by model |

## Key Fields (Data_Sheet)

| Column | Description |
|---|---|
| SL No. | Row/serial number |
| Product_ID | Unique unit identifier (e.g. `TATA001`) |
| City_Category | `Metro`, `Tier 1`, or `Tier 2` |
| Batch | Sales batch code |
| Model Name | Tata model (Nexon, Punch, Tiago, Harrier, Safari, Altroz, Tigor, Curvv, and EV variants) |
| Delivery Status | `Delivered`, `Pending`, or `In Transit` |
| Product Cost | Base cost of the vehicle |
| Taxation & Delivery Cost | Combined tax + delivery charges |
| Final Cost | Product Cost + Taxation & Delivery Cost |
| On Road Price | Final price charged to the customer |

## Highlights

- **51 units** tracked across **12 models**, spanning ICE and EV variants
- **35 Delivered · 8 Pending · 7 In Transit** at time of snapshot
- City-category segmentation (Metro / Tier 1 / Tier 2) for cost and volume comparisons
- Dashboard supports selecting an individual model to view its units sold, revenue, average sale price, and cost breakdown
- Rolled-up totals for revenue, cost, and realised / unrealised / estimated P&L
- Quick-glance KPI cards: delivery success rate, pending order value, most sold model, best-performing batch, highest tax & delivery cost, and most cost-efficient model

## Built With

- Microsoft Excel (pivot tables, dashboard, data validation, conditional formatting)

## Getting Started

1. Clone or download this repository
2. Open `car_sale_final.xlsx` in Excel (2016+ recommended for full pivot/slicer support)
3. Use the **Dashboard** sheet's model dropdown to explore per-model metrics
4. Refresh pivot tables (`Data > Refresh All`) after editing `Data_Sheet` to keep downstream sheets in sync

## Notes

- All cost figures are in the workbook's base currency (no explicit currency symbol set in the source data — confirm before publishing externally)
- Some legacy summary text is present at the bottom of `Data_Sheet`; the core transaction log is rows 2–52
