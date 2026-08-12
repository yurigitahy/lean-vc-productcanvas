---
code: P8
board: product
title: Priority and Strategy
hard_deps: [P1, P5, P6, P7]
produces: [strategic_rationale, revenue_case, sequencing, kill_criteria, funded_demand]
downstream: [M8, V8]
---

# P8 — Priority and Strategy

## What this block decides

Why this product deserves the company's next unit of capacity, ahead of the alternatives — and what would make that answer change. This is the block that gets written as advocacy. Write it as a case that could lose.

## What this block is not

- Not a pitch to leadership, although it may become one. A pitch omits the counter-case; this block requires it.
- Not a roadmap. Sequence appears only where it affects the decision.
- Not a business plan. Three numbers with visible assumptions beat a model with none.

## Required sections

1. **Strategic classification.** Which this is: new market entry, portfolio deepening, defensive response, margin repair, or platform enablement. Each carries a different bar and a different measure of success.
2. **The case for building it.** Three to five arguments, strongest first, each tied to a specific block: the problem's size from `P1`, the revenue potential from `P5`, the portfolio effect from `P6`, the outcome from `P7`.
3. **Revenue case.** A range, not a point. Show the arithmetic: addressable accounts from `P3`, realistic penetration, price from `P5`, ramp period. State the assumption most likely to be wrong.
4. **The case against.** The strongest argument for not building it, made properly. If this section is weak, the block is advocacy and should be rewritten.
5. **Opportunity cost.** What the company will not do because it does this. Named specifically — which initiative, which team, which quarter. Priority without a displaced alternative is not priority.
6. **Funded demand.** Whether identified customers are asking for this and would pay for its development. Customer-funded development is the strongest available signal and the most commonly skipped question.
7. **What must be true.** The conditions the case rests on, ranked by how much rests on each and how uncertain each is. The top of that list is what should be tested first.
8. **Sequencing.** What ships first and why: the piece that proves the riskiest assumption, or the piece that opens revenue soonest. Say which principle is being used, because they conflict.
9. **Resource shape.** Team, budget, and duration to first revenue. Rough is fine; absent is not.
10. **Kill criteria.** What observation, by what date, would end this. A product without kill criteria does not get cancelled, it gets starved quietly for years.
11. **Decision requested.** What is being asked of whom, by when. A strategy block that ends without a decision request ends nowhere.

## Evidence rules by regime

- **Greenfield.** The revenue case is a model. Show it and mark the assumption carrying the most weight.
- **Extension.** The case must include cannibalization from `P6` netted out. A gross revenue case in an extension is a misleading case.
- **Repositioning.** The comparison is not against zero but against continuing as-is. Model both, including the cost of migrating existing customers.

## Quality tests

- Does section 4 contain an argument that would actually persuade someone?
- Does the opportunity cost name a real, currently-planned alternative?
- Are the kill criteria observable by a specific date, or are they sentiments?
- Would the revenue case survive halving the penetration assumption? Show what happens if it does not.

## Canonical extract

```
P8 — Priority and Strategy
Classification:      <new market | deepening | defensive | margin | platform>
Case in one line:    <the strongest argument>
Revenue case:        <range, over what period, at what penetration>
Strongest counter:   <the best argument against>
Opportunity cost:    <what is displaced>
Funded demand:       <customers asking / paying, or none>
Riskiest assumption: <the one carrying the most weight>
First shipment:      <what, and why that first>
Kill criteria:       <observation + date>
```

## Probing questions

- Which initiative loses a quarter so this can happen?
- Which customer would pay today for this to exist?
- What would have to happen for you to stop this in six months?
- Is the revenue case built on new accounts or on existing ones buying more?

## Contradictions to watch

- `P8` claims new market entry while `P3` describes the existing customer base → the strategic justification is inflated.
- The revenue case assumes penetration incompatible with the sale type `V2` will define → cycle length and capacity do not support the ramp.
- Kill criteria depend on measurements `P7` listed as uninstrumented.
