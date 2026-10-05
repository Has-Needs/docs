# Has-Needs Development Roadmap

**Status:** V1 architecture working draft / pre-conformance implementation  
**Canonical specification:** [Has-Needs-Spec-v1.md](./Has-Needs-Spec-v1.md)

This roadmap is intentionally milestone-based rather than date-driven. Progress is measured by demonstrated protocol behavior, not by feature count.

## 1. Freeze the V1 grammar

**Objective:** Establish one implementable interpretation of the architecture.

Deliverables:
- Canonical `[entity, relation, context]` representation with `HAS | NEED | WORKING`.
- Object identifiers, lineage, receipts, and owner-scoped Data Views.
- Explicit network non-enumerability and permission boundaries.
- Persona Manager / OCA disclosure-state interfaces.
- Reference schemas and test fixtures.

**Exit criterion:** Independent reviewers can implement the core object lifecycle without relying on legacy documents.

## 2. Build the minimal reference loop

**Objective:** Demonstrate the complete sovereign exchange lifecycle with the fewest moving parts.

Deliverables:
- Three-participant simulation: Need creator, Has provider, semantic Friend node.
- Discovery → match → progressive disclosure → Working → completion → identical canonical receipt.
- Partial-consumption lineage.
- Local owner views such as “my Has,” “my Needs,” “my Working,” and receipt history.
- Transparent event trace for debugging and review.

**Exit criterion:** The full lifecycle works locally and under intermittent connectivity without a central authoritative inventory.

## 3. Prove semantic and visual interaction

**Objective:** Validate the human interface as part of the architecture.

Deliverables:
- Globe/map Data View over sovereign objects and permissioned layers.
- Literacy-agnostic icon/layer interaction.
- RGB rendering as the common visual composition surface.
- Simple operator-based Data Stories.
- Saved and streamed Data Stories capable of becoming a Has in a value exchange.
- Accessible alternate renderers: text, speech, terminal/SMS-oriented views.

**Exit criterion:** A user can inspect personal resources, create a Need, understand a match, compose a Data Story, and control disclosure without understanding the underlying schema.

## 4. Exercise hard cases

**Objective:** Attempt to break the primitives before scaling them.

Required scenarios:
- 1→1, 1→many, many→1, and many→many exchanges.
- False Has and failed physical exchange.
- Device/key loss and partial history reconstruction.
- Offline relay / store-carry-forward.
- Emergency aggregation without ownership of individual Needs.
- Direct P2P resolution alongside community or agency coordination.
- Progressive location disclosure.
- Delayed contamination / provenance tracing.
- Community and sub-community formation.
- Network suppression and ontology poisoning.

**Exit criterion:** Hard cases can be expressed without introducing hidden central authority or new ad-hoc primitives.

## 5. Validate Jitterbug transport

**Objective:** Test whether semantic routing can operate on minimal exposed information.

Deliverables:
- Minimal network + semantic rind.
- Duplicate suppression, TTL/expiry, store-carry-forward, and fast/slow planes.
- Semantic Friend node cache and routing behavior.
- BLE/constrained-message experiment.
- Compatibility tests across at least two transport adapters.

**Exit criterion:** An opaque Need can traverse an intermediary that cannot read its protected payload, reach a plausible Has, and complete an exchange.

## 6. Field and institutional validation

**Objective:** Compare Has-Needs against conventional coordination workflows.

Pilot contexts should include at least one disaster/emergency scenario and one ordinary-use scenario such as agriculture, community projects, or research participation.

Measure:
- time to first useful resolution;
- proportion of Needs reaching completion;
- personal data disclosed per successful resolution;
- direct vs institution-mediated resolution;
- recovery under network partition;
- quality of consented aggregate response pictures;
- participant comprehension and perceived agency.

**Exit criterion:** Evidence identifies where the architecture works, where it fails, and what must change before production claims are justified.

## 7. Security and production hardening

**Objective:** Replace prototype assumptions with audited production mechanisms.

Work includes:
- threat model and privacy review;
- cryptographic primitive selection and independent review;
- key rotation/recovery;
- metadata leakage analysis;
- abuse and Sybil-resistance testing by risk class;
- formal tests for lineage, conservation, duplicate suppression, and authorization;
- performance and constrained-device profiling.

**Exit criterion:** A versioned implementation profile can credibly claim conformance to a reviewed Has-Needs specification.

---

### Versioning discipline

- **Specification V1** defines the architecture.
- **Implementation 0.x** is experimental until it passes the relevant V1 conformance tests.
- Candidate technologies such as DXOS, libp2p, IPFS, SmallWeb, OCA implementations, or particular cryptographic libraries remain replaceable unless explicitly promoted into a future implementation profile.
- Historical documents remain useful for provenance and design intent but are non-normative when they conflict with V1.
