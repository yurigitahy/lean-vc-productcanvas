---
code: C7
board: success
title: Expansion Revenue
hard_deps: [P5, P6, C2, C4]
produces: [expansion_paths, triggers, cross_sell_map, nrr_hypothesis]
downstream: []
---

# C7 — Expansion Revenue

## What this block decides

How an account grows after the first sale: by which paths, triggered by what, sold by whom. Expansion is the difference between a business that compounds and one that must buy every unit of growth forever.

## What this block is not

- Not upselling as an activity. It is a set of paths with mechanisms, or it does not exist.
- Not a discount recovery plan.
- Not a substitute for a value proposition that does not sustain. Expansion into a customer who has not succeeded accelerates churn.

## Required sections

1. **Expansion paths.** Each concrete: more usage, more seats, more entities or locations, higher tier, additional modules, cross-sell into another product from `P6`. For each: the trigger, the mechanism, the approximate value, and whether it requires a sale or happens automatically under the `P5` rules.
2. **Automatic versus sold.** Which expansion happens through the pricing metric itself — usage growth billed under existing terms — and which requires a conversation. Automatic expansion is worth several times sold expansion at the same revenue, because it costs nothing to capture.
3. **Triggers.** The observable events that indicate readiness: a usage threshold, a new team, an acquisition, a successful outcome against `P7`, a contract anniversary. Tied to instrumentation.
4. **Timing against retention.** When expansion is appropriate relative to the `C2` horizon and the `P7` moment of value. Expanding before first success is the most reliable way to accelerate churn, and the pressure to do it is strongest at exactly the wrong moment.
5. **Cross-sell map.** From `P6`: which other products this customer becomes a candidate for, in what sequence, and what evidence indicates readiness. Requires the identity and usage visibility `P6` section 8 may have flagged as absent.
6. **Who sells expansion.** CS, account management, or sales. Each has a consequence: CS selling can compromise the trusted-advisor relationship the renewal depends on; sales selling requires context CS holds. State the choice and the mitigation.
7. **Expansion economics.** Cost of expansion compared with new acquisition CAC from `V7`. Expansion is normally several times cheaper, which is the argument for building the paths deliberately rather than opportunistically.
8. **NRR hypothesis.** Expected net revenue retention given expansion, contraction, and churn from `C2`. Above 100% means the base grows without new acquisition. Marked as a projection until cohorts exist.
9. **Contraction risks.** Where accounts shrink without leaving: seat reductions, usage decline, downgrade at renewal. Frequently a stronger signal than churn itself and rarely watched.
10. **Where expansion is impossible.** If the product is single-seat, single-price, and fixed-scope, say so plainly. Then the question is whether an expansion surface should be built at all, which is a `P5` question, and this block should return it there.

## Evidence rules by regime

- **Greenfield.** Expansion is hypothetical. Focus on whether the `P5` design creates a surface at all; the paths can be designed later.
- **Extension.** This product may itself be an expansion path for the existing base. State that relationship explicitly.
- **Repositioning.** Existing accounts may expand or contract under the new positioning. Model both.

## Quality tests

- Does any expansion happen without a conversation? If not, all growth costs sales time.
- Is expansion timing tied to customer success rather than to quota timing?
- Does cross-sell require data visibility `P6` says does not exist?
- Is contraction watched as closely as churn?

## Canonical extract

```
C7 — Expansion Revenue
Paths:               <path → trigger → mechanism → approximate value>
Automatic:           <which expansion needs no conversation>
Timing rule:         <not before what milestone>
Cross-sell:          <products, sequence, readiness evidence>
Sold by:             <role, and the mitigation for the conflict>
Expansion cost:      <vs. new-customer CAC from V7>
NRR hypothesis:      <figure, marked projection>
Contraction risk:    <where accounts shrink without leaving>
```

## Probing questions

- Which accounts grew last year without anyone selling them anything?
- What does a customer buy next, and who tells them it exists?
- What would make a customer reduce their spend without leaving?
- If acquisition stopped tomorrow, would revenue grow or shrink?

## Contradictions to watch

- Cross-sell targets products `P6` did not map as related, or requires unreconciled identity data.
- Expansion is scheduled before the retention horizon or the `P7` moment of value is reached.
- No expansion surface exists in `P5` while `P8`'s revenue case assumes expansion growth.
