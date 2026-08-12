# Worked example — `P1` at standard depth

A single block, generated for a synthetic company, showing the expected shape of the output.

**Everything below is invented.** The company does not exist, the figures are constructed to be internally consistent for illustration, and the external references are placeholders standing in for real research. In an actual run, external evidence comes from live search and is sourced.

Currency is written as `$` and means nothing more than one unit of the operator's reporting currency.

---

## Intake as submitted

```
COMPANY
Company:              Synthetic company operating in workforce compliance software
Existing products:    One — a certification tracking tool sold to facilities contractors
Market:               Mid-size facilities-management contractors, single country
Stage:                Paying customers on the existing product

THE PRODUCT
Working name:         Subcontractor Compliance
Description:          Verifies and monitors compliance documents for subcontracted crews
Regime:               Portfolio extension
Why now:              Three customers asked; one offered to fund development
Owner:                Head of Product

WHAT IS ALREADY DECIDED
Fixed:                Must integrate with the existing certification product
Discarded:            A manual verification service, tried in 2025, did not scale

EVIDENCE ON HAND
14 customer interviews, 8 months of support tickets, 3 lost-deal records
Competitors:          Two named point solutions, plus spreadsheets

CONSTRAINTS
Team:                 Two engineers, one designer, part-time PM
Deadline:             None stated
```

---

## Inputs consumed

- Intake, above. No prior blocks — `P1` has no hard dependencies.
- Regime: **portfolio extension**, so internal evidence is required where it exists. 14 interviews and 8 months of tickets are available and were used. No external benchmark was consulted for section 6; that gap is marked.

---

## 1. Core problem

A facilities contractor is legally and commercially accountable for work performed by crews it does not employ. The obligation transfers; the visibility does not. The contractor must be able to demonstrate, at any moment and for any crew on any site, that the required insurance, licences, and certifications were valid on the day the work was done — while the documents themselves live with dozens of subcontractors who have no incentive to keep them current and no obligation to notify anyone when they lapse.

The structural feature is a mismatch of incentive and consequence. The party holding the document bears none of the risk of it expiring; the party bearing the risk does not hold the document.

## 2. How the problem presents

**Financial.** Insurance premium loading after an audit finds gaps. Retained payments held by clients pending documentation. Occasional refused claims where cover had lapsed at the time of the incident.

**Operational.** A coordinator spends part of most days chasing certificates by email and phone. Crews are turned away at site gates. Work is rescheduled around paperwork rather than capacity.

**Relational.** Clients ask for compliance evidence with short notice and receive it slowly, which reads as disorganization regardless of whether the underlying compliance was sound.

**Political.** Nobody owns the problem. Operations blames procurement, procurement blames the subcontractors, and the person who notices the gap is usually the person least able to fix it.

*[Supplied by the operator: the coordinator time figure and the gate refusals appear in 9 of 14 interviews. Inference: the political dimension — no interview named it directly, but three described handoffs where responsibility was ambiguous.]*

## 3. Structural dependency

The contractor's compliance position is only as current as the least diligent subcontractor's filing habits, and there is no mechanism that makes diligence worth anything to the subcontractor. This does not resolve with effort: adding chasing capacity increases coverage linearly and cost linearly, which is why the manual service discarded in 2025 did not scale.

## 4. What the customer does today

A shared spreadsheet with expiry dates, maintained by one person, updated when someone remembers. Two of the fourteen use a point solution for insurance certificates only, leaving licences and certifications outside it. The remainder rely on the subcontractor confirming by email that they are covered, which is an assertion rather than a document.

## 5. Why it has not been solved

Organizational rather than technical. The work is boring, distributed, and belongs to no function. It becomes visible only during an audit or after an incident, and by then it is handled as an exception rather than as a process.

## 6. Cost of inaction

Constructed from operator-supplied figures rather than measured: coordinator time at roughly 0.4 FTE, retained payments averaging a mid-five-figure sum outstanding at any time, and one refused claim reported across the fourteen interviews in the last three years.

*No verifiable external data was found on refused-claim frequency in this segment.* That absence matters — the tail risk is the strongest argument in the problem and the least evidenced part of it. It appears again in `P2` and in `V3`.

