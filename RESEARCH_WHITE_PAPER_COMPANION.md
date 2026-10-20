# Has-Needs: Research Thesis, Designed Emergence, and Evaluation Framework
*Research companion release candidate — 20 October 2026. Research propositions, not additional V1 protocol requirements. Empirical claims remain unvalidated.*

## Abstract
Has-Needs proposes a sovereignty-first coordination architecture in which people and organizations independently express what they **have** and **need**, discover potential counterparties, voluntarily accept a commitment into **WORKING**, and preserve a mutually recognized outcome. Its research thesis is that direct, consented expression of intent—combined with local discovery, human-approved equivalence, and outcome records—can reduce the institutional cost of guessing what people need while improving coordination and accountability. This document distinguishes specified mechanisms from hypothesized benefits and outlines experiments that could refute those hypotheses.

## Opening: the person already knows something the response needs

After a flood, a person may know that their drinking water is gone, that a neighbor cannot leave an upstairs room, and that a usable cart is sitting nearby. Those facts, capabilities, and priorities exist before an agency has an intake record. The design problem is how that person can express what matters, find a useful counterpart, authorize action, and retain a record of the result—even when ordinary infrastructure is disrupted.

Has-Needs begins there. The individual originates a request and can also offer help. Someone offering water can discover the request within an appropriate fulfillment area. The participants decide whether the proposed exchange meets their conditions. Acceptance places the matched Has and Need into WORKING; the Need's pending journal preserves the accepted commitment and authorized progress. Their agreed resolution produces the same canonical receipt for their separate private histories. A failed or cancelled exchange remains distinguishable from successful delivery.

The intended immediate value is a useful action the person can understand and choose. The wider value is that many such interactions may create a timely picture of unmet requests, available capabilities, accepted obligations, and resolved exchanges through specifically authorized views. An agency can participate in that process without becoming the source of the individual's authority or gaining access to everyone's private records. Vulnerability does not imply informational poverty.

This is also the continuity proposition: the same relationships can support everyday exchange, emergency response, and recovery. People need not first become administrative cases to participate. Whether the architecture delivers this continuity under real failures is an implementation and field-research question.

## 1. Paradigm delta: from observed behavior to expressed intent
Many existing systems use administrative reports, surveys, transaction histories, or behavioral and location observations to estimate demand. These remain useful for many purposes, but **observation cannot by itself establish a person's intent**. Has-Needs starts with a participant's expressed Has or Need, with participant-controlled context and disclosure. A Need can move from expression to candidate match, explicit acceptance, work, and resolution; it is not merely a data point.

A declared Need is neither necessarily true nor representative of every resident. The claim is narrower and testable: for participating people and tasks, directly expressed intent may be more actionable and less expensive to obtain than reconstructed intent. Coverage, accessibility, consent, accuracy, and exclusion must be evaluated.

**Geography describes where fulfillment is possible.** V1 §21 separates a resource, service area, route, destination, or other sphere of possibility from a participant's actual position. Actual participant position is not retrievable through protocol operations or serialized into shared objects, journals, receipts, or routing headers. An explicitly shared rendezvous instruction is a separately authorized disclosure with its own exposure risk. Useful geographic coordination therefore begins with compatible possibilities, not a map of people's whereabouts. Aggregate views and repeated queries still require evaluation for inference and reidentification.

## 1A. Three inversions: authority, knowledge, and complexity

**Authority comes from the participant.** A person is not an institutional data source awaiting classification. They originate their own Has and Need propositions, meanings, disclosure boundaries, and authorized relationships. Institutions, companies, communities, and AI systems can be counterparties or aids without becoming the source of the participant's authority. This is a design premise, not a claim that the protocol alone overrides existing law.

**Knowledge begins with declared meaning rather than inferred preference.** An expressed Need is evidence that someone made a declaration, not proof that the statement is objectively correct. A candidate match is a conjecture; an accepted WORKING commitment is evidence of agreement; a matching receipt establishes integrity of the recorded resolution, not physical-world truth. The distinction permits research on whether voluntary declarations improve operational knowledge without converting people into continuously observed subjects.

**Complexity emerges from composition rather than a catalog of modules.** A small grammar of Has, Need, Working, contract terms, participant-controlled personas, and reciprocal evidence can support markets, governance workflows, mutual aid, research participation, and community coordination. These are deliberately anticipated emergent functions, not independent platform subsystems. The claim to test is whether this reduction produces useful new coordination patterns with lower integration and institutional overhead.

The three inversions must be assessed together. An implementation that improves matching while centralizing semantic authority, or that creates accurate dashboards by silently expanding disclosure, may improve a conventional metric while violating the architecture's central hypothesis.

