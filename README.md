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
<img width="1920" height="952" alt="Screenshot (1946)" src="https://github.com/user-attachments/assets/8b46aa88-a6df-4feb-be15-aa690a1702db" />

- Rainfall peaked in **2018 (~3199)** and dropped significantly in **2019 (~2739)**  
- Highest rainfall observed during **Rabi season**, lowest in **Zaid**  
- **Bangalore** recorded the highest rainfall, while **Mysuru** had the lowest  
- **Paddy crops** are associated with higher rainfall conditions  

---

### 🌡️ Temperature Trends
<img width="1920" height="967" alt="Screenshot (1947)" src="https://github.com/user-attachments/assets/53449efa-27f0-4251-bbb6-2fd03275fb84" />

- Temperature remained relatively stable between **2005–2018**  
- Highest during **Kharif season**, lowest in **Rabi**  
- **Bangalore** recorded highest temperatures, **Chikmagalur** lowest  
- **Ginger crops** associated with higher temperature ranges  

---

### 🌾 Yield Variability
<img width="1920" height="948" alt="Screenshot (1948)" src="https://github.com/user-attachments/assets/bd4481b3-1124-4610-ac11-3cc4cf37edd6" />

- Yield fluctuated significantly post-2012, peaking in **2014**  
- Decline observed between **2018–2019**  
- **Rabi season** shows highest average yield (~24916)  
- **Kodagu** leads in yield, while **Davangere** lags behind  
- **Cotton crops** show highest yield, **Cocoa** lowest  

---

### 💧 Humidity Observations
<img width="1920" height="937" alt="Screenshot (1949)" src="https://github.com/user-attachments/assets/acc7be88-4076-4acd-9892-e08df9e4c810" />

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
<img width="1920" height="901" alt="Screenshot (1922)" src="https://github.com/user-attachments/assets/d2c14ad8-fa51-4bc0-9946-604ffdcaa293" />


---

### 🔹 Pipeline Steps

#### 1. Data Ingestion (AWS S3)
- Created S3 bucket (`s3://powerbi-snf-prj`)  
- Uploaded raw CSV dataset  

---

#### 2. Integration with Snowflake
<img width="1920" height="878" alt="Screenshot (1927)" src="https://github.com/user-attachments/assets/053a2d23-f199-421a-a5e2-d21e0796b62f" />

- Created **Storage Integration** with AWS IAM Role  
- Configured secure access between S3 and Snowflake  
- Created database, schema, and table structures  
- Used **external stage** to load data  

---

#### 3. Data Loading & Transformation (Snowflake)
<img width="1920" height="912" alt="Screenshot (1945)" src="https://github.com/user-attachments/assets/30465793-5860-474c-8915-2efb8abf18dd" />

- Loaded data using `COPY INTO` from S3 stage  
- Performed SQL-based transformations:
  - Adjusted rainfall (+10%) and area (-10%) *(simulated for analysis)*  
  - Created derived columns:
    - `Year_Group` (Y1, Y2, Y3)  
    - `Rainfall_Group` (Low, Medium, High)  

---

#### 4. Data Visualization (Power BI)
<img width="1920" height="945" alt="Screenshot (1928)" src="https://github.com/user-attachments/assets/543300cb-1aa7-474d-8011-c9caf553b30c" />

- Connected Snowflake to Power BI via connector  
- Built interactive dashboards analyzing:
  - Environmental trends  
  - Crop performance  
  - Regional variations  

---

#### 5. Deployment (Power BI Service)
<img width="1920" height="961" alt="Screenshot (1952)" src="https://github.com/user-attachments/assets/723206d3-47cd-49b8-aa42-9c08cf81053f" />

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
