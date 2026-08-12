---
code: P1
board: product
title: Problem and Opportunity
hard_deps: []
soft_deps: [intake]
produces: [core_problem, symptoms, structural_dependency, cost_of_inaction, urgency_triggers, pain_hierarchy]
downstream: [P2, P3, P7, P8, M2, M7, V3, C8]
---

# P1 — Problem and Opportunity

## What this block decides

The problem this product exists to remove, stated so precisely that a competitor solving it differently would still recognize it as the same problem. `P1` is the only block in the canvas that must be true independently of the product. Everything else is a decision; this is a claim about the world.

## What this block is not

- Not a description of the solution. If the product were cancelled tomorrow, `P1` would still be true. Test every sentence against that.
- Not a market size argument. Opportunity here means the gap between what the customer currently endures and what is possible, not a TAM figure.
- Not the problem as the team experiences it. The team's problem is that something is hard to build. The customer's problem is that something costs them money, time, risk, or standing.
- Not a list of feature requests. Requests are the customer's proposed solution and encode their assumptions, not their problem.

## Required sections

1. **Core problem.** One paragraph. Structural, not symptomatic. The sentence should survive being read aloud to a customer without them correcting it.
2. **How the problem presents.** The symptoms, grouped: financial, operational, relational, and political. Nobody wakes up naming the structural problem; they wake up inside a symptom. Marketing and sales will speak in symptoms, so they must be enumerated here.
3. **Structural dependency or constraint.** What in the customer's situation makes this problem persist rather than resolve on its own. If the problem would resolve with ordinary effort, it is not a product opportunity.
4. **What the customer does today instead.** The status quo, named concretely: a vendor, a spreadsheet, an intern, a workaround, or acceptance. The status quo is the real competitor and appears again in `M2` and `V3`.
5. **Why it has not been solved.** Whether the constraint is technical, economic, organizational, or regulatory. Each implies a different reason the window is open now.
6. **Cost of inaction.** In money where possible, in risk where not. Twelve months of not solving it, quantified. This becomes the sales argument in `V3` and the ROI frame in `V7`.
7. **Who inside the customer feels it.** By role, and how the pain differs by role. The person who feels it is often not the person who can fix it — that gap becomes `P4` and `C1`.
8. **Urgency triggers.** The events that convert a tolerated problem into a funded one: a contract renewal, a departure, an audit, a growth threshold, a competitor move, a budget cycle. Sales cannot manufacture urgency, only detect it.
9. **Pain hierarchy.** The problem's components ranked by intensity, not by how interesting they are to solve. The ranking determines what `P2` must address first.
10. **Current state vs. desired state.** Two columns, in the customer's own terms, describing operation before and after. Avoid the product's vocabulary entirely.
11. **Evidence.** What supports this framing: interviews, tickets, lost-deal reasons, usage data, market research, or the operator's direct experience. Cite specifically. Name what is missing.
12. **What would falsify this.** The observation that would prove the problem is not real, not expensive, or not urgent. Name it, and name the cheapest way to look for it.

## Evidence rules by regime

- **Greenfield.** No internal customer evidence exists. Cite external research, competitor behavior, or the operator's direct experience, labeled as such. State the number of real conversations behind this framing; if it is zero, say so in the block.
- **Extension.** The company has customers adjacent to this problem. Tickets, calls, and churn reasons must be consulted. Reaching for external benchmarks where internal data exists is a research failure.
- **Repositioning.** Distinguish the problem the product was built for from the problem it is actually bought for. The divergence between the two is usually the reason repositioning is being considered, and it belongs in this block.

## Quality tests

- Remove the product from every sentence. Does the block still say something?
- Would a customer reading section 1 say "yes, that is my situation" or "yes, that is what your product does"? Only the first passes.
- Is there a number anywhere in sections 6 or 11? If not, name the number that should exist and does not.
- Does the pain hierarchy rank by customer intensity or by team interest? These usually differ, and the difference predicts which features get built and ignored.
- Could three different products legitimately solve this problem? If only one could, the problem was written from the solution.

## Canonical extract

```
P1 — Problem and Opportunity
Core problem:        <one sentence, product-independent>
Top three symptoms:  <the ones marketing and sales will speak in>
Status quo:          <what the customer does today instead>
Cost of inaction:    <12-month figure or the risk it stands for>
Who feels it:        <role> ; who can fix it: <role>
Urgency triggers:    <up to three events that fund a purchase>
Strongest pain:      <top of the hierarchy>
Evidence base:       <what this rests on; what is missing>
```

## Probing questions

- What did the last customer who described this problem actually say, in their words?
- What breaks first if this problem gets 30% worse?
- Who in the customer's organization is currently rewarded for the status quo continuing?
- If the customer had unlimited budget and no product like yours existed, what would they do?
- What is the last thing they bought to solve this, and why did it not close the problem?

## Contradictions to watch

- The problem is described in the product's vocabulary → the block was written backwards from a decision already made.
- The cost of inaction is smaller than the likely price in `P5` → the product may be correct and unsellable.
- The urgency triggers are absent → expect long cycles in `V2` and a nurture-heavy `M7`.