## 7. Who feels it

The compliance or operations coordinator feels it daily and cannot authorize a purchase. The operations director feels it during audits and can authorize within a threshold. The owner or CFO feels it only after an incident, and can authorize anything.

The gap between daily pain and purchasing authority is the central commercial fact in this problem and will shape `P4`, `V1`, and `V2`.

## 8. Urgency triggers

Insurance renewal. A client audit. A failed gate check that halted work. An incident, anywhere in the industry, that made the local trade press. The addition of a large client with stricter documentation requirements.

## 9. Pain hierarchy

1. Not being able to prove compliance on demand — the risk that produces retained payments and lost claims.
2. Coordinator time consumed by chasing.
3. Crews refused at gates.
4. Client perception of disorganization.

The ranking is by customer intensity, not by ease of solution. Notably, item 2 is the easiest to solve and item 1 is the one that funds a purchase.

## 10. Current versus desired state

| Today | Desired |
|---|---|
| Compliance status known at the last time someone checked | Known continuously, per crew, per site |
| Evidence assembled reactively over days | Produced on demand in minutes |
| Expiry discovered at the gate | Discovered weeks ahead, by the party who can act |
| Responsibility ambiguous | One owner, one record |

## 11. Evidence

14 interviews, 8 months of tickets, 3 lost-deal records — all internal, from adjacent customers of the existing product. Not consulted and available: renewal conversations, and the two clients who asked for this feature by name.

Missing entirely: any data from subcontractors, who are the other half of the mechanism and have never been interviewed.

## 12. What would falsify this

If contractors treat a lapsed document as a paperwork nuisance rather than as risk, the problem is item 2 in the hierarchy rather than item 1, and the product is a time-saver at a time-saver's price. The cheapest test: ask five contractors what their insurer asked for at last renewal, and whether it changed the premium.

---

**Central statement**

The contractor carries the risk of documents held by parties with no incentive to maintain them.

**Assumptions and how to kill them**

| Assumption | Falsification test |
|---|---|
| Refused claims are frequent enough to be a purchase driver | Ask five contractors and one broker about the last three years |
| Coordinator time is 0.4 FTE, not 0.1 | Two contractors log a week of the coordinator's time |
| Subcontractors will supply documents to a system if asked | Approach ten subcontractors of one customer directly |

**Downstream impact**

- `P2` must address item 1 of the hierarchy — provability — not item 2. A product framed around saving coordinator time addresses the wrong pain and will be priced against a salary rather than against risk.
- `P4` inherits a three-role structure with a gap between the person feeling the pain and the person who can buy.
- `V3` inherits the urgency triggers in section 8 as detection signals, and the evidence gap in section 6 as its weakest argument.
- `P3` must decide whether subcontractors are a second segment or an unpaid participant, which is a strategic choice, not a detail.

**Contradictions detected**

None — `P1` has no predecessors. One tension recorded for later: the funded demand mentioned in intake came from three customers who described the problem as coordinator workload, which is item 2, while this block ranks provability first. `P8` will need to reconcile who is paying for what.

**Canonical extract**

```
P1 — Problem and Opportunity
Core problem:        The contractor carries the risk of documents held by parties with no incentive to maintain them.
Top three symptoms:  Retained payments; coordinator time chasing; crews refused at gates.
Status quo:          Shared spreadsheet, one owner, updated from memory.
Cost of inaction:    ~0.4 FTE plus retained payments; tail risk of a refused claim (unevidenced).
Who feels it:        Compliance coordinator ; who can fix it: Operations director (threshold) / CFO (above)
Urgency triggers:    Insurance renewal; client audit; halted work at a gate.
Strongest pain:      Inability to prove compliance on demand.
Evidence base:       14 interviews, 8 months tickets, 3 lost deals — all contractor-side. No subcontractor evidence at all.
```

**→ Validation task:** Ask five contractors what their insurer requested at the last renewal and whether documentation gaps changed the premium. Until that exists, the strongest pain in the hierarchy rests on one reported incident across fourteen interviews, and `P2` would be built on it.
