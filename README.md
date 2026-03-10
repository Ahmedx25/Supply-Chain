# 🚚 Logistics & Supply Chain Operations Dashboard

## 📌 Project Overview
This project is a comprehensive data analysis and visualization of a logistics network in Southern California. The goal is to help Operations Managers monitor service reliability, cost efficiency, and operational risk over a 3-year period (Jan 2021 – Jan 2024). 

By analyzing over **27,000 hourly records**, this project uncovers critical operational bottlenecks and provides actionable insights to reduce late deliveries and minimize cargo damage.

## 🛠️ Technical Stack
* **Tool:** Advanced Microsoft Excel
* **ETL & Data Cleaning:** Power Query (M Code)
* **Data Modeling:** Excel Data Model & Pivot Tables
* **Visualization:** Pivot Charts, Conditional Formatting (Heatmaps), Dynamic Slicers

## 📊 Dashboard Preview
*(Insert a high-quality screenshot of your dashboard here)*
![Dashboard Preview]() 

## 🔍 The Business Problem & Key Findings
The supply chain was experiencing severe inefficiencies. Through deep-dive analysis, the following root causes were identified:

1. **The Core Bottleneck (Equipment Shortage):**
   * **Finding:** Handling equipment availability at warehouses was shockingly low at **27.7%**.
   * **Impact:** This caused significant loading/unloading delays (averaging 2.3 hours), triggering a ripple effect across the entire network.

2. **Service Reliability Failure:**
   * **Finding:** The network suffered an **82.2% Late Delivery Rate**.
   * **Impact:** Average ETA variation was +2.9 hours, indicating that current predictive planning models are unrealistic.

3. **High Cargo Damage:**
   * **Finding:** Only **27.1%** of cargo arrived in good condition. 
   * **Impact:** Massive financial loss due to damaged goods, heavily correlated with poor handling rather than just weather or traffic.

4. **Risk Heatmap Analysis:**
   * Identified specific days and hours where "Delay Probability" peaks, allowing for targeted operational interventions.

## ⚙️ Methodology & ETL Process (Power Query)
To ensure data accuracy and dynamic reporting, the following transformations were applied using Power Query:
* **Date Filtering:** Established a strict analysis window (Jan 1, 2021 - Jan 31, 2024) using a parameter table.
* **Feature Engineering:** Extracted `Year`, `Month`, `Day Name`, and `Hour` from raw timestamps for granular time-series analysis.
* **Geospatial Bucketing:** Rounded GPS coordinates (`vehicle_gps_latitude`, `vehicle_gps_longitude`) to create anonymized `Geo_Zone` clusters.
* **Risk Categorization:** Built conditional logic to create operational bands (e.g., Traffic_Band, RouteRisk_Band) and binary flags for critical KPIs (`Late_Flag`, `Cargo_Good_Flag`).

## 💡 Strategic Recommendations
1. **Urgent Warehouse Maintenance:** Prioritize equipment repair and leasing to increase availability from 27% to at least 80%, instantly reducing loading times.
2. **Buffer ETA Models:** Temporarily add a 3-hour buffer to customer delivery promises until operational bottlenecks are resolved.
3. **Handling Protocols Review:** Implement strict IoT vibration/temperature monitoring and retrain staff to address the 73% cargo damage rate.

## 📁 Repository Structure
* `dynamic_supply_chain_logistics_dataset.csv`: The raw dataset.
* `SupplyChain_Dashboard.xlsx`: The final Excel file containing the Power Query ETL, Pivot Tables, and Interactive Dashboard.
* `Dashboard_View.pdf`: A static one-page PDF export of the final dashboard.
* `images/`: Directory containing screenshots for documentation.

---
*Created by [Your Name / Ahmed Abdelfattah] - Senior Statistics & Computer Science Student*
