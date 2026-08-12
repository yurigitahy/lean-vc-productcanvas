---
code: V7
board: sales
title: Metrics and Indicators
hard_deps: [P5, P7, V1, V2]
produces: [funnel_model, cac_hypothesis, conversion_expectations, payback, ramp_plan]
downstream: [V8, C2]
---

# V7 — Metrics and Indicators

## What this block decides

The numbers the commercial operation expects to produce and the assumptions inside them — stated in advance, so that results can be read as evidence rather than as surprise.

This block produces a hypothesis. Once there are paying customers, testing it belongs in a unit economics diagnostic, not here. Say so rather than duplicating that work.

## What this block is not

- Not a dashboard specification.
- Not a target set by working backwards from a revenue goal. That produces numbers, not expectations.
- Not a unit economics model. It is the input to one.

## Required sections

1. **Funnel model.** Stage by stage from `V2`, with expected conversion at each and the reasoning behind each rate. Rates asserted without reasoning are decoration.
2. **Volume requirements.** Working backwards from the revenue case in `P8`: how many qualified leads per month, and whether `M5` can produce them. This arithmetic is where optimistic plans usually fail, and it is cheap to do now.
3. **CAC hypothesis, fully loaded.** Media plus sales payroll plus tooling plus events plus partner commissions, divided by expected new customers. Counting only media typically understates CAC substantially in a sales-assisted motion and makes payback look short.
4. **Contribution margin per customer.** Price from `P5`, less variable delivery cost, less cost to serve. Approximate is acceptable; omitting cost to serve is not, since that omission is the usual reason healthy-looking economics produce no cash.
5. **CAC payback.** CAC divided by monthly contribution margin, in months. State it plainly against the retention horizon `C2` will estimate. If payback exceeds that horizon, the model does not fund itself and everything downstream needs revisiting.
6. **Cycle and ramp.** How long from first contact to revenue, and therefore how long from launch to meaningful revenue. Include seller ramp: a new seller is not productive on day one.
7. **Expectations by channel.** Conversion and CAC by channel from `M5`, as hypotheses. Aggregate CAC averages a good channel and a bad one into a number that supports no decision.
8. **Leading indicators.** What is watched weekly, before revenue arrives, to know whether the model is holding: response rates, meeting rates, stage-to-stage movement, cycle length drift.
9. **Instrumentation.** What must be tracked, in what system, by whom, and what currently cannot be tracked. Untracked assumptions become folklore within two quarters.
10. **What would falsify the model.** The observation that would prove the funnel model wrong, and the point at which the plan is revised rather than defended.
11. **Management expectations.** What leadership should expect to see and when, especially during the period where the pipeline is building and revenue has not arrived. Setting this in advance is the difference between a normal ramp and a crisis meeting.

## Evidence rules by regime

- **Greenfield.** Every rate is borrowed or invented. Say which, and give a range rather than a point.
- **Extension.** Use the existing funnel as the baseline and state where this product differs and why.
- **Repositioning.** Historical rates describe the old positioning. State which are expected to change and in which direction.

## Quality tests

- Does each conversion rate have a stated reason?
- Does CAC include sales payroll and tooling?
- Does contribution margin include cost to serve?
- Does the required lead volume match what `M5` can plausibly produce?
- Is there a stated point at which the model is declared wrong?

## Canonical extract

```
V7 — Metrics and Indicators
Funnel:              <stage → conversion → basis>
Leads required:      <per month, to hit the P8 case>
CAC (fully loaded):  <figure and what is included>
Contribution margin: <per customer per month>
CAC payback:         <months> ; vs. C2 horizon: <shorter/longer>
Ramp:                <time from launch to meaningful revenue>
By channel:          <where CAC and conversion are expected to differ>
Cannot track:        <what is uninstrumented>
Falsified if:        <observation and date>
```

## Probing questions

- What is your CAC if you include everyone who touches a deal?
- How many leads per month does the revenue case actually require, and where do they come from?
- What do you expect to see in month two that tells you this is working?
- When does the plan get revised instead of defended?

## Contradictions to watch

- Payback exceeds the retention horizon in `C2` → the customer leaves before paying for their own acquisition. This is the canvas's most consequential contradiction; hand off to a unit economics diagnostic.
- Required lead volume exceeds what `M5` can produce → the revenue case in `P8` is unreachable regardless of execution.
- Conversion rates assume a motion different from `V2`.
