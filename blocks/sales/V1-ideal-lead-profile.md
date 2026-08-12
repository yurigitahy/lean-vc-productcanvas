---
code: V1
board: sales
title: Ideal Lead Profile
hard_deps: [P3, P4, M5]
produces: [qualification_criteria, scoring_model, disqualifiers, intake_form, routing_rules]
downstream: [V2, V4, V6, V7, C1]
---

# V1 — Ideal Lead Profile

## What this block decides

How a lead is judged before sales time is spent on it. `P3` describes the organization the product is for; this block converts that into criteria a person or a system can apply with the information actually available at first contact.

## What this block is not

- Not a restatement of the ICP. The ICP is the target; this is the instrument, constrained by what can be known early.
- Not a lead magnet strategy. That is `M7`.
- Not a CRM field list, though it produces one.

## Required sections

1. **Qualification criteria.** Each one traced to an attribute in `P3` and paired with the mechanism: why this predicts that the product will work and be bought. A criterion with no traceable mechanism is inherited from someone else's playbook.
2. **Observable at first contact.** Which criteria can be known before a conversation, from form fields, enrichment, or channel of origin. The rest require discovery and belong in the script in `V4`, not in the score.
3. **Proxies.** Where the real criterion is unobservable early, the proxy used, and the error the proxy introduces. Naming the error prevents the proxy from being mistaken for the criterion six months later.
4. **Scoring model.** Weights, thresholds, and what each band triggers: immediate contact, nurture, disqualification. Simple enough that a seller can predict the score before seeing it.
5. **Disqualifiers.** Hard stops, from `P3` section 7. Including the attractive ones. A disqualification list that costs nothing is not a real list.
6. **Buying-role signals.** How to tell whether the person in front of you is the economic buyer, a champion, or a researcher, from `P4`. Routes the conversation and sets expected cycle length.
7. **Timing signals.** Evidence of the urgency triggers from `P1` section 8. Fit predicts whether they should buy; timing predicts whether they will. A high-fit, no-timing lead is a nurture case, not a loss.
8. **Intake form.** The specific questions asked, in order, with the reason each earns its place. Every additional field costs conversion; every removed field costs qualification. State the trade being made.
9. **Source-based expectations.** Expected quality by channel from `M5`, as a hypothesis. Aggregate scoring hides the fact that the same score from two channels predicts different outcomes.
10. **Routing.** Who handles what, and what happens to leads below threshold. Leads with no defined destination are the largest silent loss in most funnels.
11. **Recalibration.** What data will be gathered to test the model, and when it is reviewed. A scoring model never revisited becomes folklore.

## Evidence rules by regime

- **Greenfield.** Every weight is a guess. Keep the model simple enough to be corrected after thirty deals rather than defended.
- **Extension.** Derive weights from which existing customers succeeded, not from which ones closed.
- **Repositioning.** The old criteria select the old customer. State explicitly which existing criteria are now disqualifiers.

## Quality tests

- Is every criterion traceable to `P3`, or did some arrive from habit?
- Can the score be computed from information available before a call?
- Does the disqualification list include a company type sales would be excited about?
- Does the form ask anything the answer to which changes nothing?

## Canonical extract

```
V1 — Ideal Lead Profile
Criteria:            <each with the P3 attribute it comes from>
Known pre-call:      <which criteria> ; requires discovery: <which>
Proxies:             <proxy → real criterion → error introduced>
Scoring:             <weights and thresholds> ; bands trigger: <actions>
Disqualifiers:       <hard stops>
Timing signals:      <evidence of urgency triggers>
Intake form:         <the questions asked>
Below threshold:     <where those leads go>
```

## Probing questions

- What do you know about a lead before anyone talks to them, honestly?
- Which criterion has never once predicted a closed deal?
- What happens today to a lead that scores 40 out of 100?
- Which fit signal only becomes visible after the second call?

## Contradictions to watch

- A criterion does not derive from any `P3` attribute → the score measures something the ICP never claimed.
- The score identifies who responds rather than who decides → long cycles and late losses; `P4` names the difference.
- Expected volume from channels in `M5` is incompatible with the qualification bar → either the bar or the channel plan is wrong.
