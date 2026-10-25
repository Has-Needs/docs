# Has-Needs
## Sovereignty as the Foundation of Human Cooperation
### A Local-First Architecture for Reciprocal Exchange, Collective Agency, and Resilient Coordination

**Author:** Om Goeckermann  
**Date:** October 2026  
**Status:** White paper — design principles and project breadth; architecture and research agenda

## Purpose, Audience, and Central Inquiry

This paper is for researchers and system designers examining how people can coordinate without surrendering authority over their identity, knowledge, commitments, and records. Its questions span human-computer interaction, crisis informatics, local-first systems, digital sovereignty, AI provenance, community governance, and the law of identity and likeness. Emergency managers, community organizations, Indigenous knowledge stewards, and potential pilot partners are important readers because they can test the architecture against real responsibilities and lived conditions.

The paper's central inquiry is: **Can a small, sovereignty-first interaction grammar let people and communities initiate useful cooperation, preserve evidence of what they authorized, and compose larger forms of coordination without placing a platform or institution in control of their identity and meaning?**

An intentionally designed side effect of this architecture is a legal and evidentiary inversion. Because participants originate their own interactions and retain their own evidence, each can produce, carry, verify, and selectively disclose cryptographic proof of attestation at “first-world” quality, without institutional status as a prerequisite. This is not a separate institutional service added to Has-Needs; it emerges from making sovereignty operational inside a setting where people can interact.

The paper presents the architecture and the design reasoning that produced it, then identifies the questions for future technical, social, and legal investigation. Cryptographic attestations provide participant-held evidence of statements and agreed interactions; their interpretation within law and institutions is one of the questions addressed in the Future Investigations section.

### Questions the architecture raises

- What must be true for participant-originated declarations and local discovery to remain usable across intermittent networks and institutional boundaries?
- Which permissions can be enforced technically, which depend on governance or law, and how can the distinction remain visible to participants?
- What follows legally and institutionally from the designed side effect that every participant can produce and carry cryptographic proof of attestation at “first-world” quality, instead of relying on institutional custody of the authoritative record?
- What evidence can participant-held reciprocal records provide, and where do they stop short of establishing physical truth or legal liability?
- How does this evidentiary inversion apply to AI-derived likeness: can source, permission, scope, and later authorized use be carried as verifiable provenance, and how should law, platforms, and communities interpret that evidence?
- How can collective authority protect Indigenous and other community-held knowledge while preserving each person's own authority?
- Which intended outcomes—agency, access, reciprocal recognition, or reduced coordination friction—occur in practice, for whom, and under what conditions?

## Abstract

Human cooperation begins with people who possess knowledge, capabilities, relationships, and resources while also seeking outcomes they cannot achieve alone. Contemporary digital systems often mediate these interactions through centrally defined accounts, inventories, workflows, and records. Has-Needs proposes a different point of departure: the sovereign participant, operating first within a locally meaningful sphere of awareness and capability. Participants express what they **Have** and **Need**, discover possible complementary relationships, voluntarily enter **Working**, and preserve reciprocal evidence of resolved exchanges on their own personal chains. Local-first peer communication and semantic discovery extend through nearby devices, relationships, and communities without requiring an external network, global database, or institution to originate an interaction.

The architecture has been deliberately derived from desired human outcomes: the opportunity to act, reciprocity, dignity, informed trust, collective efficacy, accountable commitments, resilience, and trauma mitigation through agency, choice, connection, and meaningful participation. Its design method is to identify those outcomes, derive a small set of reusable interactions, and examine the technical and social capabilities—and failure modes—that emerge when participants compose them. A person trapped beneath earthquake rubble exemplifies the design: they may possess firsthand knowledge inaccessible even to sophisticated responders, while needing urgent help. Their ability to communicate with participating devices within range offers an opportunity for purposeful action before assistance arrives. The paper describes the minimal interaction grammar, sovereign data and identity controls, Need-owned pending journals, participant-held canonical receipts, emergent communities and accountability, sovereign commerce, reciprocal recognition of displaced people, asynchronous parallel recovery, composable institutional attestations, economic pluralism, the Personal Globe, and a research program for evaluating technical feasibility and human consequences.

**Keywords:** digital sovereignty; local-first systems; human agency; peer-to-peer networking; reciprocal exchange; trauma-informed design; emergent coordination; accountability; disaster response.

---

## 1. The Person Beneath the Rubble

An earthquake has collapsed a building. A person lies trapped beneath the rubble.

They are the sole firsthand authority on their present condition and immediate Need. They know whether they are injured, whether they can move, how easily they can breathe, whether others are nearby, and what they hear or smell around them. Some of this knowledge exists nowhere else. Responders may deploy drones, satellite imagery, trained rescue personnel, and sophisticated detection equipment. Those tools can add vital evidence, but they cannot independently know the person's lived condition or make the person's own knowledge operational. An authorized assessment may contribute expertise; it must not be the gate through which the person first becomes able to speak or coordinate.

At the moment their Need is greatest, the person also possesses a uniquely valuable Has: firsthand knowledge. **The rescuers need the person’s location and condition; the person needs rescue services.** Both sides hold something indispensable to the other. The affected person’s situation is not simply data extracted by an agency: it is a contribution to the rescue, selectively shared for that purpose. This is the first example of the design’s founding principle of reciprocal value, even when one party is in extreme distress.

Imagine that their phone runs Has-Needs. Through local-first Bluetooth mesh communication, it can exchange messages with participating devices **within range**. The person can describe their condition, express a Need for assistance, and offer observations useful to others nearby. Neighbors or responders who receive the message may relay it, respond, or form a cooperative relationship. The network starts with people in reach of one another; it does not wait for an external system to create the interaction.

The first benefit need not wait for rescue. The individual has an available means of taking purposeful action and a credible possibility of being heard. Even before a reply, that possibility can create a foothold for perceived agency. Has-Needs deliberately designs for this early opportunity to act, communicate, and contribute.

The same design applies beyond disaster. A neighbor can seek help with a broken heater, a farmer can find a nearby buyer, a student can obtain instruction, and a citizen can initiate an accountable service relationship with a municipality. Each starts from a person who can express meaning and choose to cooperate.

### 1.1 Why reciprocal value is foundational

Has-Needs was designed to preserve **resolved exchanges of value**, not to build a permanent institutional inventory of people and their deficiencies. A rescue can exchange a person’s otherwise inaccessible situational knowledge for the responder’s capability to help. A neighbor can exchange companionship for companionship; a newcomer can offer everyday practical help while seeking local assistance. Value is defined in context by sovereign participants and need not have a price. Hases and Needs can be expressed before any agreement, and accepted WORKING relationships have Need-owned pending journals; final reciprocal receipts record agreed outcomes, including unsuccessful resolutions where applicable. This design preserves the possibility of contribution and recognition, without making emergency aid conditional on repayment, proof of productivity, or formal acceptance of a contract.

## 2. The Individual's Sphere of Operation

Has-Needs begins with the individual's **sphere of awareness and capability**: what they know, whom they can reach, what they can offer, and which outcomes are feasible from their circumstances. Walking distance may define one sphere. The fuel in a vehicle may expand another. A person's relationships, available tools, accessible routes, and participating communication devices define further possibilities.

These are not concentric surveillance rings around a published location. A sphere of possibility describes where a particular Has or Need can be relevant and fulfilled. A person seeking a refrigerator might initially be able to collect one nearby; the availability of a truck can extend that feasible region without requiring the person to publish their current coordinates. Physical reach, semantic relevance, and social connection interact.

Local-first networking follows from this premise. Participating devices can exchange and relay authorized messages within range; communities can extend discovery and cooperation outward as their relationships permit. Internet connectivity, institutional systems, and long-distance services can increase reach, but they are optional participants in a process that begins locally. No global inventory of people or universal centralized matching authority is required.

Communication is designed to route relevant Has and Need propositions toward possible resolution, rather than require a known destination address or a globally enumerable directory of people. Local meaning, context, and fulfillment possibility help determine where an authorized expression can travel; participating relationships and transports can extend that reach as relevant. The system routes toward a possible outcome, not toward a compulsory map of people.

This design makes a profound distinction between **a place where cooperation is possible** and **the retrievable location of a person**. Has-Needs protects actual personal location while allowing participants to disclose relevant service regions, routes, destinations, or other bounded geographic contexts.

## 3. Sovereignty as a Working Architectural Principle

In Has-Needs, sovereignty means the participant originates their own declarations and retains authority over identity facets, protected information, permissions, voluntary commitments, and their personal evidence of exchange. The individual does not need to become a subordinate account in another participant's system before making a meaningful declaration.

The **Persona Manager** acts as a concierge across user-created facets of identity. A person may appear as a neighbor, parent, contractor, volunteer, or researcher, disclosing only what a particular relationship requires. Authorized counterparties receive specific objects, predicates, or views; they do not thereby gain access to the owner's private personal chain. Permission may be scoped by recipient, purpose, duration, and data type. Revoking live access can end future authorized delivery, although it cannot make previously observed information disappear.

Sovereignty also supports collective action. Communities may establish shared purposes, membership rules, delegation, and consent procedures. A community's authority derives from its participants' chosen arrangements and does not automatically supersede their protected personal information. Traditional and Indigenous knowledge may require collective governance distinct from any single member's permission.

The central proposition is affirmative: **the capacity to choose the terms of participation is a foundation for cooperation.**

### 3.1 Design principles

The design principles are architectural constraints. They shape what the system makes possible, which authority it recognizes, and what it must leave to people and communities.

