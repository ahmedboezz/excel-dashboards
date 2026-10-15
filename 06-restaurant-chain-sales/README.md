# Restaurant Chain Sales & Operations

**Sector:** Food & Beverage / Hospitality  |  **Tools:** Excel (PivotTables, PivotCharts, Slicers)  |  **Data:** 61,339 rows, simulated

> A casual-dining chain with six branches (about 950 orders a day) wants one dashboard for owners and branch managers: which branches and day parts drive sales, how fast delivery is growing, and where food cost and kitchen speed are out of line.

*The Power BI version of this project is in [powerbi-dashboards](https://github.com/ahmedsalamsali/powerbi-dashboards/tree/main/06-restaurant-chain-sales).*

## Excel dashboard
![Excel dashboard](screenshots/excel_dashboard.png)

## Business questions

1. How did net sales, orders and average ticket change in 2025?
2. Which branches perform best, and which have cost problems?
3. Which day parts and weekdays are the busiest?
4. How is the order mix shifting between dine-in, takeaway and delivery?
5. Does kitchen preparation time affect customer ratings?

## Key insights

- Net sales grew 14.7% in 2025 to $11.18M; orders grew 12.3% and the average ticket moved from $27.03 to $27.62.
- Lunch and dinner generate 70.2% of all orders; Friday and Saturday are the busiest days.
- Delivery rose from 23.6% to 31.3% of orders; aggregator commissions cost $759.4K over two years.
- Business Bay is the fastest-growing branch (+45.5%) thanks to weekday office lunches.
- Airport has the highest average ticket ($36.92) and University the lowest ($18.54).
- Beachfront food cost is 36.5% of sales vs 30.0% elsewhere, about $208.0K of excess cost (waste or portioning).
- Day parts with prep time above 20 minutes are rated 3.96/5 vs 4.52/5 when prep is 14 minutes or less.

## Recommendations

- Audit Beachfront portion sizes and waste logs; bringing food cost in line with other branches recovers most of the excess.
- Push direct ordering through the brand's own app (loyalty points, free-delivery threshold) to cut aggregator commission.
- Add kitchen staff for lunch and dinner rush (and Beachfront in summer) to keep prep time under 15 minutes.
- Replicate the Business Bay office-lunch offer (set menus, pre-order) at Downtown and City Mall.

## What is inside

| File | Contents |
|---|---|
| `Excel/Restaurant_Sales_Dashboard.xlsx` | **Dashboard** (KPI cards: Net sales, Orders, Avg ticket, Food cost %, Avg rating; 5 PivotCharts; slicers that filter everything) · **Pivots** (6 PivotTables on one cache) · **Data** (clean Excel table) · **About** (problem, insights, data dictionary) |
| `screenshots/` | Dashboard images |

## Excel techniques

- One Excel Table (`tblData`) feeds a single pivot cache, so one *Refresh All* updates every PivotTable, chart and KPI.
- Calculated fields for ratios (AvgTicket, FoodCostPct, AvgRating, AvgPrep).
- KPI cards read the pivots with `GETPIVOTDATA` and show the change vs the previous year with colour-coded number formats (green = good).
- Slicers are connected to every PivotTable through *Report Connections*.
- Workbook theme colours, PivotChart styling, hidden gridlines and a print-ready landscape layout.

---
*All data is simulated for portfolio purposes; company names are fictional.*  
*Prepared by Ahmed Abdulsalam - Data Analyst.*

---
© 2026 Ahmed Abdulsalam. All rights reserved. See [LICENSE](../LICENSE).
