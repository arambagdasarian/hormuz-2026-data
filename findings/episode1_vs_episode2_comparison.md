# Episode 1 vs. Episode 2: was the market reaction bigger, smaller, or the same?

Vahan pulled real data for this (see `data/12_episode2_insurance_premiums.csv`) and concluded Episode 2's reaction was "much more suppressed" than Episode 1's, based on comparing growth multiples (30x vs. 7.5-12.5x). Checking the underlying sources changes the answer.

## The problem with comparing multiples here
Episode 1's 30x is measured from a clean pre-war baseline (0.25%, Feb 28). Episode 2's 7.5-12.5x is measured from an already-elevated "ceasefire" baseline (0.4-8%, depending on exact date) — premiums never actually reset to normal between the two closures. Dividing by a bigger starting number makes the multiple look smaller even if the destination is just as high. A multiple is only comparable across two events if both start from the same kind of baseline; here they don't.

## A cleaner comparison: align by days since each shock, look at the actual level
| Days since the closure began | Episode 1 (from Feb 28) | Episode 2 (from Jul 6-8) |
|---|---|---|
| Day 0 | 0.25% | ~3-8% (already elevated from the Jun 27 wobble) |
| Day ~11 | 7.5-10% | 3-10% |
| Day ~16-17 | (already near peak) | 7.5-10% |

Both episodes reach roughly the **same ceiling — about 10% of hull value** — on a similar timescale (~11-17 days). That is not a suppressed reaction. It's a comparably fast, comparably severe one; it just looks smaller if you only track the multiple instead of the actual price level.

## Best-supported answer right now
The insurance market's reaction to Episode 2 was **about as severe as Episode 1 in absolute terms**, reaching a similar peak (~10% of hull value) on a similar timeline. The appearance of a "suppressed" Episode 2 in Vahan's original write-up came from comparing relative multiples off two different, non-comparable starting points, not from an actual weaker reaction. If anything, the fact that premiums never fully came back down between closures (0.4-8% "during the ceasefire" vs. the 0.25% pre-war baseline) suggests the market treated the underlying risk as still live even during the truce — arguably a sign of *more* accumulated caution, not less.

## What's still soft
- The exact premium level right at Episode 2's day 0 (Jul 6-8) isn't directly sourced — it's inferred from the Jun 27-28 reading a few days earlier.
- The Jun 17 (0.4-0.8%) figure and the Jul 22-23 (7.5-10%) figure are both single-source and not yet cross-confirmed the way the Mar 11 and Jul 17 figures are.
- This is about the *insurance* side only. The price/flow side of Episode 2 (Kpler's 12→9 mb/d, `data/10`) still needs the same kind of day-aligned comparison to see if oil prices and flow volumes tell the same "comparably severe" story as insurance does.