## 1B. Psychological agency and trauma-informed design

A person experiencing a disaster may know their immediate condition better than any remote organization, even when infrastructure and institutions have failed. Has-Needs treats their ability to declare a request, offer a capability, choose a counterpart, and retain evidence of an agreement as a first-class design concern. The proposed psychological mechanism is **restored agency through meaningful, voluntary action**, not simply better reporting. A survivor may be both a person needing assistance and someone able to help others.

This predicts testable outcomes: compared with conventional intake, participants may report greater perceived agency, comprehension of their options, procedural fairness, and confidence that their requests were heard. Research should measure these independently of fulfillment rates, with trauma-sensitive consent, accessible alternatives, and protections against coercion. The design does not establish a clinical trauma treatment or guarantee psychological benefit.

## 1C. Sovereign information relationships and their limits

Participant-originated personas and bounded, composable access can let an individual authorize a specific use of information without transferring general control over unrelated facets. Revocation can terminate future access through a controlled live interface, but cannot erase plaintext already copied or information legitimately retained under applicable law. A declaration of ownership or an authorization token does not by itself create new legal remedies: enforceable obligations depend on law, contract, and jurisdiction.

This invites empirical comparison of disclosure minimization, participant comprehension, reidentification risk, auditability, and the costs of verifying permitted use. It also invites legal scholarship on provenance, copyright, consent, data portability, cross-jurisdiction enforcement, and whether machine-readable authorizations can improve evidentiary accountability without overstating their legal effect.

## 1D. Relationship evidence, community formation, and geographic possibility

Has-Needs does not require a universal reputation score. Where authorized, people can inspect relevant reciprocal history and integrity evidence, then decide for themselves whether a proposed relationship is acceptable. Research can compare that approach with platform-computed trust scores on calibration, exclusion, fairness, susceptibility to gaming, and informed choice.

Communities can arise from accepted commitments and shared needs rather than from prior registration into an institution's fixed organizational model. Governance is one potential counterparty: accepted service obligations, elapsed time, reassignment, and unresolved backlogs may reveal bottlenecks without claiming that a declaration alone legally binds an agency. Geographic relevance means the area in which fulfillment is possible; it need not expose where a participant physically is. Evaluate these mechanisms for accessibility, response time, power concentration, and privacy leakage.

## 1E. The Delta as an AI reasoning experiment

