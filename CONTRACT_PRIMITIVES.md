# Contract primitives — working list

Status: design draft, v0.4  
Design sessions: October 8–13, 2026  
Author: Om Goeckermann / Has-Needs, with drafting assistance from ChatGPT.

## Purpose and authority

Has-Needs expresses ordinary agreements through a minimal, composable set of contract behaviors. Money is optional. A **Need uses the eUTXO blueprint** for its conditions and transitions; a **Has uses the NFT blueprint** for object identity and provenance. Working, Pending, and receipts record the agreement lifecycle within Has-Needs' independent protocol.

This document develops contract operations for the [Has-Needs V1 architecture](./Has-Needs-Spec-v1.md). Accepted agreements and authorized progress remain in Pending; agreed resolutions generate reciprocal receipts. The primitive decomposition is a working design for expert evaluation, with open implementation details noted where relevant.

## Design decisions captured

- A Has stays simple: a declaration of available capability, quantity and context, with suggested semantic matches where useful.
- Need contracts discover compatible peers and coordinate actions under participant-authorized conditions.
- Remaining amounts, balance tracking, and portion allocation belong to an optional distribution Need smart-contract subtype, not the basic protocol.
- The core binds authorized Has/Need relationships into WORKING and records their resolution. Distribution subtypes define any quantity-specific execution and lineage rules.
- Adding a Need to a pool can constitute explicit conditional commitment when the participant accepts the displayed terms. Joining a community alone is not commitment.
- Accepted Working commitments and authorized progress persist in the Need-owned pending journal. Mutual cancellation resolves the binding with a final receipt describing the exchange and agreed release.
- Receipt writes are automatic and simultaneous. Any discrepancy between corresponding receipt hashes is treated as tampering and immediately grey-lists both participants until resolved; the chain-level flag propagates peer-to-peer through the shared ontology.
- Composable group receiving includes purchase, barter, reciprocal service, gifting and aid. Group governance is outside this initial scope.

## Starting primitive list

These are candidate contract operations and conditions, not additional object classes or a fixed core instruction set. Quantity examples below belong to optional Need contract subtypes; they do not make remaining-amount tracking a core function.

| ID | Primitive | Minimal behavior | Example |
|---|---|---|---|
| P1 | Match | Seek compatible Has/Need objects within authorized semantic, proximity, time and disclosure scope. | Find nearby berries or a carrier along a route. |
| P2 | Commit conditionally | Authorize a quantity and terms subject to explicit conditions, expiry and withdrawal rules. | Receive 60 L if a 100 L pool fills by the deadline. |
| P3 | Compose Needs | Associate independently owned Needs and evaluate a shared quantity or other fulfillment condition. | Combine 60 L and 40 L requests without transferring ownership of either. |
| P4 | Negotiate within bounds | Propose and accept terms within each participant's delegated limits; return out-of-bounds changes for explicit approval. | Accept a specified price range or a delivery-for-dinner arrangement. |
| P5 | Trigger authorized action | Act when specified conditions are met and all required authorizations are present. | At 100 L committed, activate allocation and notify participants. |
| P6 | Bind | Activate an authorized Has/Need agreement in WORKING. | Accept a delivery agreement; an optional distribution subtype separately handles quantities. |
| P7 | Amend / release | Amend with required consent or agree to end a Working binding; preserve its journal history. | Mutually release an unfulfilled collection reservation. |
| P8 | Resolve / receipt | Record the agreed final resolution, actual exchange, and obligation disposition in a canonical receipt shared identically by the parties. | Record 60 L delivered, an agreed partial fulfillment, or mutual cancellation. |

Terms such as deadlines, quantity thresholds, incentives, collection points and release conditions are parameters composed with these behaviors. They are not separate object types. The exact minimal decomposition remains open to simplification.

## First compositions — optional Need contract types

### Direct receiving

Match → authorized agreement → bind into WORKING → resolve with an outcome receipt.

The exchange may be paid, gifted or reciprocal. A buyer-facing interface can create the corresponding Need when the person specifies and accepts a quantity; a separate manual Need-writing step is unnecessary.

### Composable group receiving

1. An owner offers a distributable Has, such as 100 L water.
2. A purpose-scoped community provides context.
3. Participants voluntarily add Needs under the displayed pool terms.
4. Need contract behavior discovers compatible peers and combines conditional commitments.
5. The threshold and supplier authorization trigger the agreed allocation into WORKING.
6. Participating exchanges resolve through the existing receipt mechanism.

Example authorization: “Commit me to 60 L on these terms if the pool reaches 100 L before the deadline.”

