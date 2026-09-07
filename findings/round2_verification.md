# Verifying Vahan's round-2 answers against the data

Charts: https://claude.ai/code/artifact/e6fbfc47-8fe0-425c-b75a-22e45b93021e

## Q1 — Ceasefire vs. flow — **holds up**
Vahan: "when the ceasefire is reached, the prices drop tremendously... when the flow begins, the price stays relatively consistent and drops very steadily."

Confirmed by the data: price rose past Mar 31's $118 close to an April high near $144, then fell under $100 within that same month — the month the Apr 7-8 ceasefire was signed. It then declined slowly and steadily through May (~$110) and June (avg $85), well ahead of the Jun 17 reopening MOU. Caveat: the April high/low are monthly extremes from the IEA report, not dated ticks, so the exact day-by-day sequencing around Apr 7-8 isn't confirmed — daily April Brent data would close this gap.

## Q2 — Rerouting gap vs. shut-in — **pushes back**
Vahan: "most wells were shut down and inventory was at its lowest since 2003... it was the fact that there was low production that there was a flow loss."

The actual accounting doesn't cleanly support this. Hormuz transit fell 20.7→14.6 mb/d (−6.1), but Petroline's bypass rose 2.0→7.0 mb/d (+5.0) over the same period — netting to only a **−1.1 mb/d** combined gap. That means almost all of the "missing" Hormuz oil moved anyway, just via pipeline. This doesn't reconcile with the IEA's separately reported **12.8–14 mb/d "shut-in"** figure — those numbers can't both describe the same barrels at face value. Vahan's instinct (production matters, not just routing) may still be right, but low OECD inventory is evidence of *drawdown to cover a shortfall*, not proof of *shut-in production* — those are different mechanisms, and he conflated them. The real finding here is an unresolved discrepancy, not a confirmed answer.

## Q3 — Premium vs. price lead/lag — **needs correction**
Vahan: "prices surged 5x 3 days after the strait closed."

This conflates the two series. The **insurance premium** is what moved 5-60x — the **oil price** only moved to an index of ~117 (Mar 3) and ~164 (Mar 31) relative to the Feb 27 baseline, i.e. a 17-64% rise, not 5x. Both series do first move on the same day (Mar 3, the first trading day after the Feb 28 weekend strikes), so there's no visible lead/lag at this data's resolution — but the magnitude gap between the two series is itself the interesting result, and it's not what Vahan described.

## Bottom line for feedback to Vahan
- Q1: correct, ship it.
- Q2: his direction may be right but his evidence doesn't establish it — the shut-in vs. rerouting reconciliation is now an open puzzle worth a real dig.
- Q3: he mixed up which series moved 5x — needs a rewritten answer with the two series named separately.
