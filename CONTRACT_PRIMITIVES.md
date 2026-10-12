# Contract primitives — working list

Status: design draft, v0.3  
Design sessions: October 8–12, 2026  
Author: Om Goeckermann / Has-Needs, with drafting assistance from ChatGPT.

## Purpose and authority

Build a minimal, composable set of contract behaviors that ordinary people can select through simple interfaces. Money is optional. Has, Need, WORKING, receipts, and existing community context remain the vocabulary; this list introduces no new protocol object types.

This draft records the design direction developed in the October 8–12 discussions. The October 12 Cancel/Undo decision supersedes the earlier deal/no-deal proposal and is incorporated in the current V1 specification. The primitive decomposition below is a proposed starting list, not a finalized wire schema or executable implementation. It proposes explicit amendments to [Specification V1](./Has-Needs-Spec-v1.md); it does not silently override the frozen [expert-review baseline](https://github.com/Has-Needs/docs/tree/spec-v1.0-expert-review).

## Design decisions captured

- A Has stays simple: a declaration of available capability, quantity and context, with suggested semantic matches where useful.
- Need contracts discover compatible peers and coordinate actions under participant-authorized conditions.
- A distributable Has can retain its identity as available quantity changes. Automatic child Has creation is not required.
- Accepted portions enter WORKING. Remaining supply may stay available, subject to owner policy.
- Adding a Need to a pool can constitute explicit conditional commitment when the participant accepts the displayed terms. Joining a community alone is not commitment.
- Cancel completes the current accepted transaction and, on release, creates a reverse transaction for the other participant's approval. Both use the existing canonical receipt mechanism; there is no deal/no-deal type or outcome bit.
- Receipt writes are automatic and simultaneous. Any discrepancy between corresponding receipt hashes is treated as tampering and immediately grey-lists both participants until resolved; the chain-level flag propagates peer-to-peer through the shared ontology.
- Composable group receiving includes purchase, barter, reciprocal service, gifting and aid. Group governance is outside this initial scope.

## Starting primitive list

These are contract operations and conditions, not additional object classes.

| ID | Primitive | Minimal behavior | Example |
|---|---|---|---|
| P1 | Match | Seek compatible Has/Need objects within authorized semantic, proximity, time and disclosure scope. | Find nearby berries or a carrier along a route. |
| P2 | Commit conditionally | Authorize a quantity and terms subject to explicit conditions, expiry and withdrawal rules. | Receive 60 L if a 100 L pool fills by the deadline. |
| P3 | Compose Needs | Associate independently owned Needs and evaluate a shared quantity or other fulfillment condition. | Combine 60 L and 40 L requests without transferring ownership of either. |
| P4 | Negotiate within bounds | Propose and accept terms within each participant's delegated limits; return out-of-bounds changes for explicit approval. | Accept a specified price range or a delivery-for-dinner arrangement. |
| P5 | Trigger authorized action | Act when specified conditions are met and all required authorizations are present. | At 100 L committed, activate allocation and notify participants. |
| P6 | Allocate / bind | Commit an authorized portion of a Has into WORKING without allocating that portion twice. | Reserve 60 L from the same 100 L Has, leaving 40 L available. |
| P7 | Amend / Cancel / Undo | Amend with required consent; Cancel completes the current transaction and creates a reverse transaction for counterparty approval. | Propose reversal of a collection reservation; preserve the original receipt. |
| P8 | Complete / receipt | Record completion and actual exchange details in a canonical receipt shared identically by the parties. | Record 60 L delivered, or completion linked to a proposed reversal. |

Terms such as deadlines, quantity thresholds, incentives, collection points and release conditions are parameters composed with these behaviors. They are not separate object types. The exact minimal decomposition remains open to simplification.

## First compositions

### Direct receiving

Match → authorized agreement → allocate into WORKING → resolve with an outcome receipt.

The exchange may be paid, gifted or reciprocal. A buyer-facing interface can create the corresponding Need when the person specifies and accepts a quantity; a separate manual Need-writing step is unnecessary.

### Composable group receiving

1. An owner offers a distributable Has, such as 100 L water.
2. A purpose-scoped community provides context.
3. Participants voluntarily add Needs under the displayed pool terms.
4. Need contract behavior discovers compatible peers and combines conditional commitments.
5. The threshold and supplier authorization trigger the agreed allocation into WORKING.
6. Participating exchanges resolve through the existing receipt mechanism.

Example authorization: “Commit me to 60 L on these terms if the pool reaches 100 L before the deadline.”

Receipt boundaries across several recipients remain to be specified. Preserve each participant's authorization and the actual completed or reversed exchange.

### Scheduled distribution

Farmer Bob Farms → Saturday 10 a.m. departure sub-community → Has of 50 pints of berries.

Buyers contribute quantity-specific Needs. The contract may proceed at a threshold, at a departure cutoff with the committed quantity, or under another explicit owner-selected condition. A fill-the-load incentive is an agreed term.

The minimum farmer interface is photo, price, available quantity, departure time and collection arrangement. Payment can remain in person. Voice transcription with human confirmation is an input method, not a new contract primitive.

### Receiving with transport

A person seeking blueberries can match offers from multiple nearby farmers. Collection can occur at a marketplace or through a cyclist collecting several parcels in exchange for dinner.

Carrying capacity and dinner are Has objects; delivery and dinner requests are Needs. A delivery-dependent receiving commitment activates only when its required arrangements are authorized. Each participant retains their own terms and consent.

### Individual commercial participation

A vendor expresses a Need with audience criteria and an offered exchange. Matching users decide whether to participate and what to disclose. Negotiation remains individual; matching does not grant the vendor a demographic inventory.

## Additional basic transaction patterns

These are proposed user-selectable templates, not new protocol primitives. Each preserves individual authorization; none requires group voting or a collective identity.

| Pattern | Example | What must be expressed |
|---|---|---|
| Give / receive | Give 10 L of water without compensation. | Resource, quantity, recipient conditions and handover evidence. |
| Reciprocal exchange | Deliver parcels in exchange for dinner; exchange berries for money. | Two or more agreed contributions and their dependencies. Money is one possible contribution. |
| Temporary use / return | Borrow a pump until Sunday. | Permission to use, time window, custody, return condition and evidence. Ownership need not transfer. |
| Perform a service | Repair a bicycle or provide an hour of translation. | Desired result, capacity/time, acceptance conditions and optional reciprocal contribution. |
| Carry / hand over | Take market parcels to a recipient. | Pickup, authorized custody, destination, handover and optional compensation. |
| Grant bounded access | Share a data field or stream for a stated purpose and duration. | Authorized recipient, scope, duration and revocation/expiry behavior. Revocation stops future access; it cannot retract disclosed copies. |
| Repeat a bounded exchange | Receive five pints each Saturday for four weeks. | Repeated occurrence, quantity, authorization limits, stop conditions and separate outcomes. |
| Fulfill in stages | Supply materials, then install them. | Separately observable obligations, dependencies and outcomes; later work must not erase earlier completed exchange. |

Direct purchase and barter are variants of reciprocal exchange. Lending and rental are variants of temporary use, with compensation optional. Reservations are conditional commitments, not another transaction primitive.

## Reduction pass 1 — candidate minimal contract operations

The first eight-item list mixes discovery, conditions, composition and state-changing operations. This reduction proposes three contract operations, with declarative terms around them. It is a hypothesis to test, not an adopted replacement for P1–P8.

| Candidate operation | Meaning | Irreducible effect |
|---|---|---|
| Authorize | A participant signs exact terms or bounded permission to act when specified conditions hold. | Establish consent and its limits. |
| Bind | Activate the compatible authorized commitments, allocating the relevant portions into WORKING. | Establish an active obligation and prevent incompatible allocation. |
| Resolve | Complete the binding and preserve its canonical receipt; Cancel composes completion with a proposed reverse transaction. | Record the actual exchange and apply authorized resource consequences exactly once. |

An authorization can permit immediate binding or conditional binding. It does not require another UI approval when the previously accepted conditions are met. These operation names are an analytical decomposition, not additional protocol relation states.

### Where the original eight items go

| Original item | Reduced role |
|---|---|
| P1 Match | Discovery service used by the Need contract; proposes candidates without authority to commit anyone. |
| P2 Commit conditionally | Authorize with a predicate, deadline and withdrawal conditions. |
| P3 Compose Needs | References and aggregate conditions over independently authorized Needs. |
| P4 Negotiate within bounds | Exchange proposals; authorize a chosen proposal or delegate bounded choice. |
| P5 Trigger authorized action | Evaluate a condition and invoke a permitted operation; not unrestricted execution. |
| P6 Allocate / bind | Bind. |
| P7 Amend / Cancel / Undo | Reauthorize affected terms and safely update the binding, or complete the current transaction and propose a linked reverse transaction for counterparty approval. Mid-binding amendment remains a mechanism to specify. |
| P8 Resolve / receipt | Resolve. |

Cancel preserves completion of the current transaction and proposes its reversal. The reverse transaction requires the other participant's approval. Resource consequences must reflect the actual exchange and agreed reversal; closing a commitment does not manufacture physical supply.

### Minimum terms to carry through the reduction

- Participants and the authority each grants.
- Referenced Has/Need objects and accepted revisions.
- Contribution: quantity, capability, access scope or desired result.
- Activation and dependency conditions, including time and thresholds.
- Permitted changes, withdrawal and release conditions.
- Evidence required to resolve and the resource consequences of each outcome.
- Disclosure permissions.

These are dimensions of existing contract/context fields, not a proposed set of new objects. Price, incentives, routes, collection points and pool totals are values or conditions within them.

### Apply the same operations to different transactions

| Pattern | Authorize | Bind | Resolve |
|---|---|---|---|
| Gift | Agree to give/receive a quantity. | Reserve it for the recipient. | Record handover; use Cancel/Undo if reversal is requested. |
| Reciprocal exchange | Agree to all contributions and dependencies. | Commit the relevant resources/capacities. | Record actual exchange; do not assume physical simultaneity. |
| Temporary use | Agree to use and return conditions. | Reserve the capability for the agreed interval. | Close after the agreed lifecycle; record use and return evidence separately in the terms/details. |
| Service | Agree to the result and any contribution. | Commit the service capacity. | Record accepted work; use Cancel/Undo if reversal is requested. |
| Transport | Agree to pickup and handover obligations. | Commit carrying capacity and the relevant arrangement. | Record the actual custody/handover outcome. |
| Bounded access | Agree to permitted access and stop conditions. | Activate the authorized access. | Record what was provided and end the grant under its terms. |
| Repeated exchange | Authorize bounded recurrence. | Bind each occurrence when its conditions hold. | Receipt each occurrence without rewriting prior outcomes. |
| Staged fulfillment | Authorize obligations and dependencies. | Bind eligible stages. | Resolve each agreed stage/binding; preserve mixed results. |
| Group receiving | Authorize each person's conditional quantity. | Bind compatible allocations when the threshold and supplier authorization hold. | Resolve the agreed exchange boundaries without treating everyone as one decision maker. |

### Counterexamples to test before reducing further

1. **Loan not returned:** use was provided while the return obligation remains unmet. Define when the binding completes and what a proposed reversal requires; do not equate value exchange with successful return.
2. **One side of barter performs:** retain actual exchange details for both contributions and obligation disposition; do not claim atomic physical exchange.
3. **Amendment while WORKING:** replacing terms must not momentarily free a committed quantity or erase the prior accepted evidence. Decide whether amendment composes safely from these operations or needs its own operation.
4. **Revocation during a data stream:** stopping a live permission can happen before final resolution. Determine whether this is existing OCA behavior or a distinct contract operation that the three-operation model omits.
5. **Parallel pool commitments:** simultaneous threshold checks must not allocate the same quantity twice. Reduction does not solve allocation authority.
6. **No-show or lost connectivity:** an expired communication timer is not evidence of no physical exchange. Apply only authorized resolution rules and retain unknown outcomes as unresolved.

Current reduction result: eight initial items reduce provisionally to three state-changing contract operations plus discovery, composition and declarative conditions. Amendment and live revocation are the strongest remaining tests of whether three is sufficient. Do not force them into a smaller vocabulary by hiding necessary behavior.

## Quantity and identity

Proposed model: stable Has identity, revisable availability, protected accepted commitments, immutable outcome receipts.

| Event | Available | In WORKING | Exchanged |
|---|---:|---:|---:|
| Offer 100 L | 100 L | 0 L | 0 L |
| Allocate 60 L | 40 L | 60 L | 0 L |
| Complete 60 L | 40 L | 0 L | 60 L |

A Cancel/Undo reversal applies only the authorized resource consequences and preserves the original receipt. A receipt references the Has, the relevant accepted terms/revision, and actual quantity. Creating another Has for a remainder remains an explicit owner/contract choice.

The allocation authority and concurrency mechanism are not yet selected. Partitioned peers must not independently certify conflicting allocations. An offline proposal cannot be treated as confirmed solely because a cached Has showed availability.

## Completion, Undo and ambient evidence

Use one canonical receipt mechanism. Cancel completes the current accepted
transaction and, on release, creates a reverse transaction for the other
participant's approval. The original receipt remains immutable; the reverse
transaction references it and completes only after approval. Both are written
to participant chains through the same mechanism.

There is no deal/no-deal receipt type or outcome bit. Record the actual exchange
and agreed reversal without asserting a handover that never occurred.

Unresolved WORKING and completed/reverse transaction history can inform ambient
evidence for participant-selected filters. They do not automatically establish
blame or fraud and do not create a universal stored trust score.

Receipt-hash discrepancies are a separate integrity signal: because identical
receipt writes are automatic and simultaneous, any discrepancy is treated as
tampering and immediately grey-lists both participants until resolved. The
chain-level flag is propagated peer-to-peer through the shared ontology.
Verification compares corresponding receipt hashes, not local chain pointers
or competing truth claims.

Loss of connectivity alone does not cancel a commitment. Physical handover and
later synchronization must not cause delivered goods to be reoffered automatically.

## Smallest checks

- Two concurrent requests cannot both allocate the same remaining quantity.
- One 60 L allocation can complete while the original Has continues to offer 40 L, without a child Has.
- Cancel completes the current transaction and proposes a linked reverse transaction; reversal requires counterparty approval and applies its resource effects exactly once.
- Replayed acceptance, release or receipt messages do not repeat their effects.
- A pool acts only within every affected participant's authorization.
- Deadline, below-threshold, withdrawal and late-arrival behavior are explicit.
- Text, voice, SMS and screen-reader presentations preserve quantities, conditions, consent and pending status.
- Counterpart copies verify the same canonical receipt, while personal chain entries retain their own previous pointers.

## Open specification work

1. Allocation authority, revision ordering and recovery under partition.
2. How completion and a proposed reversal remain verifiable if one party disappears or refuses approval; a unilateral proposal must not masquerade as an approved reverse transaction.
3. How an accepted WORKING binding remains verifiable before resolution, so abandonment cannot erase it.
4. Disclosure and participant continuity needed to inspect ambient evidence across objects without creating a globally enumerable history.
5. Pool membership changes, excess demand and receipt boundaries for multiple recipients.
6. Validate the proposed Authorize / Bind / Resolve reduction against amendment, live revocation, loans, asymmetric exchange and partition; retain an additional operation if composition cannot preserve their semantics.

## Explicit V1 amendment targets

- §§9, 12 and 51: permit portion-level WORKING and continued availability under the same Has identity; remove automatic remainder creation as the default for this pattern.
- §§10–11, invariant 8 and Appendix A.4: Cancel/Undo is now incorporated in current V1; retain a linked reverse transaction rather than a deal/no-deal outcome bit.
- §23.1: hash-discrepancy grey-listing is now incorporated in current V1; further ambient-evidence filtering remains subject to review without a universal reputation score.
- §35 and related contract descriptions: document conditional participation and composable group receiving within existing community context.

Related expert review: [distributed systems #3](https://github.com/Has-Needs/docs/issues/3), [routing #6](https://github.com/Has-Needs/docs/issues/6), [accessible renderers #7](https://github.com/Has-Needs/docs/issues/7).
