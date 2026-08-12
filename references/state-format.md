# Canvas state

The state is the canvas. The generated blocks are its documentation. If the two ever disagree, the state is what later blocks read, so the state is what must be right.

## Where it lives

**Claude Code.** A file named `canvas-state.md` in the working directory, created from `templates/canvas-state.template.md`. Read at the start of every block. Rewritten at the end of every block. Full generated blocks are written alongside it as `blocks/<code>-<slug>.md` in the operator's project, not kept only in the conversation.

**Desktop or web.** The state is a document reissued at the end of every block, delimited so the operator can copy it in one action. Tell the operator plainly, once, that the canvas exists only in that document. At the start of a session where no state was pasted, ask for it before assuming the canvas is empty.

## Schema

```markdown
# Canvas state — <product name>

## Header
Product:            <name>
Scope:              product-wide | ICP:<name> | persona:<name>
Regime:             greenfield | extension | repositioning
Language:           <operator's language>
Environment:        claude-code | document
Last updated:       <date>, after <block code>

## Progress
Completed:          P1, P2, P3
Provisional:        P4 (stood in for M3)
Stale:              —
Not started:        P5–P8, M1–M8, V1–V8, C1–C8

## Open questions
- <question raised by a block and not yet answered, tagged with the block code>

## Validation tasks outstanding
- [ ] <task, block code, date issued>

## Canonical extracts

### P1 — Problem and Opportunity
<the block's canonical extract, verbatim, 5–10 lines>

### P2 — Value Proposition
<...>
```

## Rules

**Extracts are verbatim.** Never re-summarize an extract when writing state. The extract was already the compression; compressing it again loses the decision and keeps the adjectives.

**Provisional entries are marked in place.** A provisional extract carries `[PROVISIONAL]` on its first line and names which block forced it into existence. It is not a lesser extract — later blocks will read it exactly as they read a real one — so it must be a specific decision, not a hedge.

**Stale is a state, not an opinion.** When a block is completed or edited, every block in its `downstream` list, per the dependency graph, moves to `Stale`. Transitively: if `P3` changes, `V1` goes stale, and everything downstream of `V1` goes stale too. Announce the full set. Do not regenerate without being asked.

**Nothing is deleted.** When a block is regenerated, the previous extract moves to a `## Superseded` section at the bottom with the date and the reason. The reason a decision changed is frequently more useful later than either version of the decision.

**Open questions accumulate.** A question raised in `P1` and answered in `M2` is struck through, not removed, with the block code that answered it.

## Size

At completion, thirty-two extracts of five to ten lines each, plus header and lists, is roughly 300 to 400 lines. That is the working context cost of "every block depends on everything before it," and it is affordable. Full generated blocks are never all loaded at once — only the two to four declared hard dependencies for the block being written.

If the state file exceeds 600 lines, extracts are being written too long. The corrective is to compress the extract, never to drop blocks from the state.
