---
code: P7
board: product
title: Success Criteria
hard_deps: [P1, P2, P5]
produces: [customer_success_definition, activation_moment, leading_indicators, business_kpis, time_to_value]
downstream: [P8, M1, V7, C2, C3, C8]
---

# P7 — Success Criteria

## What this block decides

What success means for the customer, when it can be observed, and by which measurements — plus the company-side indicators that follow from it. `P7` is what renewal conversations are actually about, and it is usually defined too late and too vaguely to help.

## What this block is not

- Not a metrics dashboard. A list of everything measurable is the absence of a success definition.
- Not adoption metrics dressed as outcomes. Logins are not success. Somebody's problem stopping is success.
- Not the company's revenue goals. Those are `P8`.

## Required sections

1. **Customer-side definition of success.** In the customer's language, tied to the `P1` problem. One sentence the customer would agree with at renewal.
2. **The moment of value.** The first point at which the customer experiences the promise being kept. Named as a specific, observable event. Everything in `C3` is built to reach this point faster.
3. **Time to value.** How long from purchase to that moment, realistically. If it exceeds the first billing cycle, say so — it changes `P5`'s terms, `C3`'s design, and `C8`'s early-warning window.
4. **Leading indicators.** Observable signals in the first days and weeks that predict eventual success. These are what `C8` will monitor. Each must be measurable with data the company will actually have.
5. **Lagging indicators.** The outcome measurements that confirm success after the fact, with the period over which they become meaningful.
6. **Threshold values.** Not just what is measured, but at what level it counts. "Increased conversion" is not a criterion; a stated level is.
7. **Who inside the customer judges success.** By persona, from `P4`. Different personas apply different criteria, and renewal is decided by whichever of them has the most standing. Name that persona.
8. **Company-side KPIs.** Activation rate, time to value, retention, expansion, support load. Each tied to a customer-side criterion above rather than free-floating.
9. **Instrumentation.** What must be measured and does not exist yet, who builds it, and when. Uninstrumented success criteria become opinion at renewal.
10. **Failure signatures.** What the data looks like when a customer is quietly failing. Frequently distinct from low usage: a customer can be highly active and receiving nothing.
11. **Attribution honesty.** Whether the product can be shown to have caused the outcome, or only to have coincided with it. Where attribution is weak, say what proxy will be used and what its limits are.

## Evidence rules by regime

- **Greenfield.** Criteria are proposals. Say which will be validated with the first cohort and how.
- **Extension.** Reuse instrumentation and definitions from existing products where the outcome is comparable; name where the reuse is invalid.
- **Repositioning.** Success may need redefining because the buyer changed. State the old definition, the new one, and what happens to existing customers measured against the old.

## Quality tests

- Is the moment of value a specific observable event, or a phase?
- Can every leading indicator be measured with data the company already collects or has scheduled to collect?
- Does the time to value fit inside the retention horizon `C2` will estimate? If not, one of the two blocks is wrong.
- Would the customer's own boss accept these criteria as evidence?
- Is there a criterion that would be met even if the product did nothing? Remove it.

## Canonical extract

```
P7 — Success Criteria
Customer success:    <one sentence in the customer's language>
Moment of value:     <observable event>
Time to value:       <duration> ; vs. first billing cycle: <shorter/longer>
Leading indicators:  <up to three, with thresholds>
Lagging indicators:  <up to two, with the period they need>
Judged by:           <persona from P4 with the most standing at renewal>
Company KPIs:        <activation, TTV, retention targets>
Missing instrumentation: <what must be built, by whom, by when>
```

## Probing questions

- What does the customer say in month six that proves this worked?
- What is the first thing that happens that could not have happened before?
- Which of these can you measure today, without building anything?
- If the customer succeeded but attributed it to something else, would you know?

## Contradictions to watch

- Success requires usage that `P5`'s pricing makes uneconomic for the customer → success is priced out of reach.
- Time to value exceeds the onboarding window that `C3` will define → churn from customers who technically received what they bought.
- The leading indicators measure engagement while success is defined as outcome → `C8` will warn too late.
