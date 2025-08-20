# Deloitte Job Simulation (Forage) – Telemetry Downtime Dashboard

This repository showcases my work from the **Deloitte Technology Consulting Job Simulation** on [Forage](https://www.theforage.com/).  
The task was to analyze global factory telemetry data (JSON format) using **Tableau** and build an interactive dashboard to identify downtime trends.

---

## 📊 Project Overview
Daikibo, a manufacturing client, collected **1 month of telemetry data** (May 2021) from four factories:

- Meiyo (Tokyo, Japan)  
- Seiko (Osaka, Japan)  
- Berlin (Germany)  
- Shenzhen (China)  

Each site operated 9 types of machines that sent status messages every 10 minutes.  
The objective was to answer two key questions:

1. **Which location had the most machine downtime?**  
2. **Which device types failed most often at that location?**

---

## ⚙️ Approach

1. **Data Ingestion**  
   - Imported JSON telemetry data into Tableau.  
   - (This repo uses a **mock dataset** in place of the proprietary Forage file).  

2. **Calculated Field**  
   - Created a field called `Unhealthy` assigning a value of **10 minutes** for each unhealthy status.  
   - Formula:  
     ```tableau
     IF [status] = "unhealthy" THEN 10 ELSE 0 END
     ```

3. **Visualizations**  
   - **Bar Chart 1 – Down Time per Factory**  
   - **Bar Chart 2 – Down Time per Device Type**  

4. **Dashboard Design**  
   - Combined both charts into a dashboard.  
   - Enabled **cross-filtering** so selecting a factory filters device downtime accordingly.  

5. **Insights**  
   - Identified the **factory with the highest downtime**.  
   - Drilled down to the **device types most prone to failure** at that site.  

---

## 🖼️ Screenshots
<p align="center">
  <img src="dashboard_view.png" alt="Tableau Dashboard Example" width="700"/>
</p>

---

## 🛠️ Tools & Skills
- Tableau (Calculated Fields, Filter Actions, Dashboards)  
- JSON Data Processing  
- Data Visualization & KPI Analysis  
- Manufacturing / IoT Telemetry Analytics  

---

## 📂 Repository Structure
