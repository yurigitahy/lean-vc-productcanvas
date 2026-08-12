# Coherence checks

Run at the end of each board, and as the entire content of `audit` mode.

A canvas fails in production not because a block is weak but because two blocks decided different things. Four teams filling four boards in four meetings produce a document where the ICP in `P3` and the lead score in `V1` describe different companies, and nobody notices until the pipeline is full of the wrong accounts.

Each check names the two blocks, the test, and what it means. Severity is `red` when the contradiction makes downstream blocks unusable, `yellow` when it costs efficiency but the canvas still runs.

---

## Within Product

| Blocks | Test | Severity | Meaning |
|---|---|---|---|
| `P1` × `P2` | Does `P2` solve the problem `P1` isolated, or a different one? | red | Value proposition drifted to what the team can build. The most common failure in the entire canvas. |
| `P1` × `P2` | Does `P1` describe a solution rather than a problem? | red | `P1` was written backwards from a product decision already made. Everything downstream inherits the assumption. |
| `P2` × `P3` | Can the ICP in `P3` actually perceive the value in `P2` without being educated first? | yellow | If not, the real cost of sale sits in `M7` and `V2`, and neither block has been told. |
| `P3` × `P4` | Does every persona in `P4` exist inside the ICP defined in `P3`? | red | A persona outside the ICP means either the ICP is too narrow or the persona is aspirational. |
| `P2` × `P5` | Is the pricing metric in `P5` correlated with the value described in `P2`? | red | Charging per seat for value delivered per transaction. Margin drifts with customer behavior instead of with decisions. |
| `P3` × `P5` | Can the ICP afford the price, from the budget line `P5` names? | red | Either the ICP or the price is wrong. Naming which is the operator's decision, not the model's. |
| `P5` × `P7` | Does reaching the success criteria in `P7` require usage the price in `P5` makes uneconomic for the customer? | yellow | Success is priced out of reach. Shows up later as low activation. |
| `P2` × `P6` | Does `P2` depend on a capability that lives in a product `P6` did not list? | red | Hidden dependency. Shows up at build time as a surprise. |
| `P7` × any | Are the success criteria measurable with data the company will actually have? | yellow | Unmeasurable criteria become opinion at renewal time. |
| `P8` × `P3` | Does `P8` claim the product opens a new market while `P3` describes the existing customer base? | yellow | Strategic justification and segment decision disagree. Usually the justification is inflated. |

## Within Marketing

| Blocks | Test | Severity | Meaning |
|---|---|---|---|
| `P2` × `M1` | Does the pitch promise something the value proposition does not contain? | red | The pitch is writing the product. Either fix the pitch or admit `P2` was underspecified. |
| `P2` × `M2` | Positioning chosen as innovation or category creation, while `P2` describes replacing a known vendor | red | Category creation costs years of education spend that no one has budgeted. Competition positioning is usually the honest choice. |
| `M2` × `M1` | Does the pitch place the product in the category `M2` chose? | yellow | Market hears two categories, remembers neither. |
| `P4` × `M3` | Do the archetypes match how the persona actually behaves, or how the company would like to be seen? | yellow | Archetype chosen for the brand rather than the buyer. Produces tone the buyer does not respond to. |
| `M3` × `M4` | Does the tone of voice sustain the archetypes under pressure — in a bad-news email, a price increase, an outage? | yellow | Tone defined only for the happy path breaks exactly when it matters. |
| `P3` × `M5` | Is the ICP actually present in the channels `M5` lists, in the role that decides? | red | Channels chosen by team familiarity rather than by where the buyer is. |
| `P5` × `M6` | Do the network-effect incentives in `M6` — discounts, free capacity — violate the business rules in `P5`? | red | Referral programs that break the pricing model. Common and expensive. |
| `M4` × `M7` | Does the content plan sound like the tone of voice, or like the company's existing content? | yellow | Tone defined and then ignored at execution. |
| `M5` × `M8` | Does the launch use a channel not mapped in `M5`? | yellow | Either `M5` is incomplete or the launch is improvising. |

