---
code: C2
board: success
title: Retention Expectation
hard_deps: [P5, P7, V7]
produces: [retention_horizon, churn_shape, renewal_decision_model, ltv_hypothesis]
downstream: [C4, C7, C8]
---

# C2 — Retention Expectation

## What this block decides

How long a customer is expected to stay, why, and what the renewal decision actually depends on. This is the number that determines whether the acquisition cost in `V7` is recoverable.

## What this block is not

- Not an LTV calculation dressed up. It produces an LTV hypothesis and hands the arithmetic to a unit economics diagnostic once real cohorts exist.
- Not a target. Wishing for three-year retention does not produce it.
- Not a contract term. Contract term is a floor on the decision date, not on the decision.

## Required sections

1. **Expected horizon.** In months, with reasoning: switching cost, contract structure, embedded workflow, data accumulated, the alternative's cost of adoption. State whether the horizon is defended by structure or by satisfaction; satisfaction is not a retention mechanism.
2. **Churn shape.** When cancellations concentrate. In most products, early — before the moment of value in `P7` is reached. Naming the window tells `C3` and `C8` where to put their effort.
3. **The renewal decision.** Who decides, on what evidence, and when they start forming the opinion. Usually long before the renewal date and usually on evidence nobody assembled deliberately.
4. **What makes retention structural.** The mechanisms that make leaving costly or unnecessary: accumulated data, integrated workflow, trained users, contractual terms, results the customer would lose. Ranked by strength. This section is the honest answer to whether the horizon is real.
5. **Retention by segment.** Where retention is expected to differ within the ICP, and why. Blended retention hides a segment that leaves quickly, which is usually the segment sales finds easiest to close.
6. **Payback against horizon.** CAC payback from `V7` against the horizon here. If payback exceeds the horizon, the model does not fund itself, and this block is where that becomes visible. State it in one sentence, plainly, without softening.
7. **LTV hypothesis.** Price from `P5`, times gross margin, over the horizon. Marked as a projection. Name the cohort measurement that will replace it and when.
8. **What breaks retention.** The three most likely reasons a satisfied customer leaves: sponsor departure, budget cycle, acquisition, a competitor's bundled offer, or the problem in `P1` ceasing to be a priority. Some are outside the company's control, and saying so is more useful than pretending otherwise.
9. **The value that must persist.** Whether the `P2` promise keeps being delivered over time or is largely realized once. Products delivering a one-time benefit on a recurring price face a structural renewal problem that no amount of customer success work resolves.
10. **Instrumentation.** What must be measured to know retention is holding before renewal arrives, and what currently cannot be measured.

## Evidence rules by regime

- **Greenfield.** The horizon is a hypothesis, usually optimistic. State the conservative case as well and use it for planning.
- **Extension.** Use existing product retention as the baseline and state what makes this one different.
- **Repositioning.** Real churn data exists. Use it. If it contradicts the expected horizon, the data wins and the block says so.

## Quality tests

- Is the horizon defended by a structural mechanism or by satisfaction?
- Does the churn shape name a specific window?
- Is the payback comparison in section 6 stated explicitly?
- Does the product deliver recurring value, or one-time value on a recurring invoice?

## Canonical extract

```
C2 — Retention Expectation
Expected horizon:    <months> ; defended by: <structural mechanism>
Churn concentrates:  <window>
Renewal decided by:  <role>, on <evidence>, forming from <when>
Payback vs horizon:  <CAC payback> vs <horizon> → <funds itself: y/n>
LTV hypothesis:      <figure, marked projection>
Weakest segment:     <where retention is expected to be lowest>
Value persistence:   <recurring | largely one-time>
Cannot yet measure:  <what>
```

## Probing questions

- What would a customer lose by leaving that they could not rebuild in a month?
- When does the person who renews start deciding?
- Which customers do you expect to leave first, and are they the easiest to sell?
- Does the customer keep getting value, or did they get it once?

## Contradictions to watch

- Payback from `V7` exceeds the horizon here → the customer leaves before paying for their own acquisition. Escalate; this invalidates the revenue case in `P8`.
- Time to value in `P7` sits close to the churn window in section 2 → most customers decide before they experience the promise.
- Expansion in `C7` is planned before the horizon is reached.
