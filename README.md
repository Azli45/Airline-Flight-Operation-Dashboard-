# Global Airline Operations Dashboard

A Power BI dashboard analyzing 98,600+ flight records to track airline operational health — flight status breakdown, busiest airports, regional performance, and passenger demographics — built on a single interactive page.

![Dashboard Preview](Screenshot%202026-09-20%20160043.png)

## 📌 Business Problems Solved

1. **How healthy is the operation overall?**
   Tracked via 4 headline KPIs: **98.6K total flights**, **33K cancelled**, **33K delayed**, and a **33% on-time rate** — revealing that only 1 in 3 flights actually departs on schedule.

2. **What's the breakdown of flight status?**
   Donut chart shows an almost perfectly even 3-way split: **Cancelled 33.4%**, **On Time 33.3%**, **Delayed 33.3%** — status is essentially random rather than concentrated in one failure mode.

3. **Which airports handle the most traffic?**
   Top 10 busiest airports identified (San Pedro Airport leads), sized by total flight volume — useful for prioritizing where operational fixes would have the biggest impact.

4. **Which regions have the worst status mix?**
   Continent × Status matrix shows **North America** carries the highest absolute volume (32,033 flights: 10,693 cancelled / 10,696 delayed / 10,644 on-time), while **South America** and **Africa** have the smallest footprints (~10-11K flights each) — but all continents show the same roughly even 33/33/33 status split, meaning the issue is systemic, not regional.

5. **What's the passenger age profile?**
   Flights split almost evenly across **Young, Adult, and Senior** age groups — no single age segment dominates ridership.

6. **What's the gender split of passengers?**
   Near-even: **Male 49.71%**, **Female 50.29%**.

7. **Can the page be explored by region and status?**
   Yes — continent and flight-status slicers let any viewer filter every visual on the page simultaneously.

8. **Is cancellation/delay risk concentrated anywhere?**
   No — since every continent shows roughly the same 33/33/33 split, the data suggests the cancellation/delay problem is **structural across the whole network**, not caused by a specific region, which is itself a key finding worth calling out.

## 🛠️ Tools & Techniques

- **Power BI Desktop** — data modeling, visualization, report design
- **DAX** — `CALCULATE`, `COUNTROWS`, `DIVIDE`, calculated columns (`IF`/nested `IF` for age bucketing)
- **Data cleaning** — resolved a source data quality issue where pilot names duplicated passenger names in earlier dataset versions
- **Custom theming** — dark, status-color-coded design (green/amber/red) for an operations-dashboard feel

## 📊 Dataset

Airline passenger/flight dataset (~98,600 rows), covering flight status, departure dates, passenger demographics, airports, and continents. [Source: Kaggle Airline Dataset]

File used: `Airline Dataset Updated - v2.csv` (the corrected version — earlier versions of this dataset had a data quality bug where Pilot Name duplicated the passenger's name).

## 📈 Key Insights

- Flight status is almost perfectly even across On Time (33.3%), Delayed (33.3%), and Cancelled (33.4%) — only ~1 in 3 flights runs on schedule
- North America accounts for the largest share of flight volume (32,033 of 98,619 flights, ~32%)
- The even status split holds across every continent, suggesting cancellations/delays stem from a network-wide issue rather than any single region
- Passenger base is balanced by both age group and gender, with no major demographic skew

## 📂 Files

- `airline dashboard.pbix` — the Power BI file
- `Screenshot 2026-09-20 160043.png` — static preview of the dashboard
- `Airline Dataset Updated - v2.csv` — source dataset used to build the dashboard
- `LICENSE` — MIT license

## 🚀 How to Use

1. Download `airline dashboard.pbix`
2. Open in Power BI Desktop (free download from Microsoft)
3. Explore using the continent and flight status slicers

---

**Author:**  Azli Khan · Built as part of ongoing Power BI / data analytics practice.