1. **The person precedes the platform.** A participant can originate a Has, Need, or firsthand account of their own condition without first being classified, enrolled, or assessed by an institution. An agency may add valuable expertise and verification, but its assessment is not the prerequisite for the person to speak or begin coordinating.
2. **The participant supplies meaning.** The protocol provides a small grammar and accessible controls; it does not require a universal catalog of needs, occupations, identities, or value. Local vocabulary can be translated or related to other vocabularies while retaining provenance and the authority to reject a proposed equivalence.
3. **Authority follows ownership and explicit grants.** Each person controls their own objects, identity facets, permissions, and evidence. A Persona Manager presents purpose-specific views. Schema or OCA metadata can describe how to interpret an object; it does not authorize access to the value. A live grant can be revoked for future access, though revocation cannot erase information already received.
4. **Consent is an operational rule.** Discovery, ranking, translation, and AI-generated proposals do not bind participants. A valid owner or previously authorized delegate admits an agreement into Working under the Need's conditions. Community authority is defined by its members' arrangements and cannot silently absorb individual authority or collectively governed knowledge.
5. **Local-first is the starting topology.** Nearby devices and relationships can originate and relay authorized exchange. Internet services and institutions may extend reach, but they are additional participants and routes, not the source that makes a person's declaration valid.
6. **Sovereignty carries evidentiary power.** When participants originate interactions and retain their own records, an intentional consequence is that each can originate, preserve, verify, and selectively disclose cryptographic evidence without institutional status being a prerequisite. A declaration is an assertion; a match is a proposal; Working records accepted obligations in a Need-owned journal; a canonical receipt records the resolution attested by its required participants. Cryptographic integrity supports the recorded evidence; it does not prove every physical claim or decide a dispute.
7. **Reciprocity recognizes contribution without making aid conditional.** People can need help and still possess knowledge, relationships, time, or capabilities that matter. Those contributions can be recognized in the exchange, but rescue, emergency assistance, and basic dignity do not depend on repayment, productivity, or a completed contract.
8. **Trust is supported by inspectable relationships, not a universal score.** The Trust Kernel is intended to check corresponding receipt evidence continuously in the background. Trust evidence comes from authorized, recorded interactions and their outcomes—not browsing, silence, refusals, ignored or unaccepted offers, inferred personality, or proximity to strangers. Eight hops is the founder's estimate for a useful full-depth check. Its security contribution is part of the adversarial investigation described later.
9. **Accessibility and graceful degradation belong in the architecture.** Equivalent actions should work through rich interfaces, text, speech, screen readers, feature phones, SMS, terminals, and human assistance where the implementation supports them. When a transport or service is absent, the system must preserve uncertainty rather than invent delivery, consent, or finality.
10. **Compose capabilities instead of creating a platform for every domain.** Commerce, mutual aid, civic obligations, participatory research, community logistics, and recovery coordination can use the same Has/Need/Working grammar while keeping their specific rules inside their own Needs and governance.
11. **Derive, then investigate emergent outcomes.** Start with human outcomes, identify the smallest reusable interactions that could support them, and examine what additional capacities arise through composition. Agency, trust, collective efficacy, economic effects, and trauma mitigation are designed outcomes; the Future Investigations section sets out how to assess them.

### 3.2 The system's breadth: components in service of participant authority

Has-Needs is a system of systems, but not a collection of unrelated modules. Each component serves a bounded role in the same participant-originated exchange. The table distinguishes the breadth of the design from implementation claims: some components are architectural requirements, while named substrates remain replaceable candidates.

| Layer | Role in the system | Boundary that preserves the design |
|---|---|---|
| Person and continuity | Persona Manager, identity facets, owner-held objects, private personal chains | The participant originates meaning and controls which facet or record is disclosed. |
| Exchange grammar | Has, Need, Working, basic contract conditions | Three relation states stay stable across domains; Pending and receipts are evidence structures, not extra relation states. |
| Meaning and discovery | Participant-defined terms, local ontologies, semantic edges, resolution evidence, geographic spheres of possibility | Translation and matching suggest paths; they do not overwrite local meaning, reveal exact location, or decide consent. |
| Authorization and data | Positive, purpose-scoped disclosure grants; OCA descriptions; protected objects and derived views | A schema can describe data but cannot grant access. A permission applies only to its stated object, recipient, purpose, duration, and use. |
| AI likeness and derived media | Provenance-bearing source objects, identity facets, scoped authorization, and records of permitted uses | Provenance can make origin and authorization claims inspectable; it does not by itself settle ownership, create a statutory right, erase copies, or guarantee a remedy. |
| Transport and reach | Local peer-to-peer exchange, Bluetooth mesh, relays, QR rendezvous, SMS, radio, terminals, and internet-connected routes | Transport is replaceable and may fail. The protocol does not promise universal delivery or depend on one network being available. |
| Commitment and evidence | Need-owned Pending journals, coordinated review, canonical receipts, receipt-chain integrity checks | Participants decide and attest under the Need; cryptographic consistency is not a verdict about physical truth. |
| Collective coordination | Community Needs, subcommunities, explicit pooling, delegation, custody handoffs | Group membership alone grants no authority over a person's objects, data, or commitments. |
| Human interface | Personal Globe, maps, Data Views, Data Stories, voice, text, icons, screen readers, feature-phone and terminal modes | Views render permitted information; they do not become a new authoritative database or make access depend on literacy or a rich device. |
| Replaceable implementation | Candidate encodings and cryptography, DXOS/ECHO replication experiments, SmallWeb-style hosting, APIs, and external attestations | Components can support the design without owning its semantics or permissions. Specific choices require implementation and interoperability validation. |
| Emergent domains | Mutual aid, disaster response, agriculture and commerce, civic obligations, research, education, and recovery | Each domain contributes its own governance, legal duties, safety rules, and valuation; the common grammar does not erase those differences. |

This architecture distinguishes **what the design requires** from **how a prototype may implement it**. Sovereign initiation, bounded authority, voluntary Working, Need-owned commitment evidence, and participant-controlled disclosure are architectural commitments. A particular cryptographic encoding, mesh stack, storage substrate, or user-interface toolkit is a replaceable implementation choice until specified and validated.

## 4. A Minimal Grammar of Human Exchange

Has-Needs represents a meaningful interaction as:

`[entity, relation, context]`

The protocol's three relation states are **HAS**, **NEED**, and **WORKING**.

A **Has** is a sovereign declaration of something available: skill, resource, knowledge, capacity, service, permission, or information stream. A **Need** expresses a desired outcome and the conditions under which it may be fulfilled. **Working** is the active relationship established by mutual acceptance of a compatible exchange. The interface supplies accessible actions and a bounded set of basic contract primitives; people provide their own meanings rather than being required to adopt a predefined institutional ontology.

The Need is a condition-governed contract proposition, drawing an architectural analogy from eUTXO models. A Has is an individually identifiable object with provenance and continuity, drawing a separate analogy from NFT models. These analogies describe useful properties; they do not require a cryptocurrency, external blockchain, or token marketplace.

Discovery produces **proposals**, not automatic consent. A match can be suggested through local semantic relationships, previously successful contextual exchanges, and the sphere in which fulfillment is possible. AI may translate, compare, or propose within the owner's authorized scope. People decide whether to enter Working.

This small grammar can describe lending a tool, receiving care, sharing data, transporting food, conducting research, or fulfilling a public-service obligation. Specialized terms belong inside the relevant Need contract rather than requiring a different foundational platform for each domain.

### 4.1 Project breadth from one interaction grammar

The breadth of Has-Needs comes from applying the same interaction grammar to different human situations. The examples show how the shared grammar can configure different domains.

| Domain | Participant-originated interaction | Capability the shared grammar can support |
|---|---|---|
| Disaster and emergency response | A person declares a Need and offers firsthand observations; a responder or neighbor offers a relevant Has and accepts specific work. | Local discovery, voluntary coordination, an inspectable accepted obligation, and reciprocal evidence—without requiring the institution to create the person's identity or Need. |
| Everyday mutual aid | Neighbors express Needs and Hases for care, repairs, transport, food, or companionship. | Small cooperative exchanges can continue before and after an emergency; emergency aid need not be conditional on a counter-contribution. |
| Agriculture, commerce, and logistics | A farmer offers produce; buyers, transporters, storage providers, or community groups express compatible Needs and Hases. | Standing demand, pooled shipment or group purchase, explicit custody handoffs, and an owner-controlled record of the exchange, while value may be monetary, reciprocal, donated, or noncommercial. |
| Community formation and governance | People express a shared Need with purpose, membership rules, and chosen decision procedures. | A group can form around a task without requiring a pre-existing social graph; subcommunities and bounded pooling can coordinate under explicit authority. |
| Civic services | A resident expresses a service Need; an agency accepts a defined obligation into Working. | Accepted commitments and delays can become visible to authorized participants and later governance, without turning the protocol into an automatic judge or election engine. |
| Research and citizen science | A community or researcher expresses a Need for observations; participants choose whether, how, and under what conditions to contribute. | Research can be organized as reciprocal exchange with scoped consent and community knowledge safeguards, while study validity and research ethics remain independent duties. |
| Displacement and recovery | A person arriving in a new place can discover local Needs and Hases and offer self-defined capabilities without first disclosing a refugee identity. | Parallel, asynchronous access to local resources and opportunities for reciprocal participation, without making contribution a condition of assistance. |
| Knowledge and information products | An owner offers a bounded data view, attestation, or live stream in response to a defined Need. | Useful results can be shared without transferring ownership of the underlying personal record, identity, or community-held knowledge. |
| AI likeness and synthetic media | A person or community specifies provenance and authorized conditions for using a likeness or source work in an AI-derived artifact. | The design can preserve an inspectable chain of source, grant, and attested use; legal ownership, enforceability, and remedies require separate analysis. |

These are not separate applications joined by a central data warehouse. They are different configurations of sovereign propositions, discovery, permission, voluntary acceptance, bounded coordination, and participant-held evidence. Shared infrastructure makes the domains composable; it does not erase the distinct laws, safety rules, relationships, or governance that apply in each one.

### 4.2 The compact construct: Has, Need, and the data triplet

The design claim is that **Has, Need, and the entity–relation–context triplet form an unusually compact construct for participant-led interaction**. “Elegant” is meaningful here only if the reader can see what the compactness achieves.

Has and Need are independently addressable participant-originated propositions. A Has states a capability or contribution that its owner makes available under chosen conditions. A Need states a desired outcome and the conditions for fulfilling it. They can exist before a match and without being fields in a central profile. **Working** is the relation formed when the appropriate participants accept a compatible exchange under the Need's rules; it is not a system-generated match or a fourth kind of object.

The triplet **[entity, relation, context]** supplies a small descriptive grammar for what participants mean and how that meaning applies. It is distinct from the Has/Need interaction grammar: the triplet helps express a situated relation, while Has, Need, and Working govern how participants offer, request, and agree. Keeping those two levels distinct lets a system provide simple controls without prescribing a universal ontology of things, people, needs, or value.

The paper's case for elegance should be demonstrated against explicit criteria:

- **Few primitives:** domains do not require a new foundational state machine or platform for every use.
- **Independent authority:** an offer or request can be originated and held by its participant rather than being created as a row in an institutional inventory.
- **Composability:** different Hases, Needs, people, groups, and contracts can be related without expanding the base grammar each time.
- **Consent remains structural:** discovery can suggest a relationship, but only authorized acceptance enters Working.
- **Meaning remains contextual:** the triplet can carry local meaning and context without making a global taxonomy a prerequisite.
- **Evidence follows the interaction:** the same exchange grammar can preserve an accepted obligation and a participant-attested resolution.

The data triplet by itself is not claimed as a novel notation; entity–relation triples have a history in data modeling. The claim to examine is the composition: this triplet, participant-originated Has and Need objects, voluntary Working, owner-controlled identity and disclosure, and participant-held evidence working together as one interaction architecture. The architecture makes a strong comparative claim: across emergency response, commerce, civic obligations, research, and community coordination, this compact grammar can support capabilities that normally require separate platforms while preserving participant authority. The relevant test is not whether every case fits without exception, but whether the shared construct covers the consequential cases with fewer centralized assumptions and less duplicated infrastructure than existing alternatives. Where a case requires a new primitive, that boundary should be made explicit and evaluated.

## 5. From Commitment to Reciprocal Evidence

When participants mutually accept a proposed exchange, the relevant Has and Need become bound in Working and are unavailable for ordinary matching in that commitment. The **Need-owned append-only pending journal** records accepted obligations and authorized progress. Pending is a journal, not a fourth relation state.

