**HAS-NEEDS**

**Specification V1**

*A sovereign protocol with network-level non-enumerability for discovering and preserving
successful state transitions*

**VERSION 1 WORKING DRAFT FOR EXPERT REVIEW**

October 2026

**Core proposition**

**Has-Needs is not a system for describing resources.  
It is a system for discovering and preserving successful state
transitions.**

# Document status

This document is a protocol and architecture working draft, not a claim
of production security or standards compliance. Its purpose is to freeze
enough of the Has-Needs grammar to support implementation, tabletop
testing, adversarial review, and expert criticism without prematurely
locking the system to any particular blockchain, database, network
transport, cryptographic library, or application framework.

**Version authority.** This V1 document is the canonical architectural specification for Has-Needs. Older project documents may preserve historical exploration, but where they conflict with V1, V1 governs unless a later version explicitly supersedes it.

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Design discipline<br />
</strong>The specification distinguishes three things: (1) architectural
invariants that should survive implementation changes; (2) protocol
requirements that a conforming implementation must satisfy; and (3)
candidate implementation techniques that are intentionally
replaceable.</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

## Reader map

| **Part**   | **Purpose**                                         | **Primary audience**                                           |
|------------|-----------------------------------------------------|----------------------------------------------------------------|
| Part I     | Plain-language introduction and disaster origin     | Humanitarian practitioners, funders, general technical readers |
| Part II    | Normative architectural invariants                  | Architects, reviewers, standards readers                       |
| Part III   | Core object and transaction model                   | Distributed-systems engineers, protocol implementers           |
| Part IV    | Ontology, matching, discovery and non-enumerability | Semantic systems, information architecture, privacy            |
| Part V     | Persona Manager, OCA and cryptographic boundaries   | Security/privacy reviewers                                     |
| Part VI    | Transport, Jitterbug and semantic Friend nodes      | Networking and constrained-device engineers                    |
| Part VII   | Communities, communication and project coordination | Product, UX, collaboration systems                             |
| Part VIII  | Security, recovery and graceful degradation         | Adversarial reviewers                                          |
| Part IX    | Reference prototype profile and test plan           | Builders and evaluators                                        |
| Appendices | Schemas, flows, glossary and references             | Implementation and citation support                            |

## Normative vocabulary

The capitalized words MUST, MUST NOT, SHOULD, SHOULD NOT, and MAY are
used in the conventional standards sense described by BCP 14 (RFC 2119
and RFC 8174). In this working draft they express design intent rather
than IETF status.

# Part I - Introduction

## 1. Disaster is the baseline

Has-Needs began as a trauma-mitigation architecture: a way for people
affected by disaster to retain agency by capturing, controlling, and
acting on the local knowledge already present around them. At the moment
of greatest collective incapacity, local detail becomes exceptionally
valuable. Responders may have funding, equipment, staff, maps, and
authority while lacking current ground truth: which road is passable,
who has moved, which well is usable, what clinic is operating, who has a
generator, where medicine needs refrigeration, or what workaround is
already succeeding.

The core insight is that much of this information does not need to be
collected first into an institutional database and acted upon later.
People already possess it. Many also possess communications devices. The
missing layer is a direct, consent-based mechanism by which those people
can become first-class participants in the response system without
surrendering identity, location, history, or control of the information
they contribute.

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Foundational aim<br />
</strong>Trauma mitigation through the empowering capture of local
knowledge.</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

## 2. The smallest human grammar

Has-Needs begins with a minimal semantic triplet: `[entity, relation, context]`.
The `relation` field has exactly three protocol states: `HAS`, `NEED`, or
`WORKING`. A person or other sovereign participant can say, in effect,
“I need this” or “I have this.” A Need specifies a desired outcome and may
seed the ontology by stating what would count as an acceptable match. A Has
states an available capability or resource. When one or more Has and Need
objects are mutually accepted into an exchange, their relation becomes
`WORKING` for the duration of that binding. The system proposes possible
overlaps; humans make the final choice.

I NEED THIS.  
I HAVE THIS.  
WE AGREE.  
WE EXCHANGE.  
WE REMEMBER WHAT WORKED.

## 3. Plain-language trust model

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Plain-language trust model<br />
</strong>Modern cryptography keeps each person provably unique without
exposing who they are.<br />
<br />
A special routing protocol makes sure each message reaches the people
and places where it can be useful.<br />
<br />
When an exchange of value is completed, each participant receives an
identical receipt of what occurred.<br />
<br />
All of this happens inside a secure wrapper whose protected personal and
semantic data is not disclosed without explicit permission.</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

The phrase “provably unique” is a protocol requirement, not a claim that
this working draft has selected the final cryptographic construction.
The architecture must permit a participant to establish sufficient
uniqueness and continuity for the relevant interaction without requiring
global civil-identity exposure.

## 4. From recovery to sustainability

Has-Needs operationalizes widely supported practices in trauma-informed
recovery: agency, connectedness, self- and community efficacy,
meaningful participation, use of local knowledge, and respect for
dignity. These qualities do not stop being useful when the emergency
ends. The same grammar can continue through recovery into resilience,
sustainability, governance, research, commerce, finance, mutual aid,
agriculture, logistics, and ordinary project work without changing the
fundamental relationship to the individual.

The transition is therefore not “disaster application to normal
application.” It is one coordination grammar operating under different
conditions.

# Part II - Architectural invariants

The following invariants are the core of Has-Needs. A proposed
implementation that violates them may still be useful software, but it
is no longer the protocol described here.

**1. Person-first sovereignty.** The unique being is primary and exists
outside communities by default. Communities, agencies, vendors,
researchers, and governments interact with the person; they do not
become the root owner of that person’s identity or history.

**2. Canonical triplet, three relation states.** Every protocol object has a
human- and machine-readable semantic form `[entity, relation, context]`,
where `relation` is one of `HAS`, `NEED`, or `WORKING`. Has and Need remain
independently addressable sovereign objects; the triplet does not imply a
central table, shared database, or globally enumerable registry.

**3. No central authoritative inventory.** The protocol has no required
central database of Has or Need objects. Objects may live on participant
devices and chosen replicas and may move or be cached across many
transports.

**4. Network non-enumerability with sovereign self-inspection.** A participant MUST be able to inspect and enumerate the Has, Need, Working, receipt, ontology, and related objects it owns, and MAY inspect objects legitimately disclosed to it within an authorized scope. There is no ordinary protocol operation equivalent to “show me every Need owned by everyone” across other sovereign participants or across the network as a privileged global view. Discovery across sovereign boundaries is reciprocal semantic matching, not database browsing.

**5. Availability is default.** A Has or Need participates in matching
unless it is bound into Working or otherwise withdrawn by its
owner/policy. “Floating” is descriptive, not a required state field.

**6. Working is the third relation state and an active binding.** `WORKING`
means the relevant Has and Need objects have been mutually accepted into an
active agreement. Their relation changes to `WORKING`, removing the objects,
or committed portions of them, from ordinary matching for the duration of
the agreement.

