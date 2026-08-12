---
code: C1
board: success
title: Customer Stakeholders
hard_deps: [P3, P4, V1]
produces: [stakeholder_map, owner_of_success, sponsor_risk, handoff_protocol]
downstream: [C3, C5]
---

# C1 — Customer Stakeholders

## What this block decides

Who inside the customer must act for the product to deliver value, and what each of them needs from the relationship. The buyer and the person who makes it work are frequently different people, and the gap between them is where onboarding fails.

## What this block is not

- Not a repeat of `P4`. `P4` studies who buys; this studies who succeeds. The sets overlap and are not identical.
- Not a contact list.
- Not an org chart, except where reporting lines determine whether something gets done.

## Required sections

1. **Stakeholder map.** Every role that must act, with what specifically they must do and how much of their time it costs. Time cost is the most frequently omitted and most predictive item.
2. **The owner of success.** The single person whose standing improves if this works and suffers if it does not. If nobody holds that position, the account is at risk from day one and the block should say so plainly.
3. **The executive sponsor.** Who approved it, how engaged they will remain, and what makes them re-engage. Sponsor disappearance is the leading indicator of quiet churn.
4. **Implementers.** The people who do the technical or operational work, usually absent from `P4` because they are not in the sale. What they need: documentation, access, a named counterpart, and a realistic estimate of their effort.
5. **Users.** Who uses it daily, whether they chose it, and what it changes about their work. Users who did not choose the product and whose work becomes harder are the main source of silent non-adoption.
6. **Blockers.** Whose job, budget, or standing is threatened. Security, IT, an incumbent vendor's internal champion, or a team whose process is being replaced. Naming them in advance turns a surprise into a plan.
7. **Change from the buying group.** How the stakeholder set differs from `P4`'s buying group, and who appears now who was never spoken to during the sale. This is the handoff risk, stated as a list.
8. **Handoff protocol.** What sales transfers to CS: what was promised, what was assumed, which stakeholders were met, what was conceded in negotiation. A handoff without the concessions is a handoff that guarantees a broken promise.
9. **Turnover risk.** What happens if the sponsor or the owner of success leaves. In long-cycle products this is a routine event, not an edge case, and the response is a relationship with more than one person.
10. **Communication map.** Who hears what, at what cadence, from whom. Sets up `C4`.

## Evidence rules by regime

- **Greenfield.** The stakeholder map is a hypothesis; the first three implementations will correct it. Instrument who actually turns up.
- **Extension.** Existing relationships in the account are an asset and a constraint. State who already has the relationship and whether it transfers.
- **Repositioning.** Existing customers have a stakeholder set built around the old product. Say what changes for them.

## Quality tests

- Is there a named owner of success, or only a buyer?
- Does the map include someone who did not participate in the sale?
- Is a time cost stated for each stakeholder's contribution?
- Does the handoff include what was conceded, not only what was sold?

## Canonical extract

```
C1 — Customer Stakeholders
Owner of success:    <role> — or: none identified (risk)
Executive sponsor:   <role> ; re-engaged by: <what>
Implementers:        <roles, effort required>
Users:               <who, and whether they chose it>
Likely blocker:      <role, and what threatens them>
New since the sale:  <who appears now who was never met>
Handoff must include:<promises, assumptions, concessions>
Turnover exposure:   <what breaks if the sponsor leaves>
```

## Probing questions

- Who at the customer looks bad if this fails?
- Who has to do work they did not agree to during the sale?
- Which team is losing something because this was bought?
- If the sponsor left next month, who would still care?

## Contradictions to watch

- A stakeholder here has no corresponding persona in `P4`, without explanation → the person who makes onboarding succeed was never studied.
- The buyer from `V1` is not the owner of success and no bridge is described → onboarding starts with a handoff nobody owns.
- The effort required from implementers was never mentioned during the sale → the first surprise arrives in week one.
