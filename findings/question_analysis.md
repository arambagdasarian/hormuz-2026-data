For each question below, I have listed the dated data you should use from `/data/08` through `/data/11`. I have also included the main hypothesis you should test and the chart or calculation you should build next.

---

## Q1: How much of the April–June price decline came from the market “pricing in the ceasefire,” and how much came from barrels actually flowing again?

### Relevant dated points

Use `08_price_timeline_dated.csv`.

- The ceasefire was agreed on **April 7–8**.
- During April, the price fell from a high of **$144 to below $100**. The monthly average was $120.36.
- The May average was around **$110**.
- The MOU reopening Hormuz was signed on **June 17**.
- The June average was **$85**.

### What you should test

You should test whether most of the price decline happened immediately after the April 7–8 ceasefire.

The ceasefire happened during the same month in which the price fell from $144 to below $100. Actual flows did not resume until more than two months later, after the June 17 MOU. This suggests that the market may have priced in the ceasefire before barrels actually started flowing again.

Prices continued to fall during May and June, even though the reopening had not happened yet. This may reflect the market becoming more confident that the conflict would be resolved. It may not have been a direct response to actual barrels returning to the market.

### What you should build

You should put the daily or near-daily oil prices on one timeline. Mark the following event dates:

- **April 7–8:** Ceasefire
- **June 17:** MOU reopening Hormuz

Then check when most of the roughly $34-per-barrel April-to-June decline happened.

If most of the decline happened right after April 7–8, you can argue that the market was “pricing the ceasefire.” If the decline was spread evenly across the period, or happened mainly around June 17, then actual reopening and returning flows may explain more of it.

You should also compare the price timeline with:

- `03_hormuz_flow_volumes.csv`
- `10_total_exports_all_routes_kpler.csv`

The strongest evidence would be to show that the price had already fallen most of the way before physical flows recovered. That would support the argument that the market priced in the ceasefire before barrels started flowing again.

---

## Q2: Does rerouting explain the realized flow loss, or was something else happening?

### Relevant numbers

- Pre-crisis Hormuz flow was around **20–20.7 mb/d**.
- Q1 2026 Hormuz flow was **14.6 mb/d**.
- This means Hormuz flow declined by around **6.1 mb/d**.
- Petroline carried around **2 mb/d** before the crisis.
- By March 11, Petroline had reached its maximum capacity of **7 mb/d**.
- This means Petroline added around **5 mb/d** of flow.
- The IEA separately reported **12.8–14+ mb/d** in shut-in production or total supply losses after February.

### What you should test

You should test whether the decline in Hormuz traffic was mostly offset by increased pipeline use.

Hormuz lost around 6.1 mb/d, while Petroline added around 5 mb/d. This leaves a much smaller gap than the roughly 11 mb/d gap assumed in the original framing.

This means the original “not enough rerouting capacity” story may be incomplete. Some barrels were rerouted through pipelines. Other barrels may never have been produced or shipped because production was shut in.

That is a different economic story. A rerouting problem means the oil existed but had no available route. A shut-in production problem means the oil was never produced in the first place.

### What you should build

You should begin with this simple accounting calculation:

**Before the crisis:**

> Pre-crisis Hormuz flow + pre-crisis pipeline use

**During the crisis:**

> Crisis-period Hormuz flow + crisis-period pipeline use

Then compare the two totals.

If the totals are close, most of the decline in Hormuz traffic was probably offset by rerouting. The remaining difference is the unexplained residual. That residual could reflect shut-in production, lower exports, or missing routes in the data.

If there is still a large difference after including all pipeline flows, then you can argue that a large amount of oil was either stranded or never produced.

You should also find actual crisis-period utilization data for the Habshan–Fujairah pipeline. The current dataset only gives its capacity. It does not show how much oil actually moved through it during the crisis. You need that number to complete the calculation.

You should then compare your result with the IEA’s estimate of 12.8–14+ mb/d in supply losses. If the IEA number is much larger than the export-flow gap you calculate, explain that the two sources may be measuring different things.

---

## Q3: Does the insurance premium move before the oil price, after it, or at the same time?

### Relevant dated points

Compare `11_insurance_premium_dated_events.csv` with `08_price_timeline_dated.csv`.

- The strikes happened on **Saturday, February 28**, when markets were closed.
- The first trading day afterward was **March 3**.
- On March 3, Brent increased from **$72 to $84**.
- The JWC also published its listed-area expansion, JWLA-033, on March 3.
- Insurance premiums continued increasing during the following week.
- Some quotes increased by 10 times and then by around 60 times by approximately March 11.
- Brent reached **$100 on March 12**.
- This was around a 38% increase from the baseline, while some insurance premiums had increased by around 60 times.

### What you should test

You should test whether insurance premiums moved before the oil price or whether both reacted at the same time.

With the current data, both appear to have reacted on March 3, the first trading day after the strikes. We cannot clearly identify a lead or lag because the shock happened over the weekend, when the markets were closed.

The more interesting difference is the size of the reaction. Insurance premiums increased much more sharply than oil prices.

This makes sense because the insurance market may have been responding to a more binary question: is this now officially considered a war zone or not? The JWC listing can also trigger legal and contractual consequences. Oil prices respond more continuously as the market learns how many barrels are actually missing.

### What you should build

You need daily insurance-premium quotes to answer this question properly. The current dataset only has around four dated premium observations. That is not enough for a serious lead-lag analysis.

You should look for a daily war-risk premium series from Lloyd’s List or an insurance broker. Once you have it, compare the daily premium changes with the daily Brent price changes.

You can then run a lagged-correlation calculation to test whether:

- Insurance premiums move first.
- Oil prices move first.
- Both move on the same day.

Do not make a strong lead-lag claim using only the four existing points. Treat the missing daily insurance data as the main data gap for this question.

---

## Overall next step

You should choose one of these three questions first and build the chart or calculation described above.

Do not rely only on monthly or quarterly averages. All three questions require the dated files in `/data/08` through `/data/11`. Q3 especially requires a daily insurance-premium series that is not currently in the repository.

After you build the first chart, check whether the pattern supports the hypothesis. If it does not, change the argument based on what the data actually shows.