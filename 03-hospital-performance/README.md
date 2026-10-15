# Hospital Inpatient & ER Performance

**Sector:** Healthcare  |  **Tools:** Excel (PivotTables, PivotCharts, Slicers)  |  **Data:** 5,600 rows, simulated

> A 6-department general hospital wants to track patient flow and quality. Leadership asks whether the 2025 ER triage project worked, where beds are under pressure, and which patients are coming back within 30 days.

*The Power BI version of this project is in [powerbi-dashboards](https://github.com/ahmedboezz/powerbi-dashboards/tree/main/03-hospital-performance).*

## Excel dashboard
![Excel dashboard](screenshots/excel_dashboard.png)

## Business questions

1. How many patients did we admit, and how did volume move by month and season?
2. Did ER waiting time improve in 2025?
3. Which departments have the longest stays and highest bed pressure?
4. Who is readmitted within 30 days?
5. How do waiting times affect patient satisfaction?

## Key insights

- Admissions grew 5.3% in 2025 (2,728 to 2,872); winter months (Dec-Feb) carry 31.0% of the volume.
- Average ER wait fell from 64 to 56 minutes after the 2025 triage project; Fridays and Saturdays are still the slowest days.
- The 30-day readmission rate improved from 11.2% to 10.5%; patients aged 65+ are readmitted at 17.0% vs 8.9% for others.
- Internal Medicine averages 94% bed occupancy (above the 85% safe level); Pediatrics runs at 64%.
- Internal Medicine has the longest average stay (6.4 days) vs 2.8 days in Obstetrics & Gynecology.
- ER patients who waited over 90 minutes rate their stay 3.26/5 vs 4.18/5 for waits under 45 minutes.

## Recommendations

- Open winter surge beds (or flex beds from Pediatrics) for Internal Medicine from December to February.
- Extend the 2025 triage model to Friday/Saturday ER shifts, where waits are still longest.
- Add a post-discharge follow-up call within 72 hours for patients aged 65+.
- Review discharge criteria in high-readmission departments (Cardiology, Internal Medicine).

## What is inside

| File | Contents |
|---|---|
| `Excel/Hospital_Performance_Dashboard.xlsx` | **Dashboard** (KPI cards: Admissions, Avg length of stay, Avg ER wait, 30-day readmission, Patient satisfaction; 5 PivotCharts; slicers that filter everything) · **Pivots** (6 PivotTables on one cache) · **Data** (clean Excel table) · **About** (problem, insights, data dictionary) |
| `screenshots/` | Dashboard images |

## Excel techniques

- One Excel Table (`tblData`) feeds a single pivot cache, so one *Refresh All* updates every PivotTable, chart and KPI.
- Calculated fields for ratios (ReadmitRate).
- KPI cards read the pivots with `GETPIVOTDATA` and show the change vs the previous year with colour-coded number formats (green = good).
- Slicers are connected to every PivotTable through *Report Connections*.
- Workbook theme colours, PivotChart styling, hidden gridlines and a print-ready landscape layout.

---
*All data is simulated for portfolio purposes; company names are fictional.*  
*Prepared by Ahmed Abdulsalam - Data Analyst.*

---
© 2026 Ahmed Abdulsalam. All rights reserved. See [LICENSE](../LICENSE).
