---
code: M5
board: marketing
title: Relationship Channels
hard_deps: [P3, P4, M2]
produces: [channel_map, channel_by_stage, partners, channel_economics_hypothesis, concentration_risk]
downstream: [M6, M7, M8, V1, V6]
---

# M5 — Relationship Channels

## What this block decides

Where the company and the buyer actually meet, at each stage of the relationship — and which of those meeting points the company controls, rents, or borrows.

## What this block is not

- Not a media plan. Budget allocation is `M8` and `V8`.
- Not a list of platforms the company has accounts on.
- Not a funnel diagram. The unit here is a channel with an owner and an economic profile.

## Required sections

1. **Channel map by stage.** For each of six stages, the specific channels: how the buyer becomes aware, how they first make contact, how they consume information, how they buy, how they use, how they refer. Missing stages are where relationships fall through.
2. **Ownership.** For each channel: **owned** (site, list, base, product surface), **rented** (paid media, marketplaces, platforms), or **borrowed** (partners, communities, press, influencers). The ratio matters more than the count — a channel mix that is entirely rented means demand stops when spend stops.
3. **Where the ICP already is.** Grounded in `P3` section 9. Associations, events, publications, platforms, vendor ecosystems, and peer groups, with which persona from `P4` is present in each and in what role.
4. **Fit to position.** Which channels can carry the `M2` position and which cannot. A position requiring education does not survive a channel that allows one line of copy.
5. **Channel economics hypothesis.** For each significant channel: expected cost to acquire, expected cycle length, expected quality of the resulting lead. Hypotheses, labeled as such, that `V7` will test.
6. **Partners.** Who already holds a warm relationship with the ICP and does not compete. For each: what they get, what they give, why they would bother, and whether the incentive is financial or strategic. Partner channels look cheap and are rent — priced by the partner, revisable by the partner.
7. **Concentration risk.** If one channel is expected to produce most of the volume, say so and name the second channel that would be built if the first became expensive or closed. Single-channel acquisition is a single point of failure regardless of how well it performs.
8. **Owned asset strategy.** What the company is building that it will still have if every rented channel disappears: audience, list, data, product-led surface, community. With a horizon.
9. **Channel conflict.** Where two channels compete for the same buyer, or where a partner channel undercuts direct sales. Resolve before launch, or the field resolves it badly.
10. **Instrumentation.** How each channel's contribution will be attributed, and where attribution will be weak. Attribution weakness is not a reason to avoid a channel; it is a reason to know in advance which decisions cannot be made from the data.

## Evidence rules by regime

- **Greenfield.** Channel economics are entirely hypothetical. Rank channels by cost of testing, not by expected performance, and say which test runs first.
- **Extension.** Existing channels have real numbers. Use them, and state where the new product's channel behavior is expected to differ and why.
- **Repositioning.** The current channel mix may be the reason repositioning is needed. Document what the current mix delivers before proposing a new one.

## Quality tests

- Is every stage in section 1 covered by at least one channel with a named owner?
- What share of expected volume comes from channels the company does not control?
- Does any channel appear because the team is comfortable with it rather than because the ICP is there?
- Would the partner in section 6 describe the incentive the same way the company does?

## Canonical extract

```
M5 — Relationship Channels
Awareness:           <channels> ; contact: <channels> ; purchase: <channels>
Referral:            <channels or none>
Owned / rented / borrowed: <rough split of expected volume>
Primary channel:     <name> ; expected share: <%> ; backup: <name>
Partners:            <who, what they get, why they would bother>
Owned asset built:   <what, over what horizon>
Weak attribution in: <which channels>
```

## Probing questions

- If your largest channel doubled in price next quarter, what would you do that week?
- Which channel are you in because a competitor is in it?
- What do you own today that you would still have with zero media spend?
- Which partner has your ICP's attention and no product like yours?

## Contradictions to watch

- The ICP in `P3` is not actually present in the listed channels, in the deciding role → channels chosen by team familiarity.
- Channels cannot carry the education load `M2` requires → the position will not land regardless of budget.
- `M8` plans a launch on a channel not mapped here → either this block is incomplete or the launch is improvising.
