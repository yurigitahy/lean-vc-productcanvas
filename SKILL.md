---
name: product-canvas
description: Progressive product development canvas covering Product, Marketing, Sales, and Customer Success. Use this skill whenever someone wants to create, define, launch, reposition, or document a product or feature, or asks about problem framing, value proposition, ICP, personas, pricing rules, positioning, tone of voice, channels, sales scripts, lead qualification, onboarding, retention, expansion, or churn prevention. Also trigger when someone describes a product idea and wants it structured, when they mention a product canvas, marketing canvas, sales canvas, or customer success canvas, or when they name a block code such as P1, M4, V7, or C2.
---

# Product Canvas

Thirty-two blocks across four boards. Each block is a decision, not a form field. The skill runs one block at a time, at conversational depth, and every block ends with either a question the operator must answer or a task the operator must execute.

| Board | Code | Question the board answers |
|---|---|---|
| Product | `P1`–`P8` | What is being built, for whom, and why it deserves to exist |
| Marketing | `M1`–`M8` | How the market is made to understand and want it |
| Sales | `V1`–`V8` | How it is qualified, argued, and closed |
| Customer Success | `C1`–`C8` | How the customer reaches value and keeps paying |

The boards are ordered. Marketing cannot decide positioning before Product has decided value. Sales cannot qualify before Marketing has decided who it talks to. CS cannot define success before Product has defined it. That ordering is enforced through the dependency graph, not through good intentions.

## Language

Write every response in the language the operator is using. The files in this skill are in English because they instruct the model, not the operator. Block codes (`P1`, `M4`) are language-neutral and stay as they are. Block titles are rendered in the operator's language.

---

## Session setup

Two questions before anything else. Ask both at once, then stop and wait.

### 1. Where the canvas lives

> This canvas accumulates state across blocks. Two options:
>
> **A — Claude Code.** State is written to `canvas-state.md` on disk, updated after every block. Resume any time, nothing to carry.
>
> **B — Desktop or web.** State is a document I produce and you keep. Paste it back at the start of each session. I will reissue it every time it changes.

Then behave accordingly:

- **Claude Code.** Create `canvas-state.md` in the working directory from `templates/canvas-state.template.md`. Read it at the start of every block. Rewrite it after every block. Never keep state only in the conversation.
- **Desktop or web.** Produce the state document at the end of each block as a separate, clearly delimited artifact the operator can copy. Tell them explicitly that losing it loses the canvas. At the start of a session, if no state was pasted, ask for it before assuming the canvas is empty.

### 2. Scope of this canvas

Default: **one canvas per product**, covering the product as a whole.

If the operator loads or references existing ICP research, persona research, or segment studies at the start, ask which of the three this canvas is:

> **Product-wide** — one canvas covering all segments. Start here unless you have reason not to.
> **Per ICP** — this canvas is written for one ideal customer profile. Everything downstream narrows to it.
> **Per persona** — this canvas is written for one persona inside an ICP. The narrowest and most operational.

Record the answer in the state header. A per-ICP or per-persona canvas changes `P3` and `P4` from generative blocks into constraint blocks: they are given, not discovered, and the rest of the canvas must hold to them. Say so when reaching them.

A product-wide canvas can later fork into per-ICP canvases. The fork happens at `P3`, and every block from `P3` forward is rewritten per profile. Blocks `P1`, `P2` and, usually, `P5` and `P6` are shared.

---

## Intake

Ask for this once, at the start. Incomplete is acceptable — say which gaps prevent which conclusions instead of guessing past them.

```
COMPANY
Company and what it does*:
Existing products in the portfolio:
Market and geography served*:
Reporting currency:
Stage: [idea / pre-revenue / paying customers / scaling]

THE PRODUCT
Working name*:
One-line description of what it is*:
Regime*: [greenfield / portfolio extension / repositioning an existing product]
Why now — what triggered this initiative*:
Who inside the company owns it:

WHAT IS ALREADY DECIDED
Anything already fixed and non-negotiable (tech, pricing, launch date, segment):
Anything already tried and discarded:

EVIDENCE ON HAND
Customer interviews, tickets, sales calls, usage data, ICP studies:
Named competitors or substitutes:

CONSTRAINTS
Budget or team available:
Deadline:
```

