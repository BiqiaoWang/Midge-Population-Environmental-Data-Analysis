## 🦟 Midge Population & Environmental Data Analysis

## Project Overview
This project foucs on explore the relationship between midge populations, water quality parameters, and weather conditions at wastewater treatment ponds in Christchurch, New Zealand.

## Project Workflow
<img width="1536" height="1024" alt="Project Workflow" src="https://github.com/user-attachments/assets/bd7a258d-4672-4ae3-a819-d282ae6851b8" />

## Steps
### 1. Data Collection
Weather data was collected from two public sources: **NIWA DataHub** and **NASA POWER**.
- **NASA POWER** – Satellite-based observations and large-scale atmospheric models, provided in Local Solar Time (LST).
- **NIWA DataHub** – Ground-based weather station measurements, recorded in Coordinated Universal Time (UTC).

### 2. Weather Data Consistency Check
The comparison focused on temperature, rainfall, wind speed, and solar radiation at both the **daily** and **hourly** levels.

- **Daily level**: The two data sources showed high consistency, especially for temperature and solar radiation (as shown in the figure).
- **Hourly level**: Due to the different time zones used by the two datasets (NIWA uses UTC, while NASA uses LST), the initial correlation results were poor. I developed an **algorithm** to automatically perform time-shift alignment. After this step, the two datasets showed good consistency (as shown in the figure for solar radiation).

Note: Because NASA POWER is based on satellite observations and NIWA DataHub uses ground-based weather stations, temperature and solar radiation showed high consistency, while wind speed and rainfall showed moderate consistency.

### 3. Multiple datasets intergration合并 and cleaning


## Key Findings

### Tools & Skills

Python | Pandas | Matplotlib | Seaborn | Statistical Modelling | Correlation Analysis | P-value Analysis | Linear Regression | Multiple Linear Regression | PCA | Environmental Data Analysis | Data Cleaning | Data Visualisation
