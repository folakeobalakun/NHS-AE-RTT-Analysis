# NHS-AE-RTT-Analysis
Interactive Power BI dashboard tracking NHS A&amp;E 4‑hour performance and 52‑week RTT backlogs.

*Power BI report blending monthly A&E SitRep data with RTT waiting‑time returns to track national and trust‑level operational pressure.*

## Project Purpose
Elective backlogs and emergency‑department crowding are two of the most visible NHS performance issues.  
This dashboard lets managers, analysts, and clinicians **see both problems in one place**, filtering by month and region down to individual trusts.

## 🗂️ Datasets

| Source | File | Month range | Link |
|--------|------|-------------|------|
| **A&E Attendances & Emergency Admissions** | `ae_attendances_monthly.csv` | Jun 2024 → Jun 2025 | NHS England open data |
| **RTT Provider Incomplete Pathways** | `provider_incomplete.csv` | Jun 2024 → May 2025 | NHS England open data |
| **ODS Trust Lookup** | `etrust.csv` | 2025‑Q1 | NHS ODS |

_All data are aggregate, publicly available, and contain **no patient‑identifiable information**._

---

## 🗂️ Datasets

| Source | File(s) in this repo | Month range | Direct link |
|--------|---------------------|-------------|-------------|
| **A&E Attendances & Emergency Admissions** | CSV bundle inside `June 2024 – May 2025 A&E Data/` | Jun 2024 → Jun 2025 | [Browse ↗](https://github.com/folakeobalakun/NHS-AE-RTT-Analysis/tree/main/June%202024%20-%20May%202025%20A%26E%20Data) |
| **RTT Provider Incomplete Pathways** | Monthly CSVs inside `RTT June 2024 – May 2025/` | Jun 2024 → May 2025 | [Browse ↗](https://github.com/folakeobalakun/NHS-AE-RTT-Analysis/tree/main/RTT%20June%202024-May%202025) |
| **ODS Trust Lookup** | `etr.csv` (Q1 2025 snapshot) | Point‑in‑time lookup | [View ↗](https://github.com/folakeobalakun/NHS-AE-RTT-Analysis/blob/main/etr.csv) |
