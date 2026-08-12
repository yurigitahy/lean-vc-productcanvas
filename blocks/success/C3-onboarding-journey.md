---
code: C3
board: success
title: Onboarding Journey
hard_deps: [P2, P7, C1]
produces: [onboarding_timeline, milestones, effort_split, first_value_path, failure_signals]
downstream: [C4, C5]
---

# C3 — Onboarding Journey

## What this block decides

The path from purchase to the moment of value defined in `P7`, as a timeline with milestones, owners, and effort on both sides. Onboarding is where the promise in `P2` is either kept or quietly abandoned.

## What this block is not

- Not a product tutorial. Teaching the interface is `C5`; this is about reaching an outcome.
- Not a checklist of everything that must be configured. Configuration serves the path to value, not the reverse.
- Not a fixed 30-60-90 template applied because it is familiar.

## Required sections

1. **The path to first value.** The shortest sequence of steps from signature to the `P7` moment of value. Everything else in onboarding is secondary to this sequence and should be scheduled after it.
2. **Timeline with milestones.** Week by week, with a completion criterion per milestone that is observable rather than declared. Total duration must match the time to value in `P7`; if it does not, one of the two blocks is wrong.
3. **Effort split.** What the company does and what the customer must do, in hours, by stakeholder from `C1`. Customer effort is the most common unstated cost in a purchase and the most common cause of stalled implementations.
4. **Prerequisites.** What the customer must have ready before starting: data, access, decisions, people. From `P3` section 5. Prerequisites discovered mid-onboarding cost weeks.
5. **Standard versus adapted journey.** Whether this product follows the company's standard onboarding or needs its own, and which parts differ. If adapted, say what makes it different — usually the prerequisites or the stakeholder set.
6. **Kickoff.** What happens in the first meeting: expectations set, effort confirmed, success criteria from `P7` agreed with the customer in their words, sponsor engagement confirmed. Everything that goes wrong later was usually available to be seen here.
7. **The first-week experience.** What the customer sees, feels, and can do in the first week. The strongest predictor of eventual adoption and the part most often designed last.
8. **Handoff from sales.** What is received from `C1` section 8, and how the customer experiences the transition. Being re-asked questions they answered during the sale is the fastest way to spend goodwill.
9. **Stall signals.** What indicates onboarding is stalling — a missed milestone, an unresponsive implementer, a sponsor who stops attending — and what happens when each appears. Escalation defined in advance, with a named owner.
10. **Definition of done.** What must be true for onboarding to be complete: usage thresholds, milestone completion, and confirmation from the owner of success in `C1`. Without this, onboarding ends when the CS team stops paying attention.
11. **Scale shape.** How much of this is human and how much is self-serve, and what that costs per customer against the price in `P5`. High-touch onboarding on a low ticket erodes margin silently and appears in `V7` as contribution margin that does not match the plan.

## Evidence rules by regime

- **Greenfield.** The first implementations are research. Plan them as high-touch, instrument them, and state when the process gets standardized.
- **Extension.** Reuse the existing journey where the customer is the same, and state what the new product adds.
- **Repositioning.** Existing customers may need re-onboarding onto a changed product. Decide whether that happens and who pays for it.

## Quality tests

- Does the timeline match the time to value in `P7`?
- Is customer effort stated in hours, by role?
- Is every milestone observable?
- Does the cost of onboarding fit the price in `P5`?
- Is there an escalation owner for a stall, by name or role?

## Canonical extract

```
C3 — Onboarding Journey
Path to first value: <shortest sequence of steps>
Duration:            <weeks> ; matches P7 time to value: <y/n>
Customer effort:     <hours by stakeholder role>
Prerequisites:       <what must be ready before starting>
Kickoff covers:      <expectations, effort, success criteria, sponsor>
Stall signals:       <signal → escalation owner>
Done when:           <observable criteria>
Touch model:         <human vs self-serve split> ; cost vs price: <fits: y/n>
```

## Probing questions

- What is the earliest possible moment the customer could see this working?
- How many hours are you asking of someone who was not in the sales process?
- What do you do the first week a customer goes quiet?
- Which onboarding step exists because of your process rather than their outcome?

## Contradictions to watch

- Onboarding is longer than the time to value in `P7` → success is defined beyond the window in which the customer judges it.
- The touch model costs more than the price in `P5` supports → margin erodes as the base grows.
- Prerequisites in section 4 were not qualification criteria in `V1` → customers are sold who cannot start.
