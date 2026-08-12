---
code: V5
board: sales
title: Support Materials
hard_deps: [M7, V3, V4]
produces: [material_inventory, ownership, usage_rules, gaps]
downstream: []
---

# V5 — Support Materials

## What this block decides

What sellers carry, when each item is used, who produces it, and what happens when it does not exist. This is a terminal block: nothing depends on it, which makes it easy to defer and expensive to defer.

## What this block is not

- Not a content plan. `M7` decides what is published; this decides what is carried into a deal.
- Not a brand asset library.
- Not a wish list. Every item has an owner and a date or it is a gap.

## Required sections

1. **Materials by stage.** Mapped to the `V4` call map and the `V2` stages. For each stage: what the seller needs before the conversation, during it, and after it. Materials with no stage are materials nobody uses.
2. **Materials by persona.** Which item serves which persona from `P4`. The economic buyer's one-pager and the technical evaluator's documentation are different documents and are frequently the same document, badly.
3. **The core set.** The five to seven items that carry most deals: the deck, the one-pager, the proof piece, the pricing explanation, the security or compliance answer, the implementation outline, the comparison. Everything else is situational.
4. **Reuse from `M7`.** Which items already exist in the content plan and need only a sales-appropriate format. Reuse is the difference between a sales enablement effort that ships and one that does not.
5. **What must be built from scratch.** With owner and date. If there is no owner, it is a gap and should be listed as one.
6. **Usage rules.** When each item is sent, and when it is not. Sending everything at once is the most common misuse: the buyer reads none of it and the seller loses the ability to follow up with something new.
7. **The follow-up kit.** What is sent after a first call, per `V4` section 12. Usually the highest-frequency material and the least designed.
8. **Objection support.** For the objections in `V3` that require evidence rather than argument: what document answers it, and does it exist.
9. **Internal-only material.** Battlecards, pricing floors, discount authority from `P5`, escalation paths, and the honest competitive assessment. Distinguish clearly from customer-facing material; the two get confused with predictable consequences.
10. **Maintenance.** Who updates these when `P2`, `P5`, or `M2` change, and how sellers learn a version is stale. Sales material that contradicts the current position is worse than none.
11. **Gap list.** What sales needs today and does not have, ranked by how many deals it affects. This is the block's most useful output and should be stated plainly.

## Evidence rules by regime

- **Greenfield.** There are no cases. Substitute mechanism explanations, benchmarks, pilots, and guarantees, and say that is what is being done.
- **Extension.** The parent product's materials establish credibility. State what carries over and what would confuse.
- **Repositioning.** Existing materials encode the old position and are in circulation. List what must be withdrawn, and check what is already in prospects' inboxes.

## Quality tests

- Is every item tied to a stage and a persona?
- Does anything on the list exist because it is customary rather than because a seller uses it?
- Does the gap list name the item that costs the most deals?
- Is there a rule for what is sent after a first call, or does each seller improvise?

## Canonical extract

```
V5 — Support Materials
Core set:            <five to seven items with stage and persona>
Reused from M7:      <which>
Built from scratch:  <which, owner, date>
Follow-up kit:       <what is sent after a first call>
Internal-only:       <battlecards, pricing floors, escalation>
Maintenance owner:   <who> ; trigger: <what change forces an update>
Top gaps:            <ranked by deals affected>
```

## Probing questions

- What do your sellers make themselves because it does not exist?
- Which document has been sent unchanged for a year while the product changed?
- What does the buyer forward internally, and did you design it to be forwarded?

## Contradictions to watch

- Materials assert claims on the `M1` forbidden list or promise staged capability from `P2`.
- The objection support in section 8 depends on proof `P2` says does not exist.
- Nothing in the list is reused from `M7`, implying two content operations funded as one.
