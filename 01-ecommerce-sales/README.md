# E-Commerce Sales Performance

**Sector:** E-commerce / Retail  |  **Tools:** Excel (PivotTables, PivotCharts, Slicers)  |  **Data:** 5,400 rows, simulated

> An online store selling across a website, a mobile app and a marketplace wants one view of sales performance. Management asks where growth comes from, which categories and discounts hurt profit, and why customers return products.

*The Power BI version of this project is in [powerbi-dashboards](https://github.com/ahmedboezz/powerbi-dashboards/tree/main/01-ecommerce-sales).*

## Excel dashboard
![Excel dashboard](screenshots/excel_dashboard.png)

## Business questions

1. How did revenue, orders and average order value change in 2025 vs 2024?
2. Which channel and category drive revenue, and how is the channel mix shifting?
3. How much margin do discounts cost us?
4. Which categories have the highest return rate?
5. Does delivery speed affect customer ratings?

## Key insights

- Revenue grew 15.0% in 2025 ($566.1K to $650.8K), driven by order volume rather than basket size.
- Mobile App share of revenue rose from 27.7% to 43.3%; it is now the largest channel.
- November and December generate 23.3% of annual revenue (2 of 12 months), so stock and delivery capacity must peak in Q4.
- Fashion has the highest return rate (15.7%) vs 4.0% for Beauty; returns are also higher on the Marketplace channel.
- Profit margin falls from 27.6% with no discount to 1.0% at 21-30% discounts.
- Orders delivered in 6+ days are rated 3.43/5 vs 4.29/5 for 1-3 day deliveries.

## Recommendations

- Shift acquisition budget toward the Mobile App (push notifications, app-only offers); it is growing fastest.
- Cap blanket discounts at 20% and use targeted vouchers instead; deep discounts erase most of the margin.
- Add a size guide and fit reviews to Fashion product pages to cut the return rate.
- Open a regional fulfilment point or partner courier for Northern and Southern regions to cut delivery days.

## What is inside

| File | Contents |
|---|---|
| `Excel/Ecommerce_Sales_Dashboard.xlsx` | **Dashboard** (KPI cards: Revenue, Orders, Avg order value, Profit margin, Return rate; 5 PivotCharts; slicers that filter everything) · **Pivots** (6 PivotTables on one cache) · **Data** (clean Excel table) · **About** (problem, insights, data dictionary) |
| `screenshots/` | Dashboard images |

## Excel techniques

- One Excel Table (`tblData`) feeds a single pivot cache, so one *Refresh All* updates every PivotTable, chart and KPI.
- Calculated fields for ratios (AOV, Margin, ReturnRate).
- KPI cards read the pivots with `GETPIVOTDATA` and show the change vs the previous year with colour-coded number formats (green = good).
- Slicers are connected to every PivotTable through *Report Connections*.
- Workbook theme colours, PivotChart styling, hidden gridlines and a print-ready landscape layout.

---
*All data is simulated for portfolio purposes; company names are fictional.*  
*Prepared by Ahmed Abdulsalam - Data Analyst.*

---
© 2026 Ahmed Abdulsalam. All rights reserved. See [LICENSE](../LICENSE).
