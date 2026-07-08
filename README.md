# ⚡ EV Battery Swapping Analytics Dashboard

<p align="center">

![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-Advanced-blue)
![Power Query](https://img.shields.io/badge/Power%20Query-ETL-green)
![Data Analysis](https://img.shields.io/badge/Data%20Analysis-Business%20Intelligence-orange)
![Status](https://img.shields.io/badge/Project-Completed-success)

</p>

---

# 📌 Project Overview

This project demonstrates an **Enterprise Power BI Dashboard** built for an **EV Battery Swapping Network**.

The dashboard helps Operations, Business, and Management teams monitor:

- Battery Swapping Performance
- Battery Health
- IoT Device Availability
- Station Performance
- Revenue Analysis
- Operational KPIs

The project follows an enterprise-style dashboard architecture consisting of four interactive report pages.

---

# 🏗 Dashboard Architecture

```
Raw CSV Dataset
        │
        ▼
Power Query (ETL)
        │
        ▼
Star Schema Data Model
        │
        ▼
DAX Measures
        │
        ▼
Interactive Power BI Dashboard
```

---

# 📊 Dashboard Pages

## 1️⃣ Executive Dashboard

Provides an executive summary of business performance.

### KPIs

- Total Swaps
- Successful Swaps
- Failed Swaps
- Success Rate
- Failure Rate
- Total Revenue
- Active Stations
- Average Swap Time

### Visuals

- Monthly Swap Trend
- Monthly Revenue
- Revenue by City
- Top Stations
- Swap Status Distribution

---

## 2️⃣ Operations Dashboard

Designed for Operations Managers.

### KPIs

- Total Stations
- Active Riders
- Active Vehicles
- Average Swaps per Station
- Average Revenue per Station
- Peak Operating Hour

### Visuals

- Top Stations by Swaps
- Top Stations by Revenue
- Average Swap Time by Station
- Swaps by Hour
- Swaps by Weekday
- Station Performance Matrix

---

## 3️⃣ Battery & IoT Analytics

Monitors Battery Health and IoT Performance.

### KPIs

- Average Battery SoH
- Average Delta SoC
- Online IoT Devices
- Offline IoT Devices
- IoT Availability

### Visuals

- Battery SoH by City
- Delta SoC by City
- IoT Device Status
- Top Stations by Delta SoC
- Monthly Battery SoH Trend
- Battery Performance Matrix

---

## 4️⃣ Revenue Analytics

Provides financial insights for decision makers.

### KPIs

- Total Revenue
- Average Revenue per Swap
- Revenue per Station
- Revenue per Rider
- Highest Revenue City
- Highest Revenue Month
- Highest Revenue Station

### Visuals

- Revenue by Month
- Revenue by Quarter
- Revenue by City
- Revenue Contribution by City
- Revenue Performance Matrix

---

# 📸 Dashboard Preview

## Executive Dashboard

![Executive Dashboard](Screenshots/Executive%20Dashboard.png)

---

## Operations Dashboard

![Operations Dashboard](Screenshots/Operations%20Dashboard.png)

---

## Battery & IoT Analytics

![Battery & IoT](Screenshots/IoT%20%26%20Battery_Analytics.png)

---

## Revenue Analytics

![Revenue Analytics](Screenshots/Revenue%20Analytics.png)

---

# 📂 Project Structure

```
EV-Battery-Swapping-Analytics-PowerBI
│
├── Dashboard
│   ├── EV_Battery_Swapping_Analytics.pbix
│   └── README.md
│
├── Dataset
│   ├── EV_Battery_Swap_Transactions.csv
│   └── README.md
│
├── Screenshots
│   ├── Executive Dashboard.png
│   ├── Operations Dashboard.png
│   ├── IoT & Battery_Analytics.png
│   ├── Revenue Analytics.png
│   └── README.md
│
└── README.md
```

---

# 🛠 Tools & Technologies

- Microsoft Power BI
- Power Query
- DAX
- Data Modeling
- Star Schema
- Microsoft Excel
- CSV Dataset

---

# 📈 Sample DAX Measures

### Success Rate

```DAX
Success Rate =
DIVIDE(
    CALCULATE(
        COUNTROWS(EV_Battery_Swap_Transactions_100000),
        EV_Battery_Swap_Transactions_100000[Status]="Success"
    ),
    COUNTROWS(EV_Battery_Swap_Transactions_100000),
0)
```

---

### Failure Rate

```DAX
Failure Rate = 1 - [Success Rate]
```

---

### Average Swap Time

```DAX
Average Swap Time =
AVERAGE(EV_Battery_Swap_Transactions_100000[Swap_Time_Minutes])
```

---

### IoT Availability

```DAX
IoT Availability =
DIVIDE([Online Devices],[Online Devices]+[Offline Devices])
```

---

### Average Delta SoC

```DAX
Average Delta SoC =
AVERAGE(
EV_Battery_Swap_Transactions_100000[Battery_SoC_After]
-
EV_Battery_Swap_Transactions_100000[Battery_SoC_Before]
)
```

---

# 📊 Key Insights

✔ 100,000 Battery Swap Transactions

✔ 96% Successful Swaps

✔ 17.1 Million Revenue

✔ 98% IoT Availability

✔ 100 Active Battery Swapping Stations

✔ Interactive Executive Dashboard

✔ Enterprise Star Schema Model

✔ Dynamic DAX Measures

---

# 🎯 Business Value

This dashboard enables business teams to:

- Monitor operational efficiency
- Track battery health
- Measure station utilization
- Analyze revenue trends
- Improve IoT device monitoring
- Support strategic decision-making

---

# 👨‍💻 About Me

**Gulshan Raj**

Data Analyst | MIS Analyst | Power BI Developer

### Skills

- Power BI
- SQL
- Excel
- DAX
- Power Query
- Data Modeling
- Dashboard Development

---

⭐ If you found this project useful, don't forget to Star this repository.
