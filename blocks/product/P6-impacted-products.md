---
code: P6
board: product
title: Impacted Products
hard_deps: [P2, P5]
produces: [upstream_dependencies, downstream_dependents, synergies, cannibalization, integration_debt]
downstream: [P8, M6, C5, C7]
---

# P6 — Impacted Products

## What this block decides

How this product sits inside the portfolio: what it depends on, what will depend on it, what it feeds, and what it takes from. For a single-product company this block is short but not skippable — the dependencies are external instead of internal.

## What this block is not

- Not an integration list. Integrations are a means; this block is about demand and capability flow.
- Not a roadmap. Sequencing is `P8`.
- Not an architecture diagram, though it may reference one.

## Required sections

1. **Upstream dependencies.** Products, platforms, or data sources this one needs to keep the `P2` promise. For each: what specifically is needed, who owns it, and what happens if it changes or degrades.
2. **Downstream dependents.** What will rely on this product once it exists. Creates obligations that outlast the launch and constrain later pricing changes.
3. **Demand flow.** Which products generate demand for this one, and which this one generates demand for. Directional, with the mechanism named — shared customer, natural next step, or forced adjacency.
4. **Synergies worth exploiting.** Concrete: shared data, shared onboarding, shared contract, shared channel. For each, what it saves or unlocks, and what it costs to realize.
5. **Cannibalization.** Which existing revenue this product may displace, and whether that is intentional. Intentional cannibalization is a strategy; unintentional is a surprise in a board meeting.
6. **Conflicts.** Where this product competes for the same budget line, the same buyer's attention, or the same internal team as another product. Internal competition is real competition.
7. **Integration debt.** What must be built or changed in other products for this to work, who owns that work, and whether it is scheduled. Unscheduled integration debt is the most common cause of a launch slipping after the marketing is booked.
8. **Data and identity.** Whether the customer is the same entity across products, whether records reconcile, and whether usage is visible in one place. Determines whether `C7` cross-sell is operationally possible or only conceptually attractive.
9. **Portfolio position.** Whether this is an entry product, an expansion product, a retention product, or a defensive one. Each implies a different bar in `P8` and a different role in `C7`.
10. **What happens if it is not built.** Which other products are affected, and how. Frequently the strongest argument in `P8`.

## Evidence rules by regime

- **Greenfield.** Dependencies are mostly external: platforms, data providers, model vendors. Treat vendor concentration as a named risk with a repricing scenario.
- **Extension.** This is the block that decides whether an extension succeeds. Every claimed synergy must name the team that will deliver it and whether that team has been asked.
- **Repositioning.** The product already sits in the portfolio. Document the current position before proposing the new one, including dependencies nobody documented.

## Quality tests

- Does every claimed synergy have an owner and a date, or is it an aspiration?
- Is any dependency owned by a team that has not agreed to it?
- Does cross-sell in `C7` require identity reconciliation described in section 8 as absent?
- Is the cannibalization number estimated, or asserted to be zero?

## Canonical extract

```
P6 — Impacted Products
Depends on:          <products/platforms, and what specifically>
Depended on by:      <products, and what obligation that creates>
Generates demand for:<products> ; fed by: <products>
Real synergies:      <the ones with an owner and a date>
Cannibalizes:        <revenue at risk, intentional or not>
Integration debt:    <what must be built elsewhere; scheduled? y/n>
Portfolio position:  <entry | expansion | retention | defensive>
```

## Probing questions

- Which team has to do work for this to launch and has not been told?
- If the upstream vendor doubled its price, what happens to `P5`?
- Which existing product's renewal gets harder if this one exists?
- Can you see one customer's usage across all products today, in one place?

## Contradictions to watch

- `P2`'s mechanism requires a capability from a product not listed here → the dependency map is incomplete.
- `C7` proposes cross-sell into products this block does not map as related → one of the two is wrong.
- `M6` proposes a network effect that depends on cross-product data this block says is not reconciled.
