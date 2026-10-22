# Has-Needs Core Features

**Status:** Current summary aligned to [Specification V1](./Has-Needs-Spec-v1.md).  
Where this file and the specification differ, the specification governs.

Has-Needs is a deliberately prosocial, trauma-informed sovereign coordination architecture. Its design examines desired prosocial endpoints, then works back to the smallest primitives that create the conditions for those behaviors to emerge naturally. Human effects are design intentions to evaluate, not assertions of clinical efficacy.

**Indigenous wisdom and traditional knowledge remain under the authority of their holders and communities.** Has-Needs supports their controlled preservation, exchange, and withholding under culturally appropriate permissions, not their capture in an outside platform. The same Need-based exchange grammar accommodates services, knowledge, mutual aid, barter, payment, or combinations; money is simply an optional value term rather than a distinct interaction model.

## 1. Minimal semantic grammar

Has-Needs represents interaction through a compact triplet:

`[entity, relation, context]`

The `relation` field has exactly three protocol states:

- `HAS` — an available capability, resource, knowledge source, stream, or other thing that may satisfy a Need.
- `NEED` — a desired outcome and its provisional conditions for satisfactory resolution.
- `WORKING` — the active state connecting all involved Has and Needs while the Need/smart contract executes.

The triplet is a **shared grammar, not a predefined set of categories**. Has-Needs provides the graphical interface and a fixed, limited vocabulary of official basic contract primitives. People can use its prepared visual controls to give, receive, and exchange without reading, writing, or designing an interface or contract themselves. Each participant supplies the meanings of their Has, Need, and local ontology. These meanings can connect with those of others through voluntary interaction. Advanced participants can create custom contract extensions, distinct from the official primitive set. The triplet does **not** imply a central database or globally enumerable registry.

### The eUTXO / NFT architectural blueprints

Has-Needs uses **eUTXO as the blueprint for a Need**: a smart contract with explicit conditions and authorized transitions. It uses **NFT as the blueprint for a Has**: an individually identified sovereign object with provenance and continuity. These principles are implemented in Has-Needs' independent protocol, with its own reciprocal-receipt *forest of chains*. See [V1 §5.1](./Has-Needs-Spec-v1.md).

## 2. Sovereign objects and personal Data Views

This owner-first model makes agency a technical property. A person contributes information or capability without becoming a record owned by an intermediary. Contextual identity and scoped disclosure allow people to participate as neighbors, workers, family members, or responders without collapsing their social facets into one institutional profile.


A participant owns and controls their own objects and may freely inspect them.

**The Persona Manager acts as a concierge, managing interactions through any number of user-created personas while their underlying personal chain remains sacrosanct.** Each individual's manager maintains their single private chain. No outward-facing persona has direct chain access. A professional persona may expose selected work descriptions to matching without revealing the owner's other personas.

Typical local views include:
- all of my Needs;
- all of my Has;
- all current Working relationships;
- receipt history and lineage;
- objects shared with a selected persona, family, project, or community.

Has-Needs prohibits privileged network-wide enumeration of other participants' sovereign objects, not self-inspection.

## 3. Discovery and matching

**Local-first communication is the native starting condition.** A person begins within their sphere of awareness and capability, exchanging authorized messages with participating peers within range. Wider services and institutions can extend that sphere through cooperation; no external network or central directory is needed to originate an interaction. In urgent situations, the credible opportunity to communicate before a response is a deliberate agency-supporting design objective, to be evaluated empirically.


**Has-Needs inverts the platform-first Internet experience.** Sovereign participants start within locally meaningful proximity communities, their own chosen relationships, and the Has/Need interactions occurring in those contexts. Semantic discovery is heavily weighted toward relevant community-held knowledge and previously successful local resolution paths, then expands outward as needed. This is not a geographic enclosure, a universal trust score, or a central inventory.

**Geographic relevance is the sphere of possibility, not the person's current location.** The Need for a refrigerator may initially cover a small pickup area and expand dramatically when a rental truck becomes available as another Has; neither the Need nor its owner has to move. Coarse-to-fine regional scopes, analogous to ZIP-code levels or multiresolution wavelet thinking, can be matched and updated through compact semantic deltas without disclosing precise whereabouts. No particular geographic index or transform is fixed in V1.


