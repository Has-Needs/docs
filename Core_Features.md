# Has-Needs Core Features

**Status:** Current summary aligned to [Specification V1](./Has-Needs-Spec-v1.md).  
Where this file and the specification differ, the specification governs.

## 1. Minimal semantic grammar

Has-Needs represents interaction through a compact triplet:

`[entity, relation, context]`

The `relation` field has exactly three protocol states:

- `HAS` — an available capability, resource, knowledge source, stream, or other thing that may satisfy a Need.
- `NEED` — a desired outcome and its provisional conditions for satisfactory resolution.
- `WORKING` — the active state entered when one or more Has and Need objects are mutually accepted into an exchange.

The triplet is the readable semantic form of an object. It does **not** imply a central database or globally enumerable registry.

## 2. Sovereign objects and personal Data Views

A participant owns and controls their own objects and may freely inspect them.

Typical local views include:
- all of my Needs;
- all of my Has;
- all current Working relationships;
- receipt history and lineage;
- objects shared with a selected persona, family, project, or community.

Has-Needs prohibits privileged network-wide enumeration of other participants' sovereign objects, not self-inspection.

## 3. Discovery and matching

Has and Need discover one another through scoped semantic matching rather than global inventory browsing.

A Has may remain latent and respond only when a compatible Need appears. A Need may remain directly matchable even while contributing to a family, community, agency, or regional aggregate.

Machines may rank and suggest. Humans remain the final arbiters of whether a proposed match is acceptable.

## 4. Working and completion

Mutual acceptance moves the participating objects into `WORKING` for the duration of the agreement.

Completion produces the durable evidence:
- a canonical receipt shared by the participants;
- participant-local chain entries that point to that receipt;
- resulting lineage for consumed, reusable, or remaining Has objects.

There is no required global activity log and no required `SPENT` state.

## 5. Live trust vetting without reputation

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

The Persona Manager is the sovereign policy boundary controlling:
- active persona;
- identity exposure;
- location precision;
- ontology exposure;
- history and receipt disclosure;
- message filtering;
- capabilities granted to other participants.

OCA — Overlays Capture Architecture — supports layered disclosure of the same underlying object.

**Disclosure becomes a state transition:** more detail may be revealed as a relationship progresses from discovery to plausible match to acceptance to Working to completion.

## 8. Local ontology and resolution evidence

The ontology is not “the truth.” It is a scoped map of declared relationships and what has actually worked.

Has-Needs distinguishes:
- semantic edges — meaning/category relationships;
- resolution edges — evidence that a pathway produced a completed outcome;
- safety/validation edges — later evidence, certification, testing, or warnings.

Old evidence may decay in ranking without being erased.

## 9. Globe, RGB layers, and Data Stories

The primary rich interface is globe/map-based as a literacy- and language-agnostic spatial renderer.

The globe is a **Data View**, not a global database window. What appears depends on the active persona, permissions, semantic scope, and OCA disclosure state.

Heterogeneous data can be rendered into RGB layers as a common visual composition surface. Users may combine layers with simple mathematical or logical operators.

A Data Story exists as soon as the relationship is expressed, for example:

`rainfall_24h + (dew_point_today × cassava_crop)`

A story may remain transient, be saved, become an input to another story, be shared, or be offered as a `HAS` in a value exchange. A Data Story may also be a bounded live stream whose derived output is shared without exposing its raw inputs.

## 10. Communities and sub-communities

A community is a voluntary, purpose-scoped coordination space. It does not own its participants.

Communities may hold permissioned projections of Has/Need objects, shared ontology, conversations, project state, and derived views.

Sub-communities provide fractal specialization without changing the core grammar.

## 11. Jitterbug and semantic Friend nodes

Jitterbug is the transport/routing research direction for low-cost, resilient, local-first communication.

A semantic Friend node may cache ontology, store/carry/forward opaque messages, provide rendezvous or replication, and learn useful routing paths without owning the underlying content.

The older `open_n` port-expansion mechanism remains a useful transport experiment. V1 extends the concept toward a minimal network/semantic rind around protected payloads.

## 12. Graceful degradation

Has-Needs is designed to collapse downward rather than fail outright:

rich UI + AI + cloud + mesh  
→ local nodes + cached ontology  
→ direct peer-to-peer  
→ SMS / radio / terminal  
→ human relay  
→ “Who has this?” / “Who needs this?”

The technology enhances a human coordination behavior; it does not create the behavior.
