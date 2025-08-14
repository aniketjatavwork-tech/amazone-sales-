# amazone-sales-# 📊 Amazon Products Sales Analysis Dashboard

This Power BI project analyzes Amazon product sales performance using various KPIs and visual insights.  
It leverages **Power BI**, **DAX measures**, and **time intelligence functions** to track sales trends, product performance, and customer engagement.

---

## 📌 Project Overview
The dashboard provides:
- **YTD Sales**: $2.18M
- **QTD Sales**: $811.09K
- **Products Sold YTD**: 27.75K
- **YTD Rating**: 19.42M

It includes visual insights for:
- Sales by Month 📅
- Sales by Week 📈
- Sales by Product Category 🛍
- Top 5 Products by YTD Sales 🏆
- Top 5 Products by YTD Ratings ⭐

---

## 📷 Dashboard Preview
![Dashboard Preview](Dashboard.png)  
*(Replace `Dashboard.png` with your actual screenshot file name in the repo)*

---

## 🛠 Tools & Technologies
- **Power BI**
- **DAX (Data Analysis Expressions)**
- **Power Query**
- **Data Modeling**
- **Time Intelligence Functions**

---

## 📊 Key DAX Measures
```DAX
-- YTD Sales
YTD SALES =
TOTALYTD(
    SUM(Amazon_Data[Price(Dollar)]),
    'date table'[Date]
)

-- QTD Sales
QTD SALES =
TOTALQTD(
    SUM(Amazon_Data[Price(Dollar)]),
    'date table'[Date]
)

-- % Growth in YTD Sales
%GT YTD SALES =
DIVIDE(
    [QTD SALES],
    [YTD SALES],
    0
)
