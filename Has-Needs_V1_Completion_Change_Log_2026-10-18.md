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
