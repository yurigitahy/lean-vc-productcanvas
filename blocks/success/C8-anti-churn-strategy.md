---
code: C8
board: success
title: Anti-Churn Strategy
hard_deps: [P7, V3, C2, C4]
produces: [early_warning_system, intervention_playbooks, save_offers, churn_learning_loop]
downstream: []
---

# C8 — Anti-Churn Strategy

## What this block decides

How churn is detected before it is announced, what is done about it, and what is learned from the cases that end anyway. By the time a customer says they are leaving, the decision is usually months old.

## What this block is not

- Not a retention discount policy. Discounting to save an account that is not receiving value postpones the cancellation and reduces its price.
- Not a satisfaction survey program. Satisfaction correlates weakly with renewal, particularly where the person surveyed is not the person deciding.
- Not a set of arguments for the exit conversation, though it includes some.

## Required sections

1. **Early warning signals.** Ranked by predictive strength: failure to reach the `P7` moment of value, usage decline, sponsor departure, support pattern changes, silence, missed touchpoints from `C4`, non-adoption of the capability the value depends on. Each with a threshold and the data source. Signals must measure what `P7` calls success, not engagement — watching logins while success is defined as outcome produces warnings that arrive after the decision.
2. **Signal to owner.** Which signal fires what alert to whom, in what time frame. A warning system with no owner is a dashboard.
3. **Intervention playbooks.** For each of the main churn causes: unrealized value, sponsor change, budget pressure, competitor displacement, and the problem in `P1` no longer being a priority. For each, what is done, by whom, and within what window. Distinguish causes that are recoverable from causes that are not.
4. **The unrecoverable cases.** Where nothing the company does changes the outcome: the customer was mis-sold against `V1`, was acquired, or exited the market. Naming these prevents effort being spent where it cannot work — and each one should feed back into `V1` as a qualification lesson.
5. **Reuse of sale objections.** From `V3`: the reasons a customer leaves are frequently the objections that were overcome rather than resolved during the sale. Map churn causes back to objections and mark the ones that recur.
6. **Save offers.** What can be offered, by whom, within what authority — pause, downgrade, extended term, restart of onboarding, service credit. With the rule that distinguishes a save that restores value from a save that only delays the decision.
7. **The exit conversation.** How a cancellation conversation is run: what is asked, what is offered, and what is documented. Ask what actually happened, not what the exit form's categories permit.
8. **Root cause capture.** How the real reason is recorded, distinct from the stated reason. Exit-interview answers are polite and rarely accurate; the real cause is usually found in the timeline.
9. **The learning loop.** Where churn findings go: `V1` when it is a qualification failure, `C3` when it is an onboarding failure, `P2` when it is a promise failure, `P5` when it is a value-for-price failure. Churn that is only counted teaches nothing.
10. **Voluntary versus structural.** Separating customers who chose to leave from those who could not stay. The two demand different responses and blending them into a single churn rate hides both.
11. **Win-back.** Whether departed customers are re-approached, when, and on what basis. Frequently the cheapest pipeline available and almost always ignored.

## Evidence rules by regime

- **Greenfield.** No churn data exists. Build the instrumentation before the first cohort renews, or the first churn will be unexplained.
- **Extension.** Existing churn reasons from adjacent products are the best available predictor. Use them.
- **Repositioning.** Churn may rise during transition. State the expected level and how it is distinguished from ordinary churn.

## Quality tests

- Do the warning signals measure the `P7` success criteria, or engagement proxies?
- Does every signal have an owner and a response window?
- Does the playbook set include a case where the answer is to let the customer go?
- Does churn learning reach `V1` and `C3`, or stop at a report?

## Canonical extract

```
C8 — Anti-Churn Strategy
Warning signals:     <signal → threshold → source → owner>
Strongest predictor: <the one signal that matters most>
Playbooks:           <cause → intervention → window>
Unrecoverable:       <causes where intervention does not work>
Recurring objections:<the V3 objections that reappear as churn causes>
Save authority:      <what can be offered, by whom>
Root cause capture:  <how the real reason is recorded>
Learning routes to:  <V1 | C3 | P2 | P5>
```

## Probing questions

- What did you know, and when, about the last customer who left?
- Which churned customers should never have been sold to?
- What do you offer to keep an account, and does it restore value or delay the decision?
- Who reads the churn reasons and changes something because of them?

## Contradictions to watch

- Warning signals track engagement while `P7` defines success as outcome → warnings arrive after the decision.
- The churn window in `C2` is earlier than the first scheduled touchpoint in `C4` → the customer decides before anyone talks to them.
- Save offers breach the pricing rules in `P5` and become the real price list.
