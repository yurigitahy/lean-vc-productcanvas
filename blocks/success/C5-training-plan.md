---
code: C5
board: success
title: Training Plan
hard_deps: [P6, C1, C3]
produces: [curriculum, delivery_format, checkpoints, certification, internal_enablement]
downstream: [C6]
---

# C5 — Training Plan

## What this block decides

What each stakeholder must be able to do, how they learn it, and how competence is confirmed. Training that teaches the product rather than the customer's job produces users who have been trained and cannot work.

## What this block is not

- Not documentation. Documentation is reference; training is capability transfer.
- Not a feature walkthrough.
- Not one curriculum for everyone. Roles from `C1` need different things.

## Required sections

1. **Capability targets by role.** For each stakeholder in `C1`, what they must be able to do unaided, stated as tasks in their own work rather than as product features. This section is the whole plan; the rest is delivery.
2. **Sequence against the onboarding path.** Training mapped onto the `C3` timeline, so each capability arrives when it is needed rather than in a single session at the start. Front-loaded training is forgotten before it is used.
3. **Delivery format by capability.** Live session, recorded, written, in-product guidance, or shadowing. Chosen by what the capability requires: judgment needs live, procedure does not.
4. **Materials required.** Manuals, videos, quick references, sandbox environments, sample data. With owner and date. Cross-check with `M7` and `V5` — a surprising amount is reusable.
5. **Checkpoints.** How competence is confirmed at each stage: a task completed, a configuration made, a report produced. Observable, not self-reported.
6. **Certification or homologation.** Whether formal sign-off exists, who gives it, and what it gates. In regulated or high-risk contexts this may be a contractual requirement.
7. **Ongoing and refresher training.** What happens when the product changes, when staff turn over, and when a new team is added. Turnover is routine, not an edge case, and a customer with no path to train a replacement degrades quietly.
8. **Self-serve path.** What a customer can learn without the company's time, and what that saves per account. Directly a cost-to-serve lever from `C4` section 8.
9. **Train-the-trainer.** Whether a customer-side owner is created who can train others. In large accounts this is usually the difference between adoption in one team and adoption across the organization.
10. **Internal enablement.** What the company's own CS and support teams must know, and when they learn it relative to the first customer. Frequently later than it should be.
11. **Portfolio context.** From `P6`: what the customer already knows from other products in the portfolio, and what must not be re-taught.

## Evidence rules by regime

- **Greenfield.** The first customers reveal what training is actually needed. Plan the first three as live and observed, then standardize.
- **Extension.** Reuse existing training infrastructure and state what is new. Do not re-teach what the customer learned for the parent product.
- **Repositioning.** Existing customers were trained on the old framing. Decide whether they are retrained and who pays for it.

## Quality tests

- Is every capability target stated as something the person does in their job, not in the product?
- Do checkpoints observe a task, or ask whether someone feels ready?
- Is there a path for a customer to train a replacement without the company?
- Does the effort here fit the touch model in `C3` section 11?

## Canonical extract

```
C5 — Training Plan
Capability targets:  <by role, as job tasks>
Sequence:            <mapped onto the C3 timeline>
Formats:             <capability → format, with the reason>
Checkpoints:         <observable confirmations>
Self-serve path:     <what needs no company time>
Train-the-trainer:   <exists? who?>
Internal enablement: <what CS and support must know, and when>
Materials owed:      <what, owner, date>
```

## Probing questions

- What can a user do after training that they could not do before, in their own words?
- What happens when the person you trained leaves?
- Which training session do customers reschedule most?
- What are you teaching that documentation would cover better?

## Contradictions to watch

- Training covers product features while `C3` defines a path to a specific outcome → the two are teaching different things.
- Effort exceeds the touch model the price in `P5` supports.
- Portfolio overlap from `P6` is being re-taught, costing time on both sides.
