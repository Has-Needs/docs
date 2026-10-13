# Has-Needs Reference Implementation Candidates

**Status:** Non-normative implementation guidance aligned to [Specification V1](./Has-Needs-Spec-v1.md).

Has-Needs defines its architecture independently of any vendor stack or external blockchain. The **eUTXO contract model** informs Needs; the **NFT identity and provenance model** informs Has objects. The reference technologies below are replaceable implementation candidates. Personal receipt histories belong to Has-Needs itself.

## Core implementation profile

| Function | Candidate approach | Status |
|---|---|---|
| Canonical encoding | CBOR / deterministic-capable binary representation | Candidate |
| Message signing/container | COSE or equivalent standard container | Candidate |
| Signatures | Ed25519 or another audited equivalent | Candidate |
| Recipient encryption | HPKE or high-level audited equivalent | Candidate |
| Owner-defined scope comparison | Multiresolution coverage sets, routes, regions, and locally selected community context | Baseline architectural matching path; no person-location input |
| Protected cross-party spatial comparison | HE, MPC, or PSI-based designs with bounded result release | Experimental research; no V1 construction or non-leakage guarantee |
| Hashing | SHA-256 or another established cryptographic hash | Candidate |
| Object identifiers | Random domain-separated 128- or 256-bit identifiers | Candidate |
| Group messaging | MLS where a community requires it | Optional |
| Rich local-first replication | DXOS/ECHO or another CRDT substrate | Experimental |
| Delay-tolerant relay | Store/carry/forward concepts from DTN / Bundle Protocol | Experimental |
| Community service shell | SmallWeb or equivalent lightweight local service layer | Experimental |

## Application layer

A reference client will likely use:
- TypeScript/React or equivalent for rapid UI work;
- WebGL/Canvas or another capable renderer for the globe and RGB Data Views;
- local storage or CRDT-backed state for offline-first interaction;
- accessible alternate renderers for text, speech, screen readers, terminal/SMS, and feature-phone gateways.

These are implementation choices, not protocol requirements.

## Transport

The same semantic objects should be able to cross multiple transports, including:
- Bluetooth / BLE;
- local IP and WebRTC;
- libp2p or equivalent peer transport;
- SMS or low-bandwidth gateways;
- radio / serial / constrained links;
- cloud relays where useful;
- human-assisted relay.

No transport becomes the authority for object meaning.

## Persona, disclosure, and identity

The Persona Manager and OCA interfaces are architectural requirements; their specific libraries are not yet fixed.

**Identity and contract-access profile:** one owner-held receipt history supports privately separated personas. A standing signed declaration may withhold default permission for identity use. Every protected-field access is checked against a scope-limited, revocable grant; a short-lived per-contract API or equivalent capability returns only the authorized output and terminates future access following effective revocation. Storage or hosting is not identity custody, and no shared third-party account or DID directory is required to discover or validate the participant. Privacy tests must attempt cross-persona correlation, unauthorized lateral-field access, adaptive probing, and replay after revocation.

A conforming implementation must support:
- contextual personas;
- progressive disclosure;
- revocable/limited capabilities where feasible;
- *unretrievable actual participant location* from protocol-visible APIs, persisted artifacts, shared objects, relays, journals, receipts, and routing rinds;
- geographic applicability for objects independent of the issuer's position;
- bounded local or cryptographically protected proximity checks without publishing coordinates;
- owner-scoped Data Views;
- authenticated object lineage;
- provable continuity/uniqueness appropriate to interaction risk.

## Trust Kernel

The reference implementation should include a minimal Trust Kernel whose behavior and
update rules are directly inspectable.

Kernel update experiments should support:
- exposing a version/fingerprint during ordinary interactions;
- detecting stale or divergent kernels;
- delaying remediation until the next random eligible peer encounter;
- receiving a candidate kernel from that peer;
- locally validating the candidate before activation;
- retaining the prior working kernel if validation fails.

The supplying peer is a distribution path, not a root of trust. Specific validation,
reproducible-build, signing, or community-release mechanisms remain implementation
questions until the V1 kernel format is frozen.

## Trust and verification

The reference implementation should support:
- bilateral canonical receipts;
- chain consistency checks;
- live presentation of chain-hop relationship evidence without storing a trust score;
- the V1 canonical eight-hop chain verification depth;
- lower policy-selected hop thresholds when explicitly accepted;
- optional class-specific attestations for high-risk exchanges.

Trust vetting is live evidence presented to the participant; it is not a stored reputation score.

## Cryptography status

**Default geographic matching uses dynamic spheres of possibility, not exact position comparison.** A Need's coverage may expand when a complementary Has—for example a rental truck—extends feasible pickup range; the owner does not need to move or publish personal coordinates. Local proximity-community contexts and previous successful exchange pathways receive strong default relevance in discovery and routing, with outward expansion allowed. Multiresolution geographic regions and compact semantic deltas are candidate encodings, not imposed coordinate tilings or a fixed wavelet transform.

**Private geographic matching is not solved by encryption alone.** Homomorphic encryption can support arithmetic over encrypted coordinates but not by itself private threshold decisions, key agreement among mutually sovereign participants, safe result disclosure, or defenses against inference through repeated queries. HE/MPC/PSI compositions require a defined threat model, leakage analysis, performance budgets for constrained devices, and independent cryptographic review.

A reference implementation should first test overlap and ranking of authorized scope sets, including dynamic scope expansion/contraction and local-community-first discovery without lock-in. It should also test that actual position is never serialized into shared objects, routing rinds, pending journals, canonical receipts, or owner-independent query APIs. It should then assess adversarial repeated proximity probes, colluding counterparties, and physical/transport side channels. Failure to meet the privacy boundary requires deferral or owner-controlled coarse applicability rather than falling back to precise disclosure.


No proprietary or unpublished cryptographic construction is part of the V1 requirement.

The cryptographic implementation remains modular. Candidate constructions are evaluated against their defined security properties, performance, independent review, and compatibility with sovereign disclosure.

## Storage and replication

Personal chains are Has-Needs-native append-only histories pointing to canonical final-resolution receipts. Together they form the independent *forest of chains* that preserves reciprocal interaction evidence.

Optional storage/replication technologies may include:
- local filesystem or embedded database;
- CRDT replication;
- content-addressed storage such as IPFS for appropriate larger objects;
- participant-chosen backups;
- semantic Friend-node caches.

Need-owned append-only pending journals separately preserve accepted Working
commitments and progress. Compact evidence and references can be retained apart
from large payloads. A hash cannot reconstruct content whose copies are lost;
retention, redundancy, retrieval, expiry, and capacity obligations need explicit
policies. A VM per Need is an unselected isolation candidate, not a requirement.

Storage location does not create authority. Delegated execution requires explicit
scope and owner/delegate handoff rules; ordinary replicas do not gain permission
to advance agreements.

## Versioning

- Specification: **V1 working draft**
- Implementation: **0.x experimental**
- Candidate libraries: replaceable
- Production/security claims: deferred until validation and independent review