**7. Completion crosses into provenance.** There is no required “Spent”
state. Completion terminates the relevant active object lineage into
durable receipt evidence. Reusable capabilities may return to
availability; remainders become new Has objects.

**8. Only completed value exchange earns default durability.**
Exploration, observation, failed matches, browsing, and behavioral
exhaust do not automatically become permanent shared records.
Participants may retain local history, but the protocol’s default
durable artifact is completed exchange.

**9. No reputation primitive.** The system does not produce kudos,
stars, global trust scores, or social rank. It may use recent contextual
evidence that a resolution path worked under comparable conditions.

**10. Human judgment remains decisive.** Matching, AI, ontology and
routing may suggest. Human participants retain final authority over
interpersonal acceptance.

**11. Ontology is local and evidentiary.** The ontology is not “the
truth.” It is a scoped map of declared relationships and, more
importantly, what has worked. It can be private, shared selectively, and
re-ranked by recent outcomes.

**12. Disclosure is a state transition.** The Persona Manager and OCA
may reveal more or less of an object as a relationship changes. Privacy
is not a one-time access checkbox.

**13. Aggregation does not become ownership.** Higher-level actors may
receive permissioned aggregate views without absorbing the underlying
sovereign objects into an authoritative institutional inventory.

**14. Higher layers never cancel the base layer.** A Need can remain
eligible for direct person-to-person resolution even while it
contributes to a family, community, agency, or regional aggregate,
subject to the owner’s policy.

**15. Transport is replaceable.** Bluetooth, IP, WebRTC, SMS, radio,
satellite, serial, human relay, or future transports are convergence
layers. None defines Has-Needs semantics.

**16. Graceful degradation.** Loss of cloud, AI, ontology, rich UI, high
bandwidth, or a particular node should reduce sophistication rather than
invalidate the underlying Has/Need behavior.

# Part III - Core protocol model

## 5. Objects are sovereign claims, not database rows

A Has or Need object is a portable signed semantic proposition whose
authoritative meaning is controlled by its issuer and cryptographic
lineage, not by the server on which a copy happens to reside. A device,
cloud service, semantic Friend node, DXOS replica, or community service
may store or relay a copy. None becomes authoritative merely by storing
it.

participant A participant B  
\| \|  
NEED N31 \<--- semantic ---\> HAS H82  
\| \|  
+------ optional relays -+  
  
No global Needs table is required.

## 6. Identifier families

The protocol requires identifiers that remain distinct in purpose.
Implementations MAY encode them using one common binary format, but
SHOULD preserve domain separation so that an object ID cannot be
confused with a receipt ID or persona reference.

| **Identifier**                 | **Purpose**                                                                                                                                  |
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Persona / continuity reference | Identifies a cryptographic participation context without requiring public civil identity. SHOULD permit unlinkability where policy requires. |
| Has ID                         | Durably identifies one Has lineage object.                                                                                                   |
| Need ID                        | Durably identifies one Need lineage object / smart-contract-like request.                                                                    |
| Working ID                     | Identifies one accepted binding among one or more Has and Need objects.                                                                      |
| Receipt ID                     | Identifies the canonical immutable completion record.                                                                                        |
| Ontology namespace             | Names the semantic vocabulary in which a token is meaningful.                                                                                |
| Ontology token                 | Compact local or shared semantic reference, potentially opaque outside its namespace.                                                        |
| Community / sub-community ID   | Names an optional purpose-scoped coordination space.                                                                                         |
| Chain-entry ID                 | Identifies a participant-local append-only entry that points to a canonical receipt hash.                                                    |

## 7. Need object

A Need is an addressable smart-contract-like object that expresses a
desired outcome and may include the creator’s provisional definition of
satisfactory resolution. Creating a Need therefore seeds ontology: the
issuer is declaring what they currently believe may count as a match.

| **Field**    | **Level**   | **Meaning**                                                                                                    |
|--------------|-------------|----------------------------------------------------------------------------------------------------------------|
| need_id      | REQUIRED    | Unique object identifier.                                                                                      |
| issuer_ref   | REQUIRED    | Persona/capability reference sufficient to authenticate the object without forcing public identity disclosure. |
| ontology_ns  | REQUIRED    | Namespace in which the semantic token is interpreted.                                                          |
| token        | REQUIRED    | Primary semantic reference for matching/routing.                                                               |
| satisfaction | RECOMMENDED | Acceptable matches, exclusions, thresholds, substitutions, desired state, or other resolution metadata.        |
| scope        | RECOMMENDED | Time, proximity, social, community, jurisdictional, or other discovery boundary.                               |
| contract     | OPTIONAL    | Value terms, deadlines, escalation, obligations, dependencies, validation requirements.                        |
| oca_ref      | RECOMMENDED | Reference to disclosure overlays/capabilities controlled by Persona Manager.                                   |
| auth         | REQUIRED    | Integrity/authenticity material or reference.                                                                  |
| expiry       | OPTIONAL    | Time or condition after which the object no longer participates.                                               |

## 8. Has object

A Has is an independently addressable capability or resource object. It
may describe physical goods, skills, time, tools, vehicles, information,
attention, money/value, access, social reach, authority, computing
resources, or any other capability that can contribute to satisfying a
Need.

| **Field**   | **Level**   | **Meaning**                                                                           |
|-------------|-------------|---------------------------------------------------------------------------------------|
| has_id      | REQUIRED    | Unique object identifier.                                                             |
| issuer_ref  | REQUIRED    | Authenticating persona/capability reference.                                          |
| ontology_ns | REQUIRED    | Namespace for the semantic token.                                                     |
| token       | REQUIRED    | Primary capability/resource semantic reference.                                       |
| capability  | RECOMMENDED | Quantity, divisibility, renewability, scheduling, substitution, quality, constraints. |
| scope       | RECOMMENDED | Where/when/with whom the Has may respond.                                             |
| oca_ref     | RECOMMENDED | Disclosure overlays/capabilities.                                                     |
| auth        | REQUIRED    | Integrity/authenticity material or reference.                                         |

## 9. Working relation and binding

`WORKING` is the third allowed state of the triplet's `relation` field. It
represents an accepted relationship among independently addressable Has and
Need objects. When the parties accept the match, the participating objects
transition from `HAS` or `NEED` to `WORKING`; the committed objects or
portions cease ordinary matching for the duration of that contract. Working
is therefore both a semantic relation state and the protocol binding that
expresses an active exchange.

| **Field**          | **Meaning**                                                       |
|--------------------|-------------------------------------------------------------------|
| working_id         | Unique relationship identifier.                                   |
| need_refs          | One or more Need IDs.                                             |
| has_refs           | One or more Has IDs.                                              |
| terms_hash / terms | Agreed terms or canonical reference.                              |
| participants       | Capabilities required to authorize transitions.                   |
| disclosure_state   | OCA state/capabilities currently granted.                         |
| timeout / release  | Conditions returning unconsumed/reusable objects to availability. |
| auth               | Mutual or required attestations establishing the binding.         |

