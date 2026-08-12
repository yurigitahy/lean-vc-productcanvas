---
code: P4
board: product
title: Target Personas
hard_deps: [P2, P3]
produces: [persona_set, roles_in_decision, incentives, risks_perceived, central_message_per_persona]
downstream: [M3, M4, M5, V1, C1]
---

# P4 — Target Personas

## What this block decides

The people inside the ICP whose decisions determine whether this product is bought, adopted, and kept — and what each of them is actually optimizing for. Not demographics. Incentives.

When the canvas scope is per-persona, this block is a constraint block: the persona is given, and the work is to state their incentives precisely and check `P2` against them.

## What this block is not

- Not a marketing avatar with a stock photo and a coffee preference. Nothing in this block should be unfalsifiable.
- Not an org chart. Roles matter only where they change the decision.
- Not one persona per job title. Two titles with the same incentive are one persona; one title with two incentives is two.

## Required sections

1. **Persona set.** Three to five, no more. Each labeled by role in the decision, not only by job title.
2. **Role in the decision.** For each: economic buyer, technical evaluator, champion, user, gatekeeper, or blocker. Some people hold two roles; say which, because that concentration is either a shortcut or a single point of failure.
3. **Typical routine.** What their week actually contains. This is where the tone of voice in `M4` and the timing of outreach in `M5` come from. Written badly, it is filler; written well, it is the most quoted section in the canvas.
4. **What they are measured on.** The metric their own manager judges them by. Every purchase argument that does not connect to this metric is a favor being asked, not a case being made.
5. **What they buy.** Not what the product does — what this person is personally acquiring: control, time, evidence, cover, standing, or relief. Distinct per persona and frequently in tension across personas.
6. **What they fear.** The failure mode they are protecting against, including career risk. Objections in `V3` are usually fear stated as a technical concern.
7. **Perceived personal risk from this product.** Whether adopting it threatens their role, exposes their past decisions, or increases their visible accountability. The champion who quietly stalls is almost always managing this.
8. **How they inform themselves.** Sources, formats, and cadence — and which of those they trust versus merely consume.
9. **Vocabulary.** The words they use for the `P1` problem, and the words that mark an outsider. Feeds `M4` and `V4` directly.
10. **Central message per persona.** One sentence per persona that would make them lean in. This is the shortest, most reused output of the block.
11. **Tensions between personas.** Where one persona's win is another's loss. Naming these determines the sequence in `V4` and the stakeholder plan in `C1`.
12. **Who is missing.** Roles that will appear in the deal or in onboarding and have not been studied. Technical implementers and finance approvers are the usual omissions.

## Evidence rules by regime

- **Greenfield.** Personas are hypotheses drawn from analogous categories; label them and name the interview that would confirm each.
- **Extension.** Derive personas from who actually signs and who actually uses today, including the ones nobody planned for.
- **Repositioning.** The persona set may be changing. State the current buyer and the intended buyer separately, and what makes the intended one reachable.

## Quality tests

- Does every persona have a metric in section 4 that a real manager would recognize?
- Is any persona described only in positive terms? A persona without a fear and a risk has not been studied.
- Do two personas share the same central message? If so, they are one persona.
- Is the person who has to make it work after purchase in this list? If not, `C1` will inherit a stranger.

## Canonical extract

```
P4 — Target Personas
Persona A — <role>: measured on <metric>; buys <what>; fears <what>; message: "<one sentence>"
Persona B — <role>: ...
Persona C — <role>: ...
Economic buyer:      <which persona>
Likely champion:     <which persona> ; likely blocker: <which persona>
Main tension:        <between which personas, over what>
Not yet studied:     <roles known to be missing>
```

## Probing questions

- Who has to say yes, and who only has to not say no?
- Whose quarterly number changes if this works?
- Which persona has been burned before by something that looked like this?
- Who gets blamed if the implementation goes badly?

## Contradictions to watch

- A persona sits outside the ICP defined in `P3` → either `P3` is too narrow or the persona is aspirational.
- The economic buyer and the person feeling the `P1` pain are different and no bridge is described → expect stalls in `V2` and a long cycle.
- No persona is measured on anything the `P2` promise moves → the value proposition is real and unfundable in this organization.
