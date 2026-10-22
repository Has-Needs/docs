# Data Layers, Sovereign Access, and Replication

**Status:** Architectural explanation consistent with [Has-Needs Specification V1](./Has-Needs-Spec-v1.md). DXOS is a replaceable implementation candidate; OCA is a schema/semantic-overlay model, not the Has-Needs access-control authority.

## 1. Why these components are separate

Has-Needs uses several cooperating mechanisms because *description, storage, identity, permission, and proof are different functions*.

| Component | Job | What it must not become |
|---|---|---|
| **OCA — Overlays Capture Architecture** | Defines a stable capture base and content-addressed contextual overlays: meaning, labels, format, sensitivity, transformation, and presentation | An implicit permission to read the underlying value; a complete access-control engine |
| **Persona Manager** | Maintains the individual's single permanently private personal chain and acts as concierge for independently created personas; coordinates authorized protocol actions | A public chain, externally accessible identity root, or automatic cross-persona correlator |
| **Has-Needs authorization / Need contract** | Validates recipient, purpose, permitted attributes or predicates, duration, consideration, current grant, and authorized state changes | A generalized data broker; an AI system inferring consent |
| **OCA-governed projection / capability API** | Renders or computes only the attributes, predicates, or derived outputs authorized by the agreement; gates *each* permitted use | A permanent transfer of a whole object merely because one attribute was requested |
| **DXOS/ECHO, when selected** | Local-first, peer-replicated persistence and collaboration, with chosen space-level membership and offline operation | The owner of personal information, the issuer of Has-Needs permissions, or a universal directory of personas |
| **Owner-held chain, Pending journal and receipts** | Preserve verifiable declarations, accepted obligations, grant/revocation events and final exchange evidence in the native Has-Needs model | An enumerable public ledger of every personal attribute or persona |

The architecture does not require DXOS, a particular database, a blockchain, or an identity provider. Replication may be implemented by DXOS/ECHO or equivalent storage. OCA's content-addressed schema and overlay definitions are distinct from an individual person's protected **values** and from the contract authorizing use of them.

## 2. What an OCA layer means

An OCA **Capture Base** defines the stable structural attributes of a record (for example `shoe_size`, `preferred_shirt`, `audience_count`, `portrait`, or `voice_sample`). Cryptographically linked **overlays** add the context by which those attributes are interpreted: labels in a particular language, recognized formats, units/entry definitions, mappings, transformation instructions, and designations that a field is sensitive. Multiple overlays may describe the same underlying capture base without copying or rewriting all of the source values.

Has-Needs uses this layering as a *semantic projection mechanism*, while adding independently enforced sovereign authorization. **OCA schemas and overlays are tools for describing or translating meaning, not compulsory starter categories.** A sovereign Has or Need begins with the person's own expression, in their own dialect or accessible modality; descriptive schemas may be attached or inferred provisionally only as needed and authorized. A lack of standardized field labels must not prevent a person from proposing an exchange.

The layering adds the following capabilities:

1. **Base structural description:** What kinds of fields or claims this object can represent. These descriptions need not contain the person's field values.
2. **Semantic/context overlays:** What a field means for this task, audience, language, or ontology; how it is formatted or transformed.
3. **Sensitivity and persona policy:** What the owner considers protected, in which persona, and at which disclosure threshold. An OCA sensitive overlay flags attributes; **the Persona Manager and protocol enforce actual permission**.
4. **Contract-specific projection:** Which exact fields, predicates, proofs, derived products, or live API methods this recipient is authorized to receive.
5. **Provenance and verification:** What claim, source commitment, transformation, issuer attestation, grant, and revocation evidence can be shown for that projection **without exposing the undisclosed input**.

These are **conceptual access/evidence layers of the Has-Needs design**, not claims that each is one standardized OCA overlay type. OCA specifies semantic schema overlays; Has-Needs defines its own permission checks, contract lifecycle, encryption/key boundaries, and provenance evidence.

