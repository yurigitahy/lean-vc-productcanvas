# Contributing

This skill improves through use. If you ran a block on a real product and it produced something obvious, generic, or wrong, that is the most valuable contribution available.

## What is wanted

**Section additions.** A required section earns its place if omitting it would produce a decision someone regrets later. Submit it with the block code, the position in the order, and one sentence on what failure it prevents.

**Coherence checks.** `references/coherence-checks.md` is the highest-leverage file in the repository. A new check needs: the two block codes, the test, the severity, and one sentence on what the contradiction causes downstream.

**Dependency corrections.** If a block cannot be written without loading something not in its `hard_deps`, that is a bug in `references/dependency-graph.md`. Open an issue with the block and what was missing.

**Regime coverage.** `references/regimes.md` covers greenfield, portfolio extension, and repositioning. A regime with genuinely different evidence rules — regulated markets, hardware, two-sided marketplaces — is welcome if it changes what blocks require rather than only what they discuss.

**Translations.** The block files are instructions to the model, not user-facing text, and the skill responds in the operator's language. Translating them is therefore not needed and doubles the maintenance surface. Translation contributions are declined for this reason, not for lack of interest.

## What is not wanted

**Real company data.** Everything in `examples/` is invented. Do not submit intake data, canvases, transcripts, or figures from an actual business, yours or anyone else's. Examples must be synthetic and internally consistent.

**Scoring, grading, or maturity levels.** The canvas produces decisions and open questions. A score ends the conversation, which is the opposite of the intent.

**Generic product advice.** If a section can be filled without looking at the operator's specific situation, it does not belong here.

**Vocabulary from the banned list.** `references/output-contract.md` bans a set of words without concrete qualifiers. Contributions hold themselves to the same rule.

## Rules for changes

- `SKILL.md` stays under 500 lines. Content beyond that goes into `references/` with a pointer from the body.
- Block files stay under 200 lines. A block needing more is usually two blocks or a reference file.
- Every block file keeps the same section order: what it decides, what it is not, required sections, evidence rules by regime, quality tests, canonical extract, probing questions, contradictions to watch.
- Canonical extracts stay under ten lines. The extract is what 31 other blocks read; length there is paid for in every later session.
- The `description` field in the `SKILL.md` frontmatter is the trigger mechanism. Changes to it need a note on what phrasing they are meant to catch.

## Process

1. Open an issue describing the change and the failure it addresses, before writing it.
2. One concern per pull request.
3. If you change a block's required sections or its canonical extract, check that the extract still carries everything the downstream blocks listed in `dependency-graph.md` need.