## 10. Completion and the canonical receipt

Completion is the transition from live coordination to durable
provenance. The canonical receipt represents what the parties agree
actually occurred. Each participant receives the same canonical receipt
bytes or a byte-equivalent canonical encoding. The receipt itself MUST
NOT contain participant-local previous-chain pointers because those
pointers differ by personal history.

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Important receipt/chain distinction<br />
</strong>The receipt can be identical for every participant while each
participant’s append-only chain remains different. Each personal chain
appends a small local chain entry containing the same receipt hash plus
that participant’s own previous-entry pointer.</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

Canonical Receipt R92  
working_id: W44  
needs: \[N31\]  
has: \[H82\]  
exchanged_value: ...  
completion_attestations: A, B  
resulting_lineage: \[H83\]  
conversation_commitment: optional  
receipt_hash: HASH(R92)  
  
Participant A chain entry:  
prev: A_prev  
receipt_hash: HASH(R92)  
  
Participant B chain entry:  
prev: B_prev  
receipt_hash: HASH(R92)

## 11. Value exchange and default durability

Has-Needs deliberately avoids normalizing extraction. A protocol
participant may locally retain transient information according to their
own policy, but the shared durable record created by the protocol is
centered on completed value exchange. The protocol SHOULD NOT require
durable shared storage of every observation, failed match, search,
proximity event, or inferred behavior merely because it was technically
observable.

This has both privacy and psychosocial consequences: the permanent
shared record is closer to “what we accomplished together” than
“everything the system learned about you.”

## 12. Object lineage and conservation

Partially consumed Has objects SHOULD terminate into the completed
transaction rather than being silently edited downward. Any remainder
becomes a new Has with a new ID and explicit lineage to the completed
receipt. This yields auditable conservation without requiring mutable
global balances.

H1 = 100 L potable water  
N1 consumes 30 L  
  
H1 + N1 -\> WORKING -\> COMPLETE  
R1 records 30 L exchanged  
H1 terminates into provenance  
H2 = 70 L  
H2.parent = H1  
H2.originating_receipt = R1

## 13. Primitive transaction geometries

| **Geometry** | **Shape**               | **Example**                                                      |
|--------------|-------------------------|------------------------------------------------------------------|
| Pair         | 1 Has -\> 1 Need        | Simple exchange                                                  |
| Split        | 1 Has -\> many Needs    | A truckload or grant distributed among several recipients        |
| Aggregate    | many Has -\> 1 Need     | A house repair satisfied by labor + material + transport + funds |
| Pool         | many Has -\> many Needs | Coordinated distribution, mutual aid, pooled provisioning        |

These are relationship geometries, not new primitives. A core design
test is that increasingly complex coordination should be expressible by
composing Has, Need, Working, receipt, and optional community context
rather than inventing special-purpose object classes.

# Part IV - Ontology, matching, discovery and non-enumerability

## 14. Ontology: what has worked, not “the truth”

A Has-Needs ontology may contain declarative semantic relationships, but
its distinctive evidence comes from completed exchanges. A Need says
what the issuer thinks may satisfy it. A Has says what the issuer thinks
it can provide. A match proposes overlap. Human acceptance says the
overlap is worth attempting. Completion supplies stronger evidence that
the relationship was useful in that context.

DECLARED EXPECTATION  
-\> candidate match  
-\> human acceptance  
-\> attempted exchange  
-\> completed exchange  
-\> durable contextual evidence

## 15. Semantic edges and resolution edges

The protocol SHOULD distinguish semantic relationships from resolution
evidence. “Bottled water is a kind of potable water” is not the same
assertion as “this local supplier recently satisfied this kind of water
Need.” Conflating them would turn an ontology into a hidden ranking
system.

| **Edge type**          | **Question answered**                                             | **Evidence**                                               |
|------------------------|-------------------------------------------------------------------|------------------------------------------------------------|
| Semantic edge          | Meaning/category relationship                                     | Declared, imported, translated, mapped, expert asserted    |
| Resolution edge        | This pathway produced a completed outcome in context              | Receipt-derived; weighted locally by recency/context       |
| Safety/validation edge | Additional quality, certification, measurement, or later evidence | May arrive long after completion; does not rewrite history |

## 16. Local ranking without reputation

Each participant may maintain a single continuously re-ranked list of
likely resolution paths for a semantic class. This is not a reputation
score. It answers a narrower question: “For this sort of Need, under
circumstances like these, which path has worked recently for me or for
sources I have chosen to trust?”

A declarative preference may begin high in the list and remain high if
it produces successful matches. Completion and recency may move a
previously secondary path to the top. Old evidence may decay without
being erased. A worker who begins passing cases to another worker
naturally ceases to be the default if the second person becomes the one
actually completing them.

## 17. Self-pruning and novelty

The system is deliberately permitted to begin undefined. Human intellect
supplies the last step in matching; the ontology assists rather than
governs. If a “community tool space” repeatedly resolves a Need that was
initially expected to be satisfied by a “bike mechanic,” that successful
resolution may become locally useful even though it was not anticipated
by the original category. The goal is the result, not preservation of
the initial taxonomy.

## 18. Personal and shared ontology scopes

Ontology itself is a sovereign resource. A person might privately keep
the vendors they actually transact with after comparing many
alternatives, share that edge set only with family, expose another
portion to peers, and publish nothing globally. A government may publish
an asserted service ontology; individuals may accept it provisionally
while receipt-derived evidence gradually shows which services actually
resolve Needs.

## 19. Network non-enumerability: there is no global “shopping list view”

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Hard privacy invariant<br />
</strong>No participant, including an emergency manager, should be able
to issue a generic protocol query equivalent to “show me every Need owned by everyone”
merely because they hold a privileged role. A sovereign participant may freely inspect
and enumerate their own objects and any objects legitimately disclosed to them. Discovery
across sovereign boundaries begins by expressing a semantic proposition of one’s own.</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

This is a structural difference from centralized case-management and
resource databases. A Need is not published into an inspectable global
table. It floats within the owner’s chosen discovery scope. A Has may
also remain latent, responding only when an appropriate Need passes
nearby. Matching across sovereign boundaries is the encounter of independent objects, not browsing
a global inventory.

Local enumeration is explicitly permitted and useful. A Persona Manager may provide views such as “all my Needs,” “all my Has,” “everything I currently have in Working,” “my receipt history,” or “objects this community has explicitly shared with me.” These are owner- or permission-scoped Data Views, not protocol-wide discovery APIs. Early prototype methods such as `getAllNeeds()` are therefore not inherently contrary to V1 when their scope is local; conforming implementations SHOULD make that scope explicit in naming, authorization, and data boundaries.

