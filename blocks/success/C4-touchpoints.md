---
code: C4
board: success
title: Touchpoints
hard_deps: [C2, C3]
produces: [contact_calendar, trigger_based_contacts, ownership, escalation_path]
downstream: [C6, C7, C8]
---

# C4 — Touchpoints

## What this block decides

When the company contacts the customer after onboarding, why, and with what. Attention is finite; this block decides where it goes, which means deciding where it does not.

## What this block is not

- Not a check-in schedule. "Monthly check-in" with no purpose is a meeting the customer cancels by month three.
- Not the nurture content plan. `C6` decides content; this decides moments.
- Not evenly spaced by default. Even distribution of attention is the absence of a retention strategy.

## Required sections

1. **Calendar-based touchpoints.** Scheduled contacts, each with a purpose and an agenda: post-onboarding review, quarterly business review, renewal preparation, anniversary. For each: who attends from `C1`, what evidence is brought, what decision or outcome is expected.
2. **Trigger-based touchpoints.** Contacts fired by events rather than dates: usage drop, milestone reached, sponsor change, support escalation, feature adoption, contract threshold. Trigger-based contact outperforms calendar-based contact and requires the instrumentation `P7` may have listed as missing.
3. **Distribution against risk.** Touchpoints mapped against the churn window from `C2` section 2. Attention concentrated where churn concentrates, not spread evenly. Say explicitly which period gets the most contact and why.
4. **Contact by stakeholder.** Different roles from `C1` need different contact at different frequency. The executive sponsor needs infrequent, high-signal contact; the daily user needs responsiveness rather than meetings.
5. **The renewal runway.** When renewal preparation begins, working back from the decision-formation point in `C2` section 3. Beginning at the renewal date is beginning after the decision.
6. **Evidence of value.** What is brought to each touchpoint to demonstrate the `P7` criteria are being met. A review without evidence becomes a satisfaction conversation, which correlates poorly with renewal.
7. **Ownership.** Who owns each touchpoint, and what happens when that person is unavailable. Single-threaded relationships fail on vacation schedules.
8. **Cost per account.** Total human hours per account per month, against the price in `P5`. This is cost to serve, and it is the number most often left out of unit economics entirely.
9. **Tiering.** Whether all accounts receive the same treatment or contact scales with value. If tiered, the criteria and what the lowest tier actually receives.
10. **Escalation.** What happens when a touchpoint reveals a problem: who is told, in what time, with what authority to act.
11. **Silence protocol.** What happens when a customer stops responding. The most informative signal available and the one most often left unactioned.

## Evidence rules by regime

- **Greenfield.** Over-contact early to learn, then reduce deliberately. State when the reduction happens so it is a decision rather than a drift.
- **Extension.** The account already has touchpoints from other products. Consolidate rather than adding — the customer experiences one company.
- **Repositioning.** Existing customers need a contact plan for the change itself, separate from the ongoing cadence.

## Quality tests

- Does every touchpoint have a purpose that is not "check in"?
- Do touchpoints cluster where `C2` says churn concentrates?
- Is the cost per account calculated against the price?
- Is there a defined response to silence?

## Canonical extract

```
C4 — Touchpoints
Calendar-based:      <contacts with purpose and attendees>
Trigger-based:       <event → contact → owner>
Concentrated in:     <the period, matching the C2 churn window>
Renewal runway:      <starts how long before renewal>
Evidence brought:    <what demonstrates P7 criteria>
Cost per account:    <hours/month> ; vs. price: <fits: y/n>
Tiering:             <criteria and what the lowest tier gets>
Silence protocol:    <what happens after how long>
```

## Probing questions

- Which of your scheduled meetings would the customer cancel first?
- What do you do the week a customer's usage drops by half?
- When do you first mention renewal, and when do they decide?
- What does an account in your lowest tier actually receive?

## Contradictions to watch

- Touchpoints are evenly spread while `C2` names a concentrated churn window → attention is not where risk is.
- Trigger-based contacts require instrumentation `P7` listed as missing.
- Cost per account exceeds what `P5` supports → high-touch service on a ticket that cannot fund it.