**Layering is not linear compulsory exposure.** A recipient need not first see name, address, and picture before learning an authorized shirt-size predicate. The owner may disclose a high-value derived proof while the original artifact, identifying features, and unrelated overlays remain withheld.

## 3. Granular Need / Has flow

**Example: a clothing vendor wants to know whether a person wears size M.**

```text
Vendor: NEED  clothing-size-compatibility = M
             purpose = recommend a specific garment
             grant  = this vendor, this use, until expiration

Owner's private record, interpreted through OCA:
        Capture Base: shoe_size, shirt_size, hair_color, ...
        semantic overlays: label, units, format, mapping
        sensitive designations: owner/persona policy

Persona Manager: check relevance; ask owner or apply exact
                 narrowly preauthorized preference

Possible approved HAS projection:
        shirt_size_is_M = true
        [no name, exact measurements, shoe size, hair color,
         other personas, source file, or full dataset]

Owner approves + requester agrees:
        NEED + HAS -> WORKING
        Need-owned Pending journal: scope, recipient, obligation
        Bounded API: authorized predicate only
        Canonical final receipt: agreed outcome; same receipt hash
                               for both personal chains
```

A stronger attestation or a numerical measurement may be requested **as a further Need with new consent**, not silently inferred from the earlier permission. A choice to release a predicate does not imply a choice to release the raw attribute. A grant can be intentionally one-time, time-limited, price-limited, or purpose-bound.

**Converse flow: a participant offers a Has.** A person may advertise only the compatible semantic fact `audience_reach >= 100000` under a promotional persona. A vendor's Need may seek that capability and offer a fee. The persona can reveal an attestation of reach after matching, while unrelated identity, follower records, and social relationships remain protected. A subsequent permission to promote something is a separately scoped agreed use, not blanket access to the account.

## 4. Layered provenance and AI derivatives

The owner can retain separate but linked evidence for an artifact:

- **Origin claim:** the owner's statement identifying a source artifact, creator, or controlled persona.
- **Integrity commitment:** content hash, self-addressing identifier, or signed reference to a particular version.
- **Origin or qualification attestation:** a human witness, issuer, tool event, measurement, credential, or other independent evidence where available.
- **Transformation lineage:** proof/reference that a specified derivative was created from a specified source, with a declared process (for example, a synthetic voice derived from a permitted sample).
- **Authorization evidence:** exactly which recipient received permission for which source, derivative, scope, output, and duration.
- **Revocation/supersession evidence:** an authenticated change affecting *future authorized use*.

A verification view may reveal **a fact about provenance** without disclosing the sensitive source. OCA can supply the structural and semantic contexts used to describe these attestations, and the Persona Manager decides which layers and underlying content to present. Identity, likeness, creative work, inferred personality, and AI derivatives therefore need not collapse into a single all-or-nothing disclosure.

Verification of a signature, cryptographic hash, schema, or chain proves a *specific technical proposition*, not automatically the real-world truth of a claim. The evidence remains independently examinable in different jurisdictions; legal findings and remedies are separate questions.

## 5. DXOS placement and boundaries

DXOS/ECHO is a candidate local-first CRDT-backed object store supporting offline work and controlled peer collaboration through **spaces**. Its spaces are units of sharing and access control at the storage/replication level. If DXOS is selected, Has-Needs must avoid assuming that a member of a shared DXOS space has permission to read every OCA-defined attribute stored there.

Implementations therefore **MUST NOT** put an entire unencrypted personal capture record into a replicated or shared space merely to make one permitted field available. Owner-held sources, encrypted payload partitions, and per-recipient capability projections must preserve the narrower Has-Needs contract scope. The Persona Manager manages the boundary; the authorization-checking protocol validates each grant. Optional DXOS identity components may support devices or replication but do not become a mandatory Has-Needs identity authority.

