> **Current architecture, 21 October 2026:** [WORKING contracts, delegation, streams, and outcomes](./WORKING_CONTRACTS_AND_DELEGATION.md). The dated narrative or review below is retained as history; use the current specification and this guide for contract execution, permissions, and reciprocal receipts.

# Has-Needs V1 completion change log

**Date:** 2026-10-18  
**Status:** Applied changes and remaining implementation-profile work.  
**Authority:** [Specification V1](./Has-Needs-Spec-v1.md) remains canonical; [gap review](./Has-Needs_V1_Gap_Review_2026-10-18.md) and [Paradigm Delta](./Has-Needs_Paradigm_Delta_Review_2026-10-14.md) provide review context.

## Implemented in the current V1 document

| Area | Location | Change |
|---|---|---|
| Need authority | §8.1 | Distinguish matches from authorized assignments; require coordination through Need authority |
| Owner-first continuity | §8.1 | Record the owner's primary update role and trauma-informed rationale |
| Offline community action | §8.1 | Allow prior bounded community delegation and owner-addressed journal updates on reconnection |
| Permission provenance | §24.5 | Require scoped valid grants for protocol-mediated personal-data uses |
| Portable evidence | §24.5 | Define selective verification of reciprocal receipts and issuer attestations without a central registry |
| Tests | §51.1 | Add authority, delegation, parallel Needs, invalid token, portable proof, and interrupted-finalization scenarios |

## Disseminated by audience

- [README](./README.md): compact statement of personal evidence portability.
- [Introduction](./INTRODUCTION.md): personal-data authorization and cross-institutional continuity explained in human terms.
- [Core Features](./Core_Features.md): permission tokens, bounded APIs, attestations, and verifiable proof.
- [Paradigm Delta](./Has-Needs_Paradigm_Delta_Review_2026-10-14.md): corrects the institutional-first and legally dependent evidence assumptions.
- [Gap review](./Has-Needs_V1_Gap_Review_2026-10-18.md): tracks enforcement and conformance questions.

## Re-scan: what is still open, without expanding the core

**P0 implementation profiles:** (1) crash-safe finalization of identical receipts across personal chains; (2) authoritative Need/journal ordering under partition and retries; (3) delegate handoff, expiration, and revocation under disconnection. These are wire-level/conformance matters; the owner-first authority invariant is now stated.

**P1 implementation profiles:** (4) portable proof bundle encoding and verifier status checks; (5) community QR invitation authentication and cross-ontology translation provenance; (6) cryptographic suite migration and key continuity; (7) protected proximity query abuse and rate limits; (8) accessibility-equivalent text/SMS/speech interaction.

**Editorial consistency:** The existing specification already describes private chains, non-enumerability, community pooling, owner-controlled disclosure, and asynchronous Need journals. These do not require additional relation states, a centralized registry, a global lock service, or separate aid/refugee/commerce protocols.

**Completion distinction:** The **normative architectural clarification pass is committed**. A claim that every production interoperability profile has been implemented or empirically validated would be premature. The remaining work should be tracked as bounded tests/profiles rather than expanding the V1 architecture.

## Founder decision: Question 1 — asynchronous receipt finalization

AI tools provide match candidates; humans choose and mutually accept. Candidate selection is distinct from WORKING execution and cryptographic completion. Both participants' Ready authorization of an identical canonical receipt is not itself finalization. Until that receipt is recorded identically on every required personal chain, the transaction remains incomplete and cannot pass normal reciprocal verification. This is a synchronization state, **not** a new human choice or fourth Has-Needs relation. DXOS/ECHO is the intended asynchronous persistence and coordination context; the protocol should state the verification invariant and not duplicate the infrastructure's replication mechanism. Equivalent local-first implementations may satisfy the same invariant. Remaining test: one chain writes, the other disconnects, then reconnects and records the same receipt; verification becomes valid only after both records exist.

## Founder decision: Question 2 — executive Need, communication, and non-mediation

The Need smart contract is the executive function: it executes its specified conditions, and no completion point exists until those terms are satisfied. Ordinary progress messages are communication between participants, associated with the Need and retained as part of its history; they do not automatically become independent state transitions or require special conflict mediation. If a contract-defined operation requires an offline participant, that operation waits for them. Participants may voluntarily contact others or negotiate a different exchange under existing authority. Has-Needs does not mediate disputes or guarantee that people remain reachable. Do not add a general progress-merging workflow or autonomous resolution engine.

**Deliberate noncompetition:** Has-Needs is not a replacement for banking, payment processors, aid agencies, governments, or existing commercial infrastructure. It is designed as a neutral coordination, information-resolution, and reciprocal-evidence layer that these actors and individuals can use. Its contribution is more granular and timely evidence of expressed Needs, offered capabilities, accepted commitments, and realized exchanges. Efficiency gains and savings can be measured against observed outcomes; they should not be presumed. Avoid inventing custody, payment clearing, arbitration, or institutional displacement as default protocol functions.

## Founder decision: Question 3 — two distinct pooling forms

**Transport consolidation is not authority delegation.** Alice's individual shipment may travel alongside other packages because a transporter only departs with a full load. Alice retains authority over her item and its Need. The vendor agrees to transfer it to the shipper, the shipper accepts responsibility to deliver it, and Alice receives it at the end. This is a three-participant chain of agreed responsibility and custody, not a delegation of Alice's acceptance authority to the driver. Pooling the physical load does not pool ownership or control.

**Collective pooled Need:** Multiple participants may combine requirements, such as quantities of water after a disaster, into a pool Need. Joining that pool under its terms grants the pool's authorized representative the defined acceptance authority for the collective resource. The pooling act supplies the authority; no separate delegation subsystem is required. Preserve individual provenance and any terms of participation.

**Community is not geographic:** A Has-Needs community is any grouping of participants formed by agreement, relationship, or purpose. A location-based disaster group is only one example; a shipping cohort, remote collaboration, research group, or temporary association also qualifies. Do not silently equate community with neighborhood, town, or geographic jurisdiction.

**Specification correction needed:** The recent §8.1 wording suggesting that community pooling always delegates fulfillment authority is too broad. Revise it to distinguish physical/logistical pooling from an explicitly collective Need with representative acceptance authority. Confirm that existing community language does not impose a geographic definition.

