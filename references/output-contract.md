# Output contract

The shape every block response takes, regardless of which block it is.

## Anatomy

**1. Header — inputs consumed**

Three to six lines. Name the hard dependencies used and the one decision taken from each. Mark any `[PROVISIONAL]` input and say what it was assumed to be. This exists so the operator can see the block's foundations before reading its conclusions, and so a reader six months later knows what the block was built on.

**2. Body — the required sections**

Each block file lists its required sections in order. Follow that order. Number them. Every section carries a heading in the operator's language.

A section is written, not filled. The difference: filling restates the input in the section's vocabulary; writing produces a claim that was not in the input and could be wrong. If a section can only be filled, say the section is empty and name what would populate it.

Sections that call for external evidence carry a source or the explicit note that no verifiable external data was found. Never present inference in the register of fact.

**3. Central statement**

One sentence, set apart, that a person could repeat from memory. Not a summary of the section — the decision itself, in its most compressed defensible form. Most blocks in the canvas fail downstream because nobody can remember what was decided.

**4. Assumptions and how to kill them**

Every consequential assumption made in the block, each paired with the cheapest test that would falsify it. An assumption without a falsification test is a belief and should be labeled as one.

**5. Downstream impact**

Which blocks this constrains, and how. Specifically: name the block code and the constraint. "This makes `V1` a filter on inventory volume, not on company size." A block that constrains nothing downstream was probably not a decision.

**6. Contradictions detected**

Run the checks listed at the end of the block file plus the relevant rows of `coherence-checks.md`. Report contradictions with earlier blocks by code. Say which side you believe is wrong and why. Do not resolve it unilaterally — that is the operator's call — but do take a position.

**7. Canonical extract**

The compressed record that enters state. Format is defined per block. Five to ten lines. This is what every later block will read instead of this document, so it must survive the loss of everything above it.

**8. Close**

Exactly one of:

- **→ To continue:** the question the operator must answer for the reasoning to close.
- **→ Validation task:** the concrete action the operator must execute to verify this block.

Never both. Never neither. Never a menu of next steps.

---

## Depth levels

| Level | Body length | When |
|---|---|---|
| `outline` | One paragraph per required section | Retrofitting a canvas onto a product that already exists and works |
| standard | Roughly five pages total | Default |
| `deep` | Every required section expanded with sub-sections, alternatives considered and rejected with reasons, and worked examples | On request; offer unprompted for `P2`, `P3`, `P5`, `P7`, `M2`, `V7`, `C2` |

Depth changes the body only. Header, central statement, assumptions, downstream impact, contradictions, extract, and close are mandatory at every level.

---

## Rules that override the operator's phrasing

- **One block per response.** If asked for a whole board at once, produce the first block and say the rest follow one at a time, and why: a board delivered as a document gets read, a board delivered as a conversation gets decided.
- **No scores, grades, or maturity levels.** The canvas produces decisions and open questions. A score ends the conversation, which is the opposite of the intent.
- **No template language.** If a sentence would be true of any product in any category, delete it.
- **Concrete over hedged.** "Three of the five named competitors price per seat" beats "pricing in this category varies."
- **Numbers where numbers exist.** Where they do not exist, name the number that should exist and does not — that is often the block's most useful output.

## Banned vocabulary

Never use without a concrete qualifier attached: *promising, innovative, robust, disruptive, scalable, seamless, game-changing, best-in-class, cutting-edge, holistic, synergistic, leverage* (as a verb), *unlock, empower, revolutionize*.

The test is not the word, it is whether removing the word changes the meaning of the sentence. If it does not, the sentence was decoration.

## Handling thin input

When the operator's input is too thin to write a section honestly, the failure mode to avoid is generating plausible content that reads like a decision and is actually the model's guess. Instead:

1. Write the sections that the input does support.
2. For the rest, name what is missing, in the form of the specific question that would resolve it.
3. Close on that question rather than a validation task.

A half-written block with an honest gap is worth more than a complete block that is three-quarters invention, because the second one becomes a hard dependency for six other blocks and propagates.
