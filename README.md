# Carrier Performance Scorecard (Power BI + DAX + SQL)

**What it does:** Executive view of OTIF %, transit variance, and cost/mi by carrier, mode, and lane.  
**Why it matters:** Pinpoints underperforming lanes/carriers and informs routing-guide & negotiation decisions.

## Screens
![KPIs](assets/scorecard_kpis.png)
![Carrier × Mode](assets/matrix_carrier_mode.png)
![Lane Drill](assets/lane_drill_table.png)

## How to use
1. Open `pbix/Carrier_Scorecard.pbix`.
2. (Optional) Connect to `/data` CSVs and refresh.
3. Use slicers for Carrier, Mode, Service Level, Month.
4. Try the **KPIs ↔ Lanes** bookmark and **Metric field parameter**.

## SQL (optional)
Run `sql/kpis.sql` (DuckDB/SQLite) to create:
- `v_ship_base` (transit, SLA, on-time flag)
- `v_carrier_kpi`
- `v_lane_kpi`
- `v_top_late_lanes`

## Theme
Import `theme/rb-minimal.json` for a clean, modern layout.

> Data are **synthetic**. No real company data used.