At resolution, participants review the same proposed outcome and may each add their own comments and choose what parts of their own contributions are disclosed or encrypted. A changed proposed record resets readiness. Once the required parties are ready on the same version, their Persona Managers preserve **identical canonical receipts** on their respective private personal chains. Each person's chain has its own lineage; the shared receipt is the common evidence of the exchange. These independent histories form a **forest of chains**.

Agreed cancellation and agreed partial fulfillment can be recorded accurately under the applicable contract. An unresolved obligation remains distinguishable from a completed exchange. Matching cryptographic receipts support integrity of the recorded agreement, not proof that every claim about the physical world was true.

This distinction matters socially. A declaration is an assertion. A suggested match is a hypothesis. Acceptance is a commitment. A mutually resolved receipt is attested evidence of the recorded outcome. Keeping these kinds of knowledge distinct makes later learning and accountability more reliable.

## 6. Designed Emergence: Deliberate Social Outcomes from Small Mechanisms

Has-Needs uses **designed emergence**: work backward from complex human and collective outcomes, then reduce the moving parts to the smallest interactions that can create the conditions for them. Trauma mitigation, resilient cooperation, accountable personhood, democratic witness, and alternatives to extractive exchange were not added later as separate features; they are outcomes the architecture was deliberately designed to make possible through the same sovereign interaction environment.

The causal spine is consistent across domains: a sovereign participant originates a contextual Has or Need; local, semantic discovery proposes relevant counterparts; authorized mutual acceptance enters Working; the Need-owned journal preserves accepted obligations and progress; participants review and attest the resolution; and the resulting evidence can inform later discovery, community coordination, participatory science, and accountability. The broader functions are compositions and views of this same interaction—not separate applications with separate authorities.

**Trauma mitigation.** This was an explicit design target. The person under rubble is not only a message source for responders: they can act from firsthand knowledge, express a Need, make a contribution, choose what to reveal, see whether anyone has accepted a commitment, and retain evidence of what followed. Those interactions are designed to counter helplessness, isolation, and loss of control by restoring opportunities for agency, connection, reciprocity, and expectation. The intended mechanisms and human outcomes are specified for investigation in Section 15.

**Agency.** Directly expressing a Need or Has gives a participant a way to initiate action. Voluntary acceptance preserves choice. Receiving material updates on an accepted commitment supports continuity and predictability. In a disaster, the opportunity to communicate and contribute matters before any tangible improvement occurs.

**Reciprocity and recognition.** A person can be simultaneously in need and capable of contributing. A resolved exchange creates participant-held evidence of both sides' involvement, rather than a one-sided record of aid delivered to a passive recipient.

**Informed trust.** Participants may inspect authorized reciprocal relationship evidence, receipt consistency, and the paths connecting them. Trust remains a human judgment grounded in available evidence; the architecture does not need a universal reputation score.

**Collective efficacy.** A Community can itself be expressed as a Need with purpose, participation rules, and a continuing journal. Members can coordinate labor, pool capabilities under explicit authority, form subcommunities, and preserve their own participation records. Larger coordination arises from voluntary relationships among people and groups.

**Institutional accountability.** A citizen's Need for water service, for example, can be accepted by the responsible authority into Working. The accepted obligation and its timing become inspectable by authorized parties. Patterns of delayed or unresolved commitments can help communities distinguish capacity shortfalls from management bottlenecks. These records provide evidence for human governance; they do not automatically adjudicate fault or decide elections.

**Resilience.** Everyday cooperative relationships, local knowledge, and authorized communication pathways remain relevant in an emergency. Local-first operation means the basic interaction does not depend on an institution's prior awareness of the individual.

**Learning without extraction.** Successful, contextually understood resolutions can inform evolving local ontologies. The ontology is a working map of what has proved useful in particular contexts, not an imposed universal taxonomy. Individuals and communities control what information and derived evidence they share.

**Participatory science by default.** The Has/Need grammar can make research a reciprocal, participant-directed activity. A community can state a question as a Need; a researcher can publish a Need that explains the study's importance, local relevance, requested contribution, and compensation; participants can offer observations or expertise through purpose-scoped Hases and choose what they share. Working records the agreed terms, while participant-held receipts can document contributions and the return of findings or other value. Repeated exchanges can produce consented, contextual evidence for local learning and longer-term study. Participatory science is therefore a designed emergent capability of ordinary Has-Needs interactions, not a separate research portal or a requirement that people become passive subjects.

**Provenance for AI-derived likeness.** The same ownership, permission, and evidence mechanisms can be composed to associate an AI-generated image, voice, or other likeness with its source material, the person or community whose identity or knowledge it invokes, the scope of authorization, and later attestations about use. A participant could define permitted purpose, duration, audience, transformation, attribution, and compensation through a specific Need or grant; a recipient could provide evidence of a bounded use. This creates a potentially significant legal and practical capacity: to make provenance and authorization claims inspectable and carry them with the derived artifact or its record.

One intentionally designed side effect is a reversal of evidentiary access. Formal attestations, provenance records, and chain-of-custody evidence are commonly generated or held by institutions and platforms; an individual may be left with a claim that is difficult to substantiate in the systems where decisions are made. Has-Needs does not add an institution-like evidence service as its primary purpose. Rather, when sovereignty is made operational within an interaction setting, each participant can attest to their own statements and actions, preserve corresponding evidence, verify another attestation, and disclose a bounded proof when needed. The intended quality is not a weaker personal substitute for institutional evidence: it is cryptographic proof available to all participants, at “first-world” quality, with each participant retaining control of their own record.

This capacity does not automatically establish ownership of every likeness, make a license enforceable in every jurisdiction, prevent copying, erase a generated artifact after revocation, or guarantee a remedy. Nor does a signature establish that its underlying factual assertion is true. Those questions depend on applicable law, platform behavior, source rights, community governance, and facts about the use. The designed emergent consequence is that provenance-and-permission relationships can become attestable and portable within the same sovereign interaction grammar. How institutions, courts, and communities should interpret equal-quality participant-held evidence is a central legal and policy question raised by the architecture.

## 7. Human Factors, Trauma, and Testable Psychological Claims

The disaster opening expresses a deliberate trauma-mitigation design choice. Under extreme uncertainty, a person may experience loss of control, isolation, and inability to affect events. Has-Needs is designed to offer an early, credible opportunity to communicate, contribute, choose, and participate. The goal is not merely to make better reports available to institutions; it is to give the affected person a meaningful place in the cooperative process from the outset.

The relevant psychological concepts must be kept distinct. **Perceived agency** concerns whether one's actions can influence circumstances. **Self-efficacy** concerns belief in one's capacity to perform actions that affect outcomes (Bandura, 1977). A communication opportunity might support either, but a message sent without acknowledgment, or a commitment repeatedly ignored, could also deepen distress. Trauma-informed design therefore requires attention to expectations, accessibility, follow-through, and the participant's ability to choose what to disclose.

The trauma-mitigation design should be evaluated with affected people, with measures tied to its intended mechanisms rather than inferred solely from interface features. Measures include perceived agency before any response, communication success and acknowledgment, perceived safety, burden of participation, continuity of contact, and subsequent well-being. Research ethics must account for vulnerable participants, consent, and situations in which the system cannot deliver help.

The conceptual background includes self-efficacy research (Bandura, 1977), self-determination theory (Ryan & Deci, 2000), and principles of mass-trauma intervention emphasizing safety, calming, individual and collective efficacy, connectedness, and hope (Hobfoll et al., 2007). These literatures motivate hypotheses; they do not establish the effectiveness of Has-Needs.


## 8. Research Foundations: Agency, Coping Efficacy, and Collective Resilience

The psychological rationale for Has-Needs draws on established work. The architecture translates those principles into an explicit interaction design whose effects can be evaluated. Hobfoll and colleagues' consensus synthesis identifies five principles for early and mid-term intervention following mass trauma: **safety, calming, self- and collective efficacy, connectedness, and hope** [1]. Has-Needs' emphasis on immediate, voluntary, meaningful action is most directly related to efficacy and connectedness. It does not replace clinical care, emergency services, or the other conditions necessary for safety.

Benight and Bandura's synthesis of post-traumatic recovery research places **perceived coping self-efficacy** at the center of adaptation to adversity [2]. In Has-Needs, the distinction between *being able to declare a Need*, *having the declaration received*, *obtaining a response*, and *receiving assistance* is therefore psychologically consequential. An interface should distinguish those events rather than offer false assurance. The hypothesis is that a credible opportunity to act and communicate can support perceived agency before the environment has materially improved. The hypothesis does not imply that transmission alone reliably improves mental health.

Norris and colleagues describe community resilience as a process drawing on four adaptive capacities: economic development, social capital, information and communication, and community competence [3]. Has-Needs proposes a common interaction grammar through which participants can mobilize and combine these capacities. A community can identify a missing resource, form an agreement to supply it, preserve the accepted obligation, and retain reciprocal evidence of the outcome. Such coordination may improve adaptive capacity, but success depends on adoption, accessibility, physical resources, reliable communication, governance, and equitable participation.

These sources suggest testable propositions:

1. **Immediate agency:** Compared with an otherwise equivalent reporting-only interface, a participant-controlled Has/Need interaction may increase perceived ability to influence an unfolding situation before receiving aid.
2. **Collective efficacy:** Communities using visible voluntary commitments and locally held reciprocal evidence may report greater confidence in their ability to solve shared problems.
3. **Coordination:** Locally originated Needs and Hases may reduce the time between an observation, its discovery by a relevant participant, and an accepted action.
4. **Accountability:** An append-only record of accepted Working obligations may make stalled work and recurring workflow bottlenecks more observable without requiring a central dossier of participants.

Evaluation should include adverse outcomes: messages that cannot be delivered, promises that go unfulfilled, misleading signals of acknowledgment, coerced disclosure, inequitable device access, exposure of sensitive context, and new burdens placed on people already under stress. Trauma-informed design is an empirical responsibility, not an efficacy label.

## 9. A Documented Stress Test: Los Angeles County's January 2025 Fires

The January 2025 Eaton and Palisades fires provide a concrete case for examining the architecture against observed operational constraints. Los Angeles County commissioned an independent McChrystal Group after-action review of alerting and evacuation. The County describes its findings as a combination of outdated policies, inconsistent practices, and communications vulnerabilities, **not one single point of failure** [4]. A separate Citygate Associates investigation, revised in May 2026, reconstructed the Eaton Fire's evacuation decisions and the information reasonably available to command at each stage [5]. These reports should be read together rather than treated as interchangeable accounts.

### 9.1 Events and information gaps

The Citygate report records the following sequence (all times local):

