# Has-Needs V1 cross-document release audit — 20 October 2026

**Scope:** Editorial and architectural cross-review of [V1](./Has-Needs-Spec-v1.md), [Paradigm Delta](./Has-Needs_Paradigm_Delta_Review_2026-10-14.md), and [Research Companion](./RESEARCH_WHITE_PAPER_COMPANION.md), on branch `review/v1-reference-editorial-2026-10-14`. This is a **document audit**, not an executed implementation test, independent security assessment, empirical validation, or certification.

## Decision

**Research companion: editorial release candidate. V1: architectural release candidate, NOT implementation-conformance certified.** The core premises align across documents. Do not represent the reference tests as passed or the open security/serialization choices as production-ready. The Delta is interpretive, V1 normative, research companion non-normative.

## Traceability matrix

| Delta premise | V1 authority | Research treatment | Editorial finding |
|---|---|---|---|
| Participant-originated authority | Part II invariant 1; §§22–24 | §§1A, 1C; H8 | Aligned; no claim that a declaration automatically changes law |
| Declaration ≠ match ≠ acceptance ≠ receipt | Invariants 6–10; §§7–11 | §§1A, 2; H2–H4 | Aligned; integrity not physical truth |
| Grammar and designed emergence | Invariant 2; §§5–13, 35–39 | §§1A, 3; H9 | Aligned; contract complexity still requires measurement |
| Agency and trauma-informed design | §§1, 4.1, 53 | §1B; H7 | Aligned as hypothesis, not proven therapy |
| Non-enumerability and no universal ontology | Invariants 3–4, 11; §§14–19 | §§1, 1A, 3 | Aligned; empirical leakage evaluation outstanding |
| Trust without reputation score | Invariant 9; §23.1 | §1D; H10 | Aligned; grey-list is integrity flag, not social rank |
| Geographic possibility, not whereabouts | §§21, 31.1 | §§1, 1D; H8 | Aligned; side-channel tests outstanding |
| Bounded persona disclosure and revocation | §§22–25 | §1C; H8 | Aligned; copies already disclosed cannot be recalled |
| AI proposes, humans authorize | Invariant 10; §14.2 | §4; H4, H11 | Aligned; narrow preauthorization is deterministic |
| Communities and accountable governance | §§35–39 | §§1D, 3, 6 | Aligned; accepted obligations do not imply automatic legal enforcement |
| Delta as an AI primer | Delta reader orientation | §1E; H11 | Aligned; BIAS source contents not yet verified |

## Conformance and release blockers

**B1 — Canonical receipt encoding and multi-party atomicity.** V1 §10 requires byte-identical canonical receipts on all required private chains and explicitly treats delayed/missing copies differently from hash mismatch. Appendix A says exact encoding remains open. Define canonical serialization, hash domain separation, signing order, finalization/retry behavior under partition, and recovery from partial append; test these against §§10, 23.1 and tests T17–T19. A design document is not proof of atomic multi-device completion.

**B2 — Pending journal convergence and unresolved obligation lifecycle.** V1 §7.1 leaves journal ordering, replication, checkpoints, retention open; §10.1 leaves abandoned-binding closure open; §23.1 leaves journal comparison/reconciliation unspecified. Specify conflict handling, permissioned event visibility, replica convergence, and recovery without treating silence as consent or fabricating closure.

**B3 — Non-enumerability and privacy threat model.** V1 §§19, 21, 24, 31 claim network-level non-enumerability and no protocol operation returning actual participant position, while recognizing inference risks. Define attacker capabilities, query-rate/aggregation leakage, repeated predicate probes, colluding relays, metadata traffic analysis, and acceptance thresholds. Demonstrate via adversarial tests T16a–T16e, T16c, T28–T34.

**B4 — Cryptographic authorization and recovery.** V1 specifies replaceable cryptographic profiles but not a fully interoperable wire/permission scheme. Before implementation certification, select a test profile for persona capabilities, consent grant/revocation, key rotation, multi-device recovery, receipt attestations, and relay authentication; produce negative tests for forged/replayed grants and stale replicas.

**B5 — Implemented evidence is absent from this review.** V1 §52 explicitly says test cases are review cases, not passing results. Execute and publish T1–T35 (including subcases) with reproducible traces, failures, and independent review before claiming conformance. Human outcomes and disaster-cost hypotheses require separate field research.

## Editorial consistency findings

- **No invented fourth relation state:** floating is descriptive; pending is evidence; Working is the third relation; final receipt is an outcome. V1 §§7–11 and Delta agree.
- **No central reputation or custody:** receipt-linked evidence is human-interpreted. Grey-list for demonstrated hash discrepancy is distinct from judgment of physical facts.
- **No unconditional privacy claim:** the actual-position prohibition is a protocol requirement; threat-model testing remains necessary for side channels.
- **No conflation of economics with proof:** the one-time 5% proposal concerns mutually assessed *realized efficiency savings*, not total disaster losses; historical comparisons alone do not prove causality.
- **White-paper testability improved:** agency, sovereign disclosure, emergent composition, relationship evidence, and interpretive priming now have explicit falsifiable hypotheses H7–H11.
- **Editorial issue to monitor:** V1 §10 says all required participants must be ready for the same version, while participant-specific comments/exposure remain independently controlled. A canonical version must bind both parties' chosen metadata and access envelopes without giving either party an editorial veto; implement and test this exact boundary.
- **External BIAS protocol:** linked as a candidate companion, not audited or incorporated as normative text. Verify its actual current contents before claiming its rules are applied.

## Release gate

The **documentation cross-review is complete at the architectural level** and records no demonstrated contradiction that requires changing the three-state V1 core. **Final conformance certification is not complete** until B1–B5 are resolved and tested. Avoid replacing “release candidate” with “final validated” based solely on editorial review. Record future spec deltas against this audit rather than silently adding features.