Receipt boundaries across several recipients remain to be specified. Preserve each participant's authorization and the actual exchange and agreed resolution.

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
| Bind | Activate compatible authorized Has/Need commitments into WORKING. | Establish an active obligation within the accepted authority. |
| Resolve | Resolve the binding with the required consent and preserve its canonical final receipt; retain pending journal evidence. | Record the actual exchange and apply authorized resource consequences exactly once. |

An authorization can permit immediate binding or conditional binding. It does not require another UI approval when the previously accepted conditions are met. These operation names are an analytical decomposition, not additional protocol relation states.

### Where the original eight items go

| Original item | Reduced role |
|---|---|
| P1 Match | Discovery service used by the Need contract; proposes candidates without authority to commit anyone. |
| P2 Commit conditionally | Authorize with a predicate, deadline and withdrawal conditions. |
| P3 Compose Needs | References and aggregate conditions over independently authorized Needs. |
| P4 Negotiate within bounds | Exchange proposals; authorize a chosen proposal or delegate bounded choice. |
| P5 Trigger authorized action | Evaluate a condition and invoke a permitted operation; not unrestricted execution. |
| P6 Bind | Bind; any quantity allocation is subtype-specific execution. |
| P7 Amend / release | Reauthorize affected terms and safely update the binding, or mutually resolve it and record the agreed release. Mid-binding amendment remains a mechanism to specify. |
| P8 Resolve / receipt | Resolve. |

Mutual cancellation records what occurred and the agreed release. Pending history remains intact.

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
| Gift | Agree to give/receive a quantity. | Reserve it for the recipient. | Record handover or the agreed cancellation and release. |
| Reciprocal exchange | Agree to all contributions and dependencies. | Commit the relevant resources/capacities. | Record actual exchange; do not assume physical simultaneity. |
| Temporary use | Agree to use and return conditions. | Reserve the capability for the agreed interval. | Close after the agreed lifecycle; record use and return evidence separately in the terms/details. |
| Service | Agree to the result and any contribution. | Commit the service capacity. | Record accepted work and the agreed disposition of remaining obligations. |
| Transport | Agree to pickup and handover obligations. | Commit carrying capacity and the relevant arrangement. | Record the actual custody/handover outcome. |
| Bounded access | Agree to permitted access and stop conditions. | Activate the authorized access. | Record what was provided and end the grant under its terms. |
| Repeated exchange | Authorize bounded recurrence. | Bind each occurrence when its conditions hold. | Receipt each occurrence without rewriting prior outcomes. |
| Staged fulfillment | Authorize obligations and dependencies. | Bind eligible stages. | Resolve each agreed stage/binding; preserve mixed results. |
| Group receiving | Authorize each person's conditional quantity. | Bind compatible allocations when the threshold and supplier authorization hold. | Resolve the agreed exchange boundaries without treating everyone as one decision maker. |

### Counterexamples to test before reducing further

1. **Loan not returned:** use was provided while the return obligation remains unmet. Define when the binding completes and how remaining obligations are resolved; do not equate value exchange with successful return.
2. **One side of barter performs:** retain actual exchange details for both contributions and obligation disposition; do not claim atomic physical exchange.
3. **Amendment while WORKING:** replacing terms must not momentarily free a committed quantity or erase the prior accepted evidence. Decide whether amendment composes safely from these operations or needs its own operation.
4. **Revocation during a data stream:** stopping a live permission can happen before final resolution. Determine whether this is existing OCA behavior or a distinct contract operation that the three-operation model omits.
5. **Parallel pool commitments:** simultaneous threshold checks must not allocate the same quantity twice. Reduction does not solve allocation authority.
6. **No-show or lost connectivity:** an expired communication timer is not evidence of no physical exchange. Apply only authorized resolution rules and retain unknown outcomes as unresolved.

Current reduction result: eight initial items reduce provisionally to three state-changing contract operations plus discovery, composition and declarative conditions. Amendment and live revocation are the strongest remaining tests of whether three is sufficient. Do not force them into a smaller vocabulary by hiding necessary behavior.

## Optional distribution Need smart-contract subtype

Remaining-quantity management is not a basic Has-Needs function. A specialized
Need smart contract can execute it where required. This proposed subtype is a
contract template over the existing grammar, not a new core protocol object.

The subtype would define quantity units, authorized allocation, remaining supply,
release, concurrency, and resulting lineage. The following is one candidate
behavior to evaluate, not a mandatory stable-Has-identity policy:

| Event | Available | In Working | Exchanged |
|---|---:|---:|---:|
| Offer 100 L | 100 L | 0 L | 0 L |
| Allocate 60 L | 40 L | 60 L | 0 L |
| Fulfill 60 L | 40 L | 0 L | 60 L |

Under this candidate, the Has retains its identity. A different subtype may
define explicit child-object lineage. Neither behavior belongs in the core
invariants. Final receipts still record actual exchange and agreed resolution.
The subtype must specify concurrent allocation and recovery before it can claim
to prevent conflicting quantities; cached availability is not fresh authority.