| Recorded event | Time | Architectural question |
| --- | --- | --- |
| Initial advisory notifications covering 12 zones | Jan. 7, **6:48 p.m.** | Can residents and field participants express locally observed conditions and assistance needs alongside official alerts? |
| Initial evacuation orders for selected eastern zones | Jan. 7, **7:26 p.m.** | Can official warnings be carried into local relationships while preserving the authority of the issuing agency? |
| Numerous separate structure-fire requests, approximately one every two minutes during one hour | Jan. 8, **1:00–2:00 a.m.** | Can accepted tasks, urgent unmet Needs, and scarce available Hases be distinguished in a live, distributed coordination view? |
| Incident Command began evaluating expanded western evacuation zones after critical radio reports | Jan. 8, **2:18 a.m.** | Can relevant firsthand observations become visible sooner to appropriate participants without claiming they automatically warrant an evacuation order? |
| Evacuation orders issued for 13 zones west of Lake Avenue | Jan. 8, **3:25 a.m.** | Can authorized orders be relayed, acknowledged where possible, and distinguished from unconfirmed delivery? |

The Citygate review also describes the absence of real-time aerial fire-spread intelligence because aircraft were grounded by extreme winds. It concludes that Incident Command did **not** improperly withhold earlier western evacuation orders on the evidence then available; it specifically disputes a previously reported interpretation of communications at approximately 11:24 p.m. [5]. This is crucial: a credible Has-Needs analysis should identify **information and coordination opportunities**, not retrospectively assert that officials ignored facts the report says they did not possess.

### 9.2 What Has-Needs would change in the workflow

**Locally originated observations.** A resident who sees fire movement, a blocked route, a person unable to evacuate, or an available vehicle can express that observation or capability directly within their local sphere. Such information remains an attributed participant declaration until verified or accepted; it does not automatically become an official fire perimeter or evacuation instruction.

**Reciprocal assistance rather than intake alone.** A person requesting transport and a nearby person offering a vehicle may discover one another and voluntarily enter Working. A designated emergency service can participate with its own authorized commitments. Where the circumstances allow, these relationships can begin without waiting for a central inventory to be populated.

**Commitment visibility.** The Need-owned pending journal distinguishes a request, a proposed match, an accepted obligation, work in progress, and an agreed resolution. It can reveal which tasks remain unaccepted or unresolved and help authorized participants redirect scarce resources. This is especially relevant to a period with repeated structure-fire calls and constrained responders; it does not create additional firefighters, vehicles, or safe routes.

**Operational accountability.** For an agency that accepts a particular Need, the accepted conditions and subsequent journal events can expose elapsed time and bottlenecks. The design is meant to support learning and improvement, not infer misconduct from a delay or impose universal deadlines on emergencies.

**After-action evidence.** Participant-controlled records of accepted commitments and resolutions could make it easier to reconstruct what people attempted, what was acknowledged, and which outcomes were agreed. They complement—not replace—dispatch logs, incident command records, physical evidence, and independent investigation.

### 9.3 Testing avoided loss without inventing a savings figure

The proposition that earlier local coordination could have prevented substantial property loss is worth investigating, but **the reviewed reports do not establish a Has-Needs counterfactual or a dollar amount saved**. A defensible estimate requires a bounded incident, an intervention point at which the relevant information and resources actually existed, a plausible change in action, and an independently supportable loss valuation.

For each candidate event, an evaluation should record: (a) the earliest available local observation; (b) the feasible peer-to-peer delivery path; (c) the authorized recipient and decision rights; (d) the earliest realistic acknowledgment and commitment; (e) whether an action could safely have changed the outcome; and (f) the uncertainty around avoided loss. A replay or tabletop exercise could compare conventional information flow with a simulated Has-Needs flow, including device and network constraints. Only then should any estimate in the millions of dollars be published.

This case exposes the proposed innovation particularly clearly: **the person on the ground is both a source of knowledge and an autonomous participant capable of initiating a cooperative response**. The emergency institution remains essential, but it is no longer the sole possible origin of meaningful action.


### 9.4 Counterfactual opportunities ranked by evidentiary strength

The two McChrystal Group reviews and the separate Citygate investigation address different operational periods and questions. The September 2025 review concerns warnings and evacuations; the September 2026 review addresses recovery and repopulation, including communications, volunteers and donations, housing, and access and functional needs. Citygate's May 2026 revised investigation reconstructs evacuation command decisions. These are **documented classes of failure or constraint**, not proof that a proposed software system would have changed a specific fire's course [4–6].

| Candidate intervention | Documented basis | Has-Needs mechanism | Counterfactual strength and boundary |
| --- | --- | --- | --- |
| **A. Match an evacuation assistance Need to a locally available Has** | Reviews identify communications and resource constraints; recovery review includes people with access and functional needs [4–6]. | A person requests accessible transport; a neighbor or authorized provider offers a vehicle; both explicitly accept Working; status is visible to authorized participants. | **High design relevance, unproven impact.** Requires a real available driver, safe route, reachable devices, consent, and enough time. A match is not a rescue. |
| **B. Relay a field observation to a relevant decision-maker** | September 2025 review found inconsistent field reporting, unconnected platforms, and unreliable cellular communications [4]. Citygate reconstructed evolving fire intelligence and its limits [5]. | Participant-originated Has of an observation, contextual matching, permitted peer relay, clear acknowledgment status. | **High design relevance, uncertain timing benefit.** An observation must have existed early enough, been deliverable, been credible, and changed a lawful decision. |
| **C. Expose unresolved requests amid simultaneous calls** | Citygate reports heavy structure-fire call volume during the overnight escalation and constrained suppression resources [5]. | Need-owned pending journals distinguish unmatched, accepted, in-progress, and resolved work; authorized views reveal congestion. | **Medium design relevance.** Visibility does not create firefighters or suppression capacity; may support triage only when actionable resources exist. |
| **D. Coordinate volunteers, donations, and short-term recovery** | September 2026 recovery review addresses volunteer/donation management, shelter and housing, recovery, and repopulation; it identifies 26 findings and 25 recommendations [6]. | Community Needs, bounded delegations, scoped Hases, acceptance, progress journals, reciprocal receipts. | **High suitability for prospective field testing.** This may be a more measurable initial pilot than attempting to change wildfire command decisions. |
| **E. Reconstruct who knew, committed, and completed what** | The county's reviews relied on disparate records, interviews, and after-action reconstruction [4–6]. | Consent-bounded journals and participant-held canonical receipts, with event provenance and selective sharing. | **Strong auditability hypothesis.** A receipt documents a mutually recorded outcome, not independent truth about the physical event. |

**Priority for empirical study:** Begin with **D (recovery coordination)** and **A (assistance matching)** in controlled or prospective deployments, because observable completion, wait times, and resource utilization can be measured without assuming that software could safely override fire command. Evaluate **B (field intelligence)** through replay with subject-matter experts and then live exercises. Study **C (triage)** only with resource-capacity and safety constraints included.

### 9.5 What the timeline permits—and does not permit us to conclude

The previously cited Eaton timeline includes an escalation in structure-fire requests between approximately **1:00 and 2:00 a.m.**, a critical fire-movement report around **2:18–2:19 a.m.**, and western evacuation orders around **3:25 a.m.** [5]. These timestamps establish an observable interval for analyzing information transfer and decision-making; they **do not** establish an hour of avoidable delay. The Citygate investigation concludes that command decisions were appropriate to the information available at the time. The earlier McChrystal review and independent reporting identify broader communication and organizational weaknesses, but their scopes and conclusions should not be collapsed into one finding [4–5].

A rigorous event replay therefore asks, for each hypothesized earlier observation: **Who knew what, at what time?** Was it recorded contemporaneously? Was a participating peer reachable? Would the proposed semantic and geographic context have directed the observation to someone with decision authority? Could its reliability have been assessed without exposing a vulnerable resident? What other facts, personnel, or safe routes were necessary? An earlier notification only changes an outcome when this full causal chain is supported.

### 9.5a West Altadena: the untransmitted observation as an operational failure mode

The precise distinction is between **an observation existing in the field** and **that observation reaching the authorized decision-maker in actionable form**. Subsequent reporting on dispatch and sheriff records describes a west Altadena house/vehicle/tree fire call at approximately **1:30 a.m.**, deputies responding to a house-fire report around **2:30 a.m.**, and deputies reporting substantial fire activity on both sides of Lake Avenue at **2:43 a.m.** A critical radio report of westward fire movement reached command at approximately **2:18–2:19 a.m.**, and orders for much of western Altadena were issued at **3:25 a.m.** [7–8]. These records do **not** establish that the first 1:30 a.m. report was left entirely unchecked until 2:30 or 3:00 a.m.; call time, response time, field observation, onward transmission, command acknowledgment, and evacuation order are different events.

Reporting on the October 2026 review describes an especially consequential example: a paramedic squad reportedly observed dangerous conditions while operating outside the fire incident assignment, with the result that its information was not relayed to incident personnel [9]. That is an architectural information-flow failure worth investigating independently of whether an individual commander made a reasonable decision on the information received. Citygate's May 2026 review concluded that evacuation decisions were not improperly delayed; other subsequent analyses of dispatch records raise questions about the availability and transmission of earlier field intelligence [5, 7–9]. Both findings must remain visible.

In a Has-Needs counterfactual, an authorized responder or resident could originate a time-stamped, scoped **Has of observed conditions**, and an incident function could express a **Need for current field intelligence**. Local discovery and permitted relays might surface that observation across organizational assignment boundaries. The recipient's acknowledgment, subsequent acceptance of a task, and final resolution would be separate evidence events. None of these steps automatically converts an observation into an official warning, verifies fire spread, or guarantees delivery.

The strongest initial measure is therefore not speculative property value saved but **observation-to-action latency**: time from the earliest contemporaneously recorded observation to authorized receipt, assessment, decision, assignment, and completion, with explicit missing-data markers. This also permits analysis of how long a resource was available but undiscovered, how long an accepted Need remained unresolved, and which bottlenecks repeated across an incident.

### 9.5b Economic value of making efficiency measurable

Has-Needs proposes two separable benefits: **(1) potentially better decisions and coordination** and **(2) finer-grained evidence with which to measure actual performance and improvement**. The second is not contingent on proving that every earlier observation would have changed an evacuation decision. If participating individuals and agencies record locally originated Needs, relevant Hases, mutual acceptance into Working, journaled progress, and reciprocal resolutions, they create an event-level basis for reconstructing the *actual* coordination process.

A useful study compares baseline dispatch/incident logs and post-event reconstruction against an authorized Has-Needs event stream. Candidate measures include: time to first receipt; time to first meaningful acknowledgment; time to acceptance; elapsed Working time; resolution rate; unaccepted-Need backlog; time a suitable Has remained undiscovered; repeated reassignment; and coverage/completeness of after-action evidence. Researchers must distinguish **missing record** from **no action**, adjust for participation bias, and preserve privacy through scoped disclosure. The personal chain is not a universal public audit log; any emergency-manager view is assembled from data its owners have authorized.

This produces a stronger economic rationale than a headline avoided-loss estimate. With appropriate controls, agencies could estimate changes in resource utilization, waiting time, duplication, and completion rates from observed operational data rather than rely entirely on retrospective estimates. Attributing a particular cost saving still requires a credible counterfactual, but **the measurements used to construct that counterfactual become substantially more specific and auditable**. This is a testable architectural advantage, not yet a demonstrated deployment result.

