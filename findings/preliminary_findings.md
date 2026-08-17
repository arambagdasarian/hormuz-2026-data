# Preliminary findings (starting points, not conclusions)

These are quick observations from the data in `/data`, meant to seed discussion — not a finished analysis. Numbers pulled from public reporting (IEA, EIA, Lloyd's List, and press coverage citing them); several are marked `unverified` or flagged for a primary-source check in the CSVs themselves.

## 1. Price response looks much bigger than the physical volume loss
Hormuz throughput fell from a ~20.7 mb/d baseline (2025-Q4) to 14.6 mb/d in Q1 2026 — a ~30% drop. Over the same window, physical crude spiked to nearly $150/bbl at the peak, and Brent rose >45% since the conflict began. A 30% supply-side hit producing a 45%+ (and briefly much larger) price move implies either a very low short-run elasticity, a large fear/precautionary premium layered on top of the physical shortfall, or both — worth separating in the model (see original elasticity idea).

## 2. Insurance premiums moved far faster and further than the oil price
War risk premiums jumped 5x within 48 hours of the Feb 28 event, and some quotes reportedly hit ~60x pre-crisis rates within days — while Brent's move, though large, was on a totally different scale (45% vs. 5900%). This suggests the insurance/freight market was pricing tail risk almost instantly, while the crude price reflected the realized physical shortage more gradually. That gap is itself a testable question: did the insurance market "lead" the oil price, or were they responding to different things entirely (insurers pricing vessel/crew risk, oil traders pricing barrels)?

## 3. The rerouting gap is real and large
Combined Saudi + UAE pipeline bypass capacity tops out around 9 mb/d, with only ~2.6 mb/d of that actually spare/usable during the crisis. Against a ~20 mb/d Hormuz baseline, that means even maxed-out bypass capacity covers under half of normal flow — consistent with the ~30% realized flow decline actually observed. This is a clean, checkable number: does the *realized* Q1 2026 flow loss (~6 mb/d) roughly match what bypass pipelines *couldn't* cover?

## 4. Price fell before the Strait actually reopened
Brent dropped from its ~$144/bbl April peak to a $85/bbl June average — a decline that started around the mid-April ceasefire, well before the mid-June reopening. That timing suggests markets were pricing the *probability* of resolution, not the actual restored barrel flow, which is the same dynamic idea #2 (insurance-as-probability) was built around. Worth lining this up on a single time axis against the war-risk premium data to see which one moved first.

## 5. Episode 1 vs. Episode 2 is not yet apples-to-apples in this dataset
We have good Q1 2026 (Episode 1, starting Feb 28) volume/price data, but the vessel-transit collapse to ~10/day by July 23 (Episode 2, starting July 6) is a *traffic count*, not a flow-volume (mb/d) figure, and we don't yet have Episode 2 price or war-risk premium data at the same resolution as Episode 1. That's the single biggest gap before the two-episode comparison in the research design can actually run.

## Open data gaps to flag for Vahan
- No verified pre-conflict (Jan 2026) Brent baseline price yet — needed as the "before" point for every % change calculation.
- No Episode 2 (July–August) price, premium, or mb/d flow series yet — only vessel-count data.
- Baltic Dirty Tanker Index (freight rates) not yet pulled — would let him separate "cost of the ship" from "cost of the barrel" from "cost of the insurance."
- Cape of Good Hope rerouting distance/cost/time-added figures not yet found in a primary source — flagged in `04_pipeline_bypass_capacity.csv`.