## Pending journals, resolution, and ambient evidence

Acceptance into Working creates evidence in the Need-owned append-only pending
journal. Authorized progress and unresolved commitments remain there. The final
receipt records the agreed resolution and actual exchange: fulfillment, mutual
cancellation, or agreed partial fulfillment. Receipts append in resolution order,
not acceptance order. Resolution records the agreed outcome through the same canonical receipt structure.

A unilateral cancellation request or silence is not mutual resolution. Closure
when one party disappears remains an open mechanism. Pending evidence must survive.
Unresolved commitments and disclosed resolution history can inform personal filters
without automatically assigning blame or creating a stored universal trust score.

Because receipt writes are automatic and simultaneous, corresponding canonical
receipt hashes should never differ. Any discrepancy is treated as tampering;
both participants are immediately grey-listed until resolved, and the chain-level
flag propagates peer-to-peer through the shared ontology. Local chain pointers,
missing copies, and incomplete journal synchronization are not a demonstrated
discrepancy between corresponding canonical receipt hashes.

Loss of connectivity alone does not cancel a commitment. Physical handover and
later synchronization must not cause delivered goods to be reoffered automatically.

## Communities, delegation, and shipper terms

An open-ended community Need retains its execution context while individual
bindings resolve. Sharing an object grants visibility, pooling grants explicitly
bounded collective authority, and clustering retains required individual approval.
Subcommunities keep separate journals, permissions, and conversations; parent access
does not imply subgroup access. Hosting does not itself confer authority to act.

An offline contributor's pool can act under prior delegation. Every interaction
contacts the relevant owner or expressly authorized endpoint. Owner/delegate
handoff, revocation, expiry, and conflicting allocations remain mechanisms to test.
“I Need a friendly node” uses the same ongoing community model for storage, relay,
and any explicitly delegated execution.

Shipper terms include capacity, allocated items, authorization cutoff, physical
readiness, departure, delivery evidence, and missed-readiness consequences. An
absent item is not shipped; later shipment under changed terms requires the
applicable authorization. A shipper is a contract role to decompose, not one
assumed indivisible primitive.

The Authorize / Bind / Resolve reduction must also be checked against journal
append, association, delegated execution, and continuing hosting. Its minimality
is not yet established.

## Smallest checks

- For the optional distribution subtype, concurrent requests cannot allocate the same quantity twice.
- For the candidate stable-identity distribution subtype, a 60 L allocation can resolve while the original Has offers 40 L; the basic protocol does not require this accounting.
- Mutual cancellation preserves Pending history and records the agreed resolution and release exactly once.
- B may resolve before earlier-accepted A; final receipts append in resolution order.
- A silent participant leaves an unresolved, evidenced obligation, not fabricated mutual closure.
- Replayed acceptance, release or receipt messages do not repeat their effects.
- A pool acts only within every affected participant's authorization.
- Deadline, below-threshold, withdrawal and late-arrival behavior are explicit.
- Text, voice, SMS and screen-reader presentations preserve quantities, conditions, consent and pending status.
- Counterpart copies verify the same canonical receipt, while personal chain entries retain their own previous pointers.

## Open specification work

1. Optional distribution-subtype allocation authority, revision ordering, and recovery under partition.
2. How an abandoned binding can eventually close if a participant disappears; a unilateral claim must not masquerade as mutual agreement.
3. How an accepted WORKING binding remains verifiable before resolution, so abandonment cannot erase it.
4. Disclosure and participant continuity needed to inspect ambient evidence across objects without creating a globally enumerable history.
5. Pool membership changes, excess demand and receipt boundaries for multiple recipients.
6. Validate the proposed Authorize / Bind / Resolve reduction against amendment, live revocation, loans, asymmetric exchange and partition; retain an additional operation if composition cannot preserve their semantics.

## V1 alignment and remaining work

- §§7–12 and invariant 8 describe pending evidence and final resolution. §12 places quantity and remainder handling in optional distribution Need contract subtypes. Journal ordering, subtype allocation, and abandoned-binding closure remain open.
- §23.1 preserves canonical hash-discrepancy grey-listing and separates it from incomplete journal synchronization and contextual interaction evidence.
- §§35–37 distinguish ongoing communities, sharing, pooling, clustering, delegation, and isolated subgroup conversations.
- Appendix A is illustrative, not a frozen wire schema. Final resolution fields and journal references require implementation review.

Related expert review: [distributed systems #3](https://github.com/Has-Needs/docs/issues/3), [routing #6](https://github.com/Has-Needs/docs/issues/6), [accessible renderers #7](https://github.com/Has-Needs/docs/issues/7).