## 20. Emergency manager example: fire status

An emergency manager who wants citizen ground truth does not request
“all citizen Needs” or silently observe the population. The manager
creates a scoped Need such as FIRE STATUS. A citizen may possess a
compatible Has such as FIRE REPORT and voluntarily elect to respond.
That exchange may occur pseudonymously, at coarse location resolution,
or with progressively greater disclosure if the citizen chooses.

Emergency manager:  
NEED token=FIRE_STATUS  
scope=county / 2h  
requested fields=severity, approximate location, direction  
  
Citizen:  
HAS token=FIRE_REPORT  
disclosure state=coarse location only  
  
MATCH? -\> citizen chooses -\> report exchanged -\> receipt/aggregation
policy applies

If responders need better spatial organization, they can request more
precise location as part of a transparent value proposition: for
example, “allow this level of location precision so we can organize a
delivery or evacuation route.” The data is volunteered for a stated
purpose rather than extracted simply because it exists.

## 21. Aggregation is a derived view

A set of sovereign Needs can contribute to an aggregate without being
captured by it. An aid organization may learn that approximately 214
food Needs exist in a region, while the individual Needs remain
independently matchable through direct, family, community, commercial,
or other pathways. Aggregation SHOULD be permissioned, scoped, and
revocable where feasible; it MUST NOT silently convert a derived view
into ownership of the underlying objects.

N1 --\\  
N2 ----\\  
N3 ------\> permissioned aggregate -\> aid provider view  
N4 ----//  
N5 --//  
  
Meanwhile:  
N1 -\> direct local Has  
N3 -\> family Has  
N4 -\> shop Has  
  
Higher-level coordination adds paths; it does not cancel lower-level
matching.

# Part V - Persona Manager, OCA and privacy boundaries

## 22. Persona Manager

The Persona Manager mediates outward projection from the sovereign
participant. It is responsible for deciding which participation context
is active and what any relationship may learn. It SHOULD be able to
control identifier exposure, ontology exposure, location precision,
forwarding scope, relationship visibility, history disclosure, receipt
disclosure, and OCA capability grants.

## 23. Provably unique without exposed identity

The protocol requires a method by which a participant can demonstrate
sufficient uniqueness or continuity for the risk of the interaction
without making a global civil identity universally visible. “Provably
unique” is therefore contextual. A low-risk exchange may require little
more than continuity of a pseudonymous cryptographic persona; a
regulated or safety-critical interaction may require additional
attestation. The mechanism is intentionally not frozen in V1.

## 24. OCA: Overlays Capture Architecture

OCA treats disclosure as layered expression rather than a single
encrypted/not-encrypted switch. The same underlying object may expose
different semantic surfaces to different relationships. A capability
grant can reveal an additional overlay without replacing the base
object.

| **Relationship state** | **Illustrative disclosure**                                                |
|------------------------|----------------------------------------------------------------------------|
| Public/local mesh      | Anonymous semantic class, coarse scope, lifetime                           |
| Plausible match        | Additional quantity/constraints or compatibility detail                    |
| Accepted match         | Rendezvous/contact/contract detail as explicitly permitted                 |
| Working                | Operational details necessary to perform the exchange                      |
| Completion             | Receipt evidence and only the durable fields authorized by contract/policy |

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Core principle<br />
</strong>Disclosure becomes a state transition.</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

## 25. The secure wrapper requirement

Protected personal and semantic content MUST NOT become readable merely
because a relay, cache, community host, cloud service, or routing node
carries the object. The architecture intends explicit permission to be
the normal path to semantic disclosure. However, experts should
distinguish protected content from unavoidable side channels: transport
timing, radio proximity, packet size, and connection metadata can leak
information unless separately mitigated. V1 therefore treats metadata
minimization and unlinkability as security work, not as already-solved
guarantees.

## 26. Loss, recovery and continuity

Permanent loss of one device or key should not imply permanent loss of
personhood. Because completed exchanges create corresponding evidence in
other participants’ records, a person may rebuild sufficient continuity
from backups, counterpart receipts, trusted attestations, and surviving
chain fragments. The reconstructed history may be incomplete;
completeness is not required for new participation.

new key/persona  
-\> local backup fragments  
-\> counterpart receipt proofs  
-\> trusted continuity attestations  
-\> sufficient reconstructed history  
-\> new interactions

# Part VI - Transport and semantic routing

## 27. The transport is a semantic fabric, not one network

Has-Needs should not select one transport. It defines a small semantic
object and permits transport adapters to encode only what a particular
medium requires. The same object may move through Bluetooth, Wi-Fi, IP,
WebRTC, SMS, packet radio, satellite, serial, delay-tolerant links,
shared terminals, feature phones, or human intermediaries.

## 28. Fast plane and slow plane

| **Plane**  | **Purpose**                           | **Typical content**                                                                                       |
|------------|---------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Fast plane | Tiny live coordination signals        | New Has/Need, match offer, acceptance, Working, release, completion, urgency, expiry                      |
| Slow plane | Eventual convergence and richer state | Ontology deltas, receipts, chain validation, key changes, revocation, community history, ranking evidence |

A scarce radio link SHOULD prioritize live human coordination over
background maintenance. Random validation and ontology synchronization
can wait for bandwidth; an urgent Need may not.

## 29. Semantic datagram

The wire representation is not yet frozen. A minimal semantic datagram
is expected to contain some subset of the following, with
transport-specific omission or compression when context makes a field
implicit.

| **Field**               | **Role**                                                 |
|-------------------------|----------------------------------------------------------|
| version                 | Protocol/encoding version                                |
| object fingerprint      | Duplicate suppression and object reference               |
| kind                    | Has / Need / selected control signal                     |
| ontology namespace      | Context in which token has meaning                       |
| semantic token          | Compact routing/matching reference                       |
| scope / lifetime        | Where/how long it may propagate                          |
| priority / urgency      | Forwarding relevance where allowed                       |
| disclosure state        | Current OCA surface/capability hint                      |
| auth/integrity          | Proof or reference sufficient to reject tampering/replay |
| optional opaque payload | Encrypted or detached richer content                     |

## 30. Jitterbug: routing from the rind

Jitterbug asks how much useful forwarding can be decided from a message
header alone. The Has-Needs answer is to expose a small routing rind
containing only what a node is permitted to know. A relay may decide
that a message is new, alive, locally relevant, and historically likely
to resolve through a particular neighbor without opening the protected
payload.

\[ NETWORK RIND \]\[ SEMANTIC RIND \]\[ ENCRYPTED OCA LAYERS \]  
  
Network rind:  
version \| fingerprint \| TTL \| hop/age \| novelty \| priority  
  
Semantic rind:  
H/N \| ontology namespace \| token \| scope \| disclosure class  
  
Payload:  
opaque unless explicit capability permits disclosure

## 31. Routing toward resolution