Each individual's Persona Manager maintains their **permanently private personal chain** and facilitates interactions through independently created personas. Neither external actors nor outward personas receive direct chain access; recipients receive only specific authorized receipt-derived projections. Each recipient receives only the relevant contract evidence or projected proof; a common public key, stable owner identifier, or global chain pointer must not silently correlate personas.

## 6. Revocation and offline operation

For current information, an agreement can create a dedicated live API or equivalent revocable capability. Each request checks recipient and grant validity and produces **only the allowed OCA-governed projection**. Revocation closes future controlled access without revealing other portions of the owner-held source. Previously released snapshots cannot be erased. With offline peers, implementers must define revocation propagation, expiry/leases, caching, and synchronization so that a partitioned replica does not indefinitely continue supplying new values under a stale grant.

**A signed standing declaration is the default; a narrowly issued capability is the exception.** The public declaration can state no free access or uninvited use and require a valid contract for protected identity use. A discoverable Has or matching Need is not an access grant. OCA can show what a request *means*; only the owner and the contract-validation mechanism can authorize release.

## Composable API streams and delegated storage

Each entity can provide data within its control to another through a composable API governed by a Need smart contract, with standard templates and custom options. The WORKING state connects the involved Has and Needs throughout execution. Personal data streams and a Community's stream of all communications to a secure storage channel use the same mechanism, preserving each contributor's disclosure scope.

The Community determines responsible parties and permissions for its Need. Delegating storage or moving the stream to relieve resource pressure does not enlarge reading or execution authority. Delegation changes require the contract's authorization; encrypted storage can retain identical receipt content without making that content readable to its custodian.

At resolution the complete contract record, including communications and authorized handoffs, is encapsulated. Persona Managers write identical canonical receipts simultaneously in direct peer-to-peer coordination and mutually verify them. Corroboration compares identical encrypted entries without requiring decryption or core-chain access. Receipt finalization is distinct from background storage replication.

## 7. Conformance scenarios

| Scenario | Expected outcome |
|---|---|
| Vendor requests shirt size | Vendor learns only expressly authorized value/predicate, not adjacent fields or whole capture record |
| Vendor requests more detail after a match | Owner must approve a new or amended disclosure scope |
| Two personas of the same owner transact separately | Counterparties cannot infer common chain ownership from authorized views, stored schema, replication handles, proof identifiers, or receipt references |
| Owner proves audience threshold | Recipient obtains appropriately attested predicate, not followers or civil identity |
| OCA flags a protected field | Neither the overlay flag nor knowledge of the schema grants a reading capability |
| Shared DXOS space member reads stored objects | Space access never overrides field/facet-specific owner contracts |
| Owner revokes a live stream | Further controlled requests fail within defined effective revocation policy; past snapshots remain outside retroactive control |
| Owner proves provenance of derived voice | Reviewer sees approved lineage and authorization evidence but not undisclosed source recordings |
| Offline replica rejoins after revocation | Reconciliation and leases prevent unauthorized future access while preserving recorded evidence |

## 8. External references and architectural dependencies

- [OCA Technical Specification](https://oca.colossi.network/specification/) — Capture Base, linked overlays, sensitive metadata, SAIDs and format/label semantics.
- [OCA Introduction](https://oca.colossi.network/guide/introduction.html) — content-centric, cryptographically linked schema and semantic layers.
- [DXOS/ECHO introduction](https://dxos.org/docs/echo/introduction/) — local-first replication, offline writes, ECHO spaces and their sharing boundary.
- [Specification V1](./Has-Needs-Spec-v1.md) — normative rules for Has/Need/Working, Persona Manager, scoped disclosure, Pending and receipts.
- [Technical Stack](./Tech_Stack.md) — replaceable implementation components.

**Architectural summary:** DXOS may transport and retain protected source state. OCA explains fields, semantic and contextual overlays, and their provenance references. The Persona Manager chooses what facet may become visible. The Need contract and protocol validate *who may receive precisely which projection under which conditions*. A granted, revocable API supplies only that projection; reciprocal evidence records the resulting agreed exchange.
