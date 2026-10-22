# Has-Needs Governance

Has-Needs currently uses a **benevolent-dictator / lead-maintainer model**.

The project welcomes technical criticism, implementation proposals, experiments, pull requests, design challenges, and research collaboration. Contributors are encouraged to challenge assumptions and propose better mechanisms.

At the same time, architectural coherence matters. Until a different governance model is deliberately adopted, the project lead retains final authority over:

- the canonical Has-Needs specification;
- protocol invariants and version boundaries;
- acceptance of normative architectural changes;
- release/version designation;
- resolution of design disputes that cannot be settled by evidence or consensus.

This model is intended to preserve a coherent architecture while the project is still proving its foundations, not to discourage participation.

## Decision principle

Strong proposals should win on evidence.

Changes that improve sovereignty, privacy, resilience, accessibility, semantic simplicity, inspectability, or demonstrated real-world performance are welcome even when they challenge earlier design choices.

## Community-tested transparency

Security-sensitive mechanisms, especially the Trust Kernel, should be inspectable, testable, reproducible where practical, and open to adversarial review.

Authority should come from transparent rules and evidence rather than from an opaque central service.

## Normative authority

[Has-Needs Specification V1](./Has-Needs-Spec-v1.md) is the current canonical architectural document.

Experimental implementations, persona scenarios, historical documents, candidate technology choices, and prototypes may inform the protocol but do not supersede the specification unless explicitly incorporated into a later version.

## Future governance

As the contributor community matures, governance may evolve. Any transition away from the current model should be explicit, documented, and designed to preserve both participant sovereignty and architectural coherence.

## Governance of a participating Community

The repository's maintenance model above is separate from a Community's chosen governance. A Community can form through an open-ended, one-to-many Need smart contract specifying its purpose, DAO policies, responsible parties, delegation, and permissions. Its Has and Needs remain connected in the WORKING state while that contract executes. Streaming communications to secure storage preserves those permissions. See [the WORKING state, delegation, and streams](./WORKING_CONTRACTS_AND_DELEGATION.md).