**Geographic reference is universal; actual location is sacrosanct and must be unretrievable through Has-Needs.** Every Has, Need, Working interaction, and applicable community or derived view carries a notion of geographic relevance through its semantic context: a service region, route, destination, remote/unbounded applicability, unknown geography, or protected reference. This does not imply that the participant's actual coordinates are available. Has-Needs provides no protocol retrieval operation for a person's actual location, and no durable shared object, receipt, journal, or routable address contains precise participant coordinates.

Ordinary geographic matching compares owner-declared areas of possibility, service regions, and feasibility contexts rather than private person-to-person coordinates. For rare cases that need secret exact-position computation, a transient position can be checked locally; homomorphic encryption (HE), secure multiparty computation (MPC), or private-set methods are replaceable research candidates for protected comparisons. Results must not form a retrievable location history or an unrestricted adaptive-probing oracle. HE alone cannot prevent location inference through repeated responses or communication metadata. Where secure matching is unavailable, the match is deferred or performed using intentionally disclosed broad applicability—not precise-location exposure.


Has and Need discover one another through scoped semantic matching rather than global inventory browsing.

A Has may remain latent and respond only when a compatible Need appears. A Need may remain directly matchable even while contributing to a family, community, agency, or regional aggregate.

Machines may rank and suggest. Humans remain the final arbiters of whether a proposed match is acceptable.

**Data exchange is reciprocal.** A vendor can express a Need for a chosen attribute; the owner may respond with only that fact, a proof predicate, a permitted stream, or no response. Equally, an individual can issue a Has of selected data or social reach and discover compatible vendor Needs. An audience-holder with 100,000 Instagram followers, for example, may negotiate compensation for a promotion or a narrow proof of reach without relinquishing the account or the rest of their identity. This replaces brokered profiles with direct, consented propositions; the vendor cannot enumerate the network or profile those who decline.

## 4. Working, pending journals, and final receipts

Mutual acceptance is also an intentional behavioral design: a participant knowingly commits, creating an incentive for diligence and truthful expectations. Authorized participants can inspect recorded Pending events and make their own judgments about commitments and progress. The Pending journal is not a fourth protocol state: it records accepted `WORKING` events and subsequent authorized progress until an agreed resolution earns a final receipt.


Mutual match acceptance places the associated Has and Need in `WORKING` together, unavailable to ordinary matching while the Need executes its own conditions. The Need's pending journal preserves accepted commitments and authorized progress, without adding a fourth relation state. Remaining quantities and allocations are optional Need subtype behavior.

When the Need's conditions are satisfied, each participant independently marks completion and may add optional commentary or metadata. Each contributor chooses what to leave plaintext or encrypted. Both can view the transaction's communications, the other's contributions and intended exposure before committing, but cannot edit or suppress the other's words. Each marks **Not ready** or **Ready to commit**; a changed record requires renewed readiness. Once both are ready on the same version, their Persona Managers simultaneously write identical canonical transaction receipts and compare receipt hashes. A valid receipt itself establishes completion, without another 'verified' label.

Agreed cancellation or partial fulfillment uses the same receipt structure while recording the actual outcome. Unresolved commitments remain in the Need's pending journal. Local chain pointers differ; the canonical receipt is identical. No deal/no-deal outcome bit, required global activity log, or fourth `SPENT` state is introduced.

The Need is a smart contract with standard templates and custom options. Its WORKING state connects all involved Has and Needs during execution, including authorized delegation and recorded handoffs. Agreed template expiry can release associated objects and record an on-chain outcome. Personal filters may reduce exposure to matches based on disclosed no-deal outcomes; ignored candidates remain outside that evidence.

Identical canonical entries support corroboration even with fully encrypted contents. Selected plaintext through Bob the woodworker's facet can describe a deck and accurate quote; Jim's facet can show prompt payment. Neither disclosure requires public access to a core chain. After completion, each participant independently starts random hops outward into ongoing background verification.

## 5. Live trust vetting without reputation

Trust evidence is presented for human interpretation, not converted into a synthetic measure of moral worth. **Vetting uses recorded events only.** Resolved, mutually held receipts support chain-hop relationship checks; authorized Pending records may reveal accepted yet unresolved commitments, without treating them as completed transactions or wrongdoing. Searches, rejected proposals, passive observation and inferred behavior are excluded. Visible relationship paths help participants recognize known peers, inspect uncertainty, and choose their own verification depth. These are intended conditions for confidence and informed caution, not guarantees of honest behavior.


Has-Needs does not store a numerical trust score.

