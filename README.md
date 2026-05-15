# Kalimati Vegetable Price Analysis — Power BI Dashboard

![Tool](https://img.shields.io/badge/Tool-Power%20BI-yellow)
![Status](https://img.shields.io/badge/status-complete-brightgreen)
![Records](https://img.shields.io/badge/records-96K-blue)

**Author:** Sushmita Shrestha  
**Tool:** Power BI Desktop  
**Data:** Kalimati Fruits and Vegetables Market, Kathmandu  
**Period:** January 2021 — September 2023  

---

## Overview

Interactive Power BI dashboard analyzing vegetable and fruit price trends at Kalimati Market — Nepal's largest wholesale produce market. Built on 96,000+ daily price records across 2.5 years, covering minimum, maximum, and average prices by commodity.

---

## Dashboard Features

| Visual | Type | Insight |
|--------|------|---------|
| Total Records, Max Price, Overall Average | KPI Cards | Sector-level summary |
| Price trend over time | Line Chart | Seasonal and volatility patterns |
| Top 10 commodities by average price | Bar Chart | Premium vs staple produce |
| Average price by commodity and month | Matrix | Month-on-month comparison |
| Filter by commodity | Slicer | Interactive filtering across all visuals |

---

## Key Findings

1. **Asparagus is the most expensive commodity** — average price nearly 3x the market average of Rs 123, reflecting its status as a premium imported product with limited local supply

2. **Premium produce dominates the top 10** — Strawberry, Kiwi, Avocado, and Mint all rank above common staples, suggesting Kalimati serves both wholesale and premium retail segments

3. **Asparagus price spike — late 2021** — prices surged to Rs 3,000 in November–December 2021 against a normal range of Rs 500–800, likely reflecting post-COVID supply chain disruption and import restrictions

4. **Staple vegetables are stable** — commodities like Banana, Arum, and Barela show minimal price variance across the 2.5-year period, indicating steady domestic supply

5. **Seasonal patterns visible** — several commodities show recurring price increases in winter months (Nov–Jan), consistent with reduced local harvests and higher transport costs

---

## Data Cleaning (Power Query)

- Removed null rows in price columns before type conversion
- Renamed columns: `Commodity`, `Date`, `Unit`, `Min Price`, `Max Price`, `Avg Price`
- Converted price columns from text to Decimal Number
- Set Date column to Date type for time intelligence functions

## DAX Measures

```
Average Price = AVERAGE('kalimati'[Avg Price])
Max Price = MAX('kalimati'[Max Price])
Total Records = COUNTROWS('kalimati')
```

---

## Project Structure

```
kalimati-powerbi-dashboard/
│
├── README.md
├── kalimati_price_analysis_bi.pdf     ← exported dashboard
└── dashboard_screenshot.png         ← full dashboard preview
```

---

## How to Open

1. Download Power BI Desktop — [powerbi.microsoft.com](https://powerbi.microsoft.com/desktop)
2. Download the `.pbix` file from this repo
3. Open in Power BI Desktop
4. Use the Commodity slicer to filter by individual vegetable or fruit

---

