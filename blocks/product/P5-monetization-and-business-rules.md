---
code: P5
board: product
title: Monetization and Business Rules
hard_deps: [P2, P3]
produces: [pricing_metric, packaging, price_points, business_rules, discount_policy, cost_to_serve_drivers]
downstream: [P6, P7, P8, M6, V2, V7, C2, C7]
---

# P5 — Monetization and Business Rules

## What this block decides

How the product converts delivered value into revenue, and the rules that govern it. This is the most load-bearing block in the canvas — eight blocks read it — and the one most often decided by imitation.

## What this block is not

- Not a price list. The price is the last decision in this block, not the first.
- Not a cost calculation. Cost sets the floor. Value in `P2` sets the ceiling. This block chooses a point and, more importantly, a metric.
- Not a discount policy alone, though it must contain one.
- Not a unit economics model. Once there are paying customers, the arithmetic belongs in a unit economics diagnostic, not here. This block produces the hypothesis that diagnostic will test.

## Required sections

1. **Pricing metric.** What the customer is charged per: seat, transaction, outcome, capacity, usage, flat access. Chosen by correlation with the value described in `P2`, not by category convention. State the correlation explicitly: when the customer gets twice the value, does the invoice roughly double?
2. **Why not the alternatives.** The metrics rejected and why. This is where imitation gets caught. If the chosen metric is the category default, say whether that is a decision or an inheritance.
3. **Cost unit versus pricing unit.** What the company pays per, versus what it charges per. Where these differ, margin drifts with customer behavior rather than with company decisions. Name the drift and its direction.
4. **Packaging.** Tiers, editions, or a single offer. For each tier: who it is for, what is included, and what is deliberately withheld. A tier that exists only for price anchoring should be labeled as such internally.
5. **Price points and their basis.** The numbers, with the reasoning: value share, competitive reference, cost-plus, or willingness-to-pay evidence. State which. Absent evidence, say the number is a hypothesis and name the test.
6. **Value capture ratio.** Price against the economic value in `P2`. Below roughly a third of value captured, the customer's case is easy and the company is leaving money. Above two thirds, the customer's case requires belief and the cycle lengthens.
7. **Business rules.** The mechanics: billing cycle, contract term, minimums, overage handling, seat true-ups, usage caps, fair-use limits, data retention, cancellation terms, price escalation. Each rule creates behavior; name the behavior it creates.
8. **Utilization thresholds.** What consumption level changes the price, the margin, or the service level. This is where usage-based models leak and where flat models cross-subsidize.
9. **Discount policy.** Who can approve what, against what. Without a policy, the first large deal sets the real price list.
10. **What drives cost to serve.** The customer behaviors that make one account more expensive than another at the same price. Feeds `C2` and `C4`. Ignoring this is the most common reason a healthy-looking gross margin does not produce cash.
11. **Onboarding, implementation, and one-time fees.** Whether they exist, what they cover, and whether they are priced to recover cost or to signal commitment. Never blended into recurring revenue.
12. **Expansion surface.** How an account grows without a new sale: more usage, more seats, more modules, more entities. If there is no expansion surface, say so — `C7` will have nothing to work with and all growth must be purchased.
13. **Free, trial, or pilot.** If any: what it costs to deliver, what converts, and what the exit criteria are. An open-ended pilot is a discount with no expiry.

## Evidence rules by regime

- **Greenfield.** Every price point is a hypothesis. The block must name the willingness-to-pay test that will run before launch.
- **Extension.** State how this price relates to the existing portfolio's prices, and whether it cannibalizes, anchors, or is anchored by them.
- **Repositioning.** There is an installed base on an existing price. State the migration: grandfathering, forced migration, or dual price lists, and what each does to churn in `C8`.

## Quality tests

- Does the pricing metric move with value, or with something merely easy to count?
- Would two customers extracting very different value pay meaningfully different amounts? If not, one of them is subsidizing the other and section 8 must say which.
- Does every business rule in section 7 have a named behavior it produces?
- Can a salesperson explain the price in one sentence? Pricing complexity is paid for in cycle length.
- Is the expansion surface real, or is it a rename of the initial sale?

## Canonical extract

```
P5 — Monetization and Business Rules
Pricing metric:      <unit> ; correlates with value because <mechanism>
Cost unit:           <unit> ; drift risk: <direction>
Packaging:           <tiers and who each is for>
Price points:        <numbers> ; basis: <evidence or hypothesis>
Value capture:       <share of the P2 economic value>
Key rules:           <term, minimum, cap, escalation>
Cost-to-serve driver:<the behavior that makes an account expensive>
Expansion surface:   <how an account grows without a new sale>
One-time fees:       <if any, and what they cover>
```

## Probing questions

- If you raised price 40% on a differentiated tier, which customers would leave — from data, or from guessing?
- Which customer behavior costs you the most and is currently free?
- What does the customer's finance team compare this invoice to?
- Which rule would you break for a large enough deal? That is your real policy.

## Contradictions to watch

- The pricing metric does not track the value described in `P2` → margin will drift with customer behavior; `V7` will surface it as unexplained CAC payback variance.
- The ICP in `P3` cannot fund this from the budget line named → either the price or the ICP is wrong.
- Network-effect incentives proposed in `M6` violate rules set here → resolve before `M6` is generated.
- No expansion surface, while `C7` is expected to produce growth → tell `C7` now.
