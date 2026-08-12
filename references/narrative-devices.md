# Narrative devices

`output-contract.md` decides what a block contains. This file decides how it reads.

The distinction matters because the two failure modes are different. A block can contain every required section and still be forgettable — a memorandum that gets filed. What makes a block get quoted six months later in a meeting nobody planned is the register: the buyer's own voice, assertions that carry weight because they stand alone, and a closing line someone can repeat.

These devices are obligations, not options. Use them where they apply. The synthetic examples below come from the same invented company as `examples/` — a compliance product sold to facilities contractors — and exist only to show the shape.

---

## 1. The buyer's voice, in quotes

Wherever a block describes what a customer thinks, believes, fears, or asks, write it as a sentence they would actually say. In quotes. In their vocabulary from `P4`, not the company's.

A described belief is inert. A quoted belief is testable — the operator reads it and either recognizes it or does not, and that reaction is worth more than a paragraph of characterization.

> Weak: *Contractors tend to view compliance documentation as an administrative burden rather than as a risk exposure.*
>
> Strong: *"It's paperwork. Someone chases it, it gets filed, we move on."*

**Where this is mandatory:** `P1` sections 1 and 2, `P3` awareness levels, `P4` throughout, `V3` sections 1 and 7, `C8` exit conversations.

## 2. The evolving question

The strongest form of device 1: the same person's internal question, tracked as it changes across a ladder — awareness stages in `P3`, the pain journey in `V3`, the buying process in `V2`. Written as a chain, with arrows, not as a table of stages.

> Unaware: *"It's paperwork."*
> → Problem-aware: *"We got held up at a gate twice this month and nobody could tell me why."*
> → Solution-aware: *"Someone has to own this, and it can't be a spreadsheet."*
> → Product-aware: *"Does this actually get documents out of the subcontractors, or just store what we already have?"*
> → Ready: *"What does it cost, how long to set up, and what does my insurer say about it?"*

This chain does more work than any other single element in the canvas. Marketing reads it for message sequencing, sales reads it for qualification, product reads it for what must be obvious in the first session. Produce it wherever a block covers a progression of belief.

## 3. The isolated assertion

The core claim of a section does not live inside a paragraph. It sits alone, after a break, on its own line.

Structure: build the case in two or three sentences, break, land the claim, break, then draw the consequence.

> The contractor may own the contract, the site, the insurance policy, and the client relationship.
>
> It does not own the document that proves any of it.
>
> That single gap is why the obligation and the visibility sit in different places, and it does not close with effort.

Use this once per major section, at most. Used three times in a row it becomes a tic and the emphasis stops registering.

## 4. Enumeration as evidence

Where a claim depends on scope, show the scope as a list rather than asserting it. A list of ten concrete things the customer owns, or ten symptoms they experience, makes an abstract argument physical in a way a summary sentence cannot.

> The contractor invests in:
> - the client relationship
> - the site supervision
> - the insurance policy
> - the induction process
> - the crew scheduling
> - the incident reporting
> - the audit response
>
> and still cannot answer, on the day it is asked, whether the crew on site was covered.

The rhetorical work is in the length of the list and the turn at the end. A three-item list does not produce it.

## 5. Central message per section

`output-contract.md` requires one central statement per block. This file adds: any section that produces a message someone will carry into a meeting gets its own, set apart, one sentence.

Typical: one per persona in `P4`, one per positioning strategy considered in `M2`, one per persona variant in `M4`, one per argument in `V3`, one per intervention playbook in `C8`.

> **Central message —** *"Your coordinator should be doing the work, not proving that someone else did theirs."*

## 6. Variants, with the rejected ones visible

Where a block produces language — a pitch, a punchline, a message, a positioning line — do not produce one. Produce four to six, then say which is chosen and why the others are not.

Showing the rejects is not padding. The operator's reaction to a rejected version is the fastest available signal about what they actually believe, and it frequently overturns the choice.

> **Considered:**
> 1. *"Compliance you can prove, not compliance you hope for."* — clean, but claims certainty the staged roadmap in `P2` does not yet support.
> 2. *"Stop chasing certificates."* — lands with the coordinator, who cannot buy. Wrong persona.
> 3. *"Your subcontractors' paperwork is your liability."* — accurate, and reads as an accusation of the buyer's current practice.
> 4. *"Know who is covered, on any site, on any day."* — **chosen.** Names the decision moment, makes no claim about mechanism, survives the roadmap staging.

Where the operator's personas differ sharply, produce a variant per persona and label it as such — the version for a finance approver and the version for an operations director are different documents in one line.

## 7. Cross-functional directives inside the block

A `P` block that only speaks to product has under-delivered. Where a decision constrains another function, write a short titled passage aimed at that function, inside the block.

Not the compressed downstream-impact list from `output-contract.md` — that stays. This is a developed passage: *what marketing should exploit here*, *what sales needs to diagnose in the first call*, *what CS should watch for in month one*. Two or three paragraphs, written to be read by that team without the rest of the block.

**Where this is mandatory:** `P1`, `P2`, `P3`, `P5`, `P7`. These are the blocks other functions inherit and rarely read in full.

## 8. Before and after, in the customer's terms

Where a block describes change, produce two columns in the customer's vocabulary, with the product absent from both. Then, below them, the one-line version of the transition:

> They move from *"we file what we're sent"* to *"we know what's missing before it matters."*

The compressed line is the part that survives. Write it deliberately rather than letting the table stand alone.

## 9. Escalating questions

Where a block lists questions — discovery in `V3`, probing anywhere — order them from safe to sharp and say that is the order. A question the buyer can answer without thinking does no work; a sharp question asked first closes the conversation. The ladder is the deliverable, not the set.

## 10. The definitive north

The last thing in every block, immediately before the closing question or validation task: one short passage, titled, that states what was decided and what it commits the company to. Not a summary of the sections. The decision, at its most compressed and most defensible.

> **Definitive north —** This product is sold against risk, not against administrative time. Every downstream decision — price, buyer, channel, script — follows from that, and the moment the conversation drifts to coordinator hours, the wrong deal is being built.

If this passage cannot be written, the block did not decide anything and should say so plainly rather than closing on a summary.

---

## Anti-patterns

These break the register faster than the devices build it.

- **Evidence labels pulverized through the prose.** Concentrating them is what `output-contract.md` requires. Marking every clause turns an argument into a footnote apparatus.
- **Adjectives doing the work of claims.** If removing an adjective leaves the sentence's meaning intact, the sentence was decorated rather than written.
- **Symmetry for its own sake.** Four bullets because three looked unfinished. The list length should follow the content.
- **The isolated assertion used for an obvious statement.** Reserved for claims that carry weight. Used on a truism it reads as self-importance.
- **Quoting the buyer in the company's vocabulary.** A quote containing the product's category name is a quote the company wrote.
- **Hedging the definitive north.** "We should probably position around risk" is not a north. Either the decision was made or the block is unfinished.

## When to suppress these devices

- **`audit` mode.** Reporting contradictions is a list, not an essay. Devices 1 through 8 do not apply; keep 9 and 10.
- **`outline` depth.** The compressed decisions only. Keep device 10, drop the rest.
- **Thin input.** When a section is being written honestly and there is little to say, saying it plainly beats dressing it. A quoted buyer voice invented to fill a gap is the worst possible output of this file — it manufactures evidence in the register of evidence.
