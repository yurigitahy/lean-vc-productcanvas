---
code: V6
board: sales
title: Demand Anticipation
hard_deps: [M7, M8, V1]
produces: [pre_launch_plan, waitlist_mechanics, design_partners, warm_pipeline_target]
downstream: [V8]
---

# V6 — Demand Anticipation

## What this block decides

What is done before the product is available, so that launch day starts with a pipeline instead of with an announcement. A launch that begins generating demand on launch day has wasted the months of building.

## What this block is not

- Not the launch itself. `M8` is the moment; this is the runway.
- Not a waitlist by default. A waitlist with no mechanism for advancing interest is a list of people who will not remember signing up.
- Not pre-selling something that cannot be delivered. Everything promised here is bounded by `P2`, including its staging.

## Required sections

1. **Objective.** What state the pipeline should be in on launch day, in numbers: qualified conversations held, design partners committed, waitlist of stated size and known quality. Without a number, this block becomes activity.
2. **Warming the market.** Which `M7` content runs before launch to establish the problem framing from `P1` and the `M2` position, so the launch lands on prepared ground rather than explaining itself.
3. **Audience assembly.** How an audience is built ahead of the product: list, community, events, partner audiences from `M5`. What is being collected, and with what permission.
4. **Design partners or early customers.** How many, chosen by what criteria from `V1`, and what each side commits to. What they get — pricing, influence, support — and what is expected in return: usage, feedback, a reference. Undocumented, this becomes a set of permanent discounts.
5. **Qualification during anticipation.** Interest is not intent. How signals collected pre-launch are scored against `V1`, so launch-day outreach starts with the ones that matter.
6. **What is promised and what is not.** Explicit boundaries. Pre-launch conversations create expectations that arrive as churn later if the delivered product is narrower than the anticipated one.
7. **Sequence and timing.** How many weeks of runway, what runs when, and the last responsible moment for each action.
8. **Objection collection.** Pre-launch conversations are the cheapest source of real objections. What is captured, by whom, and how it flows back into `V3` and `M2`.
9. **Handoff to launch.** What `M8` and `V8` receive from this: the list, the segmentation, the objection log, the committed partners.
10. **Failure mode.** What happens if anticipation produces less than the target — whether the launch date moves, the target moves, or the plan proceeds anyway. Decided in advance, not in the week of.

## Evidence rules by regime

- **Greenfield.** This is where the riskiest assumptions in `P8` can be tested cheaply. Weight the plan toward learning, not only toward list size.
- **Extension.** The existing base is the fastest source of anticipation and the easiest to over-ask. State how many times the base is contacted before launch.
- **Repositioning.** Anticipation must not confuse existing customers about what they already have. State what they are told and when.

## Quality tests

- Is there a number in section 1?
- Are design partner commitments written down on both sides?
- Does pre-launch outreach qualify, or only collect?
- Is the failure decision made in advance?

## Canonical extract

```
V6 — Demand Anticipation
Launch-day target:   <conversations, partners, list size and quality>
Runway:              <weeks> ; warming content: <which M7 pieces>
Audience source:     <where the pre-launch audience comes from>
Design partners:     <how many, criteria, what each side commits>
Promised / not:      <explicit boundaries>
Objection capture:   <how it flows back to V3>
If target missed:    <date moves | target moves | proceed>
```

## Probing questions

- Who would take a call about this next week, by name?
- What do you tell someone who wants it now and cannot have it?
- What are you learning during the runway that would change the launch?

## Contradictions to watch

- Pre-launch promises exceed what `P2` delivers at launch, including staging → churn arrives in the first quarter.
- Anticipation targets require volume from channels `M5` cannot produce in the runway.
- Design partner terms conflict with the pricing rules in `P5`.