### 9.5c Communication overhead, duplicated verification, and interoperable evidence

Communication inefficiency is a measurable operational cost, not merely a technical inconvenience. A systematic review of disaster situational-awareness technologies screened 1,459 articles and 36 after-action reports and included 302 sources. It identified unreliable or delayed communications, labor-intensive analysis and visualization, and insufficient interoperability among information sources as major constraints [10]. A 2025 study specifically examines communication inefficiencies between emergency managers and health professionals, including the coordination burden of preventing duplicated tasks among multiple agencies [11]. NIST separately identifies standards, access control, and governance as barriers to interoperable real-time public-safety data [12]. These findings support the problem definition; they do not establish a universal percentage of emergency resources wasted.

**Duplicated verification is a distinct failure mode.** A report may be inspected separately by fire, law enforcement, emergency medical services, utilities, or public works because each agency cannot see what another has observed, checked, or accepted responsibility for. This can consume travel time, personnel hours, dispatch capacity, and attention, while creating apparently conflicting accounts. The present sources establish the general cross-agency problem; they do not independently establish a specific number of duplicate Altadena verification dispatches. That incident-level claim requires dispatch records or an after-action finding that explicitly identifies them.

Has-Needs offers a composable response: an observation is a participant-controlled **Has** with source and context; a verification requirement is a **Need** whose contract specifies acceptable evidence and qualified parties. Acceptance enters **Working** and becomes visible, within authorized scope, as verification in progress. The Need-owned pending journal records authorized steps, and agreed resolution generates reciprocal evidence. Other agencies can discover that verification already exists and decide whether it satisfies their separate statutory, operational, or evidentiary obligations. The design does not turn an assertion into established fact, eliminate independent checks where required, or create a centralized incident-wide inventory.

The proposed efficiency metrics are: **duplicate site visits per unique issue; responder-hours spent on repeat verification; elapsed time from first observation to accepted verification; time spent reconciling contradictory records; number of separate agency requests for the same fact; and fraction of verifications reusable under valid permissions**. Each measure requires event deduplication, an incident identifier or privacy-preserving equivalence test, provenance, access policy, and controls for cases where independent corroboration is appropriate. Comparative exercises should test whether the mechanism reduces redundant effort *without* reducing verification quality or safety.

This extends the paper's economic argument: Has-Needs could improve response efficiency while making communication and verification overhead visible as recorded operational events. The architecture proposes a way to measure such costs, not a pre-established savings rate.

### 9.5d Recurring communication failure across major incidents: evidence beyond Los Angeles

Communication breakdown in disasters is a recurring empirical finding, not merely an anecdote from the Eaton Fire. A 2023 scoping review of **32 publications** on sudden-onset major incidents reported communication breakdown in **25 (78.1%)**, inter-authority communication challenges in **18 (56.3%)**, and system overload or incompatibility in **9 (28.1%)** [13]. These percentages describe the **papers included in the review**, not the probability that a future disaster will suffer a given failure. A separate systematic review synthesizing **302 articles and after-action reports** identified unreliable or delayed communications, time-intensive analysis, and poor interoperability as major constraints on disaster situational awareness [10]. Another literature review identifies technological, organizational, and social barriers across the stages of crisis management [14].

The historical record illustrates several distinct failure modes:

| Incident or evidence | Documented problem | Implication for Has-Needs |
| --- | --- | --- |
| **September 11, 2001** | NIST documents incompatible first-responder radio systems and overcrowded channels during World Trade Center response [15]. | Shared semantic objects and peer-to-peer coordination could supplement voice channels where participating transports remain available; the protocol does not make incompatible radios physically interoperable. |
| **Hurricane Katrina, 2005** | A federal communications panel documented incompatible frequency assignments and overload of limited mutual-aid channels; the Senate's investigation distinguished loss of basic operability from lack of interoperability [16, 17]. | Locally initiated interactions and multiple transport options reduce dependence on a single coordination pathway, subject to real device availability, power, reach, and security. |
| **Maui wildfires, 2023** | A Maui Fire Department after-action account described cellular infrastructure losses and overloaded fire-radio frequencies [18]. A Commerce Department Inspector General audit found that FirstNet services were not effective in supporting the public-safety response [19]. | A participating local mesh may offer additional paths and local coordination opportunities, but it is neither a guarantee of delivery nor a replacement for fire radio or incident command. |
| **Eaton and Palisades fires, 2025** | Los Angeles County's independent review identified outdated policies, inconsistent practices, and communications vulnerabilities, and recommended improved interoperable communications and field-accessible tools [4]. | Need-owned journals, explicit acceptance, scoped shared evidence, and local-originated reports could address information-flow and coordination problems at the application layer. |

The Maui record also shows why specificity matters: the **Maui Police Department** reported its public-safety radio system remained functional and reported no radio issues in its own preliminary after-action review [20]. An incident may therefore contain both a functioning agency radio system and serious communications failures elsewhere. The paper should not flatten these different observations into a claim that every radio system failed.

#### From communication volume to operational cost

A congested channel is not the same as an overloaded coordination process. A radio may transmit successfully while an observation remains unassigned, unacknowledged, unverifiable, or invisible to another agency. Likewise, a shared dashboard may display information without recording whether anyone has accepted responsibility for acting on it. Has-Needs is designed to preserve the transition from *observation* to *Need*, *proposed match*, *accepted Working obligation*, *progress*, and *resolved reciprocal evidence*. These stages make delay and duplication measurable while leaving judgment and authority with the participants.

A prospective study should measure **observation-to-acknowledgment**, **acknowledgment-to-acceptance**, **acceptance-to-action**, **action-to-resolution**, the number of **independent repeat-verification deployments**, **responder-hours spent on duplicated work**, and the share of accepted Needs that remain unresolved. The counterfactual is not simply that a mesh can carry more messages: it is that **fewer messages and repeated investigations may be needed to achieve a documented, actionable resolution**.

Existing radio, broadband, and incident-management investments remain necessary. Has-Needs' distinctive proposed contribution is an interoperable *meaning-and-commitment layer* carried by whatever participating transport is available. Whether it reduces congestion, repeated verification, or cost must be established through incident replay, controlled exercises, and prospective deployments—not inferred from historical failures alone.

### 9.6 Economic evaluation: transparent scenarios, not historical savings claims

The economic unit should be **a verified changed outcome**, not a count of messages or matches. For a specific class of avoidable loss, a first-pass model is:

`Expected avoided loss = N × p(reachable) × p(actionable | reachable) × p(successful intervention | actionable) × value of loss avoided − incremental intervention costs`

Here `N` is the number of independently identified at-risk cases that could feasibly have been affected; probabilities must be estimated from pilot data or a carefully specified expert-elicitation protocol. Cases must be deduplicated and losses must not be counted twice. A credible model should also include **zero-benefit and adverse-outcome cases** (for example, an unsafe route suggested by incomplete information).

The following figures are **illustrative sensitivity calculations, not measured Los Angeles County data**. They demonstrate how a multimillion-dollar proposition could be tested rather than asserted:

| Hypothetical scenario | At-risk cases (`N`) | Reachable × actionable × successful | Assumed avoided loss per successful case | Gross expected avoided loss |
| --- | ---: | ---: | ---: | ---: |
| Limited coordination benefit | 100 | 0.50 × 0.20 × 0.25 = 2.5% | $100,000 | **$250,000** |
| Moderate coordination benefit | 200 | 0.60 × 0.35 × 0.40 = 8.4% | $150,000 | **$2,520,000** |
| Strong coordination benefit | 300 | 0.75 × 0.50 × 0.50 = 18.75% | $200,000 | **$11,250,000** |

These rows are **not forecasts**, and none of the assumed case counts, probabilities, or property values is established by the after-action reports. They are deliberately exposed parameters to prevent a compelling narrative from becoming a fictitious estimate. Net benefit must subtract deployment, training, device, staffing, false-positive, and operating costs. Property-loss modeling must not substitute for independent life-safety analysis or place monetary value above safe evacuation decisions.

A publication-quality estimate would require an incident-level dataset: time-stamped Need/Has opportunities; participating-device coverage; safe available resources; authorized decision pathways; matched controls or comparable historical cases; observed intervention success; and independently sourced property valuations. Report uncertainty intervals and sensitivity to missing participants, correlated failures, and selection bias. If those inputs cannot be established, the correct result is **not estimable from available evidence**.

### 9.7 Prospective validation design

A feasible first study would randomize comparable disaster-preparedness exercises or recovery-service workflows between conventional intake/coordination and an additional Has-Needs local-first participation layer. Pre-register outcomes: time to first meaningful acknowledgment; time to accepted Working; completion rate; unmet-Need duration; duplication of effort; successful safe assistance; user-perceived agency; and the proportion of accepted obligations with reconstructable outcomes. Include a matched observational arm if randomization is impractical, while acknowledging its weaker causal inference.

The pilot should preserve the distinction between an **issued message**, a **received message**, an **accepted commitment**, and a **completed result**. Official evacuation orders remain the responsibility of authorized public officials. Human subjects and safety review are necessary where vulnerable populations, emergency simulations, or sensitive data are involved.

This is the defensible economic proposition: Has-Needs may improve the conversion of **locally known possibility into authorized, completed cooperation**. The size and monetary value of that improvement remain research questions.

## 10. Communities, Civic Commitments, and Public Accountability

A Has-Needs Community is a contract-governed cooperative relationship, expressed through a specialized Need. It may be temporary, enduring, nested, or overlapping. Members can establish who admits participants, who can act on behalf of the group, what information is shared, and how commitments are tracked. A local rescue group, a household, an agricultural buying group, and a research collective can share the same underlying grammar while applying different rules.

Public institutions can participate as counterparties without becoming the owners of citizen declarations. A municipality that accepts a service Need creates an observable obligation under the agreed terms. Authorized views can show accepted work, elapsed time, progress, and unresolved backlogs. Where recurring delays accumulate, managers and communities can ask whether additional resources, different procedures, or leadership changes are warranted. The protocol records relationships and evidence; public decision-making remains with legitimate human processes.

This is a proposed accountability capability, not a claim that software alone produces responsive government. It requires correct authority mapping, honest participation, protection against coercion and retaliation, and careful rules for public versus private reporting.

### 10.1 From citizen expression to a continuous public agenda

A citizen's Need is already a meaningful expression of a desired outcome. It does not have to be translated into a periodic survey response, campaign slogan, or institution-owned ticket before becoming actionable. Multiple citizens may express related Needs, organize a Community Need around a common objective, and selectively share the resulting evidence. Over time, authorized views of those Needs form a **living stream of public priorities**: what people seek to accomplish, what help is available, which matters are under way, and what remains unresolved. This is a deliberate emergent consequence of the same minimal grammar used for ordinary exchange, not a separate political polling subsystem.

The stream does not imply that every expressed desire is a binding obligation on government. Authority, legal mandates, budgets, competing priorities, privacy, and consent still matter. Its innovation is to preserve the connection between a person's expressed intention and the subsequent disposition of that intention, rather than discarding the expression once it has been counted.

