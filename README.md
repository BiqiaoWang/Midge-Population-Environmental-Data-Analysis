> 🚧 This project is currently being updated.
## 🦟 Midge Population & Environmental Data Analysis

## Project Overview
This project foucs on explore the relationship between midge populations, water quality parameters, and weather conditions at wastewater treatment ponds in Christchurch, New Zealand.

## Project Workflow
<img width="800" alt="workflow diagram" src="https://github.com/user-attachments/assets/edc3efc7-37bb-4817-841c-77ac19257d50">

## What Factors Affect Midge Populations?
<p align="center">
  <img
    src="https://github.com/user-attachments/assets/19100bfc-7fb2-4022-81f7-9544e7baedd6"
    alt="Potential Factors Affecting Midge Populations"
    width="500">
</p>

## Steps
## 1. Data Collection
Weather data was collected from two public sources: **NIWA DataHub** and **NASA POWER**.
- **NASA POWER** – Satellite-based observations and large-scale atmospheric models, provided in Local Solar Time (LST).
- **NIWA DataHub** – Ground-based weather station measurements, recorded in Coordinated Universal Time (UTC).

## 2. Weather Data Consistency Check
The comparison focused on temperature, rainfall, wind speed, and solar radiation at both the **daily** and **hourly** levels.

- **Daily level**: The two data sources showed high consistency, especially for temperature and solar radiation (as shown in the figure).
- **Hourly level**: Due to the different time zones used by the two datasets (NIWA uses UTC, while NASA uses LST), the initial correlation results were poor. I developed an **algorithm** to automatically perform time-shift alignment. After this step, the two datasets showed good consistency (as shown in the figure for solar radiation).

Note: Because NASA POWER is based on satellite observations and NIWA DataHub uses ground-based weather stations, temperature and solar radiation showed high consistency, while wind speed and rainfall showed moderate consistency.

## 3.🧹 Messy Real-World Data Cleaning

### Regular Data Cleaning

- Removed irrelevant or empty columns.
- Removed duplicate records.
- Removed rows with missing values (`Number`).

### Challenges💡⭐ 

#### 1. Uneven Sampling Frequency
The sampling frequency varied across different years and months.  Some years had many sampling days, while others had much fewer observations.

**Method:** 
Average midge count per seasonal year = Total midge count ÷ Number of sampling days

This standardisation reduced the impact of uneven sampling effort and allowed fair comparisons between different seasonal years.

#### 2. Calendar Year to Seasonal Year
Because midges are mainly active during the warmer months (summer), I converted the data from **calendar year** to **seasonal year (July–June)**, which better reflects the midge life cycle in New Zealand.

#### 3. Long-to-Wide Format Transformation
The water quality dataset was originally stored in **long format**, where each row represented one parameter measurement.
I grouped similar parameters, standardised parameter names, and reshaped the dataset into **wide format**.

#### 4. Small Sample Size
After merging the water quality dataset with the midge dataset, the number of matched dates was very limited.

To increase the number of matched observations, I aggregated both datasets from **daily level to weekly level** before merging.

I also added **p-values** to better evaluate the reliability of the results.

#### 5. Multiple Data Source Integration

## 4. 📈 Statistical Methods

### Correlation Analysis

- Pearson correlation analysis
- Correlation coefficients
- p-values for statistical significance

**Purpose:** Identify relationships between midge counts and environmental variables.

---

### Multiple Linear Regression

- Built a multiple linear regression model for Pond 1.
- Evaluated the combined effects of multiple water quality variables on midge abundance.

---

### Simple Linear Regression

- Built a simple linear regression model for Pond 2.
- Used dissolved oxygen as the predictor variable.

---

### Principal Component Analysis (PCA)

- Reduced multiple water quality variables into a smaller number of principal components.
- Identified the main environmental factors influencing water quality.

---

## Key Findings

### Tools & Skills

Python | Pandas | Matplotlib | Seaborn | Statistical Modelling | Correlation Analysis | P-value Analysis | Linear Regression | Multiple Linear Regression | PCA | Environmental Data Analysis | Data Cleaning | Data Visualisation
