# 🌍 Global EV Market Intelligence Dashboard

## 📌 Project Overview
This end-to-end Business Intelligence project analyzes the global Electric Vehicle (EV) market from 2015 to 2025. It transforms raw multi-source data into a strategic tool for executives to track revenue trends, regional performance, and individual model specifications.

---

## 🏗️ Data Architecture: The Star Schema
To ensure high performance and scalability, I implemented a **Star Schema** model:
* **Fact Table:** `Sales` (containing transactional data, revenue, and CO2 metrics).
* **Dimension Tables:** `Region` (Geographic hierarchy) and `Model` (Technical specs like Range, Battery, and Segment).
* **Date Dimension:** A custom DAX-generated `Calendar` table to enable seamless Time-Intelligence.

---

## 🧠 Advanced DAX Implementation
I moved beyond standard aggregations to create complex logic for business growth analysis:

* **Time Intelligence (YoY Analysis):** Calculated using `SAMEPERIODLASTYEAR` to compare current performance against the previous year.
* **Safe Division:** Utilized the `DIVIDE` function to calculate Growth % without encountering "Infinity" errors during data gaps.
* **Granularity Control:** Engineered measures to aggregate Average Price and Total Deliveries correctly at the model level.

---

## 📊 Dashboard Deep-Dive
### 1. Executive Summary
* **KPI Banner:** Real-time tracking of Revenue, YoY Growth, and Sustainability impact (CO2 Saved).
* **Grid Layout:** Optimized visual hierarchy featuring a Global Heatmap and a 10-year Revenue Trend chart.
* **Edit Interactions:** Configured the report so that the Year Slicer filters KPIs while the Line Chart maintains an "All-Time" historical view (2015-2025).

### 2. Regional Deep-Dive (Drill-Through)
* **Operational Detail:** Right-click functionality allows users to jump from a map bubble to a specific regional breakdown.
* **Consumer Preferences:** Donut charts visualizing the market share of AWD vs RWD vehicles by region.

### 3. Model Performance Tracker
* **Micro-Analysis:** A dedicated page to analyze individual car models (e.g., Tesla Model Y, Audi Q8 e-tron).
* **Technical Specs:** Dynamic cards showing Battery capacity (kWh) and Range (km) for the selected vehicle.

---

## 🛠️ Tech Stack
* **Power BI Desktop:** Modeling, DAX and Visualization.
* **Power Query (M):** ETL and data cleaning.
* **GitHub:** Version control and documentation.

---
*Developed by Tejvarun Kattola*