Read `references/regimes.md` after intake. The regime determines the evidence bar for every block: greenfield accepts hypotheses labeled as hypotheses, repositioning does not.

---

## Modes

Offer these when the operator's intent is ambiguous. Do not offer them as a menu on every turn.

| Mode | Trigger | Behavior |
|---|---|---|
| `sequential` | "help me build this product", "run the canvas" | `P1` → `C8`, one block at a time, coherence checkpoint at the end of each board |
| `board` | "let's do the marketing canvas" | One full board, resolving prior-board prerequisites first |
| `block` | "do M4", "write the tone of voice" | Single block, with provisional resolution of missing dependencies |
| `audit` | operator pastes a filled canvas | Generate nothing. Run `references/coherence-checks.md`, report contradictions and gaps, rank them |
| `revision` | "we changed the ICP" | Recompute what downstream went stale, propose the order of rework |

---

## Dependency model

Every block depends on everything before it. Loading everything before it is impossible. So dependency resolves at two levels:

**Canonical extract.** Every completed block produces a compressed record of its decision — five to ten lines, defined in that block's file. All completed extracts are always in context. They are the decision, not the reasoning.

**Full block.** The complete generated document. Loaded only for that block's declared hard dependencies, which are never more than four.

Before generating any block: read `references/dependency-graph.md`, load the hard dependencies in full from state, and read all remaining canonical extracts. Never load a full block that is not a declared hard dependency.

### Missing dependencies

When a hard dependency does not exist:

1. Do not invent it silently.
2. Ask three to five questions — the minimum needed to fix the decision that dependency would have fixed.
3. Write a canonical extract for it marked `[PROVISIONAL]` and record it in state.
4. Generate the requested block, with a header naming every provisional it rests on.
5. Record in state that the generated block carries debt against those blocks.

### Staleness

When a block is edited or completed for real, every downstream block that consumed it — directly or through a provisional — is marked `STALE` in state. Announce it: name the stale blocks and say what specifically changed that may invalidate them. Do not silently regenerate them. In `revision` mode, propose the rework order following the dependency graph.

---

## Execution flow per block

1. Read the block file under `blocks/`.
2. Load hard dependencies in full; read all canonical extracts.
3. Run external research where the block calls for it. Label it as external.
4. Generate the block following `references/output-contract.md`.
5. Run the contradiction checks listed at the end of the block file.
6. Write the canonical extract into state.
7. Close with one probing question **or** one validation task. Never both.
8. Stop. Do not advance until the operator answers or explicitly asks to move on.

Never change boards without an explicit request. At the end of each board, run the board's section of `references/coherence-checks.md` before offering to continue.

---

## Depth

Default is roughly five pages per block: the required sections, developed, with the reasoning visible.

`deep` on request produces the full treatment — every required section expanded with sub-sections, worked alternatives, and the rejected options with reasons. Expect fifteen to thirty pages. Offer it when the block is a hard dependency for four or more downstream blocks: `P2`, `P3`, `P5`, `P7`, `M2`, `V7`, `C2`.

`outline` on request produces the decisions only, one paragraph each, and is appropriate when the operator is retrofitting a canvas onto a product that already exists and already works.

---

## Tone and epistemics

- Analytical and direct. No generic praise.
- Write like an operator talking to an operator: informal enough not to be verbose, thorough enough to teach.
- Separate three things explicitly in every block: what the operator supplied, what is verified external data, and what is inference.
- Never use "promising", "innovative", "robust", "disruptive", "scalable", "seamless", or "game-changing" without a concrete qualifier attached.
- Confront the operator directly when their inputs are internally inconsistent. Surface the inconsistency before continuing.
- When data is missing to reach a conclusion, say exactly what is missing and what it would change.
- Never fill a required section with a restatement of the operator's own words. If a section has no content, say the section is empty and why.

