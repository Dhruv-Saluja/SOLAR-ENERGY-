# Solar Power Generation Analysis and Performance Monitoring System

**Company:** Kiefer India Pvt. Ltd. (Internship Project)  
**Domain:** Renewable Energy Analytics  
**Tech Stack:** Python (Pandas, Matplotlib, Seaborn), Jupyter Notebook, Power BI  

## Project Overview
This project analyzes real-world solar power plant data to monitor energy generation, calculate inverter conversion efficiency, and automatically detect hardware faults. The system processes time-series generation and weather sensor data to provide actionable insights for plant maintenance and operations.

## Dataset
The project utilizes the **Solar Power Generation Dataset** (Plant 1) collected over a 34-day period in India. It includes:
*   **Generation Data:** Date/Time, DC Power, AC Power, Daily Yield, Total Yield, and Inverter IDs.
*   **Weather Sensor Data:** Ambient Temperature, Module Temperature, and Solar Irradiation.

## Pipeline Modules
The analytics pipeline is divided into 6 core modules:
1. **Data Cleaning & Preprocessing:** Standardized datetime formats and merged generation and weather data into a single star-schema architecture.
2. **Power Generation Analysis:** Analyzed daily aggregates to identify historical patterns in AC and DC power output.
3. **Inverter-wise Performance Analysis:** Compared the total lifetime yield of 22 distinct inverters to identify the highest and lowest grid contributors.
4. **Efficiency Calculation:** Calculated the real-time conversion efficiency `(AC Power / DC Power) * 100` of the plant's inverters, handling zero-generation nighttime intervals.
5. **Weather Impact Analysis:** Evaluated the statistical correlation between environmental factors (irradiation and temperature) and power output.
6. **Fault Detection:** Engineered a monitoring threshold to flag inverters dropping below 90% conversion efficiency, pinpointing hardware requiring immediate maintenance.

## Business Intelligence Dashboard
The cleaned and transformed data was exported to **Power BI** to build an interactive monitoring dashboard featuring:
*   KPI Cards for Average Power, Efficiency, and Irradiation.
*   Time-series tracking of weather's impact on generation.
*   Conditional formatting to instantly highlight faulty inverters in red for plant operators.

## How to Run
1. Clone the repository.
2. Open `notebooks/Solar_Performance_Analysis.ipynb` in Jupyter or Google Colab.
3. Ensure the raw CSV datasets are in the correct directory.
4. Run all cells to execute the ETL pipeline, generate EDA charts, and export the cleaned CSV.
5. Open `dashboards/Solar_Monitoring_Dashboard.pbix` in Power BI Desktop to view the interactive report.