Traditional routing asks where a destination address is. Has-Needs can
additionally ask where a semantic class has recently found successful
resolution. A local node might learn that token A4:17 frequently
completes through neighbor B and frequently expires through neighbor C.
It need not know that A4:17 means potable water in order to prefer the
successful path.

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Routing principle<br />
</strong>Jitterbug does not have to route packets toward addresses
alone. It can route exposed semantic intent toward historically
successful resolution paths using only the message rind.</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

## 32. Semantic Friend node

A “shoebox” or other volunteered local node can act as a semantic Friend
node: a locally persistent replica, ontology cache, store-carry-forward
relay, offline rendezvous point, duplicate-suppression cache, validation
participant, and increasingly intelligent semantic router. People may
deliberately host and share useful ontology as a form of being helpful
to their family, peers, neighborhood, or profession.

The Friend node MUST NOT become the owner of the people or objects it
assists. Its intelligence improves routing but is not required for
participation: a dumb relay may forward; a smart Friend may prefer paths
associated with previous completion.

## 33. Existing standards worth borrowing, not inheriting wholesale

The protocol should reuse mature components where they fit while keeping
Has-Needs semantics independent. CBOR is specifically designed for small
code/message size; COSE supplies signing/MAC/encryption structures over
CBOR; HPKE provides a standard public-key encryption construction; MLS
addresses asynchronous secure group messaging; Bundle Protocol v7
formalizes store-carry-forward for delay-tolerant networks. Bluetooth
Mesh provides TTL, message caching, managed flooding and directed
forwarding. These are candidate building blocks, not definitions of
Has-Needs.

## 33.1 Shared ontology as semantic compression

A local ontology should usually synchronize as a relatively expensive
seed event followed by append-style deltas. Once two peers share a
namespace and token dictionary, common meanings do not need to be
retransmitted in full. A constrained transport can send a compact token
plus only the semantic difference required for this interaction. The
receiving device reconstructs richer meaning from local context.

Initial synchronization:  
namespace A4 + token dictionary + selected resolution edges  
  
Later fast-plane message:  
N \| A4:17 \| qty=20 \| ttl=3  
  
Receiver reconstructs locally:  
A4:17 = potable water  
known substitutions / exclusions / recent resolution paths

This makes successful local coordination cumulative: the community
becomes cheaper to communicate within as shared semantic context grows.
A semantic Friend node may act as an ontology host or cache, but the
ontology remains scoped and selectively shareable rather than globally
authoritative.

## 33.2 Canonical meaning, transport expression and rendering

Has-Needs separates canonical meaning from both wire encoding and human
presentation. The same semantic object may be aggressively compressed on
Bluetooth, rendered as plain text on a terminal or Deaf-accessible text
interface, spoken by a voice system, shown as an icon for low-literacy
use, plotted on a map, aggregated for an emergency manager, or supplied
to a local reasoning engine. None of these presentations is the
canonical object.