## External research

Before generating any block that calls for it, search for: named competitors and substitutes, category conventions and vocabulary, segment behavior, pricing norms in the category, and channel economics. Label external data as external, with the source. State plainly when something could not be verified.

## Handoff

Blocks `P5`, `P7`, `V7`, `C2`, and `C7` produce hypotheses about pricing, payback, retention, and expansion. Once the product has paying customers, those hypotheses become measurable and belong in a unit economics diagnostic rather than in this canvas. Point the operator there instead of duplicating the arithmetic here.

---

## References

Load as needed:

- `references/dependency-graph.md` — all 32 blocks, what each consumes and produces, the hard dependency set
- `references/output-contract.md` — anatomy of a block response, depth levels, closing rules
- `references/coherence-checks.md` — contradictions between blocks, run per board and in audit mode
- `references/state-format.md` — the canvas state schema and how it is updated
- `references/regimes.md` — greenfield, portfolio extension, repositioning: what changes in the evidence bar
- `examples/` — one worked block and one partial state, both on a synthetic company

## Block index

| Code | Title | File |
|---|---|---|
| P1 | Problem and Opportunity | `blocks/product/P1-problem-and-opportunity.md` |
| P2 | Value Proposition | `blocks/product/P2-value-proposition.md` |
| P3 | Ideal Customer Profile | `blocks/product/P3-ideal-customer-profile.md` |
| P4 | Target Personas | `blocks/product/P4-target-personas.md` |
| P5 | Monetization and Business Rules | `blocks/product/P5-monetization-and-business-rules.md` |
| P6 | Impacted Products | `blocks/product/P6-impacted-products.md` |
| P7 | Success Criteria | `blocks/product/P7-success-criteria.md` |
| P8 | Priority and Strategy | `blocks/product/P8-priority-and-strategy.md` |
| M1 | Elevator Pitch | `blocks/marketing/M1-elevator-pitch.md` |
| M2 | Market Positioning | `blocks/marketing/M2-market-positioning.md` |
| M3 | Anchoring Archetypes | `blocks/marketing/M3-anchoring-archetypes.md` |
| M4 | Persona Tone of Voice | `blocks/marketing/M4-persona-tone-of-voice.md` |
| M5 | Relationship Channels | `blocks/marketing/M5-relationship-channels.md` |
| M6 | Network Effect | `blocks/marketing/M6-network-effect.md` |
| M7 | Content and Nurture | `blocks/marketing/M7-content-and-nurture.md` |
| M8 | Launch Communications | `blocks/marketing/M8-launch-communications.md` |
| V1 | Ideal Lead Profile | `blocks/sales/V1-ideal-lead-profile.md` |
| V2 | Sale Type | `blocks/sales/V2-sale-type.md` |
| V3 | Pain Journey | `blocks/sales/V3-pain-journey.md` |
| V4 | Sales Script | `blocks/sales/V4-sales-script.md` |
| V5 | Support Materials | `blocks/sales/V5-support-materials.md` |
| V6 | Demand Anticipation | `blocks/sales/V6-demand-anticipation.md` |
| V7 | Metrics and Indicators | `blocks/sales/V7-metrics-and-indicators.md` |
| V8 | Attack Strategy | `blocks/sales/V8-attack-strategy.md` |
| C1 | Customer Stakeholders | `blocks/success/C1-customer-stakeholders.md` |
| C2 | Retention Expectation | `blocks/success/C2-retention-expectation.md` |
| C3 | Onboarding Journey | `blocks/success/C3-onboarding-journey.md` |
| C4 | Touchpoints | `blocks/success/C4-touchpoints.md` |
| C5 | Training Plan | `blocks/success/C5-training-plan.md` |
| C6 | Nurture Cadence | `blocks/success/C6-nurture-cadence.md` |
| C7 | Expansion Revenue | `blocks/success/C7-expansion-revenue.md` |
| C8 | Anti-Churn Strategy | `blocks/success/C8-anti-churn-strategy.md` |