## Within Sales

| Blocks | Test | Severity | Meaning |
|---|---|---|---|
| `P3` × `V1` | Does every qualification criterion in `V1` derive from an attribute stated in `P3`? | red | The score is measuring something the ICP never claimed. Pipeline fills with accounts that fit the score and not the product. |
| `P4` × `V1` | Does the lead profile identify who decides, or only who responds? | yellow | Qualifying the influencer as the buyer. Long cycles, late losses. |
| `P5` × `V2` | Does the sale type match the ticket? Consultative selling on a low ticket, self-serve on a high one | red | Cost of sale and price are structurally mismatched. `V7` will show it as unrecoverable CAC. |
| `P1` × `V3` | Does every trigger in the pain journey trace to a symptom named in `P1`? | yellow | Sales arguments invented at the desk rather than derived from the problem. |
| `M2` × `V3` | Do the objections in `V3` include the ones the positioning in `M2` creates? | yellow | Choosing a position creates predictable objections. Not preparing for them is a choice too. |
| `V1` × `V4` | Does the script qualify against `V1` in the first minutes, or pitch first and qualify later? | yellow | Pitch-first scripts consume the most expensive resource on the least likely accounts. |
| `P5` × `P7` × `V7` | Do ticket, expected CAC, and time to success criteria produce a defensible payback? | red | Where the canvas meets arithmetic. If payback exceeds the retention horizon in `C2`, the model does not fund itself. Hand off to a unit economics diagnostic. |
| `V7` × `V2` | Are the conversion expectations consistent with the sale type and cycle length? | yellow | Enterprise conversion rates applied to a self-serve funnel, or the reverse. |
| `M8` × `V8` | Do the launch calendar and the attack plan agree on dates and sequence? | red | Two teams, two calendars, one launch. |

## Within Customer Success

| Blocks | Test | Severity | Meaning |
|---|---|---|---|
| `P4` × `C1` | Does every stakeholder in `C1` appear as a persona in `P4`, or is it explained why not? | yellow | The person who makes onboarding succeed was never studied. Frequent with technical implementers. |
| `V1` × `C1` | Is the person sold to the person who has to succeed? | yellow | When they differ, onboarding starts with a handoff nobody owns. |
| `P7` × `C3` | Are the success criteria reachable inside the onboarding window `C3` defines? | red | Success defined beyond the horizon in which the customer will judge it. Produces churn from customers who technically got what they bought. |
| `P5` × `C2` | Does the retention horizon in `C2` exceed the payback implied by `P5` and `V7`? | red | The customer leaves before paying for their own acquisition. |
| `C2` × `C4` | Do the touchpoints cluster where churn actually happens, or spread evenly? | yellow | Even distribution of attention is the absence of a retention strategy. |
| `C3` × `C5` | Does the training plan cover the steps onboarding depends on, in the same sequence? | yellow | Training built around the product's feature list rather than the customer's path. |
| `P6` × `C7` | Does expansion propose cross-sell into products `P6` did not map as related? | red | Cross-sell paths that do not exist, or that require integration work nobody scheduled. |
| `C2` × `C7` | Does expansion begin before the retention horizon is reached? | yellow | Selling more to a customer who has not yet succeeded at the first purchase. Accelerates churn. |
| `V3` × `C8` | Do the anti-churn arguments reuse the objections already answered in the sale? | yellow | The reasons for leaving are usually the objections that were overcome rather than resolved. |
| `P7` × `C8` | Does the churn early-warning system measure the same things `P7` calls success? | red | Watching engagement while success is defined as outcome. Warnings arrive after the decision to leave. |

---

## Reporting

Rank by severity, then by how many downstream blocks each contradiction affects. Report at most the top five and say how many others exist. A list of twenty contradictions gets none of them fixed.

For each: name both block codes, state the contradiction in one sentence, take a position on which side is likely wrong, and name the cheapest way to find out.
