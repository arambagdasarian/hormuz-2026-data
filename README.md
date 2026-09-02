# Hormuz 2026 — data starter kit

A first pass at pulling structured data out of the sources Vahan already skimmed (IEA Oil Market Report, EIA chokepoints brief, Lloyd's List war-risk piece), plus a few more to fill gaps, ahead of building out the research project on the two 2026 Strait of Hormuz closures.

## What's here

- `data/01_event_timeline.csv` — dated sequence of the crisis: Feb 28 closure, ceasefire, June reopening, July breakdown, current state
- `data/02_brent_price_timeline.csv` — Brent/physical crude price points through the crisis (monthly resolution)
- `data/03_hormuz_flow_volumes.csv` — actual mb/d and vessel-transit-count flow through the Strait, before and during
- `data/04_pipeline_bypass_capacity.csv` — Saudi/UAE pipeline bypass *capacity* vs. the Hormuz baseline
- `data/05_war_risk_premiums.csv` — tanker war-risk insurance premium moves (% of hull value, $/voyage)
- `data/06_global_supply_demand.csv` — global oil supply/demand and OPEC+ output figures
- `data/07_inventory_drawdowns.csv` — OECD/global inventory drawdowns and strategic reserve levels
- `data/08_price_timeline_dated.csv` — **day-level** Brent prices tied to specific events (added for round 2)
- `data/09_pipeline_utilization_actual.csv` — what the bypass pipelines *actually carried*, not just their rated capacity (added for round 2)
- `data/10_total_exports_all_routes_kpler.csv` — net regional crude exports across all routes combined — the cleanest single "how much oil actually got out" number, covering both closures (added for round 2)
- `data/11_insurance_premium_dated_events.csv` — dated insurance-market events, incl. the exact JWC circular date (added for round 2)
- `findings/preliminary_findings.md` — five quick observations from round 1, plus the original list of data gaps
- `findings/question_analysis.md` — round 2: one section per of Vahan's three chosen questions, with the relevant dated numbers, a working hypothesis, and a specific chart/calculation to build next
- `sources.md` — every source used, including the three Vahan already read

## Status

Round 2. Vahan picked three questions out of round 1's prompts:
1. How much of the April-June price decline was "pricing the ceasefire" vs. "barrels actually flowing again"?
2. Does the rerouting gap explain the realized flow loss, or is something else going on?
3. Does the insurance premium move predict the oil price move, lag it, or do they move together?

Files 08-11 were added specifically to answer these. `findings/question_analysis.md` is the place to start — it lays out what the data suggests for each question and names the next chart/calculation to build.

Known gap: Q3 really needs a daily insurance-premium series to test lead/lag properly; this repo only has four dated premium points so far.

## For Vahan

Read `findings/question_analysis.md`. Pick one of your three questions, build the chart or calculation it describes, and tell me what you actually see — does the working hypothesis hold up, or does the data say something different?
