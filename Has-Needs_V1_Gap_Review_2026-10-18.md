# Has-Needs V1 gap review and Paradigm Delta comprehension audit

**Date:** 2026-10-18  
**Basis:** Current [V1 specification](./Has-Needs-Spec-v1.md), [Paradigm Delta](./Has-Needs_Paradigm_Delta_Review_2026-10-14.md), and [Assistant Orientation](./Has-Needs_Assistant_Orientation_2026-10-14.md).  
**Status:** Review and proposed validation agenda only. **V1 has not been changed.**

## Executive finding

The recent humanitarian, commercial, research, and economic insights largely **derive from V1's existing primitives**. Do not add a refugee state, disaster-recovery engine, monetary value requirement, centralized aid inventory, institution-owned identity, or global trust score. The next specification pass should focus on interoperability, concurrency, security, and failure recovery. New applications belong primarily in examples, implementation profiles, and tests.

**Editorial opening for recovery:** “Aid often arrives in shipments and scheduled distributions. People must adapt to whatever is available that day—even when their Needs arise earlier, later, or in a different order. Has-Needs reverses the starting point: each person can express a Need when it matters, and matching resources can be engaged as they become available.” This mechanism is universal, not disaster-specific.

## A. Existing coverage; no new primitive required

| Insight | V1 source | Assessment |
|---|---|---|
| A trapped person holds critical situational information needed by rescuers | §§1, 2, 20, 27–31, 40 | Clarify as reciprocal Has/Need value in introductory example; no price-equivalence or pay-to-rescue requirement |
| Parallel asynchronous progress | §§7.1, 9–10, 35, 38 | Already follows from independent Need/Working bindings; add concurrency tests rather than a new state |
| Refugee/newcomer recognition and QR community entry | §§14, 18, 35, 39 | Community invitation and cross-ontology example are useful; avoid compulsory refugee category |
| Nonmonetary, gifted, community-defined value | Part II, §§7–8, 13–14, 35 | Existing open grammar supports it; avoid prescribing a political economy |
| Standing commercial Needs evaluated privately | §§19.1–19.2, 22, 24.1 | Already specified; ensure tests prohibit disclosure of nonrespondents |
| Institutional attestations and revocable API projections | §24.1 | Already articulated; issuer and lifecycle profile needed |
| Crypto agility and possible post-quantum migration | §§40, 50 | Existing intent; not yet a migration protocol |
| Community-originated participatory research | §§7, 14, 35, 53.1 | Application of existing grammar; add research scenarios, not a separate research subsystem |

## B. Interoperability and failure-mode gaps

**G1 — Interrupted bilateral finalization (high).** §10 requires identical canonical receipts on all required personal chains, but the wire-level prepare/commit/retry protocol is unspecified. If A writes while B is offline, how is provisional versus final state represented, recovered, and protected against double finalization? **Proposed test:** crash at each finalization step, partition peers, replay messages, restore from backups; no conflicting canonical receipts and no false finalized state.

**G2 — Concurrent commitment of scarce Has (high).** §§9, 12, 35.2 prohibit unauthorized duplicate allocation but do not define reservation or conflict resolution when two disconnected communities match the same Has. **Proposed test:** concurrent offline bindings, delegated pool plus direct offer, conflicting releases; exactly the authorized commitments survive, with evidence of rejected conflicts.

**G3 — Need-owned journal convergence (high).** §7.1 explicitly leaves ordering, replication, checkpoints, and retention as implementation work. **Proposed test:** reorder, duplicate, omit, and delay signed journal entries among peers; reconstruct a consistent, auditable authorized history without permitting owner rewrites of counterpart evidence.

**G4 — Delegated endpoint handoff under partition (high).** §35.3 leaves delegation revocation, expiry, and concurrency open. **Proposed test:** an agency or community endpoint changes while offline and both old/new endpoints attempt action; enforce previously authorized scope without silent double commitment.

**G5 — Emergency information routing and safe escalation (high).** §§20, 27–31 define local-first protected discovery, but end-to-end delivery acknowledgment, priority, re-routing, and minimum necessary location disclosure need a reference profile. **Proposed test:** trapped individual offers situation/location within a specific rescue agreement; relay forwards without broad location exposure; responder receives useful information when a path exists; absence of bilateral receipt does not block rescue.

**G6 — QR invitation authenticity and inclusive entry (medium).** §39 describes portable onboarding but not a community-invitation trust profile. **Proposed test:** forged QR, stale community key, offline first contact, feature phone, screen reader, and language mismatch; invitation cannot silently obtain protected data or impersonate an authority.

**G7 — Cross-ontology translation safety (medium).** §§14, 18 allow local and shared meaning but lack an interoperable provenance/ambiguity format. **Proposed test:** translate informal and foreign skills to locally useful search terms, preserve source meaning, expose uncertainty, never silently turn equivalence into professional licensure or expose restricted community knowledge.

**G8 — Institutional attestation lifecycle (medium).** §24.1 allows scoped issuer assertions but leaves credential freshness, correction, revocation, issuer compromise, and offline verification profiles open. **Proposed test:** expired, superseded, fraudulent, and corrected bank/education attestations; no unauthorized access to the private chain.