When a participant wants more confidence in a potential interaction, the system
can perform a live chain-hop vetting process and show the evidence directly.

A first-order connection means the parties already share an in-chain interaction.
If the candidate is not grey-listed and is not excluded by the participant's
personal filters, that direct relationship is treated as trusted for ordinary use.

Otherwise the interface may check outward through receipt-linked relationships
and visibly show:
- current hop depth;
- nearest verified relationship distance;
- second- and third-order connections;
- receipt/chain consistency;
- grey-list status;
- personal-filter results.

**Eight hops is the canonical full verification depth in V1.** A participant or
contract may knowingly accept fewer hops, such as three, when that is sufficient
for the interaction.

The display helps the human understand the social/receipt topology. It does not
collapse that evidence into a stored reputation or trust number.

**Grey-listing:** Because receipt writes are automatic and simultaneous, the
corresponding receipt hashes should never differ. Any discrepancy is treated as
tampering and immediately grey-lists both participants until resolved. This
chain-level flag is a shared ontology category propagated peer-to-peer.
Verification compares receipt hashes; it does not judge whose account is true
or compare participant-local previous-chain pointers.

Missing copies, unresolved obligations, and incomplete journal synchronization
are distinct from an actual canonical receipt-hash discrepancy. The graph can
show disclosed event links and counterpart context; short history alone is not
misconduct. Selecting an event supports human inspection without a stored score.

## 6. Transparent Trust Kernel

The Trust Kernel is a small, inspectable, community-testable execution and validation
surface for security-sensitive protocol rules.

During an interaction, participants can identify the kernel version/fingerprint in use.
If the current interaction reveals that a local kernel is stale or invalid, that same
counterparty does not automatically become the updater. The node waits for the **next
random eligible peer** and may receive a replacement candidate from that peer.

The supplying peer is not trusted merely because it supplied the code. The candidate
must pass local transparent validation before activation.

This separates **detection** from **repair**, avoids a fixed update authority, and lets
community-tested kernel versions propagate organically through ordinary interactions.

## 7. Persona Manager and OCA

Persona separation reflects ordinary human social boundaries. Different relationships legitimately use different user-created personas; OCA governs selected authorized data disclosure without requiring wholesale exposure. The intended effects are dignity, safety, and control; they require real-world assessment.


A person MAY issue a **standing sovereign declaration**: no free access and no uninvited use of protected identity or personal artifacts. Under Has-Needs, uses require a positive owner-authorized contract; neither discovery nor possession creates an implicit license. The declaration and subsequent grant/denial evidence are independently verifiable. This establishes a binding protocol boundary and supports evidence or challenges outside it, without assuming every external jurisdiction automatically adopts the same legal rule.

The Persona Manager is the sovereign policy boundary controlling:
- active persona;
- identity exposure;
- location applicability and its independently protected actual position (not retrievable through protocol);
- ontology exposure;
- history and receipt disclosure;
- message filtering;
- capabilities granted to other participants.

OCA — Overlays Capture Architecture — supplies a stable *Capture Base* of field names and types, with cryptographically linked overlays for context, labels, formats, mappings and sensitivity. **OCA metadata describes attributes; it does not grant access to their values.** The Persona Manager and a separate capability gate enforce precisely what may be projected, including one attribute, a predicate, derived data or a live stream. See [DXOS/OCA Architectural Choices](./DXOS_OCA_ARCHITECTURE.md).

**DXOS ECHO is a replaceable local-first replication candidate.** Owner-private Spaces can retain sources, while selected shared Spaces may hold approved projections. Replication is not consent: copying readable data to a recipient cannot later be guaranteed reversible.

**Disclosure becomes a state transition:** a person may approve narrower or broader projections as needed. Entering Working does not itself unlock data.

**Layered provenance is separate from disclosure:** the OCA schema version, origin attestation, derivation, grant/revocation, Pending evidence and final receipt can be independently verified without exposing all the inputs.

**Sovereign provenance for human artifacts.** An owner may register protected identity, appearance, voice, creative work, and chosen personal artifacts, together with signed claims and permitted-use terms. An AI-derived likeness or inferred personality is a distinct derivative object whose lineage and permissions may be recorded without publishing the underlying personal inputs. These signed records provide portable evidence independently of any government registry; identity binding and legal remedies can be evaluated separately.

**Contract-specific, revocable API.** A vendor's Need can request a particular datum; the owner can grant a Has projection through an OCA-limited API whose exact permission, recipient, purpose, duration, and value terms are tied to an agreement. Revocation cuts off future controlled access to live data, though already copied material cannot be retracted.

