---
code: C6
board: success
title: Nurture Cadence
hard_deps: [M7, C4, C5]
produces: [customer_content_plan, lifecycle_triggers, adoption_campaigns, community]
downstream: []
---

# C6 — Nurture Cadence

## What this block decides

What the customer receives between touchpoints — the communication that maintains value, deepens adoption, and keeps the company present without requiring a meeting.

## What this block is not

- Not a newsletter. A newsletter is a format; this is a purpose per message.
- Not marketing to existing customers. The audience already bought; the argument is different.
- Not the touchpoint calendar. `C4` decides moments requiring a person; this covers what runs between them.

## Required sections

1. **Purpose by lifecycle stage.** Post-onboarding, steady state, pre-renewal, and post-renewal each need different communication. Stage-blind nurture reads as noise.
2. **Adoption campaigns.** Sequences that drive specific behaviors: adopting an underused capability tied to the `P7` criteria, completing a configuration, involving a second team. Each with the behavior targeted and how it is measured.
3. **Trigger-based messages.** Fired by usage or lifecycle events rather than dates: a milestone reached, a capability unused after a defined period, a new user added, a threshold crossed. Requires the instrumentation `P7` may have flagged as missing.
4. **Content inventory.** What is sent, drawn primarily from `M7`. Product updates, use cases from other customers, benchmarks, best practice. State what is reused and what is customer-only.
5. **Reuse from acquisition.** Which `M7` pieces serve existing customers directly, and which must be rewritten because the audience already bought. The reuse is the main lever available to a small team; the rewrite is the part usually skipped.
6. **Cadence and volume.** How often, on what channels, with what unsubscribe consequence. Over-communication with existing customers costs the channel that renewal preparation depends on.
7. **Segmentation.** By adoption level, by segment from `P3`, by stakeholder role from `C1`. The executive sponsor and the daily user need different messages at different frequencies.
8. **Community or peer exposure.** Whether customers are connected to each other, and what that produces: reduced support load, peer proof, referral input to `M6`. Also what it risks — a public place for complaints, which most companies discover after launching one.
9. **Renewal preparation content.** What arrives in the runway from `C4` section 5, building the evidence of value before the conversation rather than during it.
10. **Ownership and measurement.** Who writes and sends, and what each sequence is expected to move: adoption rate, support deflection, expansion signals.

## Evidence rules by regime

- **Greenfield.** With few customers, personal communication beats sequences. State the customer count at which automation begins.
- **Extension.** Existing customers already receive communication from the company. Consolidate. Two teams emailing the same person is a familiar and avoidable failure.
- **Repositioning.** Existing customers need to understand what changed and what it means for them, separately from acquisition messaging.

## Quality tests

- Does every sequence target a behavior, or only deliver information?
- Is anything sent to customers that was written for prospects and never adjusted?
- Does total volume, across all teams, hold up from the customer's side?
- Does the renewal runway carry evidence, or announcements?

## Canonical extract

```
C6 — Nurture Cadence
By stage:            <post-onboarding | steady | pre-renewal purposes>
Adoption campaigns:  <behavior targeted → sequence → measure>
Triggers:            <event → message>
Reused from M7:      <which> ; customer-only: <which>
Cadence:             <frequency by channel and segment>
Community:           <exists? what it produces and risks>
Renewal runway:      <what is sent in the C4 runway>
Owner:               <who writes and sends>
```

## Probing questions

- How many emails does one customer receive from your company in a month, across all teams?
- Which capability do customers pay for and never adopt?
- What do you send in the ninety days before renewal?
- Would a customer notice if this stopped?

## Contradictions to watch

- Triggers depend on instrumentation `P7` said does not exist.
- Content reused from `M7` addresses buyers rather than owners, and reads as a pitch to someone who already bought.
- Adoption campaigns target capabilities the price tier in `P5` does not include.
