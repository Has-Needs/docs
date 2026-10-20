# Has-Needs: Research Thesis, Designed Emergence, and Evaluation Framework
*White-paper companion draft — 20 October 2026. Research propositions, not additional V1 protocol requirements.*

## Abstract
Has-Needs proposes a sovereignty-first coordination architecture in which people and organizations independently express what they **have** and **need**, discover potential counterparties, voluntarily accept a commitment into **WORKING**, and preserve a mutually recognized outcome. Its research thesis is that direct, consented expression of intent—combined with local discovery, human-approved equivalence, and outcome records—can reduce the institutional cost of guessing what people need while improving coordination and accountability. This document distinguishes specified mechanisms from hypothesized benefits and outlines experiments that could refute those hypotheses.

## 1. Paradigm delta: from observed behavior to expressed intent
Many existing systems use administrative reports, surveys, transaction histories, or behavioral and location observations to estimate demand. These remain useful for many purposes, but **observation cannot by itself establish a person's intent**. Has-Needs starts with a participant's expressed Has or Need, with participant-controlled context and disclosure. A Need can move from expression to candidate match, explicit acceptance, work, and resolution; it is not merely a data point.

A declared Need is neither necessarily true nor representative of every resident. The claim is narrower and testable: for participating people and tasks, directly expressed intent may be more actionable and less expensive to obtain than reconstructed intent. Coverage, accessibility, consent, accuracy, and exclusion must be evaluated.

**Georeferenced, not necessarily surveilled.** Participants may share location at an appropriate precision and duration for a particular purpose; useful live geographic coordination must not imply mandatory continuous tracking, publication of exact addresses, or compulsory participation. Aggregate geographic views require explicit disclosure rules and safeguards against reidentification.

## 2. Formal coordination model
The core independent objects are **Has** and **Need**, with contextual meaning supplied by participants rather than imposed by a universal institutional taxonomy. Discovery suggests possible matches; only authorized participants determine whether an exchange is meaningful. Explicit mutual acceptance creates a WORKING commitment. A pending journal records progress and resolution; completed exchanges produce a canonical receipt recognized by the parties. Cancellation and no-deal outcomes must remain distinguishable from successful fulfillment.

A minimal research event model is: `event_id`, `event_time`, `actor_role` (privacy-preserving), `object_kind`, `consented_context`, `geographic_precision`, `state_before`, `state_after`, `commitment_id`, `outcome`, and `evidence_class`. This is an *analytical schema*, not a requirement to expose identity, plaintext, or private location on a public ledger. Observability must be derived only from authorized views.

## 3. Intentional emergence: causal mechanisms and failure conditions
The architecture deliberately seeks downstream effects from a small set of rules. Each is a **hypothesis**, not a guaranteed consequence.

| Design decision | Proposed causal mechanism | Predicted emergent outcome | Important failure mode |
|---|---|---|---|
| Independent Has and Need declarations | Participants reveal actionable supply and demand | Reduced need-discovery and inference work | Low adoption or misleading declarations |
| Human-approved matching and completion | Actual exchanges provide evidence of locally valid equivalence | A practical ontology of what worked | Selection bias; ambiguous outcomes |
| WORKING commitments and outcome receipts | Commitments and delays become visible to authorized parties | Operational accountability and bottleneck discovery | Off-platform work or strategic gaming |
| Community pooling and delegation | Individual interests can be met through shared fulfillment | Stronger coordination as needs converge in crises | Governance capture or unequal access |
| Local-first, accessible participation | Communication continues despite infrastructure degradation | Resilient participation during disruption | Device, power, network, or accessibility failures |
| Participant-controlled identity and disclosure | People can act without surrendering unrelated personal information | Useful civic intelligence without surveillance as default | Reidentification from rare needs or fine-grained maps |
| Persistent outcome records | Later decisions can use evidence of earlier resolutions | Self-improving coordination and disaster accounting | Biased, incomplete, or incomparable records |

The architecture's democratic implication is not that every expressed Need must be fulfilled. It is that citizens and institutions can see, under appropriate permissions, what was requested, what was accepted, what remained unresolved, and where responsibility lies.

## 4. Safe AI: human–AI interdependence
AI may propose candidate matches, translations, groupings, and plausible equivalences across a large search space. It does **not** independently define human value, consent on a participant's behalf, authorize disclosure, or finalize an exchange. People decide whether a match is useful and whether the agreed outcome occurred; protocol authorization and state-transition controls enforce those decisions independently of model output.

This creates a proposed learning loop: machine-generated candidates → human acceptance/rejection → executed interaction → verified outcome → improved discovery. The outcome record is evidence of *one situated exchange*, not proof of universal semantic equivalence. Evaluation must measure hallucinated matches, harmful suggestions, automation bias, disparate performance, and whether human control is real in practice.

## 5. Disaster economics: full costs, operational savings, and payment
**Full disaster cost** and **county-realizable savings** are different quantities. Full accounting identifies direct physical losses, response operations, recovery expenditures, indirect interruption, human consequences, and long-term effects, while separating public/private incidence, stocks/flows, transfers/resource costs, and overlapping categories. Unknown values remain unknown rather than becoming zero.

The commercial proposal is a **one-time fee equal to 5% of mutually assessed, realized efficiency savings** for an adopting county, not 5% of total disaster damage. A practical starting point is comparison with a prior broadly similar event, adjusted for severity, exposed population and infrastructure, prices, time horizon, and response scope. Pre-agreeing the comparator and evidence rules is preferable to negotiating them after outcomes are known.