## 8. Local ontology and resolution evidence

The ontology is not “the truth.” It is a scoped map of declared relationships and what has actually worked. **It begins undefined in a person's own dialect and sphere of influence.** Individuals and communities can introduce their own words, images, distinctions, substitutions and associations; other vocabularies are mapped by agreement rather than assumed universally equivalent. Human-curated labels and receipt-derived outcomes extend local meaning to consenting nearby peers and farther communities over time. Indigenous wisdom remains subject to its holders' authority, including knowledge they choose not to disclose.

Has-Needs distinguishes:
- semantic edges — meaning/category relationships;
- resolution edges — evidence that a pathway produced a completed outcome;
- safety/validation edges — later evidence, certification, testing, or warnings.

Old evidence may decay in ranking without being erased.

**AI is segmented and human-guided.** Bounded components may translate, interpret, suggest ontology labels, or search within disclosed semantic scopes. Human curation contributes local meanings; authorized final receipts contribute evidence of completed resolution. AI suggestions, rejected candidates, and inferred personality attributes never become authoritative ontology or stored trust evidence simply because a model generated them. The underlying protocol remains usable without AI.

**Composable institutional attestation remains an exchange.** A person completing education and a university awarding a degree have participated in a value exchange; the university can separately verify the degree from its own record to an authorized requester. A payment processor can likewise attest to a payment it processed. The Composable API enables narrow, permission-governed proof and data access without giving institutions ownership of the person's chain or inventing a distinct certification ledger.

## 9. Globe, RGB layers, and Data Stories

The primary rich interface is globe/map-based as a literacy- and language-agnostic spatial renderer. It presents allowed geographic applicability and owner-held information, never a protocol-wide view of people's actual coordinates. A map pin is not required for a valid Has/Need.

The globe is a **Data View**, not a global database window. What appears depends on the active persona, permissions, semantic scope, and OCA disclosure state.

Heterogeneous data can be rendered into RGB layers as a common visual composition surface. Users may combine layers with simple mathematical or logical operators.

A Data Story exists as soon as the relationship is expressed, for example:

`rainfall_24h + (dew_point_today × cassava_crop)`

A story may remain transient, be saved, become an input to another story, be shared, or be offered as a `HAS` in a value exchange. A Data Story may also be a bounded live stream whose derived output is shared without exposing its raw inputs.

## 10. Communities and sub-communities

**Consented emergency coordination:** Citizens may share live situational information under accepted service Needs whose conditions define authorized recipients, purpose and duration. A responding agency can forward the same Need to an authorized emergency manager or operational sub-community without taking custody of a citizen's private chain. Each party keeps a matching canonical receipt upon completion; the agency's coordinated view includes only participating authorized disclosures.

Proximity communities are the initial, heavily weighted environments for discovery, interaction, and ongoing locally grounded ontology growth. They represent real human and geographic contexts, not automatically inferred or centrally owned social graphs. Participants can expand matching outward when their sphere of possibility, circumstances, urgency, or preference warrants it.


Repeated sovereign exchanges may establish reciprocal evidence, meaningful relationships, and eventually voluntary collective spaces without a platform owning the social graph. Has and Need are symmetrical: people who need help may also hold knowledge or skills others value. Communities therefore offer a path from aid recipient to contributor without assigning permanent social roles.


**Foundational tenet — sovereignty enables chosen interdependence.** Participants retain authority over their own identities, information, and contributions. Communities may exercise their own collective governance and cultural authority; the protocol respects rather than supplants it. Sovereign people can cooperate and organize through mutual consent and bounded delegation. Cooperation is a choice, not a condition of submission. This is the same sovereignty-first principle that underlies Has-Needs' trauma-informed design.

A community is a voluntary, purpose-scoped coordination space. It does not own its participants.

Communities may hold permissioned projections of Has/Need objects, shared ontology, conversations, project state, and derived views.

A community Need is an ongoing contract context; constituent bindings resolve
without closing the community. Subcommunities keep separate execution scopes,
journals, permissions, and conversations. Sharing with a parent is explicit.

Sharing a Has or Need grants visibility. Pooling entrusts fulfillment within
accepted delegation terms. Clustering coordinates logistics while retaining
required individual approval. Joining a community alone does not delegate resources.

