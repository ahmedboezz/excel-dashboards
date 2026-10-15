# Bank Loan Applications & Approvals

**Sector:** Banking / Finance  |  **Tools:** Excel (PivotTables, PivotCharts, Slicers)  |  **Data:** 5,200 rows, simulated

> A retail bank's lending team wants to understand its loan origination funnel: how many applications arrive by channel, how many are approved, why the rest are rejected, and how fast decisions are made.

*The Power BI version of this project is in [powerbi-dashboards](https://github.com/ahmedsalamsali/powerbi-dashboards/tree/main/05-bank-loan-applications).*

## Excel dashboard
![Excel dashboard](screenshots/excel_dashboard.png)

## Business questions

1. How many applications did we receive and approve, and how much did we lend?
2. How does approval rate change with credit score and debt-to-income?
3. Which channels are growing and which are slowest?
4. Why are applications rejected?
5. Are we meeting our decision-time SLA?

## Key insights

- Applications grew 17.7% in 2025 and approved lending reached $92.13M (23.8% vs 2024).
- Mobile App share of applications jumped from 18.8% to 32.1%; it is the fastest channel (3.3 days on average vs 9.3 in branches).
- Approval rate is 57.6% in 2025; it ranges from 16.6% for Poor credit to 78.7% for Excellent.
- 'Incomplete documents' causes 17.2% of all rejections, and 36.3% of Broker-channel rejections.
- Decisions within SLA improved from 52.9% to 71.5%; mortgages and SME loans remain the slowest products.

## Recommendations

- Add a document checklist and upload validation for Broker submissions; most of these rejections are avoidable.
- Keep shifting volume to the Mobile App (pre-filled data, instant decision for Personal Loans).
- Offer secured or smaller-amount alternatives to Fair-score applicants instead of a straight rejection.
- Set up a dedicated underwriting queue for SME loans to bring processing time inside the 10-day SLA.

## What is inside

| File | Contents |
|---|---|
| `Excel/Loan_Applications_Dashboard.xlsx` | **Dashboard** (KPI cards: Applications, Approval rate, Approved amount, Avg processing time, Decided within SLA; 5 PivotCharts; slicers that filter everything) · **Pivots** (7 PivotTables on one cache) · **Data** (clean Excel table) · **About** (problem, insights, data dictionary) |
| `screenshots/` | Dashboard images |

## Excel techniques

- One Excel Table (`tblData`) feeds a single pivot cache, so one *Refresh All* updates every PivotTable, chart and KPI.
- Calculated fields for ratios (ApprovalRate, SLARate).
- KPI cards read the pivots with `GETPIVOTDATA` and show the change vs the previous year with colour-coded number formats (green = good).
- Slicers are connected to every PivotTable through *Report Connections*.
- Workbook theme colours, PivotChart styling, hidden gridlines and a print-ready landscape layout.

---
*All data is simulated for portfolio purposes; company names are fictional.*  
*Prepared by Ahmed Abdulsalam - Data Analyst.*