Has-Needs changes the quality of the second event's measurement: consented, time-stamped Need, Has, WORKING, and resolution records can reveal work, delays, and unmet demand that historical accounting could not capture. That asymmetry is an advantage for operational learning **but a challenge for unbiased before/after comparisons**. Compare common accounting fields first; report newly visible costs and benefits separately.

### Savings primitives
1. **Avoided need discovery and inference:** expenditures actually reduced for demand estimation, monitoring, surveys, data acquisition, analytics, and related verification.
2. **Avoided discovery outreach:** outreach expenditure specifically aimed at finding needs, not public warnings, accessibility, education, or other indispensable communication.
3. **Operational coordination:** reduced duplicate dispatches, misrouted supplies, avoidable transport, idle resources, and administrative handling.
4. **Time and harm avoided:** earlier fulfillment and avoided downstream consequences, monetized only with defensible attribution and without double counting.
5. **Reassigned capacity:** report released staff hours or infrastructure separately from cash savings unless budgets demonstrably fall or a documented opportunity cost is realized.

For each primitive record the pre-event method, expense owner, unit, observed quantity, baseline comparator, evidence, uncertainty, and whether the saving overlaps another line. Deduct deployment and operation costs before determining net eligible savings. A hypothetical 40% efficiency improvement is a scenario parameter, **not** an established result.

## 6. Testable hypotheses and research design
**H1 — Inference displacement:** In comparable service workflows, direct participant expression lowers cost per accurately identified actionable Need relative to existing discovery methods. **Primary measure:** fully loaded discovery cost / validated actionable Needs; secondary measures include accuracy, time, coverage, and opt-out rate.

**H2 — Coordination:** Has-Needs reduces median and tail time from Need expression to fulfillment, controlling for severity, supply, and connectivity. **Measures:** time-to-match, time-to-acceptance, time-to-resolution, unfulfilled fraction, repeat dispatches, and resource utilization.

**H3 — Accountability:** Participating agencies identify and resolve bottlenecks faster when accepted commitments and outcomes are visible. **Measures:** overdue WORKING commitments, escalation delay, resolution time, and independently verified completion.

**H4 — Safe AI:** Human-approved AI matching improves useful candidate discovery without increasing unauthorized disclosure or erroneous commitments. **Measures:** useful-match precision/recall, human override rate, privacy incidents, and outcome quality versus non-AI discovery.

**H5 — Economic benefit:** Net, severity-adjusted county operational expenditure is lower with deployment than under a credible counterfactual. **Measures:** eligible cost by category, deployment cost, normalized total, confidence interval, and audited attribution.

**H6 — Crisis pooling:** Under higher levels of concurrent unmet demand, opt-in pooled coordination increases fulfillment per unit of scarce transport or storage capacity relative to separate fulfillment. **Measures:** pooled delivery success, delay, participant satisfaction, exclusion, and cost.

Where feasible, compare phased deployments or matched jurisdictions/workflows, use pre-registered measures and independent audits, and preserve a baseline before implementation. A simple historical flood-to-flood comparison is a useful commercial screening method but is not by itself causal proof. Document weather severity, exposure, population, policy changes, aid levels, and reporting changes. Publish null and adverse results.

## 7. Embedded research instrumentation and ethics
The eleven analytical primitives are **event, affected entity, impact, Need, resource, activity, exchange, outcome, cost consequence, counterfactual, and attributable benefit**. Each requires a definition, measurement unit, provenance, uncertainty, and double-counting rule. Participant-owned operational records can supply event traces, but budget ledgers, payroll, invoices, independent damage assessments, and counterfactual design are needed to establish financial savings.

Participation is voluntary. No inference of consent from emergency vulnerability; avoid coercive conditional access to essential services. Protect exact locations and sensitive needs through purpose limitation, minimum necessary disclosure, retention limits, revocation where technically possible, and independent security review. Public maps and aggregated statistics must be evaluated for reidentification. Report participation bias and the needs of people who cannot or choose not to use the system.

## 8. Evidence ladder and scholarly positioning
Separate: **(A) specified architectural behavior**, verifiable in protocol and code; **(B) predicted designed emergence**, supported by causal arguments but not yet observed; **(C) pilot observations**, measured with stated limitations; and **(D) independently replicated effects**. Avoid claiming Has-Needs has proven superior to every surveillance or disaster-management system before comparative studies.

The scholarly contribution to investigate is the combination of sovereign intent expression, consented geographic relevance, human–AI matching with human authority, verifiable reciprocal outcomes, and institutional cost observability. A literature review should compare participatory sensing, crowdsourced crisis mapping, resource-matching platforms, mechanism design, public-sector cost accounting, trauma-informed design, and human-in-the-loop AI. Novelty should be argued at the level of the *combined mechanism and its measurable consequences*, not by asserting that no precursor exists.

## 9. Origin and design rationale
Firsthand observations of handwritten Has/Need notices after disasters demonstrate a naturally occurring coordination pattern without centralized digital infrastructure. Experience with autonomous affinity-group spokescouncils informs the possibility of pooled action without surrendering individual sovereignty. These are design inputs and motivation, not empirical validation of the implemented protocol.

## Conclusion
Has-Needs asks a falsifiable question: **When institutions can respond to what people voluntarily say they need, rather than paying to infer needs from observed behavior, do coordination, accountability, resilience, and net costs improve?** Its contribution is a concrete architecture for testing that question while keeping participants—not AI systems or institutions—in authority over their own commitments and disclosures.