Sovereign entities can prove uniqueness without giving up identity. As such, you are able to enter collective spaces by mutual consent, without external ‘services’ like Facebook or Bluesky being involved. Has-Needs operationalizes it with a needs matching system that adapts to all interaction types.

This expresses the architectural objective; uniqueness mechanisms require the
risk-specific security validation described in the specification.

## 11. Jitterbug and semantic Friend nodes

Jitterbug is the transport/routing research direction for low-cost, resilient, local-first communication. It privileges authorized nearby community resolution paths and semantic context before wider propagation, without treating physical person-addresses as routing destinations; the locality bias is strong but overridable.

A semantic Friend node may cache ontology, store/carry/forward opaque messages, provide rendezvous or replication, and learn useful routing paths without owning the underlying content.

The owner or expressly authorized endpoint remains the authority for each
interaction. Storage alone grants none. “I Need a friendly node” uses an ongoing
community relationship defining storage, relay, and any bounded delegation.
Members can share infrastructure provision under agreed capacity and redundancy
terms. Journal retention, large-content storage, and owner/delegate handoff remain
explicit implementation questions.

Jitterbug explores a minimal network/semantic rind around protected payloads, with routing intelligence and encoding adapted to each available transport.

## 12. Graceful degradation

Continuity of useful action under failure is also a trauma-informed choice: participation remains possible without one institution, cloud provider, rich interface, or communications channel becoming the condition for agency.


Has-Needs is designed to collapse downward rather than fail outright:

rich UI + AI + cloud + mesh  
→ local nodes + cached ontology  
→ direct peer-to-peer  
→ SMS / radio / terminal  
→ human relay  
→ “Who has this?” / “Who needs this?”

The technology enhances a human coordination behavior; it does not create the behavior.


## 13. Designed prosocial emergence

Protected geographic relevance has a human purpose: disaster survivors, displaced people, and vulnerable participants can discover nearby help without being obliged to provide their actual whereabouts to an institution, vendor, relay, or counterpart. This is an engineered boundary rather than an optional location-privacy preference.


Has-Needs intentionally arranges ordinary interaction to make sovereignty, reciprocity, diligence, informed trust, belonging, and collective efficacy easier to enact. This is not covert persuasion, behavioral surveillance, a universal reputation score, or compulsory prosocial performance. The mechanisms and their intended effects are explicit:

| Mechanism | Intended emergent effect |
|---|---|
| Sovereign identity, Persona Manager, OCA | Personal boundaries, dignity, voluntary engagement |
| Symmetric Has and Need | Reciprocal contribution rather than dependency |
| Working acceptance and pending evidence | Responsibility, diligence, visible promises |
| Identical final receipts and local ontology | Evidence of what actually worked; locally preserved knowledge |
| Live chain-hop vetting without scoring | Informed trust and human discretion |
| Voluntary community formation | Connection, mutual aid, collective efficacy |
| Governance commitments and authorized workflow visibility | Responsiveness and legible operational bottlenecks |
| Graceful degradation | Continuity of participation in crisis |
| Geographic applicability without actual-location retrieval | Local cooperation and safety without disclosing a vulnerable participant's whereabouts |
| Local-community-first discovery and expanding possibility | Useful nearby cooperation before wider reach; mobility and resource access can widen the opportunity landscape |

Successful interactions can satisfy Needs and generate the conditions for future relationships, community formation, and collaborative action. These are intentionally designed possibilities, **not automatically proven outcomes**. See [Specification V1 §4.1](./Has-Needs-Spec-v1.md) and its participatory evaluation section for the hypothesis/evidence distinction, potential harms, and proposed evaluation.

## Community arrival and reciprocal recognition

A community may publish a QR onboarding point exposing permitted local resources, service Needs, and participation opportunities. Local ontology mappings can relate a newcomer's terms for skills and everyday contributions to locally understood descriptions, without automatically certifying qualifications or authorizing regulated work. A newcomer may discover shelter and food, offer practical skills or companionship, or simply observe the availability of support through the Personal Globe; emergency assistance must not depend on providing something in return. In the opening rescue scenario, **the person's firsthand location and condition are a Has the rescuers need**, just as rescue capacity is a Has the person needs. This reciprocal information/service relationship is a foundational example of the exchange model. Cooperative encounters can produce authorized evidence and may foster mutual recognition across groups; reduced prejudice and improved well-being are testable intended effects, not automatic results. QR access should have accessible non-smartphone alternatives, and geography/identity disclosures remain scoped.

