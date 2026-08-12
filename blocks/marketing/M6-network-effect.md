---
code: M6
board: marketing
title: Network Effect
hard_deps: [P5, P6, M5]
produces: [loop_type, referral_mechanics, incentive_design, viability_assessment]
downstream: [M8, C7]
---

# M6 — Network Effect

## What this block decides

Whether this product can generate demand from its own use, by what mechanism, and what that mechanism costs. The honest answer is frequently "no meaningful loop exists," and saying so is a valid and useful output of this block.

## What this block is not

- Not a referral program by default. A referral program is one mechanism, often the weakest.
- Not a growth-hacking checklist.
- Not an excuse to discount. Incentives that break `P5` are pricing decisions wearing a growth costume.

## Required sections

1. **Loop candidates.** Which of these are structurally available: **direct network effect** (the product improves as more of the same user joins), **data effect** (aggregate usage improves the product for everyone), **distribution effect** (use exposes non-users to the product), **referral effect** (users have an incentive to recruit), **content effect** (use produces artifacts that attract), **integration effect** (partners embed it). For each: available or not, and why.
2. **The strongest available loop.** One, described mechanically: who does what, who sees it, what makes them act, and how long a cycle takes. Cycle time determines whether the loop is a growth engine or a rounding error.
3. **Honest viability.** Whether the loop can produce a meaningful share of acquisition, or only a discount on paid acquisition. Most B2B loops are the second. Saying so protects `M8` and `V8` from planning around a mechanism that will not deliver.
4. **Incentive design.** What the referrer gets and what the recipient gets. Checked against `P5` business rules explicitly — discounts, free capacity, and free modules all have a cost that appears in margin.
5. **Cost of the loop.** What each loop-sourced customer costs in discounts and incentives, compared with paid acquisition. A loop more expensive than paid media is a loyalty program, not growth.
6. **Trigger moment.** When in the customer's lifecycle they are asked to participate, tied to the moment of value in `P7`. Asking before value has been delivered damages the relationship and produces low-quality referrals.
7. **Visibility surfaces.** Where non-users encounter evidence of the product: shared outputs, embedded marks, public artifacts, customer-facing interfaces. This is usually the cheapest available loop and the most often overlooked.
8. **Constraints.** Contractual, competitive, or regulatory reasons the customer cannot or will not publicize their use. In competitive markets, the best customers are frequently the least willing to be visible.
9. **Measurement.** How loop-sourced acquisition will be distinguished from other channels in `V7`, given that self-reported source data is unreliable.

## Evidence rules by regime

- **Greenfield.** Assume no loop until a mechanism is described end to end. Aspirational loops in launch plans are a common source of missed targets.
- **Extension.** Cross-product referral inside an existing base is usually the strongest available mechanism. Check against `P6` section 8 — it requires identity reconciliation.
- **Repositioning.** If a loop exists today, measure it before redesigning it.

## Quality tests

- Can you describe the loop as a sequence of five concrete actions by named parties?
- What is the cycle time, and how many cycles fit in a year?
- Does the incentive violate any rule in `P5`?
- Would a customer participate with no incentive at all? If yes, the incentive may be buying something already free.

## Canonical extract

```
M6 — Network Effect
Strongest loop:      <type> — or: no meaningful loop exists
Mechanism:           <who does what, who sees it, what makes them act>
Cycle time:          <duration>
Realistic share:     <% of acquisition, or "discount on paid only">
Incentive:           <what each side gets> ; P5-compliant: <y/n>
Cost per loop-sourced customer: <figure vs. paid>
Trigger:             <lifecycle moment, tied to P7>
Blockers:            <contractual, competitive, regulatory>
```

## Probing questions

- Who sees the product being used who is not paying for it?
- What does a customer produce with this that they would share anyway?
- At what moment would a customer feel good about recommending it?
- Why would a customer's competitor not want them to talk about it?

## Contradictions to watch

- The incentive breaks a business rule in `P5` → resolve before publishing; referral programs that break pricing are expensive to unwind.
- The loop depends on cross-product data `P6` says is not reconciled.
- The trigger fires before the moment of value in `P7` → referrals generated from customers who have not yet succeeded.
