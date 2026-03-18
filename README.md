# End-to-End-Cloud-Data-Pipeline-AWS-S3-Snowflake-Power-BI-for-Agricultural-Data

---
https://app.powerbi.com/links/gbLNxMpKH4?ctid=fd0853e9-4432-4693-8bd9-5cac61a80641&pbi_source=linkShare&bookmarkGuid=a2bdf989-758c-4b4e-8b46-8d962ba831b5
## 📌 Project Background

Modern data workflows require integrating multiple cloud platforms to handle raw data ingestion, transformation, and analysis efficiently.  

This project demonstrates an **end-to-end cloud-based data pipeline**, where agricultural data from regions in **Karnataka and Kerala (2004–2019)** is ingested, processed, and analyzed using a modern data stack.

The dataset (~3150+ records) includes environmental and agricultural variables such as:
- Rainfall
- Temperature
- Humidity
- Crop type
- Yield
- Soil type
- Irrigation method  

The goal is to simulate a real-world scenario of building a **scalable data pipeline** and enabling downstream analytics.

---

## 📈 Executive Summary

This project focuses on building a **modern data pipeline using AWS S3, Snowflake, and Power BI**, enabling seamless data ingestion, transformation, and visualization.

Raw data was stored in AWS S3, integrated with Snowflake using external stages and storage integration, and transformed using SQL. The processed data was then connected to Power BI for visualization and deployed via Power BI Service.

The analysis highlights environmental patterns across years, seasons, crops, and locations. While insights provide contextual understanding, the primary value lies in demonstrating **cloud data engineering capabilities combined with analytical reporting**.

---

## 🔍 Key Insights (Secondary Analysis)

### 🌧️ Rainfall Patterns
- Rainfall peaked in **2018 (~3199)** and dropped significantly in **2019 (~2739)**  
- Highest rainfall observed during **Rabi season**, lowest in **Zaid**  
- **Bangalore** recorded the highest rainfall, while **Mysuru** had the lowest  
- **Paddy crops** are associated with higher rainfall conditions  

---

### 🌡️ Temperature Trends
- Temperature remained relatively stable between **2005–2018**  
- Highest during **Kharif season**, lowest in **Rabi**  
- **Bangalore** recorded highest temperatures, **Chikmagalur** lowest  
- **Ginger crops** associated with higher temperature ranges  

---

### 🌾 Yield Variability
- Yield fluctuated significantly post-2012, peaking in **2014**  
- Decline observed between **2018–2019**  
- **Rabi season** shows highest average yield (~24916)  
- **Kodagu** leads in yield, while **Davangere** lags behind  
- **Cotton crops** show highest yield, **Cocoa** lowest  

---

### 💧 Humidity Observations
- Gradual increase in humidity from **2016 to 2019**  
- Minimal variation across cities and crops (~55–56 range)  
- Indicates **humidity is relatively stable and less differentiating**

---

## 💡 Key Observations

- Environmental factors such as rainfall and temperature show **seasonal dependencies**  
- Yield is highly **volatile and influenced by multiple variables**  
- Certain crops are strongly associated with specific environmental conditions  
- Some variables (e.g., humidity) show **low variability**, indicating limited analytical impact  

---

## ⚙️ Data Pipeline Architecture

### 🔹 Pipeline Flow
AWS S3 → Snowflake → Power BI Desktop → Power BI Service

---

### 🔹 Pipeline Steps

#### 1. Data Ingestion (AWS S3)
- Created S3 bucket (`s3://powerbi-snf-prj`)  
- Uploaded raw CSV dataset  

---

#### 2. Integration with Snowflake
- Created **Storage Integration** with AWS IAM Role  
- Configured secure access between S3 and Snowflake  
- Created database, schema, and table structures  
- Used **external stage** to load data  

---

#### 3. Data Loading & Transformation (Snowflake)
- Loaded data using `COPY INTO` from S3 stage  
- Performed SQL-based transformations:
  - Adjusted rainfall (+10%) and area (-10%) *(simulated for analysis)*  
  - Created derived columns:
    - `Year_Group` (Y1, Y2, Y3)  
    - `Rainfall_Group` (Low, Medium, High)  

---

#### 4. Data Visualization (Power BI)
- Connected Snowflake to Power BI via connector  
- Built interactive dashboards analyzing:
  - Environmental trends  
  - Crop performance  
  - Regional variations  

---

#### 5. Deployment (Power BI Service)
- Published report to Power BI Service  
- Enabled cloud-based access and sharing  

---

## 🛠️ Tech Stack Used

- **Cloud Storage**: AWS S3  
- **Data Warehouse**: Snowflake  
- **Querying & Transformation**: SQL  
- **Data Visualization**: Power BI Desktop  
- **Deployment & Sharing**: Power BI Service  

---

## 📊 Key Takeaway

This project demonstrates the ability to build a **modern cloud data pipeline**, integrating multiple platforms to transform raw data into structured, analysis-ready datasets.

While insights provide analytical value, the primary strength lies in:
> **designing and implementing a scalable data workflow using AWS, Snowflake, and Power BI**
https://app.powerbi.com/links/gbLNxMpKH4?ctid=fd0853e9-4432-4693-8bd9-5cac61a80641&pbi_source=linkShare&bookmarkGuid=a2bdf989-758c-4b4e-8b46-8d962ba831b5
---
