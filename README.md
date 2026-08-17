# Hormuz 2026 — data starter kit

A first pass at pulling structured data out of the sources Vahan already skimmed (IEA Oil Market Report, EIA chokepoints brief, Lloyd's List war-risk piece), plus a few more to fill gaps, ahead of building out the research project on the two 2026 Strait of Hormuz closures.

## What's here

- `data/01_event_timeline.csv` — dated sequence of the crisis: Feb 28 closure, ceasefire, June reopening, July breakdown, current state
- `data/02_brent_price_timeline.csv` — Brent/physical crude price points through the crisis
- `data/03_hormuz_flow_volumes.csv` — actual mb/d and vessel-transit-count flow through the Strait, before and during
- `data/04_pipeline_bypass_capacity.csv` — Saudi/UAE pipeline bypass capacity vs. the Hormuz baseline
- `data/05_war_risk_premiums.csv` — tanker war-risk insurance premium moves (% of hull value, $/voyage)
- `data/06_global_supply_demand.csv` — global oil supply/demand and OPEC+ output figures
- `data/07_inventory_drawdowns.csv` — OECD/global inventory drawdowns and strategic reserve levels
- `findings/preliminary_findings.md` — five quick observations from the data, plus a list of the gaps still open
- `sources.md` — every source used, including the three Vahan already read

## Status

This is a first pass, not a finished dataset. It's built from Q1–Q2 2026 (Closure #1) data mostly — Closure #2 (July onward) is thin here beyond the vessel-transit collapse. See "Open data gaps" at the bottom of `findings/preliminary_findings.md`.

Read `findings/preliminary_findings.md` first — it's five observations pulled from this data, each one flagged as a starting point rather than a conclusion.

Then: **what data-related questions do you actually want answered here?** Not "what's the right answer" — what would you want to *look up or calculate* if you had all the data you wanted? A few prompts to react to, if useful:

- Does the insurance premium move *predict* the oil price move, or do they move together, or does one lag the other?
- Is the price response to Closure #2 (July) bigger or smaller than Closure #1 (Feb), once you control for the size of the physical disruption?
- How much of the April→June price decline was "the market pricing the ceasefire" vs. "barrels actually flowing again"?
- Does the rerouting gap (bypass capacity vs. baseline flow) actually explain the size of the realized flow loss, or is something else going on?

Bring back 2-3 questions you'd actually want to chase