### 10.2 Accepted public obligations become inspectable work

Where a municipality or other authorized public body has the relevant responsibility, it can accept a compatible citizen Need. Acceptance places the parties into **WORKING** and begins the Need-owned pending journal. That journal records the agreed scope, responsible participants, authorized progress events, relevant timing, and subsequent changes. A delay, handoff, or escalation can be evaluated against the accepted terms rather than guessed from public statements. Repeated delays at the same stage can reveal a capacity constraint, procedural defect, or organizational bottleneck, without automatically assigning blame.

The distinctions among **requested**, **acknowledged**, **accepted**, **in progress**, **resolved**, and **unresolved** are essential. A request not accepted by an agency is not an agency's accepted obligation. A Working item with no agreed resolution is not a completed exchange and does not acquire a fabricated final receipt merely because its deadline has passed. An agreed unsuccessful outcome, cancellation, or no-deal resolution can produce the appropriate canonical reciprocal receipt, while the pending journal preserves the preceding commitment history. Local declarations and communications can remain locally retained even when a counterparty never receives them; cryptographic evidence must never be presented as proof of delivery when none occurred.

### 10.3 Failure evidence, citizen-held receipts, and the election-cycle view

A completed or agreed unsuccessful exchange yields **identical canonical receipts** on the participants' separate private personal chains. Each citizen's Persona Manager preserves the person's own chain; the government does not become the sole custodian of that citizen's civic history. Authorized, privacy-preserving aggregation of citizens' declarations, pending status, and resolved receipts can produce a community-facing account of public work. This is the **forest of chains** applied to democratic accountability: independent records that can be selectively connected through shared exchange evidence, rather than a single government-owned political ledger.

Consider ten citizen service Needs. Suppose a municipality accepts eight, completes two, and leaves six in Working. The resulting public view must say **ten expressed; eight accepted; two resolved successfully; six accepted and unresolved; two not accepted**—not simply “eight government failures.” If a subset of those six later ends in mutually agreed nonfulfillment, its final receipts preserve that outcome. Citizens can inspect the authorized underlying evidence and assemble a practical **shopping list of unaccomplished priorities**. They can ask where work stalled, whether resources were missing, and which proposed changes are likely to help.

At election time, candidates and incumbents can be evaluated against a more concrete record of **commitments, accomplishment, nonfulfillment, and unresolved work**. An incumbent may show legitimate constraints and delivered outcomes; a challenger may propose a different way to resolve persistent Needs. This does not make cryptographic receipts an automatic measure of political merit: they establish integrity of the agreed record, not independent truth of all field conditions, fair distribution of resources, or the causal responsibility of a particular official. It does make performance claims more contestable with evidence, and can encourage new participation and leadership between as well as during elections.

### 10.4 From one failed message to cumulative disempowerment

The human consequence of communication breakdown extends beyond the time lost by responders. A person who repeatedly identifies a Need, attempts to communicate it, and sees no acknowledgment or observable consequence may come to experience participation as futile. In communities exposed to recurrent disasters, scarcity, or prolonged institutional neglect, such experiences may compound across years. This is a **research proposition** informed by perceived control, coping self-efficacy, collective efficacy, and learned-helplessness literature; it is not a claim that every unanswered message causes trauma or that all fatalism has the same cause.

Has-Needs is designed to preserve meaningful distinctions between **an attempt to communicate**, **an actual acknowledgment**, **an accepted obligation**, and **a recorded outcome**. Even when a Need cannot be met, accurate status and participant-held evidence may provide a basis for future action and collective learning. The system must not manufacture reassuring acknowledgments or promise fulfillment. Its potential psychological contribution lies in preserving opportunities for agency, intelligible feedback, and evidence that action mattered—or that an institution did not respond.

### 10.5 Evidence during the event, rather than costly reconstruction alone

Traditional after-action reviews often must piece together partial radio logs, dispatch records, interviews, and institutionally fragmented datasets. Has-Needs could complement those sources with consented, granular records of locally originated Needs, declared Hases, accepted commitments, progress events, and reciprocal resolutions. A missing acknowledgment, repeated verification, or stalled accepted obligation becomes easier to distinguish from a completed task. This could reduce the effort of reconstructing some operational histories and improve the basis for subsequent evaluation, although no savings from avoided studies or audits are yet established.

A major economic implication is **measurement infrastructure**: the same events that coordinate work can provide denominators and timestamps for evaluating it. Researchers can compare observation-to-acknowledgment delay, accepted-to-completed intervals, repeated verification visits, responder-hours, unresolved backlogs, and documented reasons for nonfulfillment. The value is not limited to hypothetical disaster losses avoided. More reliable operational evidence may permit better allocation of scarce resources and more defensible efficiency estimates, with strict controls on privacy, selective disclosure, missing data, and self-reporting bias.

### 10.6 Derivation: one configuration, several designed emergent functions

The causal architectural chain is short:

1. **`[entity, relation, context]` with HAS, NEED, WORKING:** People originate meaningful, context-specific expressions of capability and desired outcome; public priorities and available resources become representable without a new civic data model.
2. **Local-first discovery and matching:** Relevant people, community groups, and authorized agencies can find possible cooperation from their immediate spheres outward; a reported condition can meet an available capability.
3. **Voluntary mutual acceptance:** A proposal becomes an identifiable obligation only when the appropriate parties agree; civic responsibility and resource allocation can be distinguished from unsolicited requests.
4. **Need-owned append-only pending journal:** Accepted work becomes observable as work, including handoffs, elapsed time, authorized updates, bottlenecks, and unresolved commitments. This enables coordination during the event.
5. **Mutually reviewed canonical outcome and reciprocal receipts:** Successful, partially fulfilled, cancelled, and agreed unsuccessful resolutions retain outcome-specific evidence on participants' own private chains. This supports accountability after the event.
6. **Community as a Need, plus selective disclosure and authorized Data Views:** Individual records can inform collective priorities and aggregated accomplishment views without transferring ownership of private chains to an institution.

From these same mechanisms emerge **a live citizen-defined agenda, interoperable coordination, measurable institutional throughput, evidence of failures, a community's list of remaining work, and election-time accountability**. Their emergence is designed: the primitives were selected for these consequences.

## 11. Sovereign Commerce: Open-Ended Value, Standing Needs, and Portable Provenance

Has-Needs extends the same sovereign exchange grammar into commerce without introducing a compulsory catalog of assets, occupations, customer categories, or measures of worth. A Has may represent goods, time, craft, expertise, an attested audience threshold, authorized access to a service, a willingness to listen, a prayer, a performance, or other tangible or intangible contributions. The participant defines what they can offer and on what terms; prospective counterparties decide whether it meets their Needs. The protocol does not imply ownership of other people, their followers, relationships, or cultural knowledge, nor does it override consent, community restrictions, or applicable law. Economic value is contextual and may be monetary, reciprocal, donated, or deliberately noncommercial.

### 11.1 Reversing customer discovery

A business can publish a persistent Need specifying a desired capability or customer-relevant condition. Rather than buying lists of identities or soliciting everyone who might qualify, the Need becomes discoverable within permitted scopes. A person's Persona Manager evaluates relevance against locally held Hases, facets, and preferences, and can present an opportunity privately. **The vendor is not informed that a person matched unless that sovereign participant authorizes a response.** As participants join or become newly eligible, the same standing Need can continue generating private opportunities; authorized opt-ins become the business's response stream. Composable applications may present, negotiate, or fulfill the same Need without creating a central prospect registry. Practical deployments must mitigate query probing, metadata inference, coercion, repeated solicitation, and information leakage.

A creator might expose a narrowly scoped Has asserting that a particular social-media account exceeds 200,000 followers, supported where possible by a platform-issued, fresh, verifiable attestation. That is one granular capability, not permission to disclose the creator's full profile, follower identities, or social graph. A platform-dependent metric cannot be made true merely by writing it to a sovereign chain. The creator may choose to negotiate access to their own communication efforts, not sell ownership of their followers.

### 11.2 A professional facet as a selectively inspectable history

A carpenter, service worker, artist, or independent creator may expose a **professional facet** of their Persona Manager: a bounded, owner-authorized view of relevant qualifications, exchange records, and recurring work patterns. A prospective client seeking a carpenter can request evidence of an apprenticeship with a particular school or master, a sequence of independently attested jobs, experience with whole-house construction, repeat engagements with the same client, intervals between major projects, and the volume or cadence of concurrent work. This can make selection much more specific than a résumé, keyword match, or ungrounded star rating.

The provenance chain is not a universal public employment history. A training institution or mentor can attest an apprenticeship; counterparties can authorize disclosure of canonical reciprocal receipts from resolved exchanges; the worker can choose which professional facet and underlying evidence to present. Receipts establish the agreed record and its integrity, **not independent proof of workmanship, licensure, competence, safety, or all work ever performed**. The absence of a disclosed record is not evidence that an event did not occur. Search must respect client confidentiality, privacy, permissions, and the worker's right not to reveal unrelated life history.

Patterns also require careful interpretation. Returning to the same site could mean a defect or rework, but it could equally mean planned phases, maintenance, an expansion, or a satisfied repeat customer. A five-year interval between houses could reflect capacity, preference, or specialization; it cannot by itself establish quality. Has-Needs permits the buyer to define evidence criteria and inspect authorized context rather than allowing an opaque platform to assign a universal score. A person can express a comfort threshold, request clarifying evidence, and decide whether to engage; the professional retains the right to decline disclosure or the job.

### 11.3 Economic and societal implications

Persistent sovereign matching may reduce wasted customer-acquisition effort and unwanted marketing contact. It may also reveal latent value: a skill, relationship, cultural practice, or service that no platform previously recognized as a market category can meet a newly expressed Need. Communities can aggregate compatible Needs into voluntary buying, distribution, or production commitments, and locally governed rules can preserve noncommercial or culturally restricted practices. These are design possibilities, not measured savings or proof that intermediaries become unnecessary: payments, verification, safety, consumer protection, and dispute resolution still require workable arrangements.

In resource-constrained communities, dependence on outside communications, advertising, finance, and marketplace operators can compound loss of agency. Local-first, participant-owned declarations, private matching, and portable evidence offer a potential alternative to extractive intermediation, without assuming that connectivity, institutional power, or coercion disappear. The wider psychological and democratic hypothesis is that repeated, meaningful choice over one's information, attention, commitments, and economic relationships can strengthen experienced agency. That outcome requires evaluation rather than assertion.

### 11.4 Derivation from the minimal configuration

The commercial consequences follow directly from the existing primitives: **open-ended HAS and NEED** admit contextual forms of value; **persistent discoverable Needs** produce continuing opportunities; **Persona Manager facets and scoped attestations** allow private qualification and owner-controlled professional presentation; **mutual acceptance into WORKING** turns interest into an explicit exchange; the **Need-owned pending journal** preserves execution history; and **independently held reciprocal resolution receipts** enable selectively inspectable provenance and patterns of prior transactions. **Communities and composable contracts** enable collective demand and multi-party supply. No global customer list, universal reputation score, public personal ledger, or compulsory definition of economic value is required. The design deliberately enables these emergent capabilities; their social and economic effects remain empirical questions.