**G9 — Cryptographic migration (medium).** §§40, 50 require replaceable techniques but do not specify algorithm IDs, signature suite negotiation, key succession, re-attestation, or historical verification after compromise. **Proposed test:** cross-version exchange, retired algorithm, migrated identity continuity, and archived receipt verification.

**G10 — Standing Need probing and privacy inference (medium).** §§19, 24 anticipate non-enumerability, but repeated adaptive matching can reveal predicates. **Proposed test:** malicious vendor issues variant Needs to infer private traits; demonstrate bounded disclosures and rate/scope controls.

**G11 — Completion with unreachable or unwilling participant (medium).** §10.1 intentionally leaves abandonment closure open. **Proposed test:** no response, dispute, incapacity, death, or unreachable endpoint; journal remains evidentiary without fabricated consent, and other independent Needs continue.

**G12 — Accessibility and low-bandwidth semantic equivalence (medium).** §§27–33, 39, 48 support multiple transports. **Proposed test:** one equivalent Need traverses graphical, SMS, speech, and low-bandwidth text pathways; consent and meaning do not silently change.

## C. Suggested V1.1 change control

1. **Clarifications only:** Introduce rescue as reciprocal information/capability exchange; distinguish asynchronous Need timing from scheduled institutional delivery; explicitly say this is universal behavior.
2. **Normative profiles to develop:** G1–G5 first; select canonical formats and failure semantics only after tabletop tests. Mark unsolved mechanisms openly.
3. **Examples/tests:** Community QR arrival, cross-ontology newcomer skill, independent concurrent recovery, community-originated research, private standing commerce, and institutional attestation lifecycle.
4. **No additional protocol states:** Retain HAS, NEED, WORKING; pending is Need-owned evidence; canonical resolved receipts remain privately held and byte-identical across required participants.
5. **No unearned claims:** Cryptographic agility is not current post-quantum security; ontology translation is not credential equivalence; receipt integrity is not physical truth. These are bounded engineering statements, not barriers to useful deployments.

## D. Naive-agent comprehension audit of the updated Paradigm Delta

**Methodological limitation:** This is a *fresh-reading simulation within the same assistant session*, not a blinded test by an independent model. It checks whether the document directly supplies the correct premises for eight questions; it cannot prove a naive model would apply them reliably. The Delta's new Section VIII supplies explicit correction-and-diagnostic pairs.

| Blind-style question | Correct inference supported by Delta | Reading result |
|---|---|---|
| What value does a trapped person provide? | Firsthand condition/location is an authorized Has needed by rescuers; rescue capability is the reciprocal Has | **Pass**: Section VIII explicit |
| Must a newcomer enroll in a refugee registry? | No; optional community QR, scoped ontology and voluntary participation | **Pass**: Section VIII explicit |
| Does disaster recovery need a special global scheduler? | No; ordinary independently progressing Needs/Working | **Pass**: Section VIII explicit |
| Who owns a bank's certification? | Issuer attests only its own fact; user controls authorized projection, not issuer's entire database | **Pass**, with lifecycle profile still open |
| Can a vendor see everyone matching its standing Need? | No; private local matching, disclosure only on affirmative participation | **Pass** |
| Are all signed interactions final receipts? | No; Working/pending evidence is not the identical bilateral final receipt | **Pass**, from earlier Delta sections |
| Is the system quantum-safe today? | No; replaceable cryptography enables a migration path | **Pass** |
| Is research limited to buying survey answers? | No; community questions and reciprocal participation can originate studies | **Pass** |

### Remaining naive-reader hazards

- **Document length and delayed corrections:** A new agent might read the original 14 October sections and miss Section VII/VIII appended at the end. **Improvement:** add a short 'read these corrections first' pointer at the top, without duplicating their explanations.
- **Conflation of aspiration and wire protocol:** The Delta needs an early reminder that design intentions guide reasoning, whereas V1 determines implementable behavior.
- **Unresolved failure mechanics:** The Delta should teach an assistant to say 'the architectural invariant is defined; the cross-partition mechanism remains an open implementation profile' instead of declaring a design impossible or inventing an unapproved mechanism.
- **Universal applicability:** Avoid treating parallel recovery, ontology translation, and reciprocal recognition as special refugee/disaster modules.
- **Location privacy nuance:** A person can deliberately authorize a precise rescue location to a specific recipient; that does not create a universally retrievable participant location field.

### Suggested independent blind test

Give a separate assistant only the Delta and eight questions above, without the V1 or this review. Require it to state what is architecturally fixed, what remains open, and what it would implement. Score for prohibited assumptions (global inventory, public chain, fourth state, passive recipient, mandatory payment, universal location lookup, vendor access to private matches, institution-owned identity). Then provide V1 and test whether it revises answers correctly. This independent test has **not** yet been performed.

## E. Founder decisions worth discussing before V1.1

The most consequential design questions are G1 (cross-chain finalization), G2 (concurrent Has commitment), G3 (journal convergence), and G4 (offline delegation handoff). These determine whether separate implementations can safely cooperate under partition. The other questions are important profiles and tests, but they need not block a limited implementation of the already-defined core.
