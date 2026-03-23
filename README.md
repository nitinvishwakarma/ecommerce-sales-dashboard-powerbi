# E-Commerce Sales Dashboard | Power BI

## Project Overview
This project features an end-to-end Power BI solution for tracking and analyzing retail performance across North America, managing a dataset of over **$11.53M in sales** and **$1.34M in profit**.

## Key Technical Features
- **Time Intelligence DAX:** Comparisons for YTD vs PYTD with dynamic trend indicators.
- **Advanced Ranking:** Implemented `RANKX` to identify Top 5 and Bottom 5 performing products.
- **Geographic Analysis:** Visualized regional sales distribution using latitude and longitude data.
- **Interactive UX:** Used Bookmarks and Slicers to create a seamless segment filtering experience.

## Tools Used
- Power BI Desktop
- DAX (Data Analysis Expressions)
- SQL Server (Data Cleaning)


# E-Commerce Sales Dashboard | Power BI & DAX

## Project Overview
This project involved developing a comprehensive Power BI solution 
for e-commerce sales performance tracking, analyzing a portfolio of 
**$11.53M in total sales** with a focus on product rankings, 
profitability, and geographic performance across North America.

---

## Key Technical Features

- **Time Intelligence:** Implemented YTD and PYTD DAX comparisons 
to track sales performance against previous year
- **Dynamic Rankings:** Built Top 5 and Bottom 5 product ranking 
using RANKX measures for instant performance visibility
- **Geographic Analysis:** Created map visuals across North America 
using US state latitude and longitude coordinates
- **KPI Cards:** Designed sparkline KPI cards showing 
**$11.53M sales | $1.34M profit | 11.58% margin**
- **Interactive Filtering:** Cascading slicers for region, 
category, and time period drill-down

---

## DAX Measures Used
```dax
-- Year to Date Sales
YTD Sales = TOTALYTD(SUM(Sales[Revenue]), Dates[Date])

-- Previous Year to Date Sales
PYTD Sales = CALCULATE(
    SUM(Sales[Revenue]),
    SAMEPERIODLASTYEAR(Dates[Date])
)

-- YTD vs PYTD Variance
YTD vs PYTD = [YTD Sales] - [PYTD Sales]

-- Top 5 Products Ranking
Top 5 Products = 
RANKX(ALL(Products[ProductName]), [Total Sales], , DESC, DENSE)

-- Profit Margin %
Profit Margin % = DIVIDE([Total Profit], [Total Sales]) * 100
```

---

## Screenshots

### Dashboard Overview
![Dashboard Overview](Screenshot%20E-Commerce%20Sales%20Datshboard%20-%20Overview.jpg)

---

## Live Report

> Power BI Service embedding is restricted on this account.
> Full dashboard screenshots are available in this repository.

---

## Tools Used

- Power BI Desktop
- DAX — Time Intelligence, RANKX, and KPI measures
- Power Query for data transformation
- US State geographic coordinates for map visuals

---

## Files in This Repository

| File | Description |
|---|---|
| Ecommerce Dashboard.pbix | Power BI dashboard file |
| ecommerce_data.csv | Raw e-commerce sales dataset |
| ecommerce_data_excel.xlsx | Excel version of dataset |
| us_state_long_lat_codes.csv | US state coordinates for map visual |
| IMPORTANT POINT TO NOTE.docx | Project notes and key points |
| Final Back.jpg | Dashboard background image |
| Screenshot E-Commerce Sales Datshboard - Overview.jpg | Dashboard screenshot |

---

*Project by Nitin Vishwakarma | Power BI Developer | March 2026*
