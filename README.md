# Product Canvas

A Claude Skill that develops a product across thirty-two blocks, in four boards — Product, Marketing, Sales, and Customer Success.

It is not a template and not a form. Each block is a decision with a required shape, a set of quality tests, and an explicit list of what it constrains downstream. The skill runs one block at a time and does not advance until you answer. Every block ends with either a question you have to answer or a task you have to go execute.

## What it does

| Board | Codes | The question it answers |
|---|---|---|
| Product | `P1`–`P8` | What is being built, for whom, and why it deserves to exist |
| Marketing | `M1`–`M8` | How the market is made to understand and want it |
| Sales | `V1`–`V8` | How it is qualified, argued, and closed |
| Customer Success | `C1`–`C8` | How the customer reaches value and keeps paying |

The boards are ordered, and so are the blocks inside them. Marketing cannot position before Product has decided value; Sales cannot qualify before Marketing has decided who it talks to; CS cannot define success before Product has defined it.

## What a block produces

Roughly five pages by default, `deep` on request for the blocks that carry the rest of the canvas. Every block has the same anatomy: the inputs it consumed, the developed body, the assumptions with the cheapest test that would kill each, what it constrains downstream by block code, the contradictions it detected with earlier blocks, a canonical extract for the state, a definitive north, and a single closing question or task.

The register is specified too, and separately. A block that contains every required section and reads like a memorandum has failed, so `references/narrative-devices.md` codifies what the output must do: quote the buyer in their own words rather than characterizing their beliefs, track the internal question as it evolves across awareness stages, set the load-bearing claim apart from the prose, produce language as variants with the rejected ones and their reasons visible, and close on a decision rather than a summary.

## The dependency model

Every block depends on everything before it. Loading everything before it is not possible, so dependency resolves at two levels.

Every completed block produces a **canonical extract** — five to ten lines carrying the decision, not the reasoning. All completed extracts stay available at all times. Each block additionally declares two to four **hard dependencies**, which are loaded in full. Nothing else is loaded.

This is what makes it possible to jump straight to `M4` on an empty canvas. The skill resolves the missing hard dependencies by asking a handful of questions, records the answers as extracts marked provisional, generates the block, and notes the debt. When those blocks are later done properly, everything built on the provisionals is marked stale, with the specific change named.

## Modes

| Mode | What it does |
|---|---|
| `sequential` | `P1` → `C8`, one block at a time, coherence checkpoint at the end of each board |
| `board` | One full board, resolving prior-board prerequisites first |
| `block` | A single block, with provisional resolution of what is missing |
| `audit` | Generates nothing. Takes a filled canvas and reports where it contradicts itself |
| `revision` | Something changed. Computes what went stale and proposes the rework order |

## What it is not

- Not a scoring or maturity model. It produces decisions and open questions. A score ends the conversation.
- Not sector-specific. Nothing depends on a market, a currency, or a stage.
- Not a document generator. It runs as a conversation and stops when you stop answering.
- Not a unit economics model. Blocks `P5`, `P7`, `V7`, `C2`, and `C7` produce hypotheses about price, payback, retention, and expansion. Once there are paying customers, testing those belongs in a unit economics diagnostic.

## Install

**Claude Code**

```
git clone https://github.com/yurigitahy/lean-vc-productcanvas.git ~/.claude/skills/product-canvas
```

**Claude Desktop and claude.ai**

Zip the repository contents and upload under Settings → Capabilities → Skills.

**Any other agent**

Plain Markdown with YAML frontmatter. Paste `SKILL.md` into a system prompt and load the files under `blocks/` and `references/` when the skill points to them.

## Use

Trigger it by describing what you are doing, not by naming the skill:

> We're building a new product and I need to think it through properly.
>
> Write the tone of voice for this product.
>
> Do M4.
>
> Here's our filled canvas — tell me where it contradicts itself.

It opens with two questions: where the canvas should live — a file on disk in Claude Code, or a document you carry between sessions everywhere else — and what it should cover, which is the product as a whole unless you point it at a specific ICP or persona. Everything after that follows from the intake block.

## Structure

```
.
├── SKILL.md                          Router: modes, intake, rules, dependency model
├── references/
│   ├── dependency-graph.md           All 32 blocks: consumes, produces, hard dependencies
│   ├── output-contract.md            Anatomy of a block, depth levels, banned vocabulary
│   ├── narrative-devices.md          The register a block is written in
│   ├── coherence-checks.md           Contradictions between blocks
│   ├── state-format.md               Canvas state schema
│   └── regimes.md                    Greenfield, extension, repositioning
├── blocks/
│   ├── product/                      P1–P8
│   ├── marketing/                    M1–M8
│   ├── sales/                        V1–V8
│   └── success/                      C1–C8
├── templates/
│   └── canvas-state.template.md
└── examples/
    ├── worked-block-problem-and-opportunity.md
    └── canvas-state-partial.md
```

`SKILL.md` loads whenever the skill triggers. Everything else loads only when pointed to, which is what keeps a thirty-two block canvas runnable inside a working context.

## Design principles

**One block per response.** A canvas delivered as a document gets read. A canvas delivered as a conversation gets decided.

**Contradiction is the product.** The failure mode of the canvas format is four teams filling four boards in four meetings, after which the ICP in `P3` and the lead score in `V1` describe different companies. `references/coherence-checks.md` exists to catch exactly that, and `audit` mode does nothing else.

**Provisional beats invented.** When a dependency is missing, the skill asks and marks the answer provisional rather than generating something plausible. Plausible content becomes a hard dependency for six other blocks and propagates.

**The evidence bar depends on the regime.** A hypothesis is a legitimate answer for a product that does not exist and an evasion for one that has customers. The regime is set at intake and enforced per block.

**Register is not decoration.** How a block reads determines whether its decisions survive the week it was written. Specified in `references/narrative-devices.md` and enforced per block, not left to style.

**Separate data from inference.** Every block distinguishes what the operator supplied, what is verified external data, and what is the model's reasoning. Confusing the three is how a canvas becomes flattery.

**Language follows the operator.** The files are in English because they instruct the model. The skill answers in whatever language you are using.

## Contributing

Section additions, coherence checks, dependency corrections, and new regimes are all welcome. Real company data is not. See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

[CC BY-SA 4.0](LICENSE). Use it, adapt it, run it commercially. Keep the attribution and license derivatives under the same terms.

Built and maintained by [Lean VC](https://github.com/yurigitahy).
