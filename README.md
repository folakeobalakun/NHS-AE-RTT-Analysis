# NHS-AE-RTT-Analysis
Interactive Power BI dashboard tracking NHS A&amp;E 4‑hour performance and 52‑week RTT backlogs.

*Power BI report blending monthly A&E SitRep data with RTT waiting‑time returns to track national and trust‑level operational pressure.*

## Project Purpose
Elective backlogs and emergency‑department crowding are two of the most visible NHS performance issues.  
This dashboard lets managers, analysts, and clinicians **see both problems in one place**, filtering by month and region down to individual trusts.

## Datasets

| Source | File(s) in this repo | Month range | Direct link |
|--------|---------------------|-------------|-------------|
| **A&E Attendances & Emergency Admissions** | CSV bundle inside | Jun 2024 → Jun 2025 | [Browse ↗](https://github.com/folakeobalakun/NHS-AE-RTT-Analysis/tree/main/June%202024%20-%20May%202025%20A%26E%20Data) |
| **RTT Provider Incomplete Pathways** | Monthly CSVs inside | Jun 2024 → May 2025 | [Browse ↗](https://github.com/folakeobalakun/NHS-AE-RTT-Analysis/tree/main/RTT%20June%202024-May%202025) |
| **ODS Trust Lookup** | (Q1 2025 snapshot) | Point‑in‑time lookup | [View ↗](https://github.com/folakeobalakun/NHS-AE-RTT-Analysis/blob/main/etr.csv) |

_All data are aggregate, publicly available, and contain **no patient‑identifiable information**._

## Key KPIs

| KPI | Definition (DAX) | Why it matters |
|-----|------------------|----------------|
| **4‑Hour A&E Performance %** | `SUM(SeenWithin4h) / SUM(TotalAttends)` | NHS constitutional standard is **95 %** |
| **≥52‑Week RTT Backlog %** | `SUM(Wait_52w) / SUM(Wait_Total)` | Elective waits over a year are a prime backlog metric |
| **A&E Attendances** | `SUM(TotalAttends)` | Proxy for unplanned demand |
| **Patients ≥52 w** | `SUM(Wait_52w)` | Absolute backlog burden |


## Core Visuals

| Page  | Interactive insight |
|------|---------------------|
| National Trend — 4‑Hour % vs 52‑Week Backlog % | Shows whether ED and elective pressures move together or diverge |
| Trust League Table — Sorted by Backlog % | Highlights worst‑performing trusts for the selected month |
| Demand vs Backlog Scatter | **_Add scatter.gif_** | Upper‑right quadrant = trusts with both high demand and high backlog |

| National Trend | ![National Trend – 4‑Hour % vs 52‑Week Backlog %](https://raw.githubusercontent.com/folakeobalakun/NHS-AE-RTT-Analysis/main/Visuals/Screenshot%202025-07-15%20at%2018.48.03.png) | Shows the year‑on‑year improvement in A&E four‑hour performance alongside the decline in ≥ 52‑week elective backlog |
| Trust League Table | ![Trust League Table](https://raw.githubusercontent.com/folakeobalakun/NHS-AE-RTT-Analysis/main/Visuals/Screenshot%202025-07-15%20at%2018.52.51.png) | Highlights the 20 trusts with the highest ≥ 52‑week backlog for the selected month |
| Demand vs Backlog Scatter | ![Demand vs Backlog Scatter](https://raw.githubusercontent.com/folakeobalakun/NHS-AE-RTT-Analysis/main/Visuals/Screenshot%202025-07-15%20at%2018.53.53.png) | Upper‑right quadrant = trusts with both high demand and large ≥ 52‑week backlogs |

## 🌟 Headline Findings
* **National recovery**: Four‑hour performance improved **+4 pp** from its December low; ≥ 52‑week backlog shrank by **1.5 pp** over the year.  
* **Persistent hotspots**: 12 trusts remain above the **4 % backlog risk** threshold despite national improvement.  
* **Demand‑risk correlation**: High attendances don’t always equal high backlog—North‑East hospitals manage demand well, while several South‑East independents carry disproportionate backlog.
