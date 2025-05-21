# delivery-forecasting-and-KPIs-dashboard-PowerBI_MySQL

This project analyzes a comprehensive food delivery dataset using SQL and Power BI to extract actionable insights on delivery performance, customer satisfaction, and operational efficiency. It explores key factors such as delivery times, ratings, vehicle condition, traffic density, weather, festival impact, and peak hours.

Advanced SQL techniques—including recursive date generation and predictive queries—support real-time decision-making, while the interactive Power BI dashboard visualizes KPIs across cities, time slots, and delivery conditions.

The goal is to help delivery companies optimize operations, reduce delays, and enhance customer experience through data-driven strategies.

---

##  Tech Stack

- **MySQL** for querying
- **SQL** concepts: CTEs, window functions, groupings, and aggregations
- **GitHub** for version control and collaboration
-  **Power BI Desktop** – Dashboard development and interactive visualizations  
- **Power Query** – Data transformation and cleaning  
- **DAX** – Measures, KPIs, and calculated columns

---

##  Features

-  **Delivery Time Analysis**: Track average delivery time by city, vehicle type, and customer age group.
-  **Delay Pattern Recognition**: Identify peak hours, festival periods, and traffic/weather conditions that contribute to late deliveries.
-  **Forecasting Module**: Predict delivery volume for the next 5 weeks based on historical trends.
-  **City Performance Overview**: Compare delivery trends across metropolitan, urban, and semi-urban areas.
-  **Customer Rating Correlation**: Analyze how delivery timeliness impacts customer satisfaction.
-  **Interactive Filters & Slicers**: Drill down by city, festival period, traffic, time bucket, and vehicle type.

---

## Business Problem

In the highly competitive food delivery industry, timely deliveries and high customer satisfaction are critical. Companies face challenges including:

- Delays due to traffic, weather, or vehicle conditions.
- Variations in delivery performance across cities and delivery personnel.
- Managing peak demand periods efficiently.
- Predicting late deliveries to proactively manage customer expectations.
- Understanding the impact of external factors like festivals and weather on delivery efficiency.

Addressing these issues helps reduce delivery time, improve customer ratings, and optimize resource allocation.

---

## Solution & Approach

To solve these problems, this project uses **SQL-based exploratory data analysis and predictive queries** on delivery datasets, focusing on:

- Tracking delivery ratings and performance over time.
- Comparing average delivery times across different cities, vehicle conditions, and traffic levels.
- Identifying popular order types and frequent delivery locations.
- Analyzing delivery delays during festivals and peak hours.
- Using recursive CTEs to generate complete daily delivery counts, even for days with no orders.
- Segmenting delivery times into buckets and categorizing traffic and weather conditions to predict late deliveries.
- Ranking delivery personnel by their efficiency and ratings to recognize top performers.

This data-driven approach helps businesses optimize delivery logistics, plan for high-demand periods, and enhance customer experience through improved operational insights.

---


## Overview of outputs

##### Most popular food order type in each city

