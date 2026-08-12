---
code: M4
board: marketing
title: Persona Tone of Voice
hard_deps: [P4, M2, M3]
produces: [tone_rules, vocabulary, banned_language, cta_patterns, tone_by_channel]
downstream: [M7, V3]
---

# M4 — Persona Tone of Voice

## What this block decides

How the company sounds when it talks to this buyer — as rules someone can apply, not adjectives someone can admire. The output of this block is used by writers, sellers, support agents, and any generative system producing text in the company's name.

## What this block is not

- Not three adjectives. "Confident, friendly, expert" is compatible with any writing ever produced and constrains nothing.
- Not copywriting. `M7` writes content; this block sets what content must obey.
- Not a style guide for punctuation, though it may include one.

## Required sections

1. **Register.** Where the voice sits on the axes that matter: formal/informal, assertive/consultative, technical/plain, brief/expansive. Each with the reason drawn from the persona's routine in `P4`, not from preference.
2. **Vocabulary.** The words used, the words avoided, and the words that signal an outsider. Include the buyer's own terms for the `P1` problem. A term the buyer never uses is a term that costs credibility.
3. **Sentence and structure rules.** Length, use of numbers, whether claims lead or follow evidence, whether jargon is defined or assumed. Concrete enough to be checkable.
4. **Banned language.** Category clichés, superlatives, and any phrasing that triggers the persona's specific skepticism. Should include at least three phrases the company currently uses.
5. **Tone by channel.** How the voice changes across email, landing page, sales deck, product interface, support reply, and social. The register persists; the compression changes.
6. **Tone under pressure.** How the voice sounds in the four hard cases: delivering bad news, quoting a price, saying no, and following up after silence. Most tone guides break here, and these are the messages that decide relationships.
7. **Interest triggers.** Which motivational levers are legitimate for this persona and this archetype — scarcity, exclusivity, peer proof, authority, loss framing, curiosity — and which are off-limits because they would read as manipulation to a professional buyer. Say why for each.
8. **Call to action patterns.** The specific asks used, ranked by commitment, with the phrasing for each. Include the low-commitment ask for buyers early in the awareness ladder from `P3`.
9. **Naming conventions.** How the product, its parts, and its plans are referred to. Inconsistent naming is the fastest way to sound like several companies.
10. **Examples.** Same message written three ways: correct, too far in one direction, too far in the other. Three to five messages covered. This section does more work than everything above it.
11. **Application to generated text.** The rules a language model would need to produce compliant copy without further instruction — this block should be usable as a system prompt fragment.

## Evidence rules by regime

- **Greenfield.** Ground the vocabulary in real artifacts: how the persona writes in forums, job posts, and public documents. Invented vocabulary reads as invented.
- **Extension.** State what is inherited from the parent brand voice and what deliberately differs.
- **Repositioning.** The market recognizes the old voice. State whether the shift is gradual or announced.

## Quality tests

- Could two writers, given only this block, produce copy a reader would attribute to the same company?
- Does the banned list include something the company currently does?
- Do the examples in section 10 include an actual failure, or only successes?
- Does section 6 exist and is it specific? Tone guides that skip bad news are guides for the easy half of the relationship.

## Canonical extract

```
M4 — Persona Tone of Voice
Register:            <positions on the four axes, with reasons>
Uses:                <core vocabulary>
Never uses:          <banned phrases, including current company habits>
Structure rules:     <three checkable rules>
Under pressure:      <how it sounds delivering bad news>
Legitimate triggers: <levers allowed> ; off-limits: <levers refused>
CTA ladder:          <low, medium, high commitment asks>
```

## Probing questions

- What phrasing would make this buyer close the tab?
- How does the company sound when it has to admit something went wrong?
- Which words does the buyer use that the company currently corrects?

## Contradictions to watch

- The tone does not sustain the archetypes in `M3` under the pressure cases in section 6 → the archetype was defined for the happy path only.
- Interest triggers include scarcity for a buyer `P4` describes as risk-averse and institutional → the lever reads as manipulation and costs credibility.
- The content plan in `M7` sounds like the company's existing content rather than this block → the voice was defined and then ignored.
