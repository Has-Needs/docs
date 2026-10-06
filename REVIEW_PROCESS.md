# Has-Needs Expert Review Process

**Purpose:** Turn expert criticism into reproducible tests and explicit architectural decisions.

Has-Needs review is not an endorsement process. Reviewers are invited to identify the smallest counterexample they can find.

## Review loop

Every substantive review should follow the same pattern:

`claim → challenge → test → result → specification decision`

### 1. Claim

Identify the specific architectural claim or invariant being examined.

Examples:
- network non-enumerability can coexist with useful emergency aggregation;
- canonical receipts remain verifiable across independent personal chains;
- chain-hop vetting exposes useful relationship evidence without creating reputation;
- Trust Kernel refresh avoids a privileged update authority;
- RGB/Data Story composition preserves provenance and permission boundaries.

### 2. Challenge

State the smallest scenario that may break the claim.

Prefer concrete failure cases over general concerns.

Good:
> Three colluding peers can make a fourth participant appear second-order trusted.

Less useful:
> The trust model seems risky.

### 3. Test

Turn the challenge into something observable.

A test may be:
- executable code;
- a protocol simulation;
- an adversarial message trace;
- a field scenario;
- a UX walkthrough;
- a privacy analysis;
- a mathematical argument;
- a tabletop disaster exercise.

The test should specify:
- initial conditions;
- actors;
- assumptions;
- sequence of events;
- expected invariant;
- observed result.

### 4. Result

Classify the outcome:

- **CONFIRMED** — the invariant survives the challenge.
- **CLARIFICATION** — the architecture survives, but the specification is ambiguous.
- **COUNTEREXAMPLE** — the invariant fails.
- **IMPLEMENTATION QUESTION** — the invariant is sound, but the mechanism remains unresolved.
- **NEW EVIDENCE NEEDED** — the question cannot yet be resolved without additional testing or field evidence.

### 5. Specification decision

Every significant result should end in one of four actions:

- no change;
- clarify wording;
- add or modify an implementation/conformance test;
- revise the architecture.

A challenge should not disappear into discussion history.

## Review etiquette

Strong criticism is welcome.

Please:
- attack the mechanism, not the person;
- distinguish architectural failure from implementation preference;
- identify assumptions explicitly;
- prefer minimal counterexamples;
- avoid proposing new primitives until showing why existing primitives are insufficient;
- cite external evidence where relevant;
- make uncertainty visible.

## Where to review

Central review:
https://github.com/Has-Needs/docs/issues/1

Specialist review threads:
- Security, Privacy & Cryptographic Boundaries — issue #2
- Distributed Systems, Receipts & Object Lifecycle — issue #3
- Humanitarian, Trauma-Informed & Field Operations — issue #4
- Identity, Chain-Hop Vetting & Trust Kernel — issue #5
- Jitterbug, Semantic Routing & Constrained Networks — issue #6
- UX, Accessibility, Globe/RGB Views & Data Stories — issue #7

Public Q&A:
Has-Needs organization Discussion #2

## Stable review baseline

Reviewers should evaluate the tagged expert-review snapshot rather than an evolving working copy:

`spec-v1.0-expert-review`

This allows later changes to be traced back to the challenge that caused them.

## Review record template

Use this structure when opening or replying to a review thread:

### Claim
<What specific invariant or mechanism is being challenged?>

### Counterexample / concern
<Smallest scenario that may break it.>

### Test
<How can the concern be reproduced or evaluated?>

### Result
CONFIRMED | CLARIFICATION | COUNTEREXAMPLE | IMPLEMENTATION QUESTION | NEW EVIDENCE NEEDED

### Evidence
<Code, trace, paper, field experience, calculation, screenshot, or reasoning.>

### Proposed consequence
<No change / wording clarification / new test / architectural revision.>

---

The goal is not to make Has-Needs immune to criticism.

The goal is to make every serious criticism useful.