The [Paradigm Delta](./Has-Needs_Paradigm_Delta_Review_2026-10-14.md) is an interpretive primer designed to help humans and models avoid importing conventional SaaS and institutional assumptions. It is itself testable: assign identical specification interpretation and implementation tasks to models with and without the Delta, blind-score architectural errors, and repeat after intervening context to measure persistence. A separately verified [BIAS AGENTS.md](https://bias.rest/AGENTS.md) may be studied as an additional general-purpose reasoning audit. Neither document is a substitute for normative V1 requirements.

## 2. Formal coordination model
The core independent objects are **Has** and **Need**, with contextual meaning supplied by participants rather than imposed by a universal institutional taxonomy. Discovery suggests possible matches; only authorized participants determine whether an exchange is meaningful. Explicit mutual acceptance creates a WORKING commitment. The Need owns an append-only pending journal of accepted commitments and authorized progress; agreed final resolutions produce identical canonical receipts held in the participants' separate private histories. Cancellation and no-deal outcomes must remain distinguishable from successful fulfillment.

A minimal research event model is: `event_id`, `event_time`, `actor_role` (privacy-preserving), `object_kind`, `consented_context`, `geographic_applicability`, `state_before`, `state_after`, `commitment_id`, `outcome`, and `evidence_class`. This is an *analytical schema*, not a requirement to expose identity, plaintext, or private location on a public ledger. Observability must be derived only from authorized views.

## 3. Intentional emergence: causal mechanisms and failure conditions
The architecture deliberately seeks downstream effects from a small set of rules. Each is a **hypothesis**, not a guaranteed consequence.

| Design decision | Proposed causal mechanism | Predicted emergent outcome | Important failure mode |
|---|---|---|---|
| Independent Has and Need declarations | Participants reveal actionable supply and demand | Reduced need-discovery and inference work | Low adoption or misleading declarations |
| Human-approved matching and completion | Actual exchanges provide evidence of locally valid equivalence | A practical ontology of what worked | Selection bias; ambiguous outcomes |
| WORKING commitments and outcome receipts | Commitments and delays become visible to authorized parties | Operational accountability and bottleneck discovery | Off-platform work or strategic gaming |
| Explicitly delegated pools and individually authorized logistics clusters | Participants combine fulfillment while preserving the authority specified in their agreements | Stronger coordination as needs converge in crises | Treating membership or shared transport as blanket delegation |
| Local-first, accessible participation | Communication continues despite infrastructure degradation | Resilient participation during disruption | Device, power, network, or accessibility failures |
| Participant-controlled identity and disclosure | People can act without surrendering unrelated personal information | Useful civic intelligence without surveillance as default | Reidentification from rare needs or fine-grained maps |
| Persistent outcome records | Later decisions can use evidence of earlier resolutions | Self-improving coordination and disaster accounting | Biased, incomplete, or incomparable records |

The architecture's democratic implication is not that every expressed Need must be fulfilled. It is that citizens and institutions can see, under appropriate permissions, what was requested, what was accepted, what remained unresolved, and where responsibility lies.

### 3.1 How one exchange can change the next

A successful exchange leaves more than a closed task. Under the relevant permissions, it can supply evidence that a locally meaningful request and capability worked together, a reciprocal connection for future vetting, and a resolved obligation for operational review. These are distinct uses of the same situated interaction; none requires publishing the participants' private chains.

Repeated successful interactions may make useful semantic paths easier to discover and give participants reasons to cooperate again. People can form an ongoing community Need, pool fulfillment under explicit delegation, or coordinate a shipment as a cluster while retaining individual authorization. Community membership alone grants no authority over a member's resources. This is how broader organization is intended to arise from the existing grammar.

The proposed feedback is local and conditional: useful resolution can improve subsequent discovery and cooperation, which may enable further resolution. Unresolved commitments remain in pending evidence; agreed cancellation records resolution without being counted as successful fulfillment. Research must test whether this feedback actually increases capacity, or instead concentrates opportunity among already connected participants. The ontology remains a contextual map of what has worked.

## 4. Safe AI: human–AI interdependence
AI may propose candidate matches, translations, groupings, and plausible equivalences across a large search space. It does **not** independently define human value, consent on a participant's behalf, authorize disclosure, or finalize an exchange. People decide whether a match is useful and whether the agreed outcome occurred; protocol authorization and state-transition controls enforce those decisions independently of model output.

This creates a proposed learning loop: machine-generated candidates → human acceptance/rejection → executed interaction → mutually attested resolution → improved discovery from successful fulfillment evidence. The outcome record is evidence of *one situated exchange*, not proof of universal semantic equivalence. Evaluation must measure hallucinated matches, harmful suggestions, automation bias, disparate performance, and whether human control is real in practice.

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

## 5A. Additional hypotheses from the sovereignty and emergence thesis

**H7 — Agency and procedural dignity:** In comparable voluntary intake workflows, participants using Has-Needs report higher perceived control, comprehension, and opportunity to contribute than those using conventional institutional intake, including when their requests remain unfulfilled. Compare validated self-report measures, qualitative interviews, and accessibility-stratified outcomes; guard against novelty and selection effects.

**H8 — Sovereign disclosure:** For equivalent successfully completed tasks, participant-controlled persona projections expose fewer unrelated personal attributes and yield fewer unauthorized downstream uses than standard account- or case-management workflows. Measure actual disclosure and independently test revocation limits; do not equate access termination with deletion of previously copied data.

**H9 — Emergent composition:** New coordination scenarios can be expressed using the existing Has/Need/Working/receipt grammar with fewer specialized privileged subsystems, while maintaining task success and comprehensibility. Count privileged components, novel protocol states, integration burden, and human usability; complexity can move into contracts and should not be hidden.

**H10 — Relationship evidence:** Human decision-makers shown authorized receipt-linked evidence make better-calibrated counterparty decisions than those shown opaque synthetic reputation scores, without disproportionate exclusion of newcomers. Test privacy, false confidence, gaming, and discrimination.

**H11 — Interpretive priming:** Models pre-exposed to the Paradigm Delta make fewer architecture-violating proposals on held-out Has-Needs tasks than matched controls, including after context shifts. Blind scoring and independent raters must distinguish real errors from justified critique. A verified BIAS-protocol arm can measure any incremental effect.

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

Participation is voluntary. No inference of consent from emergency vulnerability; avoid coercive conditional access to essential services. Keep actual participant positions outside shared protocol records as V1 requires. Protect authorized geographic applicability and sensitive requests through purpose limitation, minimum necessary disclosure, retention limits, revocation where technically possible, and independent security review. Public maps and aggregated statistics must be evaluated for reidentification. Report participation bias and the needs of people who cannot or choose not to use the system.

## 8. Evidence ladder and scholarly positioning
Separate: **(A) specified architectural behavior**, verifiable in protocol and code; **(B) predicted designed emergence**, supported by causal arguments but not yet observed; **(C) pilot observations**, measured with stated limitations; and **(D) independently replicated effects**. Avoid claiming Has-Needs has proven superior to every surveillance or disaster-management system before comparative studies.

The scholarly contribution to investigate is the combination of sovereign intent expression, consented geographic relevance, human–AI matching with human authority, verifiable reciprocal outcomes, and institutional cost observability. A literature review should compare participatory sensing, crowdsourced crisis mapping, resource-matching platforms, mechanism design, public-sector cost accounting, trauma-informed design, and human-in-the-loop AI. Novelty should be argued at the level of the *combined mechanism and its measurable consequences*, not by asserting that no precursor exists.

## Sovereign knowledge production: passive contribution and a post-capitalist economic pathway

A farmer may mount an old phone on a stick to collect field observations. With suitable power, sensors, connectivity, and explicit authorization, the device can contribute observations over time without requiring continuous attention. Local farmers can pool observations to improve situational awareness and predictions, use those insights to prevent losses or identify opportunities, and offer permitted data or research participation to governance bodies and international researchers under negotiated terms.

This is **passive contribution with active sovereignty**, not passive consent. The owner and participating community determine the purpose, recipients, permitted uses, compensation, and duration of each agreement; technical enforcement, offline behavior, and downstream revocation remain implementation questions. A public or commercial buyer does not acquire unrestricted rights merely by observing or aggregating the data. Collective arrangements should preserve each contributor's consent and the distinction between individual and community authority.

The economic proposition is deliberately **post-capitalist in orientation**: people and communities become sovereign producers and counterparties in knowledge exchange rather than unpaid sources of extractable behavioral data. The term describes the intended redistribution of informational authority and bargaining power; it does not assert the elimination of markets, payment, or existing institutions. Has-Needs can support ordinary sales, commons-oriented sharing, cooperative bargaining, and reciprocal non-monetary exchanges using the same primitives.

The psychological mechanism also operates **without constant intervention**. A participant who authorizes an enduring contribution can perceive continuing usefulness, recognition, and reciprocal benefit. Spatially grounded predictive information can turn passive observation into actionable foresight: seeing what may happen locally, choosing preventive action, and recognizing a beneficial outcome may strengthen perceived efficacy. That effect is an intentional research proposition, not a measured clinical result.

The **Globe UI** is conceived as a literacy- and culturally agnostic medium of exchange and relevant interaction, not merely a map. Pictorial surroundings can anchor information to a person's mental representation of place and reduce dependence on written words or imposed taxonomies. Equivalent nonvisual, text, speech, SMS, and assistive pathways remain essential; pictorial interfaces are not universally interpretable without testing. Geographic relevance must not be conflated with public disclosure of physical whereabouts.

Research directions include measuring contributor compensation and bargaining power, quality and coverage of local predictions, agency and perceived efficacy, collective resilience, and the distribution of economic returns. Distinguish native protocol observations from optional consented psychological measures and from unproven claims about net benefit.

## 9. Origin and design rationale

The founder's broader intellectual and lived history is documented separately in [Origins and Intellectual History](HAS_NEEDS_ORIGINS_AND_INTELLECTUAL_HISTORY.md). It includes repeated childhood relocation and the importance of personal continuity; a dedication to Ishi whose original wording is to be recovered; Buckminster Fuller's systems thinking; peer counseling, emergency response, and trauma research; international BBS and 2600 culture; and participatory mapping and citizen science. These are founder-reported influences, not independent historical verification or normative V1 requirements.

The design progression joins three questions: how a person can understand what matters in their immediate surroundings, how the person can exercise agency without institutional permission, and how reciprocal evidence can preserve the continuity and value of that participation. The Globe UI and passive farmer sensing example are concrete expressions of this larger proposition.


Firsthand observations of handwritten Has/Need notices after disasters demonstrate a naturally occurring coordination pattern without centralized digital infrastructure. Experience with autonomous affinity-group spokescouncils informs the possibility of pooled action without surrendering individual sovereignty. These are design inputs and motivation, not empirical validation of the implemented protocol.

## Conclusion
Has-Needs asks several connected falsifiable questions: Does participant-originated authority improve agency and the quality of voluntary cooperation? Can a small grammar of consented relationships produce accountable institutions and useful communities without centralized control of meaning? Can AI assist without acquiring authority over people? And, in disaster response, does direct declared intent reduce the costs and harms of inferring needs?

Its operational economic question remains: **When institutions can respond to what people voluntarily say they need, rather than paying to infer needs from observed behavior, do coordination, accountability, resilience, and net costs improve?** Its contribution is a concrete architecture for testing that question while keeping participants—not AI systems or institutions—in authority over their own commitments and disclosures.
