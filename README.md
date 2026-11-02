# SQL FMCG Commercial Performance & Trade Channel Dashboard

## Overview
An executive-grade commercial performance dashboard built in Power BI Desktop and connected to a local MySQL relational database. The report evaluates revenue, cost structure, gross profit margins, and distribution channel splits.

* **Live Interactive Report:** [View on Power BI Service](PASTE_YOUR_POWER_BI_URL_HERE)

---

## Data Model & Architecture
* **Star Schema Architecture:** Formed by connecting `fact_sales` with dimension tables (`dim_products`, `dim_channels`) via an ODBC MySQL driver connection.
* **Core DAX Measures:**
  * `Total Revenue = SUM(fact_sales[revenue])`
  * `Total Cost = SUM(fact_sales[cost])`
  * `Gross Profit = [Total Revenue] - [Total Cost]`
  * `Gross Margin % = DIVIDE([Gross Profit], [Total Revenue], 0)`

---

## Key Business Insights
* **Revenue Drivers:** Wholesale Distribution and Modern Trade account for the largest revenue shares across product categories.
* **Margin Health:** Gross Margin stands strong at **44.51%** with **₹195.70K** total revenue generated during the analyzed period.

---

## Project Setup & Files
* `SQL FMCG Commercial Performance & Trade Channel Dashboard.pbix` — Power BI Desktop source file.