### 11.5 Composable institutions, economic pluralism, and cryptographic longevity

The same owner-controlled, composable API pattern can accept narrowly scoped external attestations: a bank certifies an escrow event, a school attests training, a platform confirms an audience threshold, or an aid agency attests delivery. The issuer certifies only what it is competent to know; the participant controls which authorized facet and information are shared. Revoking an API permission stops future access, not information already disclosed. Institutions can contribute useful evidence without becoming owners of the participant's identity or entire history.

Because Has-Needs does not require money as the unit of value, the same grammar supports paid work, gifts, mutual aid, community pooling, barter, and other forms of economic cooperation. This makes the architecture compatible with post-capitalist economic experimentation without prescribing a single economic order. Its cryptographic mechanisms are likewise intended to be replaceable without changing the human exchange grammar, providing a migration path toward post-quantum techniques. Such migration requires versioned algorithms, keys, signatures, and a plan for historical attestations; modularity is the design advantage, not a claim of present quantum resistance.

## 12. Community Arrival, Ontology Bridges, and Reciprocal Recognition

A receiving town can post a **QR entry point** at a transit stop, shelter, or town boundary. A newcomer—alone or with a group—can discover a community’s locally published food, shelter, medical, transport, translation, and other Needs and Hases, without first wandering through unfamiliar streets or disclosing a refugee identity. The code is a discovery and onboarding invitation, not a tracking tag; useful access must also be available without a camera, smartphone, or reliable internet connection. Participating local nodes can supply available information within their actual communication reach.

Community-maintained ontology mappings can relate newcomers’ own terms for work, training, everyday abilities, and services to locally understood labels. These mappings suggest equivalences, not automatic credential recognition or authorization to practice regulated professions. An individual may offer carpentry, cleaning, pet walking, food preparation, companionship, interpretation, or another self-defined contribution. A person without formal credentials remains capable of meaningful participation; a person unable or unwilling to contribute remains entitled to assistance and dignity. Safeguards and consent still govern childcare, intimate services, and interactions involving vulnerable people.

This creates a potential pathway to **reciprocal recognition across social boundaries**: a local resident discovers a particular person through a useful cooperative encounter, while a displaced individual can exercise agency and preserve authorized evidence of participation. Repeat exchanges may make skills and relationships more visible through an optional professional or community facet. Cooperative contact and reciprocal participation are designed to support social recognition across boundaries.

The Personal Globe can make the **existence of possible support** perceptible even to a participant who chooses not to engage. Relevant nearby offers, community resources, and possible routes may appear without revealing the exact private locations or identities of providers. This is a deliberate human-factors objective: the ability to see support, consider a small contribution, and decide whether to act on one’s own terms. The system does not claim to prove that an individual is safe or socially accepted; it makes potential relationships discoverable and, where freely completed, their outcomes preservable.

### 12.1 Assistance when people actually need it: parallel, asynchronous recovery

Aid often arrives in shipments, funding cycles, and scheduled distributions. People are expected to accommodate what agencies can provide on a particular day. Someone who needs a resource before the shipment arrives—or only becomes ready for it afterward—may miss the opportunity entirely. This mismatch is a coordination problem, not a failure of the person to recover on schedule.

**Has-Needs reverses the point of departure.** People express Needs when those Needs arise; available capabilities can discover and respond to them when they become relevant. Each accepted exchange proceeds through its own Working relationship and Need-owned pending journal. A person may obtain transport today, arrange childcare tomorrow, find building materials weeks later, and rebuild professional connections throughout. Different households, services, and community functions advance in parallel, at their own pace, without waiting for a common distribution event or a single recovery phase to finish.

The mechanism is not disaster-specific: the same independent, persistent, locally discoverable Needs support ordinary healthcare access, housing, livelihoods, education, and civic services. Existing agencies can continue to work within their budgets and legal obligations while discovering demand and coordinating delivery more continuously. Has-Needs cannot supply a resource that does not exist, but it can keep an unmet Need actionable as capabilities and circumstances change.

**Intended outcome:** assistance follows the timing of people's lives rather than requiring people to conform to institutional delivery schedules. Early deployments can measure time from expression to acknowledgment, match, acceptance, and fulfillment; missed distribution opportunities; long-lived unresolved Needs; and the proportion of available resources successfully matched to actual demand. These are opportunities to learn from live use, not prerequisites for helping people now.

## 13. The Personal Globe, Accessible Interaction, and Information Value

The **Personal Globe** is a participant-centered geographic and semantic view of authorized information: one's own Hases, Needs, Working relationships, communities, receipts, relevant routes, environmental conditions, and chosen data streams. Its starting point is the participant's meaningful world, not a global database of people. Geographic layers show permitted areas of relevance without making private personal locations retrievable.

A visual layer may encode an authorized observation as a color field, intensity, or other RGB-based rendering, with provenance retained separately. Combinations of layers can produce **Data Stories**—derived expressions that can be saved, shared, streamed, or offered as a Has under explicit permissions. This concept grows from the author's earlier geographic visualization investigations.

Equivalent basic actions should remain available through text, speech, screen readers, feature phones, SMS, terminal interfaces, and human assistance. Accessibility is an architectural concern because the right to originate meaning is of limited use if the person cannot reach the controls needed to express it.

A participant may also offer a bounded data product or live stream to another participant whose Need defines the requested information, permitted uses, compensation, and duration. Research recruitment and participatory science can use the same consent-governed exchange. Sharing a useful result does not entail surrendering the underlying personal record or community knowledge.

## 14. Origins and Design Method

Has-Needs developed from work across emergency response, geographic information, logistics, community coordination, and interdisciplinary study. Its initiating question was practical: how can a person affected by a disaster act on firsthand knowledge and participate in what happens next, even before an authorized institution reaches them? The 2010 Haiti earthquake response was a formative context for the direct-participation model. The author's background in psychology and sociology, emergency management, military service, first response, humanitarian mapping, and crisis coordination informed the design constraints: people need usable choices under stress; local observations must be able to travel; and evidence must not require surrendering the person's wider identity or history.

The early design sequence is important. **Complete and total sovereignty** was the first governing tenet. The first two architectural decisions that followed were to record value exchange rather than build a general record of people, and to keep actual identity and location abstracted behind each person's **Persona Manager**. These were not later privacy refinements. They established the conditions under which interaction could occur without turning participants into platform-owned profiles or making their physical location the address by which others reached them.

The same early design bundle treated Has and Need as independently addressable, anonymous objects rather than fields in a central identity profile; matched them first by local relevance; and used a map as a language for expressing and perceiving relationships among people, resources, and places. The map was intended as a literacy-agnostic mode of interaction, not merely a dashboard. These objects are anonymous in the sense that they do not require public identifying profiles; they can still be selectively associated with a participant or persona when that participant authorizes it. Map interaction complements, rather than replaces, equivalent text, speech, screen-reader, and low-bandwidth modes.

This map-data design has a longer lineage in the author's work. The effort to make map-data interaction user-controlled began in 1996, advanced in 2008 through a NASA WorldWind plugin, and took a further conceptual step in 2025 with the creation of the data triplet **[entity, relation, context]**. The triplet made the underlying act of relating an entity to a meaning and its context explicit; the map could then serve as one powerful language for navigating those relations rather than as a display imposed on a centrally defined dataset. This chronology is part of the design method: the interface question and the sovereignty question developed together. The 1996 and 2008 dates should be linked to contemporaneous artifacts in an academic edition.


“Record value exchange” does not mean that a Need or Has cannot exist before an exchange. Participants can create and manage their own declarations. It means the system's durable reciprocal record concerns accepted obligations and their attested resolution, rather than an institution's comprehensive inventory of a person's life. The Persona Manager mediates which facet, object, or relevant geographic context is made available to a particular interaction; actual identity and location are not the global substrate.

The concept was subsequently explored through early prototypes and documentation, including a 2017 Has-Needs submission at IBM. The project's historical chronology and source trail belong in its companion history. This paper focuses on the design method that emerged from that work.

The method begins with a human condition, not a software category. It asks what the participant knows, can offer, needs, and is authorized to decide; then identifies the smallest reusable interaction that could make cooperation possible. The design tests whether the interaction preserves participant choice, works across relevant contexts, and can be combined with other interactions without changing the person's authority. It then examines failure cases: non-delivery, nonresponse, unequal bargaining power, data leakage, physical scarcity, coercion, lost devices, partitioned networks, and disputed claims.

This is **designed emergence**. The system is deliberately constrained at the level of primitives and permissions so that broader capabilities can arise through combination: a request and offer may resolve one exchange; repeated exchanges may support a community, an ontology, a marketplace, or a public accountability view. The emergence is designed as a possibility, not assumed as a guaranteed social effect. Each capability remains answerable to the rules and evidence that produced it.

### 14.1 Author background and design standpoint

The author's design standpoint combines lived experience, formal study, emergency-service preparation, military service, and sustained participation in humanitarian response. Om Goeckermann describes his childhood as a foster child and reports founding California's first high-school power-counseling program in 1985. He was part of the fifth unit on scene at the mass-casualty Coalinga I-5 accident, involving more than 300 people. His operational background includes USAF combat-crew service, nuclear, biological, and chemical first-aid instruction, hazardous-materials first-responder certification, and emergency-management education. He pursued dual degrees in psychology and sociology specifically to inform Has-Needs. His crypto investigation dates to 2015. Since 2023, he has been immersed full-time in generative AI, including model testing and rubric evaluation.

His humanitarian and mapping work includes five years full-time with SBTF while he was in school; that work provided a testing ground for Has-Needs' design assumptions across a wide range of event types around the world. It also includes volunteer photomapping and GIS Corps work; a Presidential Volunteer Service Award for Libya mapping; SMS coordination for the Kenya 2012 Uchaguzi instance; a Harvard HHI live exercise; participation in DARPA-based mapping and disaster-management exercises; numerous hackathons; and continuing participation in humanitarian communities through UNOCHA events. Since 2012, he has also been involved with URBAN (Urban Research-Based Action Network), bringing Has-Needs into conversation with community-based participatory research and participatory design science.

This background informs the deliberate design for trauma mitigation, participant agency under crisis, locally sourced knowledge, and coordination across formal and informal responders. Has-Needs is not a theory assembled in abstraction: its problem framing and design assumptions have been examined against operational and humanitarian contexts, including mass-casualty response, worldwide crisis events, live exercises, mapping deployments, and sustained technical investigation. Those experiences substantiate the architecture's practice-based origins and its relevance to real operating conditions. Performance evidence from a complete Has-Needs implementation is a separate question, addressed in the evaluation agenda. An academic edition should attach contemporaneous sources for the dated program, incident, award, and exercise claims where records are available.

