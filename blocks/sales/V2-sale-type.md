---
code: V2
board: sales
title: Sale Type
hard_deps: [P3, P5, V1]
produces: [motion, cycle_length, stages, cost_of_sale, marketing_handoff]
downstream: [V4, V7]
---

# V2 — Sale Type

## What this block decides

How this product is sold: the motion, the length, the stages, and who does what. The motion has to be affordable at the price in `P5`, which is where most sale-type decisions are actually made and rarely acknowledged.

## What this block is not

- Not a script. `V4` is the script.
- Not a CRM pipeline configuration, though it produces the stage list.
- Not an aspiration to be product-led. Product-led is a motion with prerequisites; state whether they exist.

## Required sections

1. **The motion.** Consultative, transactional, product-led, partner-led, or a hybrid with a named split. Chosen against the ticket in `P5` and the complexity of the decision in `P4`, not against fashion.
2. **Why the motion is affordable.** The cost of the motion against the price. High-touch selling on a low ticket and self-serve on a complex high ticket are both structural mismatches that `V7` will show as unrecoverable acquisition cost. Do the arithmetic here, roughly, before it becomes an operating problem.
3. **Cycle length.** Expected duration by segment, with the reasons: number of approvers from `P4`, budget cycle from `P3`, technical evaluation, procurement, security review.
4. **Stages.** Named, with the entry and exit criterion for each. Exit criteria must be observable events, not seller confidence.
5. **Who is involved when.** Seller, specialist, executive, implementation, partner. Where the cost of sale accumulates.
6. **Marketing's role in preparing the buyer.** What must be true before a conversation is productive: which `M7` content has been consumed, which beliefs are already in place. When marketing does not do this work, sellers do it at ten times the cost.
7. **Trial, pilot, or proof of concept.** Whether one exists, what it costs to run, who pays, what the exit criteria are, and what conversion has been observed or is expected. Open-ended pilots are discounts with no expiry.
8. **Procurement and legal path.** Security reviews, data processing agreements, vendor onboarding, purchase order requirements. In enterprise sales this is frequently the longest stage and the least planned for.
9. **Competitive dynamics in the deal.** Whether deals are typically contested, and by whom. Changes the script in `V4` and the material in `V5`.
10. **Capacity.** How many active deals one seller can hold given this motion, and therefore what volume from `M5` the team can absorb. A funnel larger than capacity produces slow responses and lost deals nobody records as lost.
11. **Where the motion breaks.** The segment or deal shape this motion cannot serve, and what happens to those deals.

## Evidence rules by regime

- **Greenfield.** Cycle length is a guess and is usually optimistic. Plan the ramp with a cycle at least 50% longer than expected and say that is what is being done.
- **Extension.** Use the existing cycle as a baseline and state what makes this one different.
- **Repositioning.** A new buyer changes the motion. State whether the current sales team can execute the new one.

## Quality tests

- Does the cost of the motion leave margin at the price in `P5`?
- Is every stage exit criterion an observable event?
- Does the capacity in section 10 match the volume the channel plan expects?
- Is the pilot bounded by a date and a criterion?

## Canonical extract

```
V2 — Sale Type
Motion:              <consultative | transactional | PLG | partner-led | hybrid>
Affordable because:  <cost of motion vs. P5 price>
Cycle:               <duration by segment>
Stages:              <names with exit criteria>
Involved:            <roles, and where cost accumulates>
Marketing prepares:  <beliefs that must exist before contact>
Pilot:               <exists? terms? conversion?>
Procurement path:    <steps and typical duration>
Seller capacity:     <active deals per seller>
```

## Probing questions

- How many touches before the first meaningful conversation, and who does them?
- What is the longest stage, and what actually happens during it?
- Which deals do you lose to no-decision rather than to a competitor?
- How many deals can one person carry before response time degrades?

## Contradictions to watch

- Consultative motion on a ticket that cannot fund it, or self-serve on a decision `P4` describes as multi-stakeholder → structural mismatch; `V7` will price it.
- Cycle length exceeds the ramp assumed in `P8`'s revenue case.
- Marketing preparation assumed in section 6 is not in the `M7` inventory.
