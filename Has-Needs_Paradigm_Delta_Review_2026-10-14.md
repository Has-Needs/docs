# Has-Needs: The Paradigm Delta
## A longitudinal analysis of AI misunderstandings, architectural corrections, and the teachings they reveal

**Review date:** 14 October 2026  
**Canonical reference:** [`Has-Needs/docs/Has-Needs-Spec-v1.md`](https://github.com/Has-Needs/docs/blob/main/Has-Needs-Spec-v1.md), inspected at blob `4376bc7cd500d2360ae4e63a4859d555f799d6c8`  
**Purpose:** Preserve the *difference in premises* between conventional software/AI interpretations and the founder's Has-Needs architecture. This is an interpretive companion, **not** a replacement specification or an authorization to alter V1.

### Scope and provenance of the review

This analysis compares the present V1, section by section, with representative GitHub revisions and recovered records of design conversations. The strongest historical evidence is the Git commit that displays an earlier formulation removed and a corrected formulation added. Some prior-conversation records preserve a user's correction without preserving the assistant's exact original sentence. Those cases are identified as **reconstructed misunderstanding**, rather than presented as a verbatim quotation. This is a *selective longitudinal reconstruction*, not a claim to have inspected every message or every historical commit.

The findings distinguish: **(a)** what a historical revision actually demonstrates; **(b)** a broader, reasoned inference about the conventional assumption behind that revision; and **(c)** how a future assistant ought to understand the architecture. All three matter, but they are not interchangeable.

---

# I. The inversion that the corrections collectively reveal

The recurring AI error was not ignorance of blockchain, DID, geography, ontology, governance, or psychology. It was **applying the familiar direction of causality**:

> An institution or platform defines identities, records, categories, permissible actions and evidence; people enter that structure, acquire permissions, and exchange through its services.

That model is so deeply represented in software examples and institutional language that an assistant can reproduce it while using apparently sovereign words like *privacy*, *decentralized*, *consent*, *peer-to-peer*, and *portable identity*. Those words do not reverse who has authority. They often describe nicer controls over an unchanged custodial arrangement.

Has-Needs makes the opposite construction foundational:

> A sovereign participant exists before any service or community. They create Has and Need propositions and control their meanings, disclosures, commitments, and own reciprocal history. Other participants, communities, institutions, and artificial intelligences encounter only the authority and evidence made available to them through chosen relationships.

This is not merely moving a database to a phone. The important move is **relocating semantic authority and evidentiary custody**, then allowing useful social structures to emerge from interaction. The interaction is primary; the service is contingent. A university, agency, marketer, community, or AI is a possible participant or tool, not the ontological parent of the individual.

A second inversion follows. Software systems commonly treat behavior as data to be observed, categorized, and optimized; Has-Needs privileges **declared intention, voluntary commitment, and attested resolution**. An AI-generated candidate is a conjecture. The human's meaning is a declaration. Agreement enters Working. A resolved exchange generates stronger contextual evidence. Those are different epistemic statuses, not mere stages of an engagement funnel.

A third inversion concerns complexity. Conventional product thinking asks which specialized subsystem should be attached to each use case—marketplace, identity wallet, resource inventory, case-management system, chat platform, contract engine, reputational rating, logistics dashboard, grant-management tool. Has-Needs asks what **small invariant interaction grammar** makes these outcomes expressions of the *same underlying social process*. Its distinctive intellectual work is architectural reduction and composition, not an inventory of already familiar features.

Because these inversions were often discovered through correction, V1 acquired repeated defensive clauses: *not a fourth state*, *not an execution container*, *not an external blockchain*, *not a central table*, *not a trust score*, and many more. Some express indispensable requirements. Others preserve a fossilized argument with a former misunderstanding. That difference is the editorial question.

---

# II. Longitudinal evidence: how an assumption became a correction

## The citizen as data source versus the individual as a participant

**Conventional premise:** Emergency response is organized by organizations collecting reports, verifying their quality, integrating dashboards, and assigning resources. Citizens are important sources of observations, but official processes decide which information counts and which actions are legitimate.

**Misreading revealed:** An assistant can interpret Has-Needs as *better disaster data intake* or a clever resource-matching layer for humanitarian institutions. Even praise of citizen-generated situational awareness can leave the citizen at the bottom of the hierarchy, providing raw material for an institutional picture.

**Corrective trajectory:** The October 13 historical revisions recast the Haiti lesson as a failure of the *status accorded to the affected individual*, not merely a shortfall in mapping, talent, or reporting capacity. The founder's reported call-in proposal and the dismissal it encountered are not ornamental biography: they demonstrate the institutional prior that Has-Needs reverses. Compare [the Haiti reframe commit](https://github.com/Has-Needs/docs/commit/57a45e5895f23f7454d55fe37fc535b3a02bc95d) with [V1 Part I](https://github.com/Has-Needs/docs/blob/main/Has-Needs-Spec-v1.md#part-i---introduction).

**Teaching:** A survivor is not an unverified data point waiting to become a record in the agency's system. They may simultaneously have a Need, a Has, local knowledge, authority to consent, and the capacity to form cooperative relationships. The design preserves their ability to speak, choose, contribute, and keep reciprocal evidence of the result. The original purpose—mitigating the loss of agency that compounds trauma—also applies on an ordinary day.

**Important epistemic distinction:** The history reports a firsthand account; an assistant should not silently upgrade the asserted causal links in that history into externally established events. But it should not replace the author's architectural premise with the institutional premise he is challenging.

## Representation: filling predefined categories versus originating meaning

**Conventional premise:** Interoperability requires a shared taxonomy first. The system supplies the vocabulary, classifications, and schema; a user locates their situation in the prepared catalogue, sometimes with AI classification to make the mapping easier.

**Misreading revealed:** Once the triplet `[entity, relation, context]` appeared, the model tended to treat it as another ontology schema or data-classification mechanism. At one point the document had to clarify simultaneously that people do not invent the interface and that the architecture does not impose a prepared ontology. Those are **two separate questions** that a conventional system bundles together: who builds the controls, and who supplies the meaning?

**Corrective trajectory:** The October 14 revision explicitly separated the *provided graphical controls and limited basic contract vocabulary* from the *undefined, participant-supplied local meaning*. The October 14 ontology revision likewise made no standard vocabulary prerequisite to expression through words, images, symbols, or accessible nonwritten interaction. See [local ontology correction](https://github.com/Has-Needs/docs/commit/1e0caf02ef7f479b5c810005083e45067319655e), [contract/UI correction](https://github.com/Has-Needs/docs/commit/d2702751c7753c48e2dd51aaee7154a82ff31048), and V1 §§2, 14, 33.2.

**Teaching:** A fixed **grammar of relating** is different from a fixed **ontology of things**. The software can provide simple actions without prescribing what is valuable or how someone names it. Meaning is local and may travel outward as people agree on distinctions and demonstrate successful outcomes. The semantic ontology is a history of useful, contextual mappings, not a declaration of cosmic or institutional truth. This also protects knowledge that communities choose not to share.

The pivotal question for an assistant is: **Am I helping this person express their meaning, or asking them to adopt the system's meaning as a condition of participation?**

## Objects and chains: borrowing a principle versus adopting a platform

**Conventional premise:** Terms such as eUTXO, NFT, chain, and smart contract designate known ecosystems and usually imply tokens, ledgers, wallets, minting, spending, consensus services, or chain interoperability.

**Misreading revealed:** A familiar acronym attracted an entire surrounding technology stack into explanations of Has-Needs, although the design had borrowed *properties*, not dependencies. The resulting V1 began requiring increasingly emphatic disclaimers that it did not use an outside blockchain.

**Corrective trajectory:** The October 13 revisions explicitly defined eUTXO and NFT as *architectural blueprints*: a Need expresses conditions and permitted transitions; a Has carries individual identity, provenance and continuity. The reciprocal histories are native Has-Needs objects, a **forest of personal chains**. Compare [explicit blueprint separation](https://github.com/Has-Needs/docs/commit/db860d65939a58f2046c290212ac9f3bbeac2620) with [the later affirmative formulation](https://github.com/Has-Needs/docs/commit/ea78e5d274806e982e9be19fff7866ca52995f84), and V1 §5.1.

**Teaching:** Ask which invariant motivated an analogy. Do not inherit the analogy's ecosystem. *Need = condition-governed executable proposition; Has = individually traceable capability; reciprocal receipt = participant-held attested resolution.* The chain is evidence of participation, not a universal commodity ledger. The exchange is not subordinate to a blockchain provider.

## Execution and resolution: an application's transaction outcome versus a continuing obligation

**Conventional premise:** A workflow usually follows a state machine with `created/active/success/failure/cancelled`, a transaction service, and often an additional record or reversal for unsuccessful work. Developers try to make every event fit a small enumerated outcome label.

**Documented misunderstandings:** Early October 8 discussions expressed a binary *deal/no-deal* receipt proposal. The October 12 revision tried *Cancel/Undo* by closing one transaction and creating a reverse transaction. The October 13 revision instead distinguished the **Need-owned pending journal**—which preserves accepted commitments and progress—from **identical final receipts** for mutually resolved outcomes. Quantity tracking was also removed from the universal mechanism and assigned to an optional distribution-Need contract subtype. The chronological amendments are visible in [October 12 Cancel/Undo](https://github.com/Has-Needs/docs/commit/20c4cfcad7f9e4a63148468110a9450ecbb6fdae) and [October 13 Pending/resolution reframe](https://github.com/Has-Needs/docs/commit/dfd1a058558dec5855fb67ec7bc08dd25212d96b).

**Teaching:** Do not mistake an application status label for the contract's ontology. A **Need is the self-contained executable contract**. Mutual acceptance binds the relevant Has and Need into **Working**, the third relation state. The pending journal is the accepted event history, not a fourth state or competing execution environment. The ultimate recorded object is a resolution agreed under the contract, not a synthetic classification of someone's goodness, failure, or level of activity. One Need can sustain multiple independently resolved bindings; specialized quantities follow contract terms, not universal accountancy. V1 §§7–13.

The lesson from this sequence is not that *Pending* won a naming contest. It is that **evidence of commitment and evidence of resolution are different species of evidence**. Do not erase an unresolved obligation by producing a convenient closure, and do not create unnecessary object types to rescue a familiar workflow diagram.

### The corresponding receipt and the mistaken urge to adjudicate

**Conventional premise:** A discrepancy is an opportunity for a service to evaluate competing claims, score the participants, choose a likely winner, or initiate a mediation process.

**Misreading revealed:** Former discussions extended the protocol toward automatic mediation or elaborate discrepancy interpretation. The founder repeatedly reduced this back to integrity: reciprocal canonical receipt bytes ought to match. If corresponding, validly identified receipt hashes actually differ, there is a tampering condition. The protocol reports that structural fact; it is not a court deciding who was truthful.

**Correction:** Later revision tightened the distinction among **hash mismatch**, **missing or delayed receipt**, **unresolved Working**, and **dispute about physical facts**. The final receipt must be reviewed by each participant, optional annotations and disclosure choices are independently controlled, and only matching ready-to-commit versions proceed through Persona Managers. See [receipt review and autonomy](https://github.com/Has-Needs/docs/commit/35a56aa59225b5bf7e81d4170cc78d453d374c69) and V1 §§10, 23.1. The architecture treats demonstrated mismatch as tampering, grey-lists the involved chains, and leaves substantive dispute resolution to appropriate human or contractual processes.

**Teaching:** *Integrity evidence is not a verdict about physical truth.* Keep the comparison exact and the human interpretation distinct. There is an important asymmetry: a cryptographic match supports the identity of the recorded statement; it does not establish that the statement was honest or complete in the physical world.

## Trust: a synthetic numeric judgment versus visible reciprocal relationship evidence

**Conventional premise:** Trust is a useful scalar to compute—perhaps a confidence score derived from historical interactions, hop distance, attestations, and anomaly indicators. A score can be described as contextual rather than reputational, yet still invisibly becomes the system's judgment.

**Documented mistake:** On October 5 the specification was briefly revised from *no reputation primitive* to *contextual trust score*. The next substantive revision removed the computed score and specified **live chain-hop vetting**: first-order known reciprocal connection, visible second/third-order topology, configurable verification depth (eight hops as V1 full reference), receipt consistency, grey-list evidence, and personal filters. See [score introduced](https://github.com/Has-Needs/docs/commit/ba2343f39422bd4eb36e34214c7117a2a807b84d) and [score removed](https://github.com/Has-Needs/docs/commit/4fb31d25fc4751f750950e1acbe471bf0ed42b89). Later [recorded-event correction](https://github.com/Has-Needs/docs/commit/8d26f930e7eb046faa51dffc4d79ac200bf2b2dc) explicitly excluded inferred behavior and unaccepted candidates from vetting evidence.

**Teaching:** Trust is not an attribute of a person stored by the network. It is a **human interpretation of relevant, consentedly inspectable relationship geometry and cryptographic consistency at a particular moment**. The interface reveals evidence instead of collapsing it into a synthetic number. The system remembers actual accepted interactions and outcomes, not passive browsing, refusals, ignored offers, personalities inferred by AI, or proximity to strangers.

This is a particularly instructive instance of *algorithmic overreach wearing the costume of helpfulness*: the assistant inserted a score because familiar applications often make a decision easier by hiding its provenance. Has-Needs preserves the provenance and the participant's right to decide.

## Geography: locating people versus discovering where fulfillment is possible

**Conventional premise:** Geospatial matching requires the positions of two people, or at least a service capable of retrieving their approximate coordinates to compare distance.

**Misreading revealed:** Early proximity proposals drifted toward exact-coordinate matching and cryptographic proximity computation as foundational architecture. Such methods can be useful research candidates, but the question was backwards: *what can be fulfilled where?* is not identical to *where is the person?*

**Correction:** V1 introduced **spheres of possibility**: the geographic applicability of an offer, request, service, route, neighborhood, mobility envelope, remote action, or community context. Actual participant location is a different private fact. Local proximity communities and successful local relationships are heavily weighted before search expands outward. See [geography and non-retrievability](https://github.com/Has-Needs/docs/commit/c24b6406722b48310cf74728ff007e19d1a3a13c), [local-first inversion](https://github.com/Has-Needs/docs/commit/8866ced246e622981564cb84b1993909c2f82ee4), and V1 §§21, 24.2, 31.

**Teaching:** Matching occurs across **possible outcomes**, not compulsory location disclosure. A rental truck can enlarge someone's feasible service region without moving the person. An emergency manager may need fire status for an area while having no entitlement to retrieve a reporter's home coordinates. Protected exact-position computation is an exceptional tool to evaluate, not a precondition for local relevance.

This is also a networking inversion: traditional routing finds an addressed destination; semantic routing asks where a particular Need is likely to **find resolution**. The geography of utility and the whereabouts of a human must not be silently merged.

## Identity and disclosure: granting platform permissions versus owner-held authority

**Conventional premise:** A person has an account with identifiers and aliases managed through an identity provider. A service controls the data and offers privacy settings, access-control screens, data-portability exports, and perhaps revocation of future permissions.

**Misreading revealed:** Calling multiple personas 'multiple DIDs' or separate account identities leaves the conventional root intact. Similarly, equating encryption, decentralization, or a consent banner with sovereignty fails to change who can interpret, aggregate, sell, or permanently retain the person's information.

**Correction:** The founder's owner-first model describes **one sovereign person, one private receipt history, and multiple contextual personas managed by a concierge-like Persona Manager**. The outward-facing persona is not an invitation to traverse the chain or correlate with other facets. An organization issues a Need for an attribute or ongoing access; the owner chooses whether and on what terms to supply a Has/projection. A contract-scoped API may terminate future *live* access on revocation; immutable disclosed copies are a different, expressly understood issue. See [owner-first identity and access](https://github.com/Has-Needs/docs/commit/3212ce12887747417d01bc2d119a8764b69cab0d), [persona and receipt autonomy](https://github.com/Has-Needs/docs/commit/35a56aa59225b5bf7e81d4170cc78d453d374c69), and V1 §§22–25.

**Teaching:** **Custody is not authority.** Possessing bytes or operating a server does not entitle an actor to define their meaning, own the personal relationship, inspect adjacent facets, or create future permission. OCA's descriptive metadata overlays are not the same thing as authorization; the Persona Manager and policy/contract gate control the release. Disclosure is an explicit, bounded **state transition** in a relationship, not a single blanket checkbox. A person's records are their private substrate; personas are controlled projections.

The legal proposal that unauthorized use of a protected facet should be actionable is a distinct normative project. Future assistants must distinguish the protocol's internal rule requiring positive authorization from what law *currently* recognizes in a given jurisdiction, without shrinking the design itself to existing statutory concepts.

## Community, governance, and commerce: special apps versus emergent agreements

**Conventional premise:** Community means membership in a platform-owned group; governance means submitting a ticket into an agency workflow; commerce means monetization through customer databases, leads, payment systems, and institutionally controlled transaction records. Each calls for a separate product category.

**Misreading revealed:** A familiar systems response adds modules: community admin, marketplace plugin, case-management dashboard, identity provider, data broker, grant ledger. This makes Has-Needs appear to be a collection of integrations rather than a coherent grammar.

**Correction:** The community arises from voluntarily accepted relationships. Membership alone does not transfer authority to pool a person's resources. A pooled Need involves delegated conditions; a project emerges as a nested set of Needs and Has capabilities, while a Kanban board or emergency dashboard becomes a **view**, not a new source of truth. A municipality creates a recorded obligation only when it actually accepts the citizen's Need; the emerging evidence shows workflow bottlenecks without needing an invented 'government accountability engine.' Commerce can begin with both vendors and individuals expressing bounded propositions; it does not require extracting a prospect database. See [chosen interdependence correction](https://github.com/Has-Needs/docs/commit/7350874fda0918926ae01d5270590a73ead367ea), [commercial owner-originated exchange](https://github.com/Has-Needs/docs/commit/3212ce12887747417d01bc2d119a8764b69cab0d), and V1 §§19, 35–39.

**Teaching:** Social organization is an *outcome of sovereign coordination*, not a prerequisite imposed by a platform. Communities are as real as their governance, but authority comes from members' acts of consent and appropriately bounded delegation. A successful exchange may resolve a Need, strengthen a local ontology, create reciprocal evidence, establish a relationship, and make a new voluntary group possible. These are **co-produced emergent consequences of one event**, not independent features to bolt on.

## Machine intelligence: administrator of the user's world versus bounded interpreter

**Conventional premise:** AI personalization works by watching user decisions, constructing preferences, predicting future behavior, and autonomously completing the easiest transaction paths. It is tempting to treat more comprehensive behavioral access as the price of a smarter assistant.

**Misreading revealed:** In this paradigm an unselected recommendation is treated as a training event, a declining user as a negative signal, a matched Need as tacit permission for discovery, and inferred preference as authority to act. The user is again the object of the system's model.

**Correction:** V1 separates bounded semantic interpretation, human-supplied meaning, and authenticated event evidence. AI proposes matches; people select and authorize. A protocol gate independently enforces the scope of authorized state changes. Machine interpretation does not become truth because a model predicts it, and it does not receive the keys needed to bypass participant authorization. [Recorded-event correction](https://github.com/Has-Needs/docs/commit/8d26f930e7eb046faa51dffc4d79ac200bf2b2dc), [emergent ontology revision](https://github.com/Has-Needs/docs/commit/1e0caf02ef7f479b5c810005083e45067319655e), V1 §§14.1–14.2.

**Teaching:** **AI finds possible semantic paths; people supply meanings and permissions; resolved exchanges supply evidence of what worked.** The AI is deliberately peripheral to the authority structure even when it is helpful to its operation. Segmentation and revocability are not merely engineering choices; they keep the artificial model from becoming the sovereign's administrator.

---

# III. Section-by-section reading of V1 and its inherited misconceptions

The table names the conceptual *teaching* for each main division. It is not a new feature checklist and does not propose moving the actual architecture out of V1.

| V1 location | Conventional assumption liable to intrude | Correct Has-Needs reading | Editorial implication |
|---|---|---|---|
| **Opening / Part I (§§1–4.1)** | A disaster-response proposal gains legitimacy by borrowing an institution's vocabulary, scope, and validation agenda. | Haiti crystallizes the sovereignty/trauma insight: the affected individual is a capable node of participation, not merely ground truth for an agency. Everyday and disaster life are one continuum. | Lead affirmatively with sovereign beings, value exchange, structural loss of agency, and the inversion; place provenance and longer chronology in `HISTORY.md`. State research status once where relevant. |
| **Part II (24 architectural invariants)** | A standard requirements document defines features to be implemented in the future, often with repetitive 'not X' tests. | Invariants define what makes a Has-Needs implementation itself, where authority resides, and which properties must coexist. | Keep genuinely normative negative constraints—no global enumeration, no unauthorized AI commits, no location-retrieval operation—but remove duplicated rebuttals and merge overlapping invariants into clearer positive concepts where safe. |
| **Part III (§§5–13)** | Object means database row; eUTXO/NFT means dependency; Working means job-status flag; Pending is a fourth state; quantity accounting is universal; transaction outcome must be binary. | Has/Need are sovereign propositions; Need contains the executable contract; Working is their active binding; Pending records accepted events; resolution creates identical independently held receipts; specialized distribution rules reside in Need subtypes. | One definitive lifecycle diagram, one explanation of the blockchain analogy, one normative atomic-receipt definition. Retire obsolete terminology from the architectural body and preserve its genealogy here. |
| **Part IV (§§14–21)** | Ontology is a universal controlled vocabulary, AI owns the semantic map, discovery means searching an enumerable index, proximity means locating people. | Local people originate meaning; resolved exchange teaches the scoped ontology; matching encounters compatible propositions without an omniscient inventory; geographic feasibility differs from whereabouts. | Open with the epistemic progression (declaration → candidate → acceptance → resolved evidence). Keep non-enumerability and actual-location protection as hard invariants. Move rebuttals about 'shopping list' and old API names to a migration or reviewer note if repeated. |
| **Part V (§§22–26)** | DID/account = person; pseudonyms = separate identity accounts; encryption/consent checkbox = sovereignty; metadata schema = access grant; verifier may traverse the root ledger. | One sovereign person and owner-held history; multiple contextual personas; scoped disclosure is separately authorized; custody of a copy grants no right. Live access may be revoked by contract. | Clearly differentiate schema description, evidence, delegated permission, and legal entitlement. Keep adversarial leakage and cryptographic limits as substantive security statements, not rhetorical apology. |
| **Part VI (§§27–34)** | Routing transports packets to known addresses; a network stack or named framework defines the system. | The semantic fabric transports compact intent toward potential resolution; shared local context makes the deltas cheaper; transport adapters and Friend nodes are replaceable. | Teach 'route toward resolution' before cataloguing BLE, SMS, DXOS, SmallWeb, and standards. These are options, not explanatory parents. |
| **Part VII (§§35–39.5)** | Communities are hosted groups; government workflows are ticketing systems; a project needs its own project-management schema; maps reveal everyone. | Chosen community relationships can persist; governance obligations exist only after accepted agreement; project boards and maps are sovereign Data Views of the same objects. | Tell concrete human stories and show emergent functions arising from one exchange. Avoid presenting governance, agriculture, data markets, and subcommunities as unrelated apps. |
| **Part VIII (§§40–48)** | Either strong crypto guarantees physical truth and privacy, or the architecture is invalid until every threat is solved. | Cryptographic integrity, physical truth, key recovery, adversarial transport, and later-discovered harm are distinct problems. Sovereign claims and later evidence have different roles. | Keep technical constraints and candid unknowns. This section is *where carefully bounded negative statements belong*. Replace generalized defensive language elsewhere with links here. |
| **Part IX (§§49–54)** | An architectural invention is a speculative proposal until implementation passes tests; conversely, a feature list is proof of social benefit. | The architecture has a defined identity; experiments test conformance, operational efficacy, and desired human outcomes separately. | Preserve the distinction among design, test method, implementation result, and psychosocial evidence—but do not re-litigate 'Has-Needs is not built yet' throughout the earlier exposition. |
| **Appendices / closing** | A glossary is a catalogue of conventional technologies and their imported definitions. | Local terms have Has-Needs-native meaning. Analogies are provenance for ideas, not ontological inheritance. | Include a concise **Misreadings and paradigm inversions** appendix or link to this separate training companion. Avoid making every term's definition a defensive argument. |

## Where the current V1 still betrays the revision dialogue

Examples are illustrative, not an exhaustive copy edit:

- **Document status / normative vocabulary:** Language explaining that V1 is *not a hypothetical project for somebody else to invent* is directly traceable to a prior interpretive dispute. A clean specification can announce architectural authorship and authority once, then state the design. It need not continually defend the inventor against an imaginary skeptical assistant.
- **§5.1:** The affirmative eUTXO/Has pairing is effective; the paragraph explaining no existing-chain interoperability is a legitimate compatibility boundary. Its repeated restatement in nearby files and sections turns the boundary into rhetorical foreground. One authoritative statement and cross-reference are sufficient.
- **§7.1, §9, §11:** 'Pending is not a fourth state or execution container' appears in several forms. The *positive* definitions of Need, Working, Pending, and receipt should be enough after one explicit normative distinction; the repetition exposes the earlier misunderstanding.
- **§14 and §33.2:** The valuable distinction between supplied interface and self-originating ontology is repeated because an assistant previously conflated the two. State it cleanly in ontology, make other sections refer back to it, and teach the error in this companion.
- **§19:** 'Not a global shopping list view' is a helpful security-concept heading, but the long explanation of an old `getAllNeeds()` method belongs better in an implementation migration note than in an independent V1 narrative.
- **§23.1:** The no-score distinction must remain explicit, because otherwise a future implementation can violate a core invariant. The text could still distinguish **evidence → participant judgment** directly instead of repeatedly enumerating all the conventional rating systems being rejected.
- **§24:** Distinguishing an OCA sensitive-metadata overlay from a grant is an actual security necessity. This is not a deprecatory statement; it prevents unauthorized reading. Likewise the warning that revocation cannot retrieve previously copied plaintext is a physical constraint, not an apology.
- **§41–47:** Constraints such as 'signature does not prove physical truth' and 'radio silence cannot be overcome by cryptography' add technical precision and should be retained.

The editorial principle is therefore **not to delete negatives wholesale**. It is to distinguish a **normative prohibition that constrains implementations** from a **conversation-specific rebuttal whose function is to correct an AI's mistaken analogy**. The latter belongs in assistant training, reviewer questions, history of decisions, or architecture notes. The former belongs in the spec.

---

# IV. The actual failure mode in AI reasoning

The mistakes are a recognizable sequence:

1. **Nearest-category substitution.** On hearing an unfamiliar arrangement, the model supplies the closest well-represented product category (identity wallet, marketplace, project manager, blockchain, reputation engine, case-management tool).
2. **Silent inheritance.** It imports the ordinary dependencies, authorities, and status model of that category: centralized inventory, searchable member profiles, global index, account custody, behavioral telemetry, provider validation, social scoring, cryptographic token issuance, or standard transaction closure.
3. **Helpful elaboration.** It adds an apparently reasonable component to 'solve' the mismatch: an extra state, another receipt type, a contract runtime, a quantity ledger, a score, an institutional attestation service, an automated dispute workflow.
4. **Authorial correction.** The founder points back to a simpler invariant: the individual is sovereign; the Need itself governs terms; a completed value exchange yields reciprocal evidence; local meaning emerges; the system knows only what participants authorize.
5. **Defensive residue.** The assistant amends the document with 'not X, not Y' because it remembers why it was wrong. A first-time reader, with none of that history, encounters the correction as gratuitous or confusing.

This fifth step explains the user's specific editorial complaint. The V1 document has absorbed a visible **palimpsest of unsuccessful interpretive frames**. Each rebuttal may once have prevented the assistant from reintroducing an error; collectively they shift attention away from the architecture and imply that the reader was about to make the same errors.

The right remedy is to **move the pedagogy, not erase the insight**. Keep the normative invariants and definition precision in V1. Keep this longitudinal record as an AI-orientation and peer-review supplement. The final public architecture should be read in the direction it was designed, not in the order its misconceptions were eliminated.

---

# V. Teaching future assistants to inhabit the Has-Needs frame

An assistant should orient itself with a handful of conceptual commitments *before* explaining any technology. These are rules of interpretation, not a product feature list.

**Locate the authority first.** For any claim, object, relationship, or resulting record, ask: who originates its meaning; who may authorize a transition; who is entitled to inspect it; who holds the canonical evidence? Defaulting to 'the service' is a conceptual error. A copy held elsewhere is not custody of the person's sovereignty.

**Preserve the different epistemic kinds.** A claimed Has is not delivery. A proposed match is not consent. An accepted Working relation is not completion. Pending records accepted events but does not imply guilt. Matching canonical receipts establish a recorded resolution but cannot, by themselves, prove all physical facts. A receipt-derived ontology edge is evidence that a route worked in context, not a definition of global truth.

**Ask what has to remain small.** Do not solve a hard human scenario by inventing a general-purpose extra subsystem until composition of existing Has/Need/Working, contracts, receipts, personas, views, and authorized communities has been tested. The architecture's accomplishment is the *reduction* of institutional special cases into common human interaction.

**Use analogies with discipline.** If describing a Need as eUTXO-inspired, explicitly carry over **conditions and authorized state transitions**, not a crypto token economy. If describing a Has as NFT-inspired, carry over **individuality and provenance**, not speculative collectibles. If describing a community as a group, carry over voluntary association, not platform custody. If describing trust as a graph, carry over inspectable reciprocal paths, not a ranking system.

**Preserve human evaluation.** Explain and ask clarifying questions; do not make the AI the evaluator of a person's character or the authority to choose, disclose, sign, or finalize beyond precisely preauthorized policy. Do not train on or infer moral conclusions from non-actions such as browsing, silence, and refusal.

**Let the reader discover the inversion.** Start with a familiar experience, for example a person sharing medical information, applying for services, or participating in a disaster response. Ask who currently holds the information, who sets the terms of access, whether the participant can stop live access, whether the record of successful cooperation stays with them, and whether the institution could later reconstruct relationships from what it collected. Then describe what changes when those powers remain with the individual and agreements—not simply privacy checkboxes—govern disclosure. Make the architecture visible through the choices it protects, not by lecturing that all current systems are evil or that every present-day legal protection is nonexistent.

### Three example exchanges that expose the conceptual difference

**Question: 'Isn't it just a decentralized marketplace?'**  
*Bad inherited reply:* 'Yes, a decentralized marketplace with DID, smart contracts, a reputation score, and an item registry.'  
*Has-Needs reply:* 'A market can emerge from it, but a marketplace is a special case of two sovereign participants expressing complementary conditions for value exchange. The underlying protocol does not need a platform to own the inventory, identities, or history. The same relation can express a volunteer rescue, university education, public-service commitment, or mutually exchanged access to information.'

**Question: 'How does it know who is trustworthy?'**  
*Bad inherited reply:* 'It calculates confidence from eight verification hops and combines it with behavioral indicators.'  
*Has-Needs reply:* 'It does not assign people a stored trust value. When useful, it lets the participant inspect authorized reciprocal event evidence and the shape of the relationship path: direct prior interaction, nearer and farther receipt-linked connections, integrity flags, and personal filters. The person decides whether that evidence is sufficient for this interaction.'

**Question: 'How does the emergency manager see everyone's Needs?'**  
*Bad inherited reply:* 'An authorized agency dashboard queries a regional Needs database.'  
*Has-Needs reply:* 'The agency expresses the Need for a particular operational picture. Sovereign participants and communities may answer by sharing scoped reports, derived aggregates, or other permissioned projections. The manager can assemble a useful view without gaining a protocol-wide command to enumerate people's private Needs or retrieve their actual locations.'

The same conversational discipline applies to sensitive, probing discussions about existing sovereignty. Do not conflate *legal recognition of a right*, *platform promises*, *cryptographic possession*, and *actual enforceable authority over future uses*. Their separation is the beginning of useful learning.

---

# VI. Recommendations for the documentation and AI knowledge system

**Keep V1 canonical and affirmative.** Its job is to state the architecture, invariants, protocol objects, threat model, and conformant behavior. Keep negative MUST NOT constraints when they protect sovereignty and security. Collapse conversational anti-misunderstandings to one precise statement plus cross-reference.

**Preserve the misunderstands here, with dated references.** The material is unusually valuable for assistant onboarding because it teaches the *failed reasoning pattern*, not merely the right answer. A future model instructed with 20 definitions may still import a centralized architecture; a model taught to recognize nearest-category substitution may stop before doing so.

**Give future assistants a short interpretive guide before the full spec.** It should explain the locus of authority, the epistemic ladder from declaration to receipt, the distinction between interaction grammar and ontology, the difference between local applicability and human location, and the restriction of AI to authorized assistance. The accompanying [`Has-Needs_Assistant_Orientation_2026-10-14.md`](./Has-Needs_Assistant_Orientation_2026-10-14.md) is a candidate.

**Maintain three separate audiences and three separate tasks.** A public README invites; a one-page introduction creates intuition; V1 enables technical implementation. This longitudinal companion teaches an assistant **how not to misinterpret** the other three. Moving rebuttals here allows the canonical documents to become clearer without discarding the 15-plus-year reasoning that brought them into focus.

**Use a recurring editorial test:** 'Would this sentence still be needed if no previous assistant had made the error it contradicts?' If yes because it defines a necessary constraint or security boundary, retain it. If no, relocate it. If it contains an essential insight but begins defensively, rewrite it positively: *what the architecture is, why that structure was chosen, and what follows from it*.

This approach serves both rigor and authorship. Academic and technical weight comes from coherent definitions, explicit invariants, defensible threat models, traceable decisions, and testable claims—not from repeated apologies for what the architecture is not.

---

# Selected primary revision trail

- [2026-10-05 — score temporarily introduced](https://github.com/Has-Needs/docs/commit/ba2343f39422bd4eb36e34214c7117a2a807b84d), then [replaced by live evidence](https://github.com/Has-Needs/docs/commit/4fb31d25fc4751f750950e1acbe471bf0ed42b89)
- [2026-10-08 — contract primitive draft](https://github.com/Has-Needs/docs/commit/5730f0cacc857f35dfb9c59de5e486c8026e3ce1)
- [2026-10-12 — Cancel/Undo draft](https://github.com/Has-Needs/docs/commit/20c4cfcad7f9e4a63148468110a9450ecbb6fdae)
- [2026-10-13 — pending journal supersedes forced outcomes](https://github.com/Has-Needs/docs/commit/dfd1a058558dec5855fb67ec7bc08dd25212d96b)
- [2026-10-13 — vetting restricted to authorized recorded events](https://github.com/Has-Needs/docs/commit/8d26f930e7eb046faa51dffc4d79ac200bf2b2dc)
- [2026-10-13 — independent eUTXO/NFT conceptual models](https://github.com/Has-Needs/docs/commit/db860d65939a58f2046c290212ac9f3bbeac2620)
- [2026-10-13 — actual location separated from spheres of possibility](https://github.com/Has-Needs/docs/commit/c24b6406722b48310cf74728ff007e19d1a3a13c)
- [2026-10-13 — local-first discovery inversion](https://github.com/Has-Needs/docs/commit/8866ced246e622981564cb84b1993909c2f82ee4)
- [2026-10-13 — Haiti reframe to first-class citizen participation](https://github.com/Has-Needs/docs/commit/57a45e5895f23f7454d55fe37fc535b3a02bc95d)
- [2026-10-13 — community sovereignty enables chosen interdependence](https://github.com/Has-Needs/docs/commit/7350874fda0918926ae01d5270590a73ead367ea)
- [2026-10-13 — DSRP over-attribution corrected](https://github.com/Has-Needs/docs/commit/eb27964ff497d99d36388018d4d977c4227941c4)
- [2026-10-14 — local meaning and unprescribed ontology clarified](https://github.com/Has-Needs/docs/commit/1e0caf02ef7f479b5c810005083e45067319655e)
- [2026-10-14 — provided UI distinguished from user-supplied meaning](https://github.com/Has-Needs/docs/commit/d2702751c7753c48e2dd51aaee7154a82ff31048)
- [2026-10-14 — README returned to human-centered story](https://github.com/Has-Needs/docs/commit/b7484dc8ebdd11d4a16b9cf805344a4a81c796ba)

**Editorial status:** Research and interpretive analysis for the founder's review. No modifications to the canonical V1 specification are implied or performed by this file.