The **Paradigm Delta** companion records how conventional software and AI assumptions repeatedly obscured these design choices. It documents the distinction between the person as an authoritative originator of firsthand meaning and the person as an object of institutional assessment; between a fixed grammar and a fixed ontology; between borrowing architectural properties from eUTXO/NFT models and adopting their platforms; between voluntary commitment and an application status; between location of people and geographic applicability; and between an AI's interpretation and the owner's authority. Those distinctions are central to reading this paper.

## 15. Future Investigations

The investigations below address distinct questions that should not be collapsed into one verdict: whether an implementation conforms to the architecture; how it performs under disruption; what human and social outcomes its designed mechanisms produce; and how participant-held evidence is interpreted by institutions and law. The architecture specifies provisions that support a reasoned expectation of advantage over systems dependent on central registration, global inventories, or continuously available infrastructure when communication is disrupted or authority is fragmented. Comparative studies should test continuity, participant access, privacy, evidentiary availability, action latency, commitment persistence, reconciliation, and duplicated work against named systems under shared scenarios. The resilience requirements are architectural; measuring the degree of advantage is a future investigation.

1. **Local-first feasibility.** Test message creation, relay, delivery, synchronization, and recovery among participating devices within range, including constrained and intermittently connected environments. Evaluate meaningful accessibility equivalence across rich and minimal interfaces.
2. **Contract and receipt conformance.** Test acceptance into Working, Need-owned journal continuity, conflicting or delayed updates, agreed cancellation, partial outcomes, identical canonical receipt generation, and partition reconciliation.
3. **Sovereignty and privacy.** Threat-model persona separation, selective disclosure, unauthorized enumeration, inference from repeated matching queries, metadata leakage, and limitations of revocation. Audit that geographic applicability does not expose retrievable actual personal location.
4. **Human factors.** Evaluate whether opportunities for purposeful communication, acknowledgment, consent, and progress visibility improve perceived agency and situational self-efficacy. Include adverse effects, nonresponse, false expectations, and accessibility failures.
5. **Social and institutional effects.** Study community formation, reciprocal participation, contextual trust judgments, service-request completion times, backlog visibility, and the effects of accountability evidence on decision-making. Distinguish correlation, causal impact, and the simple existence of a record.
6. **Knowledge and information exchange.** Assess locally curated ontologies, receipt-derived contextual learning, participatory research, collective permissions, and the usefulness of Personal Globe/Data Story views without extractive profiling.
7. **AI provenance and likeness.** Evaluate how source attribution, scoped permissions, derivative lineage, collective knowledge rights, and attestations of use can travel with AI-derived images, voices, or other artifacts; distinguish technical provenance from legal ownership, enforceability, and remedies.

The architecture's comparative contribution is its **composition**: sovereign initiation, local-first discovery, voluntary commitments, participant-held reciprocal evidence, and designed social emergence. Further comparative work should examine that composition alongside peer-to-peer systems, community resource matching, disaster communications, personal data stores, smart-contract systems, and civic case-management tools, identifying where alternatives meet the same requirements and where they rely on different authority or infrastructure assumptions.

### 15.1 Participatory research as reciprocal exchange

Communities can express questions they want investigated as Needs, while researchers publish Needs that state the study's importance, local relevance, requested contribution, and compensation. Individuals and communities decide whether to participate, what to disclose, and under what terms; researchers contribute study design, analysis, and results. Has-Needs is designed to make participatory science an ordinary consequence of reciprocal exchange: community members can shape questions, contribute observations or expertise, and retain evidence of their participation and the value returned. This extends research beyond paid convenience-sample surveys and makes community members co-designers rather than merely subjects. It does not by itself ensure representative sampling: recruitment pathways, consent, selection effects, and research ethics remain part of the study design. Evaluation should examine community relevance, inclusion, participant agency, data quality, and whether findings return useful value to participating communities.

### 15.2 Research as a companion to deployment

Has-Needs is built to be used, observed, and improved. Its intended effects—agency, reciprocal recognition, responsive assistance, social connectedness, and more effective coordination—are design propositions that guide deployment and prospective study. Research should identify which conditions produce these effects, for whom, by what mechanisms, and with what tradeoffs. People need not wait for categorical experimental proof before they can express Needs, offer Hases, and begin mutually authorized exchanges.

## 16. Conclusion

Has-Needs begins with a person, not a platform. That person can express what they know, what they have, and what they need within the sphere where they can act and communicate. Others may respond, contribute, commit, and expand what becomes possible. Their cooperation can produce communities, practical knowledge, inspectable obligations, and reciprocal evidence that remains with the participants.

The person beneath the rubble makes the purpose visible. Their firsthand knowledge matters. Their need matters. And the opportunity to act and potentially be heard matters **before** a rescue team arrives.

**Sovereignty is where cooperation begins. The network grows through what people accomplish together.**

---

## References and primary reports

- Bandura, A. (1977). Self-efficacy: Toward a unifying theory of behavioral change. *Psychological Review, 84*(2), 191–215. https://doi.org/10.1037/0033-295X.84.2.191
- Hobfoll, S. E., et al. (2007). Five essential elements of immediate and mid-term mass trauma intervention: Empirical evidence. *Psychiatry, 70*(4), 283–315. https://doi.org/10.1521/psyc.2007.70.4.283
- Ryan, R. M., & Deci, E. L. (2000). Self-determination theory and the facilitation of intrinsic motivation, social development, and well-being. *American Psychologist, 55*(1), 68–78. https://doi.org/10.1037/0003-066X.55.1.68
- Ostrom, E. (1990). *Governing the Commons: The Evolution of Institutions for Collective Action*. Cambridge University Press.

**Source note:** The cited works provide conceptual context, not experimental evidence for Has-Needs. Historical and comparative technical claims should be supported with independent sources when presented as established findings. The normative implementation reference is the project's V1 specification.

### Newly verified research and incident sources

[1] Hobfoll, S. E., et al. (2007). Five essential elements of immediate and mid-term mass trauma intervention: Empirical evidence. *Psychiatry, 70*(4), 283–315. https://doi.org/10.1521/psyc.2007.70.4.283

[2] Benight, C. C., & Bandura, A. (2004). Social cognitive theory of posttraumatic recovery: The role of perceived self-efficacy. *Behaviour Research and Therapy, 42*(10), 1129–1148. https://doi.org/10.1016/j.brat.2003.08.008

[3] Norris, F. H., Stevens, S. P., Pfefferbaum, B., Wyche, K. F., & Pfefferbaum, R. L. (2008). Community resilience as a metaphor, theory, set of capacities, and strategy for disaster readiness. *American Journal of Community Psychology, 41*, 127–150. https://doi.org/10.1007/s10464-007-9156-6

[4] Los Angeles County. *Eaton & Palisades Fires After-Action Reviews and Reports*, including the McChrystal Group review of alert notification systems and evacuation policies. https://lacounty.gov/aar/

[5] Citygate Associates. (2026, revised May 19). *Investigation Report of the Eaton Fire Evacuation Alerts*. https://file.lacounty.gov/SDSInter/lac/1208708_InvestigationReportoftheEatonFireEvacuationAlerts_05-18-26_.pdf

[6] Los Angeles County / McChrystal Group. (2026, September). *After-Action Review of Recovery and Repopulation Efforts for the Eaton and Palisades Fires*. County report collection: https://lacounty.gov/aar/ ; County release: https://lacounty.gov/2026/09/11/la-county-releases-second-after-action-review-covering-recovery-and-repopulation-operations-following-2025-wildfires/

[7] Toohey, G. (2026, May 29). *New 911 records deepen questions about why west Altadena was left vulnerable*. Los Angeles Times. https://www.latimes.com/california/story/2026-05-29/more-missed-opportunities-to-evacuate-west-altadena-during-eaton-fire-new-911-records-from-sheriff

[8] Los Angeles County Fire Department. (2026, May 18). *Independent investigation findings of West Altadena evacuation decisions*. https://recovery.lacounty.gov/2026/05/18/county-of-los-angeles-fire-department-releases-independent-investigation-findings-of-west-altadena-evacuation-decisions/

[9] Los Angeles Times. (2026, October 2). *Long-awaited investigation outlines failures of Eaton, Palisades fires*. https://www.latimes.com/environment/story/2026-10-02/long-awaited-investigation-outlines-failures-of-eaton-palisades-fires

[10] *Technologies Enabling Situational Awareness During Disaster Response: A Systematic Review*. *Disaster Medicine and Public Health Preparedness*. https://www.cambridge.org/core/journals/disaster-medicine-and-public-health-preparedness/article/technologies-enabling-situational-awareness-during-disaster-response-a-systematic-review/4B303623ECEF3F0413C68F1462DFC00F

[11] *Exploring communication inefficiencies in disaster response: Perspectives of emergency managers and health professionals*. (2025). *International Journal of Disaster Risk Reduction*. https://doi.org/10.1016/j.ijdrr.2025.105393

[12] Voss, B. M., & Anderson, E. W. (2019). *Interoperability of real-time public safety data: Challenges and possible future states*. National Institute of Standards and Technology. https://www.nist.gov/publications/interoperability-real-time-public-safety-data-challenges-and-possible-future-states

[13] *Communication in Sudden-Onset Major Incidents: Patterns and Challenges—Scoping Review*. (2023). *Disaster Medicine and Public Health Preparedness*. https://pubmed.ncbi.nlm.nih.gov/37681689/

[14] Fischer, D., Posegga, O., & Fischbach, K. (2016). *Communication Barriers in Crisis Management: A Literature Review*. ECIS Research Papers. https://aisel.aisnet.org/ecis2016_rp/168/

[15] National Institute of Standards and Technology. *World Trade Center Investigation: Public Safety Communications*. https://www.nist.gov/world-trade-center-investigation

[16] Independent Panel Reviewing the Impact of Hurricane Katrina on Communications Networks. (2006). *Report and Recommendations to the Federal Communications Commission*. https://www.govinfo.gov/content/pkg/GOVPUB-CC-PURL-gpo20415/pdf/GOVPUB-CC-PURL-gpo20415.pdf

[17] United States Senate Committee on Homeland Security and Governmental Affairs. (2006). *Hurricane Katrina: A Nation Still Unprepared*, Chapter 18, Communication Voids. https://www.hsgac.senate.gov/wp-content/uploads/imo/media/doc/Katrina/FullReport.pdf

[18] Maui Fire Department. (2023/2024). *Maui Wildfires After-Action Report*. Indexed by the Wildland Fire Lessons Learned Center. https://www.lessons.wildfire.gov/incident/maui-wildfires-2023

[19] U.S. Department of Commerce, Office of Inspector General. (2024). *Nationwide Public Safety Broadband Network Was Not Always Available to First Responders During the Catastrophic 2023 Maui Wildfires* (OIG-25-004-A). https://www.oversight.gov/reports/audit/nationwide-public-safety-broadband-network-was-not-always-available-first-responders

[20] Maui Police Department. (2024). *Maui Wildfires of August 8, 2023: Preliminary After-Action Report*. https://www.mauipolice.com/uploads/1/3/1/2/131209824/aar_3-28-24.pdf