## Owner-authorized information and portable evidence

The individual is the starting authority for personal information use. A contract or permission token documents authorized recipient, data projection, purpose, scope, duration, and agreed value. A data use without a valid applicable token is unauthorized under the Has-Needs protocol; applicable law separately determines remedies and exceptions. Composable APIs expose only agreed projections, while institutions attest facts within their own competence without gaining access to the person's private receipt chain. Identical canonical receipts and selective attestation proofs give people portable, independently verifiable evidence of participation across institutions and borders. Signature verification does not require sophisticated local legal infrastructure, though evidence weight, credential recognition, and legal admissibility vary by jurisdiction.

## Asynchronous parallel fulfillment and participatory research

Aid and services are often delivered in scheduled batches even when people's Needs arise at different times. Has-Needs starts with each person's actionable Need; matching, acceptance, Working journals, and resolution progress independently as capabilities become available. Multiple people and multiple recovery or everyday-life pathways can proceed in parallel. This coordination mechanism cannot create absent supplies, but does not require participants to wait for unrelated distribution cycles. Communities may publish research questions as Needs and researchers may publish standing Needs for observations, participants, and collaborators; consent, study quality, and community-defined benefit remain explicit.

## Institutional composability and crypto agility

Owner-controlled, purpose-scoped APIs allow qualified institutions to contribute attestations (such as payments, training, or aid delivery) without obtaining the entire personal history. Revocation stops future authorized access, not past disclosure. The value grammar accommodates gifts, monetary commerce, pooling, and post-capitalist arrangements. Replaceable cryptographic algorithms provide a design path for post-quantum migration, subject to versioning, key management, and historical-record verification.

## Sovereign commerce: standing Needs, open-ended assets, and professional facets

### Sovereign commerce and professional provenance

The same HAS/NEED/WORKING grammar enables commerce without a fixed catalog of what counts as value. A sovereign participant can offer goods, skill, time, expertise, an attested social-media audience threshold, or intangible contributions on chosen terms. A business can publish a **standing Need** describing whom or what it seeks; eligible participants' Persona Managers evaluate it privately and offer the opportunity to their owners. **The business sees only responses that participants authorize**, not a list of everyone who matched. As new people join or become eligible, the Need can continue to create opportunities.

Creators and tradespeople can expose a limited **professional facet**: verified training or apprenticeship, selected reciprocal exchange receipts, repeat engagements, project types, and cadence of work. A customer may search these authorized patterns to reach their own comfort threshold without relying on a universal reputation score. A return visit may mean maintenance, a new phase, a repeat satisfied client, or rework; a receipt authenticates an agreed record, not independent quality or completeness. The worker chooses what to disclose, and counterparties' confidentiality remains protected. These capabilities emerge from sovereign Hases and Needs, Persona Manager facets, voluntary WORKING commitments, Need-owned journals, and independently held reciprocal receipts—not a central customer database or public personal ledger.

A creator may disclose a platform-attested threshold such as 200,000 followers as one granular Has, without transferring the identities or rights of followers. A social-platform metric needs a credible issuer and freshness conditions; merely recording a claim on a personal chain does not verify it. Persistent Needs can be presented through composable applications as new people qualify, while preventing vendors from enumerating private matches. Communities can pool demand voluntarily, and noncommercial or culturally restricted Hases remain governed by their owners and communities. Privacy protections must consider repeated-query inference, contact probing, client confidentiality, and selective-disclosure bias. The potential reductions in unwanted solicitation, extractive intermediation, and perceived disempowerment are research hypotheses, not measured outcomes.

## Composable streams and the self-pruning tree

An entity can provide controlled data through a composable API under its Need's permissions. A Community formed by an open-ended, one-to-many Need can stream its communications to secure storage, choosing responsible parties while preserving contributor permissions. The same WORKING state supports a driver accepting a package, the sender recording the handoff, and a delegated Community representative receiving pooled items. Individual deliveries still require the recipient or their delegate.

Organizational delegation can follow the hierarchy to the worker who fulfills a Need. The completed exchange makes that endpoint prominent in local resolution evidence, helping later requests take the recent effective route while retaining hierarchy for fallback. This is the self-pruning tree. Records of responsibility and fulfillment also support civic budget reconciliation; the public-funding disclosure policy remains open. See [the WORKING state, delegation, and streams](./WORKING_CONTRACTS_AND_DELEGATION.md).
