---
code: V8
board: sales
title: Attack Strategy
hard_deps: [P8, M8, V6, V7]
produces: [launch_sequence, target_accounts, capacity_plan, weekly_cadence, contingencies]
downstream: []
---

# V8 — Attack Strategy

## What this block decides

The commercial plan for the launch window: who is contacted in what order, by whom, with what capacity, against what weekly expectation. `M8` decides what the market hears; this decides what the company does.

## What this block is not

- Not a revenue forecast. `V7` produced the model; this is the execution against it.
- Not a project plan for building the product.
- Not a list of activities. Every action has an owner, a date, and an expected output.

## Required sections

1. **Target list.** The specific accounts or segments approached first, selected against `V1`, ordered by fit and by the timing signals from `P1`. Named where the count allows it. A launch aimed at a segment rather than at accounts starts slower than it needs to.
2. **Sequence by tier.** Design partners and warm contacts from `V6` first, then high-fit known accounts, then broad channel activation. Warm before cold, always: the first weeks produce the references the rest of the quarter needs.
3. **Weekly calendar.** For the launch window, typically eight to twelve weeks: what happens each week, who owns it, what output is expected. Enough detail that a missed week is visible in the week it is missed.
4. **Capacity.** Sellers available, deals each can carry from `V2` section 10, and therefore the volume the plan can absorb. Where capacity binds, say what is cut: volume, coverage, or quality of follow-up. It will be one of them.
5. **Coordination with `M8`.** The exact points where marketing activity and sales activity must line up: the day outreach starts relative to the announcement, which content is live before the first email, when paid amplification begins. Dates must match `M8` exactly.
6. **Partner activation.** What partners from `M5` do, when, and what they need in order to do it. Partners require more lead time than internal teams and are usually given less.
7. **Objection readiness.** Confirmation that `V3` objections have prepared answers and `V5` materials exist for the ones needing evidence. A launch that discovers its objections in the first week loses the first week.
8. **Weekly expectations.** The numbers expected each week from `V7`: conversations, meetings, opportunities, closes. Stated in advance so that a shortfall is a signal rather than a debate.
9. **Review cadence.** When the plan is reviewed, who attends, and what evidence changes it. Weekly during the launch window is the usual minimum.
10. **Contingencies.** For the three most likely failures: volume below expectation, cycle longer than modeled, a competitor response. Each with a prepared move and the trigger that fires it.
11. **Exit from launch mode.** When the launch window ends and the operation becomes steady-state, and what changes at that point. Launch intensity is not sustainable and should have a stated end.

## Evidence rules by regime

- **Greenfield.** Plan the first weeks around learning as much as around closing. The first twenty conversations are worth more as evidence than as pipeline.
- **Extension.** The existing base is the fastest path to early wins. Say how the base is approached without disrupting existing renewals.
- **Repositioning.** Existing customers and existing pipeline need handling before the market does. Contacts mid-cycle under the old positioning are the most fragile group in a repositioning.

## Quality tests

- Does every week in section 3 have an owner and an expected output?
- Do the dates match `M8` exactly?
- Does the plan fit the capacity in section 4, or does it assume an unstated hire?
- Is there a trigger that would change the plan rather than a hope that it holds?

## Canonical extract

```
V8 — Attack Strategy
First targets:       <accounts or segment, and the selection basis>
Sequence:            <warm → high-fit → broad>
Window:              <weeks> ; weekly owner: <role>
Capacity:            <sellers × deals each> ; binding constraint: <what>
Sync points with M8: <the dates that must match>
Partner activation:  <who, when, what they need>
Weekly targets:      <conversations, meetings, opportunities>
Contingencies:       <trigger → move>
Exit criteria:       <when launch mode ends>
```

## Probing questions

- Which twenty accounts are contacted in week one, and who is contacting them?
- What is the plan if week three produces half the expected meetings?
- Who does the extra work when the launch generates more interest than expected?
- What stops being done during the launch window?

## Contradictions to watch

- Dates disagree with `M8` → the launch is running on two calendars.
- Volume exceeds seller capacity from `V2` → response times degrade exactly when attention is highest.
- Weekly targets are inconsistent with the funnel model in `V7`, implying either a different funnel or an unstated hope.
