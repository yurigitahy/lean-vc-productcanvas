---
code: P3
board: product
title: Ideal Customer Profile
hard_deps: [P1, P2]
produces: [icp_definition, firmographics, fit_signals, disqualifiers, awareness_levels, adjacent_segments]
downstream: [P4, P5, M1, M5, V1, V2, C1]
---

# P3 — Ideal Customer Profile

## What this block decides

Which organizations this product is for, defined by observable attributes rather than by aspiration. The test of a good ICP is operational: someone in sales must be able to look at a company and say yes or no without asking the product team.

When the canvas scope is per-ICP, this block is a **constraint block**: the ICP is given, and the work is to state it precisely and check that `P1` and `P2` actually hold for it. Say so at the top of the block.

## What this block is not

- Not a market segment. "Mid-market retail" is a segment. An ICP is the subset of that segment where the problem in `P1` is acute, the value in `P2` is perceivable, and the budget exists.
- Not a persona. Persona is a person, ICP is an organization. `P4` handles people.
- Not a wish list of logos. Aspirational ICPs produce qualification criteria nobody can apply.
- Not everyone who could use it. Could-use is a capability statement; ICP is a prioritization.

## Required sections

1. **ICP definition.** One paragraph naming the organization type, in the form: companies that [structural characteristic] and therefore [experience the P1 problem acutely].
2. **Firmographics.** Size, revenue band, headcount, geography, industry, ownership structure, growth stage. Each with a stated reason it matters — an attribute without a mechanism is a filter borrowed from someone else's ICP.
3. **Operational signals of fit.** Observable evidence that the `P1` problem is present and expensive here: volume thresholds, team structures, tool stacks, process characteristics. These are the raw material for the `V1` lead score.
4. **Budget and authority.** Which budget line pays, who controls it, what approval threshold triggers additional signatures. Determines cycle length in `V2` and the persona set in `P4`.
5. **Technical and operational prerequisites.** What the customer must already have for the product to work: data, integrations, staff, process maturity. Prerequisites become onboarding scope in `C3` and disqualifiers in `V1`.
6. **Absorption capacity.** Whether the organization can actually adopt this: change tolerance, competing initiatives, available attention. High-fit organizations that cannot absorb produce the slowest, most expensive churn.
7. **Disqualifiers.** The attributes that make a company a bad customer even when they want to buy. Named explicitly, because sales will otherwise sell to them. Include the ones that are commercially attractive and operationally destructive.
8. **Awareness levels.** How this ICP moves from unaware to purchase-ready: what they believe at each stage, what question they are asking, and what changes their mind. Five stages: unaware, problem-aware, solution-aware, product-aware, ready to buy. This section feeds `M2`, `M7`, and `V3` directly and is often the most useful part of the block.
9. **Where they concentrate.** Associations, events, platforms, publications, communities, and vendor relationships. Raw material for `M5`.
10. **Adjacent segments.** Who almost fits, and what would have to be true for them to fit. Prevents the ICP from silently expanding under sales pressure.
11. **Sizing.** How many organizations match, and how that was estimated. A rough count with a stated method beats a precise number with none.
12. **Beachhead.** If the ICP is broader than the company can serve now, which subset is first and why. Sequence, not exclusion.

## Evidence rules by regime

- **Greenfield.** Fit signals are hypotheses. Rank them by how cheaply each can be tested against a list of real companies.
- **Extension.** Derive the ICP from the existing base: which current customers would buy this, and what do they have in common that the others do not. Say explicitly which attributes came from data and which from assumption.
- **Repositioning.** The ICP must be derived from who currently retains and expands, not from who the company wishes bought it. If retention data contradicts the stated ICP, the data wins and the block says so.

## Quality tests

- Could a salesperson apply this definition to a list of 100 companies and sort them without asking a question? If not, the ICP is not operational yet.
- Is every firmographic attribute tied to a mechanism, or are some there because they are easy to filter on?
- Do the disqualifiers include at least one profitable-looking customer type? An ICP with only unattractive disqualifiers has not made a real choice.
- Does the awareness ladder describe belief changes, or only funnel stages?

## Canonical extract

```
P3 — Ideal Customer Profile
ICP:                 <organization type + why the P1 problem is acute there>
Firmographics:       <size, geography, industry, stage>
Top fit signals:     <three observable, verifiable signals>
Budget line:         <where the money comes from> ; approver: <role>
Prerequisites:       <what must already exist>
Disqualifiers:       <up to three, including one attractive-looking one>
Dominant awareness:  <which stage most of the ICP sits in today>
Beachhead:           <first subset, and why>
```

## Probing questions

- Which of your best current customers would you not sell to again, and what do they have in common?
- What is true of a company the day before it becomes a good fit?
- Which attribute do you filter on today that has never predicted anything?
- Where does this ICP go when they have a problem they cannot name yet?

## Contradictions to watch

- The ICP cannot perceive the value in `P2` without education → `M7` and `V2` carry a cost that has not been budgeted.
- The ICP cannot afford the price implied by `P2`'s economic value → either the ICP or the pricing model in `P5` is wrong.
- Fit signals require data the company cannot obtain before a sales call → `V1` will score on proxies; say which.