canonical Has/Need object  
\|  
transport-specific expression  
\|-- BLE  
\|-- SMS  
\|-- IP  
\`-- human relay  
\|  
local reconstruction  
\|  
renderer / reasoning  
text \| icon \| speech \| map \| agency view \| Sattva/AI

A Sattva-like deterministic reasoning layer may assist with semantic
normalization, ambiguity detection, matching, routing relevance,
compression, anomaly flags, and deciding when an expensive language
model is useful. It remains advisory: it does not become the authority
that decides whether a human Need is satisfied.

## 34. DXOS and SmallWeb placement

DXOS is relevant as an optional rich-peer substrate for local-first
replicated state: its ECHO layer provides secure P2P CRDT replication,
offline writes, multiple writers, and spaces. SmallWeb is relevant as a
lightweight way to instantiate community-facing services by mapping
directories to subdomains. Neither should define the wire primitive. A
Has or Need must remain meaningful if both are replaced.

# Part VII - Communities, communication and projects

## 35. Community is a purpose-scoped coordination space

The sovereign being exists outside communities by default. A community
is an optional place for communication around any purpose or goal and
may collect permissioned Has and Need objects, shared ontology
fragments, project state, and task groups. It is logical rather than
identical to one server: state may be replicated across members,
semantic Friend nodes, cloud services, or local-first peers.

## 36. Communication follows semantic context

Communication around a specific match is finite. Negotiation, decisions,
and disclosures exist to complete that Working relationship and may be
committed into the receipt context at completion according to policy.
Community communication is different: it remains appendable while the
community remains active. A person leaving may take their own content
and authorized history; other participants may retain legitimate copies
of material that was already shared with them.

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Record distinction<br />
</strong>Receipts are closed records. Communities are continuing
records.</th>
</tr>
</thead>
<tbody>
</tbody>
</table>

## 37. Sub-communities instead of noise-control bureaucracy

When attention becomes dense around a subproblem, participants can form
a sub-community rather than forcing one giant channel to rely on
increasingly elaborate notification filters. The same grammar repeats
fractally.

Build House  
Framing  
Electrical  
Service Entrance  
Permit Coordination  
Materials  
Inspection

A sub-community is not merely a chat channel. It can have its own Has,
Need, members, ontology, disclosure boundaries, conversations, and
receipts. When no longer useful, activity simply decays; useful receipts
and ontology evidence remain.

## 38. Project management emerges from Has/Need coordination

A project such as “build the house” can be a community whose unresolved
Needs and available Has objects constitute much of the live project
state. Kanban boards, Gantt charts, maps, budgets, and checklists become
views over the same semantic substrate rather than separate systems of
record.

COMMUNITY: Build House  
  
Needs: permit \| excavation \| framing \| electrical \| roofing \|
inspection  
Has: architect \| excavator \| carpenter \| truck \| donated lumber \|
budget  
  
Each accepted match -\> Working -\> completion -\> receipt -\> new
state/Needs

## 39. Rapid onboarding through portable context

Workers can enter a new project with selected capabilities, provenance,
and trusted ontology already available to their Persona Manager. They do
not need to be recreated inside the project’s database. The community
receives only the projection explicitly relevant to the task.

## 39.1 Data Views are sovereign projections

Data Views are a major interaction feature. They let a participant render, filter,
group, sort, compare, and act on objects they own or are authorized to see without
creating a second system of record. A Data View is a projection over the same
Has-Needs substrate.

Examples include:

- all of my current Needs;
- all of my current Has objects;
- everything I currently have in Working;
- my completed exchanges and receipt lineage;
- objects relevant to one persona, family, project, community, or place;
- an emergency-manager operational picture derived from consented reports;
- a project board, timeline, resource layer, budget view, or Gantt view.

A Data View MAY combine owned objects with objects explicitly disclosed by others,
derived aggregates, ontology, and locally computed routing or resolution evidence.
The view MUST NOT silently expand the participant’s authority over underlying objects.
Changing a view changes representation and attention, not ownership.

## 39.2 The globe/map is the primary literacy-agnostic spatial renderer

The default rich interface SHOULD be globe- or map-based. This is not because
location must be revealed; location remains sacrosanct and disclosure-controlled.
The spatial interface is valuable because geography, proximity, direction, scale,
movement, and relationship can be understood with minimal dependence on literacy,
language, or institutional vocabulary.

The globe is therefore best understood as a Data View over a participant’s sovereign
information space. It may render the user’s own Has, Need and Working objects, local
ontology, candidate matches, community projections, routes, hazards, receipts,
or permissioned public resources as icons, layers, relationships, and spatial patterns.

What appears on the globe depends on the active Persona, OCA disclosure state,
permissions, semantic scope, and selected Data View. It is not a window onto a
globally enumerable database.

A person affected by disaster might see nearby resources and unresolved Needs.
An emergency manager might see a consented fire-status layer and response assets.
A farmer might see produce, buyers, transport, water, weather, and market-day
commitments. A displaced person entering a town might scan a QR code and receive a
local resource view without surrendering identity. The underlying protocol objects
remain the same.

Rich visual interaction SHOULD favor direct manipulation, icons, spatial layers,
simple gestures, and locally meaningful symbols. Text, speech, SMS, terminal,
screen-reader, and other renderers remain first-class alternatives. Renderer choice
MUST NOT alter protocol semantics.

## 39.3 RGB layers as a visual lingua franca

The rich interface SHOULD be able to render heterogeneous sovereign data sources into
RGB visual layers. RGB is a presentation and composition surface, not the canonical
storage format and not a claim that arbitrary semantic data can be uniquely encoded in
a single color value.

A source may be a Has, Need, receipt-derived history, sensor stream, location history,
weather field, transaction history, community aggregate, ontology category, or other
authorized data. Its underlying representation remains intact. The renderer maps
selected dimensions into a color field, gradient, intensity, pattern, or other RGB layer.

This creates a common interaction language across otherwise unrelated data while
preserving provenance back to the originals.

## 39.4 Data Stories are live semantic expressions

A Data Story exists as soon as selected layers are related by an operator. It does not
need to be saved, named, published, packaged, or exchanged first. The expression itself
is already a meaningful derived view.

For example:

    rainfall_24h + (dew_point_today × cassava_crop)

is a Data Story at the moment it is rendered. It expresses a situated relationship
between current environmental conditions and a specific crop. The underlying rainfall,
dew-point, and crop data remain intact; the expression creates a temporary semantic
relationship among them.

Simple mathematical or logical operators MAY include addition, subtraction, difference,
intersection, multiplication, thresholding, masking, normalization, and temporal
comparison. The operator set is an interface choice, but each derived expression SHOULD
retain provenance to its inputs, transformation, time scope, and permissions.

A Data Story MAY remain transient. If useful, it MAY be saved or named, becoming a
reusable derived object or live view. It may then serve as an input to another story,
be shared with a person or community, or be offered as a Has in a value exchange.

## 39.5 Streamed Data Stories as value exchange

A Data Story MAY also be a bounded live stream computed from continuously changing
inputs. A participant can expose the derived stream without necessarily exposing the
underlying raw sources.

Another participant may express a Need for the resulting data product. The owner may
respond with a compatible Has whose contract specifies the story, transformation,
resolution, frequency, duration, compensation or reciprocal value, and disclosure
conditions.

This makes data sharing an ordinary Has/Need value exchange rather than a platform
privilege.

# Part VIII - Security, adversarial conditions and graceful degradation

## 40. Security goals

- Authenticate objects and transitions without requiring universal
  identity exposure.

- Prevent unauthorized modification and replay of protected protocol
  objects.

- Limit disclosure to Persona/OCA policy and explicit contract
  progression.

- Avoid centralized or network-wide enumeration of other participants’ Needs, Has objects, histories, and identities while preserving full owner visibility into a participant’s own state and permissioned local holdings.

- Permit local/offline verification of as much evidence as practical.

- Preserve enough distributed evidence to recover continuity after
  device/key loss.

- Minimize the consequences of compromised relays, caches, and community
  services.

- Keep algorithm choice replaceable so prototype cryptography can be
  hardened later.

## 41. What cryptography can and cannot prove

Cryptography can prove control of keys, integrity of statements,
continuity of object lineage, and mutual attestation of completion. It
does not automatically prove that a physical claim is true. Someone can
sign a false Has. The protocol relies on the exchange itself, optional
class-specific validation, and later evidence to distinguish claims from
outcomes.

## 42. False Has and physical truth

If a participant claims to have 5,000 liters of water and a collector
arrives to find none, the attempted exchange fails. That failure need
not become a public reputation event. Locally, the path may be
deprioritized. For safety-critical semantic classes the Need may require
additional attestations or measurements before Working or completion.

## 43. Long-latency harms and exposure tracing

Completion means the agreed exchange occurred; it does not mean the
exchange was universally safe forever. The architecture’s immutable
lineage can become especially valuable when harm is discovered later. If
a well, tanker, material batch, shelter, or medicine source is later
found unsafe, participants may determine whether their own receipt
lineage intersects the source and selectively warn others who can prove
relevant exposure. Later evidence updates interpretation without
rewriting the original completed history.

## 44. Key/device loss

Because counterparties retain their own matching evidence, the forest of
chains acts as a distributed partial backup of historical existence
without any one counterparty possessing the whole person. Recovery may
be patchy and still sufficient. The protocol should optimize for “enough
continuity to resume sovereign participation,” not perfect historical
reconstruction.

## 45. Network suppression

A hostile actor that physically controls all available communications
can suppress traffic; no cryptography can force a disconnected radio to
transmit. Has-Needs reduces the value of controlling one infrastructure
by making useful organization cheap to regenerate: direct peer-to-peer,
local Friend nodes, community services, SMS/radio relays, human
intermediaries, and other paths can coexist. The system should prefer
multipath availability over dependence on one authoritative network.

## 46. Ontology poisoning

A malicious actor may publish bad semantic mappings or misleading
service claims. The damage is limited by local ranking, source
provenance, human acceptance, and the fact that completion evidence is
contextual rather than a universal truth score. A public ontology is
advisory; it does not overwrite a person’s private understanding merely
because it is widely published.

## 47. Extreme scarcity

Has-Needs cannot create absent physical resources. Scarcity, triage,
eligibility, rationing, lottery, or vulnerability rules can be expressed
in Need scope and contract conditions or in transparent
community/governance processes. The matching layer should not silently
invent distributive-justice rules.

## 48. Graceful degradation ladder

AI + rich UI + cloud + mesh + shared ontology  
\|  
local nodes + cached ontology  
\|  
peer-to-peer devices  
\|  
SMS / radio / terminals  
\|  
human relay  
\|  
"Who has this?" / "Who needs this?"

The primitive survives because it formalizes a human behavior that
predates the technology. The technology enhances reach, privacy,
persistence, validation, and efficiency; it should not become a
prerequisite for the underlying coordination pattern.

# Part IX - Reference prototype profile and validation plan

## 49. Prototype objective

The next implementation should prove the complete semantic loop before
attempting industrial-strength cryptography or a production mesh. The
goal is not a polished application. It is to demonstrate that the
primitives remain sufficient under increasingly difficult scenarios.

## 50. Reference Prototype Profile A (replaceable)

The following is a deliberately conservative implementation profile for
experimentation. It is not part of the architectural core and may be
replaced without changing Has-Needs semantics.

| **Function**             | **Candidate**                                            | **Reason**                                              |
|--------------------------|----------------------------------------------------------|---------------------------------------------------------|
| Canonical encoding       | CBOR (RFC 8949)                                          | Compact, deterministic-capable binary representation    |
| Signing/container        | COSE (RFC 9052) with a standard supported signature      | Avoid inventing message-security framing                |
| Prototype signatures     | Ed25519 or equivalent audited library                    | Fast, small keys/signatures; implementation convenience |
| Recipient encryption     | HPKE (RFC 9180) or high-level audited library equivalent | OCA capability payloads / per-recipient disclosure      |
| Hash                     | SHA-256 or another established cryptographic hash        | Object/receipt commitments and duplicate fingerprints   |
| Object IDs               | Random 128- or 256-bit values with domain separation     | Simple prototype uniqueness; no global allocator        |
| Group messaging          | Optional MLS (RFC 9420) only where justified             | Not required in core; useful for richer communities     |
| Delay tolerant relay     | Borrow Bundle Protocol concepts; do not require BPv7     | Store/carry/forward, expiry, custody-like behavior      |
| Local-first rich replica | Optional DXOS/ECHO experiment                            | Offline CRDT state; not wire authority                  |
| Community app shell      | Optional SmallWeb experiment                             | Rapidly instantiate views/services; not identity root   |

## 51. Three-person complete-loop simulation

The first executable reference should use three participants: Alice
creates a Need, Bob has a compatible Has, and Carol runs a semantic
Friend node. The Friend must be able to relay the object without reading
protected payload. Alice and Bob progressively disclose, accept, enter
Working, communicate, complete, receive the same canonical receipt,
append local receipt pointers, and update their local ontology/routing
evidence.

N31 CREATED  
N31 TOKEN=A4:17  
N31 DISCLOSURE=0  
  
H82 DISCOVERED  
MATCH N31 \<-\> H82 PROPOSED  
  
DISCLOSURE -\> 1  
MATCH ACCEPTED  
N31 + H82 -\> WORKING  
  
VALUE EXCHANGED  
CANONICAL RECEIPT R44 CREATED  
R44 copied to both participants  
local chain entries point to HASH(R44)  
  
If H82 partially consumed:  
H82 terminates  
H83 minted as remainder  
  
Local ontology / semantic routing evidence updates

## 52. Required tabletop / integration tests

| **Test**                  | **Scenario**                      | **Pass condition**                                                               |
|---------------------------|-----------------------------------|----------------------------------------------------------------------------------|
| T1 Pair                   | 1 Has -\> 1 Need                  | Identical receipt; both local chain pointers verify                              |
| T2 Split                  | 1 Has -\> many Needs              | Original Has terminates; correct new remainders/lineage                          |
| T3 Aggregate              | many Has -\> 1 Need               | One Need completed from independent capability sources                           |
| T4 Offline Friend         | Recipient unavailable             | Friend stores/carries/forwards without payload disclosure                        |
| T5 Fire-status query      | Agency wants local intelligence   | Agency expresses Need; citizens voluntarily answer with Has; no Need enumeration |
| T6 Aggregated food Needs  | Aid provider wants demand picture | Derived count/area appears without transferring ownership of individual Needs    |
| T7 False Has              | Claim fails at pickup             | No global reputation required; local path deprioritizes                          |
| T8 Device/key loss        | Participant loses primary device  | Sufficient continuity rebuilt from backup + counterpart receipts/attestations    |
| T9 Delayed contamination  | Water source later unsafe         | Users can determine exposure lineage; historical receipt remains immutable       |
| T10 Sub-community         | Project becomes noisy             | Participants bud a scoped group; Has/Need grammar unchanged                      |
| T11 Transport degradation | Cloud and internet removed        | Local/peer/human mechanisms preserve basic coordination                          |
| T12 Ontology novelty      | Unexpected resolver succeeds      | New local resolution edge emerges without taxonomy rewrite                       |

## 53. Evaluation metrics

- Time to first useful resolution, not merely time to first data
  collection.

- Number and proportion of Needs reaching completed exchange.

- Amount of personal data disclosed per successful resolution.

- Number of steps requiring institutional mediation versus direct
  resolution.

- Ability to function under partition, intermittent connectivity and
  loss of a node.

- Accuracy with which useful aggregate response pictures emerge from
  consented exchanges.

- Rate of unnecessary retransmission and duplicate processing on
  constrained transports.

- Human comprehension: can participants explain why a match was proposed
  and what will be disclosed next?

- Ontology efficiency: do successful local paths become easier/cheaper
  to discover over repeated trials?

- Recovery quality after key/device loss: can the participant resume
  useful interaction with a partially reconstructed history?

## 54. Expert review questions

1.  Can the two-primitives-plus-binding model express the hard scenarios
    without inventing hidden central state?

2.  Can non-enumerability be maintained while still supporting useful
    emergency aggregation and public-interest situational awareness?

3.  What minimum uniqueness/anti-Sybil properties are required by risk
    class, and which cryptographic constructions best satisfy them
    without global identity exposure?

4.  Can OCA capability transitions be made compact enough for
    constrained links without creating dangerous metadata side channels?

5.  What semantic information must be exposed in the routing rind to
    make Jitterbug effective, and what should remain opaque?

6.  How should canonical receipts commit to match conversation without
    making private communication unnecessarily durable?

7.  What is the smallest recovery protocol that can re-establish
    continuity from counterpart receipt evidence after key/device loss?

8.  How should a Friend node learn routing success while preventing its
    local routing table from becoming a covert reputation or
    surveillance system?

9.  Which transport adapters can preserve the same semantics at
    radically different bandwidths, and what fields can be inferred
    rather than transmitted?

10. What formal properties can be proven about lineage, conservation,
    duplicate suppression, and non-enumerability in a reference
    implementation?

# Appendix A - Compact conceptual schemas

## A.1 Need

Need {  
relation = NEED  
need_id  
issuer_ref  
ontology_ns  
token  
satisfaction?  
scope?  
contract?  
expiry?  
oca_ref?  
auth  
}

## A.2 Has

Has {  
relation = HAS  
has_id  
issuer_ref  
ontology_ns  
token  
capability?  
scope?  
oca_ref?  
auth  
}

## A.3 Working

Working {  
relation = WORKING  
working_id  
need_refs\[\]  
has_refs\[\]  
agreed_terms  
disclosure_state  
release_conditions?  
attestations  
}

## A.4 Canonical Receipt

Receipt {  
receipt_id  
working_id  
need_refs\[\]  
has_refs\[\]  
completion_claim  
value_exchange  
resulting_lineage\[\]  
conversation_commitment?  
completion_attestations\[\]  
}

## A.5 Participant-local chain entry

ChainEntry {  
previous_entry_hash  
canonical_receipt_hash  
local_timestamp_or_sequence?  
local_attestation  
}

# Appendix B - Illustrative message flow

Alice / Persona Friend node Bob / Persona  
\| \| \|  
\| NEED N31 rind ------\> \| ---- cached/relay ---\> \|  
\| \| \|  
\| \<------ candidate response / match ------------\|  
\| \|  
\| -- OCA capability / more detail --------------\> \|  
\| \<-------------- reciprocal disclosure --------- \|  
\| \|  
\| ======== humans accept; Working W44 =========== \|  
\| \|  
\| \<-------------- working conversation ----------\>\|  
\| \|  
\| ================ completion =================== \|  
\| \|  
\| \<------ identical canonical Receipt R92 ------\> \|  
\| \|  
local chain local chain  
append HASH(R92) append HASH(R92)

# Appendix C - Terms

| **Term**             | **Meaning**                                                                                                                                        |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Has                  | An independently addressable sovereign claim of available capability/resource.                                                                     |
| Need                 | An independently addressable smart-contract-like sovereign claim of desired outcome and possible satisfaction conditions.                          |
| Working              | Accepted temporary binding among one or more Has/Need objects.                                                                                     |
| Receipt              | Canonical immutable evidence of a completed value exchange, copied identically to participants.                                                    |
| Forest of chains     | The set of participant-local append-only histories whose entries point to shared canonical receipts.                                               |
| Persona Manager      | Sovereign policy boundary controlling identity context and outward projection.                                                                     |
| OCA                  | Overlays Capture Architecture; layered, state-dependent disclosure of one underlying object.                                                       |
| Semantic Friend node | Volunteered local node that can cache, relay, host ontology, provide rendezvous/replication, and optionally route using local resolution evidence. |
| Ontology token       | Compact semantic reference meaningful inside a namespace.                                                                                          |
| Resolution edge      | Local evidence that a semantic/path relationship actually produced a completed outcome.                                                            |
| Non-enumerability    | Property that Has/Need discovery occurs by semantic encounter rather than privileged browsing of a complete central inventory.                     |
| Jitterbug            | Proposed routing approach in which useful forwarding decisions can be made from a minimal exposed header/rind without opening protected payload.   |
| Fast plane           | Low-bandwidth live coordination messages.                                                                                                          |
| Slow plane           | Background synchronization, validation, receipt and ontology convergence.                                                                          |

# Appendix D - Selected evidence and implementation references

These references are informative. They support the disaster rationale or
identify mature implementation components worth evaluating; none is
claimed to define Has-Needs.

**\[1\] Hobfoll et al. (2007), “Five essential elements of immediate and
mid-term mass trauma intervention.”** Identifies safety, calming,
self/community efficacy, connectedness and hope as empirically supported
principles. [<u>Source</u>](https://pubmed.ncbi.nlm.nih.gov/18181708/)

**\[2\] IASC Guidelines for Mental Health and Psychosocial Support in
Emergency Settings (2007).** Major inter-agency humanitarian guidance
spanning community mobilization, coordination, information, protection
and recovery.
[<u>Source</u>](https://www.who.int/publications/i/item/iasc-guidelines-for-mental-health-and-psychosocial-support-in-emergency-settings)

**\[3\] Norris et al. (2008), “Community resilience as a metaphor,
theory, set of capacities, and strategy for disaster readiness.”** Major
resilience synthesis emphasizing social capital,
information/communication and community competence.
[<u>Source</u>](https://pubmed.ncbi.nlm.nih.gov/18157631/)

**\[4\] UNDRR (2023), Thematic report on local, Indigenous and
traditional knowledge for disaster risk reduction in the Pacific.**
Calls for stronger integration, documentation and access to
local/Indigenous/traditional knowledge.
[<u>Source</u>](https://www.undrr.org/publication/thematic-report-local-indigenous-and-traditional-knowledge-disaster-risk-reduction)

**\[5\] RFC 8949 - Concise Binary Object Representation (CBOR).**
Compact/extensible binary data format designed for small code and
message sizes.
[<u>Source</u>](https://www.rfc-editor.org/rfc/rfc8949.html)

**\[6\] RFC 9052 - CBOR Object Signing and Encryption (COSE).**
Signatures, MACs, encryption and key structures over CBOR.
[<u>Source</u>](https://www.rfc-editor.org/rfc/rfc9052.html)

**\[7\] RFC 9171 - Bundle Protocol Version 7.** Standards-track
store-carry-forward / delay-tolerant bundle protocol.
[<u>Source</u>](https://www.rfc-editor.org/rfc/rfc9171.html)

**\[8\] RFC 9180 - Hybrid Public Key Encryption (HPKE).** Standard
hybrid public-key encryption construction suitable for
recipient-specific protected payloads.
[<u>Source</u>](https://www.rfc-editor.org/rfc/rfc9180.html)

**\[9\] RFC 9420 - Messaging Layer Security (MLS).** Asynchronous group
key establishment with forward secrecy and post-compromise security.
[<u>Source</u>](https://www.rfc-editor.org/rfc/rfc9420.html)

**\[10\] Bluetooth Mesh Protocol Specification v1.1 and Directed
Forwarding overview.** TTL, message caching, managed flooding,
friendship behavior and directed forwarding are relevant transport
precedents.
[<u>Source</u>](https://www.bluetooth.com/wp-content/uploads/Files/Specification/HTML/MshPRT_v1.1/out/en/index-en.html)

**\[11\] DXOS ECHO documentation.** Current example of P2P CRDT
replication, offline writes and client-held data; candidate rich-peer
substrate only.
[<u>Source</u>](https://dxos.org/docs/echo/introduction/)

**\[12\] SmallWeb documentation.** Current example of lightweight
app/service instantiation from directory/subdomain structure; candidate
community interaction shell only.
[<u>Source</u>](https://www.smallweb.run/docs/guides/http)

# Closing statement

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Has-Needs in one paragraph<br />
</strong>The protocol starts with two independently addressable
sovereign objects: Has and Need. They are not rows in a central database
and are not globally enumerable. They discover one another through
scoped semantic matching; people decide whether to bind them into
Working; disclosure can increase only as permitted; completed value
exchange produces an identical canonical receipt for the participants;
and those receipts create a local, self-pruning evidence map of what has
actually worked. Communities, agencies, AI, cloud services, mesh
networks, and richer applications may all participate, but none becomes
the owner of the person or the authoritative inventory of the
world.</th>
</tr>
</thead>
<tbody>
</tbody>
</table>