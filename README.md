# 📊 Atlas Labs | Attrition Dashboard

## 📌 Overview
This project is a **Power BI dashboard** that analyzes employee attrition trends at Atlas Labs. It provides HR and leadership teams with insights into factors influencing workforce turnover, enabling data-driven decisions to improve retention.

The dashboard visualizes attrition by multiple dimensions such as department, job role, tenure, overtime, hire date, and travel frequency.

---

## 🚀 Features

* **Overall Attrition Rate:** Displays the company-wide attrition rate (16.1%).
* **Attrition by Department & Job Role:** Identifies which roles and departments have the highest attrition rates.
* **Attrition by Travel Frequency:** Compares attrition between frequent travelers, occasional travelers, and non-traveling employees.
* **Attrition by Overtime Requirement:** Shows how mandatory overtime correlates with higher attrition.
* **Attrition by Tenure:** Analyzes attrition trends across different years of service.
* **Attrition by Hire Date:** Tracks attrition trends based on year of hiring.

---

## 🛠️ Tools & Technologies
* **Power BI Desktop** – Data visualization and dashboard creation.
* **DAX (Data Analysis Expressions)** – Used for calculated measures and KPIs.
* **Data Source:** [Specify your source here, e.g., HR_Data.csv or SQL Server]

---

## 📈 Key DAX Measures Used
To help users understand the logic, here are some of the primary measures:

**Attrition Rate:**
```dax
Attrition Rate = 
DIVIDE(
    COUNTROWS(FILTER('Employee', 'Employee'[Attrition] = "Yes")), 
    COUNTROWS('Employee'), 
    0
)
