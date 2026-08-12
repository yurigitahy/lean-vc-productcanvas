# Dependency graph

Every block depends on everything before it. Only a few of those dependencies are load-bearing. This file names which.

**Hard dependency** — the block cannot be generated without this one. Load it in full. Never more than four per block.

**Soft context** — read the canonical extract, not the full block. All completed extracts are always available.

**Downstream** — blocks that go `STALE` when this one changes.

---

## Product

| Code | Block | Hard dependencies | Downstream |
|---|---|---|---|
| `P1` | Problem and Opportunity | — | P2, P3, P7, P8, M2, M7, V3, C8 |
| `P2` | Value Proposition | P1 | P3, P4, P5, P6, P7, M1, M2, C3 |
| `P3` | Ideal Customer Profile | P1, P2 | P4, P5, M1, M5, V1, V2, C1 |
| `P4` | Target Personas | P2, P3 | M3, M4, M5, V1, C1 |
| `P5` | Monetization and Business Rules | P2, P3 | P6, P7, P8, M6, V2, V7, C2, C7 |
| `P6` | Impacted Products | P2, P5 | P8, M6, C5, C7 |
| `P7` | Success Criteria | P1, P2, P5 | P8, M1, V7, C2, C3, C8 |
| `P8` | Priority and Strategy | P1, P5, P6, P7 | M8, V8 |

## Marketing

| Code | Block | Hard dependencies | Downstream |
|---|---|---|---|
| `M1` | Elevator Pitch | P2, P3, P7 | M2, V4 |
| `M2` | Market Positioning | P1, P2, M1 | M3, M4, M5, M8, V3 |
| `M3` | Anchoring Archetypes | P4, M2 | M4 |
| `M4` | Persona Tone of Voice | P4, M2, M3 | M7, V3 |
| `M5` | Relationship Channels | P3, P4, M2 | M6, M7, M8, V1, V6 |
| `M6` | Network Effect | P5, P6, M5 | M8, C7 |
| `M7` | Content and Nurture | P1, M4, M5 | M8, V5, V6, C6 |
| `M8` | Launch Communications | P8, M2, M5, M7 | V6, V8 |

## Sales

| Code | Block | Hard dependencies | Downstream |
|---|---|---|---|
| `V1` | Ideal Lead Profile | P3, P4, M5 | V2, V4, V6, V7, C1 |
| `V2` | Sale Type | P3, P5, V1 | V4, V7 |
| `V3` | Pain Journey | P1, M2, M4 | V4, V5, C8 |
| `V4` | Sales Script | M1, V1, V2, V3 | V5 |
| `V5` | Support Materials | M7, V3, V4 | — |
| `V6` | Demand Anticipation | M7, M8, V1 | V8 |
| `V7` | Metrics and Indicators | P5, P7, V1, V2 | V8, C2 |
| `V8` | Attack Strategy | P8, M8, V6, V7 | — |

## Customer Success

| Code | Block | Hard dependencies | Downstream |
|---|---|---|---|
| `C1` | Customer Stakeholders | P3, P4, V1 | C3, C5 |
| `C2` | Retention Expectation | P5, P7, V7 | C4, C7, C8 |
| `C3` | Onboarding Journey | P2, P7, C1 | C4, C5 |
| `C4` | Touchpoints | C2, C3 | C6, C7, C8 |
| `C5` | Training Plan | P6, C1, C3 | C6 |
| `C6` | Nurture Cadence | M7, C4, C5 | — |
| `C7` | Expansion Revenue | P5, P6, C2, C4 | — |
| `C8` | Anti-Churn Strategy | P7, V3, C2, C4 | — |

---

## Load-bearing blocks

Counting how often each block appears as a hard dependency:

| Block | Times a hard dependency |
|---|---|
| `P5` Monetization and Business Rules | 8 |
| `P2` Value Proposition | 7 |
| `P3` Ideal Customer Profile | 6 |
| `P7` Success Criteria | 5 |
| `P1` Problem and Opportunity | 4 |
| `P4` Target Personas | 4 |
| `M2` Market Positioning | 4 |
| `M5` Relationship Channels | 4 |

Everything else is depended on three times or fewer. Two consequences:

1. The cost of getting `P2`, `P3`, `P5`, and `P7` wrong is roughly an order of magnitude higher than the cost of getting `V5` or `C6` wrong. Spend the depth there. Offer `deep` on those four by default.
2. When an operator wants to skip straight to a downstream block, the provisional questions that matter most are the ones standing in for these eight. Ask those carefully; the rest can be resolved with a single question.

## Terminal blocks

`V5`, `V8`, `C6`, `C7`, `C8` have no downstream. They can be regenerated freely without invalidating anything. They are also the blocks most safely produced in isolation when an operator wants a quick, low-commitment output.

## Fork points

When a canvas forks from product-wide into per-ICP or per-persona:

- **Shared across forks:** `P1`, `P2`, `P5`, `P6`, `P8`, `M2`, `M6`
- **Forked per ICP:** `P3`, `P4`, `P7`, `M1`, `M5`, `M7`, `V1`, `V2`, `V7`, `C1`, `C2`, `C3`, `C7`
- **Forked per persona:** `M3`, `M4`, `V3`, `V4`, `V5`, `C4`, `C5`, `C6`, `C8`

`M8` and `V6` and `V8` are per-launch rather than per-profile: one launch may address several profiles at once, and the block should say which.

## Cycles that are not cycles

Three pairs look circular and are not. Resolve them in this order:

- `P5` ↔ `V7`. `P5` sets price and business rules as a hypothesis. `V7` derives CAC, conversion, and payback from that hypothesis and may falsify it. When it does, `P5` is revised and everything downstream of `P5` goes stale. That is the intended loop, run once, not a dependency.
- `P7` ↔ `C2`. `P7` defines what success means. `C2` estimates how long the customer stays given that definition and the price. If `C2` produces a horizon shorter than the time needed to reach `P7`'s success criteria, `P7` is wrong, not `C2`.
- `M2` ↔ `M1`. `M1` is written first, deliberately, because a pitch that cannot be written in three sentences signals a value proposition that is not yet decided. `M2` then formalizes the category and may force `M1` to be rewritten. Expect one rewrite; treat a second as evidence that `P2` is unresolved.
