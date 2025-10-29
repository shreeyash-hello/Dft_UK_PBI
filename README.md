# 🚗 Regional Vehicle Growth & Infrastructure Demand Dashboard

## 📘 Project Overview
This Power BI project analyses **UK Department for Transport (DfT) vehicle licensing data** to uncover how vehicle ownership and composition vary across regions and over time.  
The goal is to help **transport planners, local councils, and policymakers** make informed decisions about **road infrastructure, and parking capacity** based on regional vehicle growth patterns.

---

## 🎯 Objective
Vehicle growth rates differ widely between UK regions — yet infrastructure investments are often distributed uniformly.  
This dashboard enables stakeholders to:
- Identify regions with **the highest number of licensed vehicles**
- Compare **growth trends by region and body type**
- Forecast **future infrastructure and transport demands**
- Support **data-driven planning** for sustainability and EV rollout

---

## 🧾 Data Source
- **Dataset:** [DfT VEH1104 — Licensed vehicles by body type and region](https://www.gov.uk/government/statistical-data-sets/veh01-vehicles-registered-for-the-first-time)
- **Publisher:** UK Department for Transport (DfT)
- **Time Period:** 1994–2025 (Quarterly updates)

---

## 🧹 Data Preparation & Modelling
Data transformation was performed in **Power Query** and the data model was built within **Power BI**.

### Data Cleaning
- Removed multi-level headers and standardised column names.
- Unpivoted wide regional data into a long format (`Date`, `Region`, `BodyType`, `Vehicle_Count`).
- Converted `Vehicle_Count` to numeric and standardised into millions.
- Extracted the `Year` field from `Date` for time-based analysis.
- Removed irrelevant or missing regions such as “Between Keepers” and “Unknown”.

### Data Model
- Built a simple **star schema**:
  - **Fact Table:** Vehicle counts by `Region`, `BodyType`, and `Date`
  - **Dimension Tables:** Date (calendar), Region, BodyType
- Relationships created to support time-series analysis and filtering.

### Tools Used
- **Microsoft Power BI Desktop** — Data cleaning, modelling, and visualization  
- **Power Query Editor** — Data transformation  
- **Excel (.xlsx)** — Original dataset format  

---

## 📊 Dashboard Summary

The dashboard is divided into **three interactive pages**, each designed to answer specific business questions and provide actionable insights.

---

### 🟦 PAGE 1 — Overview Dashboard
**Purpose:**  
Provide a national-level snapshot of total licensed vehicles and composition by vehicle type.

**Visuals:**
- **KPI Card:** Displays total licensed vehicles in the UK (42.26 million as of Q2 2025)
- **Bar Chart:** Shows vehicle count by country (England, Scotland, Wales, Northern Ireland)
- **Donut Chart:** Displays the composition of vehicle types (Cars, Vans, Motorcycles, etc.)
- **Slicers:** For `BodyType` and `Date` to adjust focus dynamically

**Insights:**
- The UK has **42.26 million licensed vehicles**, with **England** holding the majority share.  
- **Cars** dominate the total fleet (~83%), while **light goods vehicles (vans)** have seen strong growth due to e-commerce expansion.  
- **Motorcycles** and **buses** make up a small but consistent portion of the fleet.  

**Business Relevance:**
- Indicates where to prioritize **EV charger installations** and **road maintenance investments**.  
- Highlights the growing importance of **van infrastructure** in delivery-heavy regions.

---

### 🟩 PAGE 2 — Regional Trends
**Purpose:**  
Explore regional vehicle growth patterns and understand which areas have seen the largest increases over time.

**Visuals:**
- **Clustered Bar Chart:** Total vehicles by region (latest year)
- **Interactive Line Chart:** Shows vehicle growth trends over time by body type
- Clicking a region in the bar chart filters the line chart to that region’s data
- **Slicers:** Optional filters for year and body type

**Insights:**
- **South East England** leads in total licensed vehicles, followed by the **North West** and **East** regions.  
- Vehicle growth has been **consistent since 2010**, especially in **light goods vehicles (vans)**, reflecting commercial growth.  
- **London** shows slower growth due to congestion charges and public transport usage.  
- **Rural regions** (like the South West) maintain higher motorcycle usage.

**Business Relevance:**
- Helps transport planners forecast future road usage and **allocate maintenance budgets efficiently**.  
- Identifies **fast-growing areas** that may require **additional EV infrastructure and parking facilities**.

---

### 🟨 PAGE 3 — Vehicle Type Insights
**Purpose:**  
Dive deeper into specific body types (e.g., cars, vans, motorcycles) and their distribution across regions and years.

**Visuals:**
- **Slicers:** For `BodyType` and `Year`
- **Dynamic Title:** Updates automatically to show the selected vehicle type
- **Pie Chart:** Displays the regional share of the selected vehicle type

**Insights:**
- **Light goods vehicles** (vans) have grown the fastest since 2010, especially in the **South East** and **East Midlands**, indicating the logistics and delivery industry’s rise.  
- **Motorcycles** are more common in the **South West** and **rural regions**, possibly due to accessibility and tourism.  
- **Buses and coaches** show a declining trend across most regions, reflecting lower public transport reliance post-pandemic.

**Business Relevance:**
- Supports **policy design** for sustainable mobility and EV conversion strategies.  
- Informs local councils on **vehicle-type-specific demand** for parking and road infrastructure.  
- Highlights potential areas to **promote EV adoption** in commercial fleets.

---

## 📈 Key Takeaways
- Total UK vehicles: **42.26 million (as of 2025 Q2)**  
- **Cars** remain dominant, but **light goods vehicles** are growing fastest.  
- **South East England** and **North West** regions lead in total counts and growth.  
- **London**’s slower growth reflects the shift toward public transport and low-emission zones.  
- Insights can directly inform **road planning**, and **budget allocation**.

---

## 🚀 Future Improvements
- Add **forecasting models** (ARIMA or Prophet) for vehicle growth projections.  
- Include **CO₂ emissions estimates** to support sustainability planning.  
- Automate dataset refresh using Power BI Service and scheduled updates.


## 🛠️ Tools & Technologies
| Tool | Purpose |
|------|----------|
| **Power BI Desktop** | Data visualization and analysis |
| **Power Query Editor** | Data transformation |
| **Microsoft Excel (.xlsx)** | Source dataset |
| **DAX** | Measures and KPIs |
| **Power BI Interactivity** | Cross-filtering and slicer-driven insights |

---

## 🧩 Business Impact
This dashboard provides valuable insights to:
- **Local councils** for road and parking capacity planning  
- **Logistics companies** to assess vehicle density and delivery potential  
- **Sustainability teams** for monitoring transportation trends

📊 **Result:**  
A dynamic, interactive Power BI dashboard that simplifies complex vehicle registration data into clear, actionable insights for policy and infrastructure planning across the UK.
