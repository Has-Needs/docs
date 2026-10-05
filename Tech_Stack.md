# Has-Needs Reference Implementation Candidates

**Status:** Non-normative implementation guidance aligned to [Specification V1](./Has-Needs-Spec-v1.md).

Has-Needs is defined by protocol invariants, not by a fixed vendor stack. The technologies below are candidates for a reference implementation and may be replaced without changing protocol semantics.

## Core implementation profile

| Function | Candidate approach | Status |
|---|---|---|
| Canonical encoding | CBOR / deterministic-capable binary representation | Candidate |
| Message signing/container | COSE or equivalent standard container | Candidate |
| Signatures | Ed25519 or another audited equivalent | Candidate |
| Recipient encryption | HPKE or high-level audited equivalent | Candidate |
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

A conforming implementation must support:
- contextual personas;
- progressive disclosure;
- revocable/limited capabilities where feasible;
- location minimization;
- owner-scoped Data Views;
- authenticated object lineage;
- provable continuity/uniqueness appropriate to interaction risk.

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

No proprietary or unpublished cryptographic construction is part of the V1 requirement.

Earlier documents referenced **HOKKAIDO** as if it were a selected implementation. It is not currently a normative or validated component. If a complete construction becomes available, it can be evaluated behind the protocol's replaceable cryptographic interfaces.

## Storage and replication

Personal chains are append-only evidentiary structures pointing to canonical completed-exchange receipts. They do not require a global blockchain or consensus ledger.

Optional storage/replication technologies may include:
- local filesystem or embedded database;
- CRDT replication;
- content-addressed storage such as IPFS for appropriate larger objects;
- participant-chosen backups;
- semantic Friend-node caches.

Storage location does not create authority.

## Versioning

- Specification: **V1 working draft**
- Implementation: **0.x experimental**
- Candidate libraries: replaceable
- Production/security claims: deferred until validation and independent review