![image](https://github.com/user-attachments/assets/fc9151f4-4748-4497-b458-d796e1595f62)

output

![image](https://github.com/user-attachments/assets/e3c87a8f-43d7-4e09-8308-ad37c1b5bd77)

##### Festival vs. Non-Festival delivery time comparison

![image](https://github.com/user-attachments/assets/be66004e-205e-4c88-a4b6-8feaea9f1e1d)

output

![image](https://github.com/user-attachments/assets/66b35de3-9491-4b07-ac7a-11e4b6563020)

##### Top delivery person by delivery time & rating

![image](https://github.com/user-attachments/assets/9bcd2fbc-d238-4b14-9846-220a90b3bde8)

output

![image](https://github.com/user-attachments/assets/26608dc2-eeca-4c43-873a-4b13c604170c)

##### How delivery times vary by city

![image](https://github.com/user-attachments/assets/3ee68bcc-632e-4c10-974b-bbc0ff347e8c)

output

![image](https://github.com/user-attachments/assets/d6767f96-40b9-47fa-b827-69f41055d754)

##### Daily Delivery Count 

![image](https://github.com/user-attachments/assets/176f7b92-e433-4e03-bbf5-0d7a815a05b6)

output

![image](https://github.com/user-attachments/assets/1d829ef8-05e5-4372-8549-73336a599873)

#####  Average rating by age group

![image](https://github.com/user-attachments/assets/b62dc563-48e7-4859-96d9-6fc6068cb0a3)

output

![image](https://github.com/user-attachments/assets/94cf8f57-8860-46f3-94fd-dd9197ed4bf1)

## 📊 Dashboard Views


![image](https://github.com/user-attachments/assets/6516df05-8683-42c2-9b5a-ba1b5b982356)

![image](https://github.com/user-attachments/assets/30e20622-4351-4841-bed8-df7fc0a3de36)

![image](https://github.com/user-attachments/assets/073b66d3-07bc-4b7c-b30b-48faf57743cd)

![image](https://github.com/user-attachments/assets/7716ce8a-43c3-4b02-a28b-98d7a6317fb4)

![image](https://github.com/user-attachments/assets/caa1250b-fc8a-4b43-9c44-095a5dbcf7bb)







  ##  Project Workflow

1. **Data Ingestion**  
   Loaded datasets covering order details, delivery times, vehicle information, traffic density, weather, and customer ratings.

2. **Data Cleaning & Transformation**  
   - Removed nulls and inconsistencies  
   - Parsed delivery duration  
   - Standardized city, weather, and vehicle-type fields  

3. **Data Modeling**  
   - Defined relationships between tables  
   - Created calculated columns for delay percentages and averages  

4. **Dashboard Design**  
   - Built themed, visually intuitive reports  
   - Integrated dynamic filters, charts, and KPI cards  

5. **Insight Extraction & Forecasting**  
   - Uncovered high-risk delivery patterns  
   - Applied forecasting logic to project future deliveries

---

##  Key Analysis Questions

- What is the average delivery time across cities and time segments?
- Which vehicle type performs best in various traffic and weather conditions?
- When do most delivery delays happen?
- How do customer ratings vary based on delivery timeliness?
- What does the delivery volume forecast look like for the next 5 weeks?

---



###  Overview Dashboard
- Total Deliveries, Average Delivery Time, Rating
- Delivery Volume by Age Group
- Orders by Time Segment (e.g., 6PM–Midnight)

###  Traffic & Timing Analysis
- Delivery Time by Traffic Density and Weather Conditions
- Delays by Time of Day

###  Delivery Partner Performance
- Performance by Vehicle Type (e.g., Scooter, Motorcycle, E-Scooter)
- Delivery Time vs Rating Correlation

###  Factors Contributing to Delays
- Festival Impact
- Traffic × Weather × Time Bucket Combinations (Top Delay Scenarios)

###  Forecast View
- Weekly Delivery Trend (Past & Next 5 Weeks)
- Expected Order Volume Stability (~2.8K/week)

>  Dynamic slicers for: City, Festival, Traffic, Weather, Vehicle Type, Time Bucket

---

##  Sample DAX Measures

``DAX
Average Delivery Time = AVERAGE('Orders'[Delivery_Time])
On-Time Percentage = DIVIDE([On-Time Orders], [Total Orders], 0)
Late Deliveries = CALCULATE([Total Orders], 'Orders'[Status] = "Late")



##  Sample Insights

-  **70.85%** of on-time deliveries receive higher customer ratings.
-  **6PM–Midnight** is the busiest delivery window and the most delay-prone.
-  Deliveries made during **Jam traffic + Foggy weather** conditions face up to a **76% delay rate**.

---

##  Limitations

-  **70.85%** of on-time deliveries receive higher customer ratings.
-  **6PM–Midnight** is the busiest delivery window and the most delay-prone.
-  Deliveries made during **Jam traffic + Foggy weather** conditions face up to a **76% delay rate**.
- The dataset does **not include financial or operational costs**.
- Forecasting is based on **historical delivery trends**, not real-time data.
- Customer feedback is limited to **star ratings only**, lacking qualitative insights.

---

##  How to Use

1. **Clone this repository**
2. **Open** `Delivery_Performance_Dashboard.pbix` **in Power BI Desktop**
3. **Explore the dashboards** using built-in filters and slicers
4. **Customize the visuals** or connect your own dataset as needed

## Repository Structure

- `scripts` — Contains all SQL scripts for data analysis and queries.
- `README.md` — Project overview and documentation.
- `dataset` — Folder for sample or raw data files.
- `reports/` — Summary reports or export results.
- `.pdf` - powerbi report in pdf
- `.pbix`- visualizations

---

## Author
### — Sudeshna Dey
###  — Contact & Contributions

####  Email: sudeshnadey1000@gmail.com
####  LinkedIn: https://www.linkedin.com/in/sudeshna-dey-724a811a0/
 Have feedback or suggestions? I'm always open to improving and collaborating!
 
If you find this project helpful:
Give it a star
Thanks for visiting — and happy data analyzing!

