# Working analysis for Vahan's 3 questions

These sections lay out the dated data now available for each question (see `/data/08` through `/data/11`), a working hypothesis the data seems to support, and a specific chart/calculation to build next. None of these are finished answers — they're the setup so the actual analysis is Vahan's to run.

---

## Q1: How much of the April-June price decline was "pricing the ceasefire" vs. "barrels actually flowing again"?

**Relevant dated points** (`08_price_timeline_dated.csv`):
- Ceasefire agreed **April 7-8**
- April itself swung from a **$144 high to under $100 low** within the same month (avg $120.36)
- May: ~$110
- June (MOU reopens Hormuz **June 17**): month averaged **$85**

**What this suggests:** the ceasefire date falls *inside* the same month the price collapsed from its peak — meaning a large chunk of the drop likely happened on the ceasefire announcement itself, well before any barrels physically resumed flowing (reopening didn't happen until June 17, over two months later). The price kept drifting down through May and June even as actual reopening was still pending, which looks more like continued probability-of-resolution repricing than a response to realized flow.

**What to build:** plot the daily(ish) price points against the event dates (Apr 7-8 ceasefire, Jun 17 MOU) on one timeline. If most of the ~$34/bbl April-to-June decline happened in the days right after Apr 7-8, that's "pricing the ceasefire." If it's spread evenly or concentrated near Jun 17, that's closer to "barrels flowing." Pair this with `03_hormuz_flow_volumes.csv` and `10_total_exports_all_routes_kpler.csv` — if flow didn't actually recover meaningfully until after Jun 17 while price had already fallen most of the way by then, that's the cleanest evidence for the "priced the ceasefire" side.

---

## Q2: Does the rerouting gap explain the realized flow loss, or is something else going on?

**Relevant numbers:**
- Pre-crisis Hormuz baseline: **~20-20.7 mb/d**
- Q1 2026 realized Hormuz flow: **14.6 mb/d** → a **~6.1 mb/d** net loss
- Petroline (Saudi bypass pipeline): went from **~2 mb/d pre-crisis** to its **7 mb/d max by March 11** — a **~5 mb/d increase**
- IEA separately reports **12.8-14+ mb/d shut-in / total supply losses** since February

**Working hypothesis - this is the interesting part:** if pipelines added ~5 mb/d of *new* flow, but the Strait itself only lost ~6.1 mb/d net, the physical "couldn't find a route" gap is much smaller than the ~11 mb/d gap implied by (baseline flow) minus (max bypass capacity) that the original framing assumed. Most of the barrels that "disappeared" may not be barrels that had nowhere to go — they may be barrels that were **never produced/shipped at all** (shut-in production, per the IEA's 12.8-14 mb/d figure), which is a completely different economic story than a rerouting bottleneck.

**What to build:** a simple accounting identity check: (pre-crisis Hormuz + pre-crisis pipeline use) vs. (crisis Hormuz + crisis pipeline use). If those two totals are close, the "gap" is mostly explained by shut-in production, not stranded oil — rerouting capacity turns out not to be the binding constraint. If there's still a large unexplained residual, *that's* the oil that had nowhere to go. Vahan should also pull actual Habshan-Fujairah utilization (only capacity is in this dataset so far, not actual crisis-period flow) to complete the pipeline side.

---

## Q3: Does the insurance premium move predict the oil price move, lag it, or do they move together?

**Relevant dated points** (`11_insurance_premium_dated_events.csv` vs `08_price_timeline_dated.csv`):
- Strikes: **Feb 28** (Saturday, no trading)
- First trading day after: **March 3** — Brent jumps to $84 (from $72 on Feb 27) **the same day** the JWC published its listed-area expansion (JWLA-033)
- Premiums then kept climbing through the following week (10x, then ~60x on some quotes by ~March 11)
- Brent, meanwhile, only reached $100 by **March 12** — a ~38% rise from baseline, versus a reported ~60x premium spike

**Working hypothesis:** both markets reacted on the same first trading day (there's no lead/lag visible at this resolution since markets were closed over the weekend when the actual shock happened) — but premiums scaled up far more aggressively (multiples of 10-60x) than the oil price did (+38-64% by mid-March) over the following two weeks. That's consistent with the insurance market pricing a discrete, almost binary "war zone / not war zone" risk (the JWC listing is a legal/contractual trigger, not a continuous market price), while the oil price moved more gradually as the market absorbed the actual barrel shortfall.

**What to build:** Vahan needs daily (not just event-date) premium quotes to really test lead/lag — this dataset only has ~4 dated premium points. Lloyd's List or a broker's daily war-risk index would let him actually run a lagged-correlation check instead of eyeballing four points against a price series. Flag this as the priority data gap if he wants a rigorous answer to this specific question.

---

## Overall note
None of Q1-Q3 can be fully answered with monthly/quarterly aggregates — all three need the *dated* files (08-11), and Q3 in particular needs a real daily insurance premium series that isn't in this repo yet. Good next step for Vahan: pick one question, build the one chart described above, and see if the pattern holds up or falls apart.
