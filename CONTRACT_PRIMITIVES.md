# Contract primitives — working list

Status: design draft, v0.2  
Design session: October 8, 2026  
Author: Om Goeckermann / Has-Needs, with drafting assistance from ChatGPT.

## Purpose and authority

Build a minimal, composable set of contract behaviors that ordinary people can select through simple interfaces. Money is optional. Has, Need, WORKING, receipts, and existing community context remain the vocabulary; this list introduces no new protocol object types.

This draft records the design direction developed in the October 8 discussion. The primitive decomposition below is a proposed starting list, not a finalized wire schema or executable implementation. It proposes explicit amendments to [Specification V1](./Has-Needs-Spec-v1.md); it does not silently override the frozen [expert-review baseline](https://github.com/Has-Needs/docs/tree/spec-v1.0-expert-review).

## Design decisions captured

- A Has stays simple: a declaration of available capability, quantity and context, with suggested semantic matches where useful.
- Need contracts discover compatible peers and coordinate actions under participant-authorized conditions.
- A distributable Has can retain its identity as available quantity changes. Automatic child Has creation is not required.
- Accepted portions enter WORKING. Remaining supply may stay available, subject to owner policy.
- Adding a Need to a pool can constitute explicit conditional commitment when the participant accepts the displayed terms. Joining a community alone is not commitment.
- Resolved accepted interactions produce one receipt structure with an outcome bit: 1 = deal/value exchange; 0 = no-deal/no exchange. Unresolved WORKING is not automatically 0.
- No-deal is an outcome, not a fault finding. Its occurrence can inform an ambient metric without requiring an explanation.
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
| P7 | Amend / release | Amend accepted commitments with required consent, or release them under agreed conditions. | Cancel a collection reservation and restore its unexchanged quantity. |
| P8 | Resolve / receipt | Record the authorized outcome and actual exchange details in a canonical receipt shared by the parties. | Record 60 L delivered, or close an interaction as no-deal. |

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

Receipt boundaries for mixed outcomes across several recipients remain to be specified. Do not collapse a mixture of completed and uncompleted exchanges into one misleading group-wide outcome bit.

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
| Resolve | Close the binding under its authorized outcome rules and preserve the canonical outcome receipt. | Record deal/no-deal and apply the specified resource consequences exactly once. |

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
| P7 Amend / release | Proposed composition: reauthorize affected terms and safely update the binding, or Resolve when the agreement ends. Mid-binding amendment remains a mechanism to specify. |
| P8 Resolve / receipt | Resolve. |

No-deal closure releases only what remains unexchanged. A partial deal records what occurred and releases any unfulfilled remainder under the agreed closure terms. Closing a commitment does not manufacture physical supply.

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
| Gift | Agree to give/receive a quantity. | Reserve it for the recipient. | Record handover or no-deal. |
| Reciprocal exchange | Agree to all contributions and dependencies. | Commit the relevant resources/capacities. | Record actual exchange; do not assume physical simultaneity. |
| Temporary use | Agree to use and return conditions. | Reserve the capability for the agreed interval. | Close after the agreed lifecycle; record use and return evidence separately in the terms/details. |
| Service | Agree to the result and any contribution. | Commit the service capacity. | Record accepted work or no-deal under the terms. |
| Transport | Agree to pickup and handover obligations. | Commit carrying capacity and the relevant arrangement. | Record the actual custody/handover outcome. |
| Bounded access | Agree to permitted access and stop conditions. | Activate the authorized access. | Record what was provided and end the grant under its terms. |
| Repeated exchange | Authorize bounded recurrence. | Bind each occurrence when its conditions hold. | Receipt each occurrence without rewriting prior outcomes. |
| Staged fulfillment | Authorize obligations and dependencies. | Bind eligible stages. | Resolve each agreed stage/binding; preserve mixed results. |
| Group receiving | Authorize each person's conditional quantity. | Bind compatible allocations when the threshold and supplier authorization hold. | Resolve the agreed exchange boundaries without treating everyone as one decision maker. |

### Counterexamples to test before reducing further

1. **Loan not returned:** use was provided, so outcome 1 may coexist with an unmet return obligation. The bit indicates exchange, not complete performance. Define when the binding closes; do not equate value exchange with successful return.
2. **One side of barter performs:** a single bit cannot describe both contributions. Retain actual exchange details and obligation disposition; do not claim atomic physical exchange.
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

A no-deal release instead restores the unexchanged allocation under the agreed terms. A receipt references the Has, the relevant accepted terms/revision, and actual quantity. Creating another Has for a remainder remains an explicit owner/contract choice.

The allocation authority and concurrency mechanism are not yet selected. Partitioned peers must not independently certify conflicting allocations. An offline proposal cannot be treated as confirmed solely because a cached Has showed availability.

## Outcome and ambient evidence

One receipt type, with:

- outcome = 1: value exchange occurred; record the actual exchange.
- outcome = 0: the accepted interaction resolved without value exchange.
- no final outcome receipt: the binding remains unresolved, pending the applicable resolution rules.

A partial exchange can have outcome 1; actual quantities and agreed closure establish what occurred. The bit alone does not claim complete satisfaction of every original term.

No-deal frequency and unresolved bindings may provide ambient interaction evidence for participant-selected filters. They do not automatically establish blame or fraud. No universal stored trust score is required.

Loss of connectivity alone does not cancel a commitment. Physical handover and later synchronization must not cause delivered goods to be reoffered automatically.

## Smallest checks

- Two concurrent requests cannot both allocate the same remaining quantity.
- One 60 L allocation can complete while the original Has continues to offer 40 L, without a child Has.
- A no-deal closure releases only the unexchanged allocation, exactly once.
- Replayed acceptance, release or receipt messages do not repeat their effects.
- A pool acts only within every affected participant's authorization.
- Deadline, below-threshold, withdrawal and late-arrival behavior are explicit.
- Text, voice, SMS and screen-reader presentations preserve quantities, conditions, consent and pending status.
- Counterpart copies verify the same canonical receipt, while personal chain entries retain their own previous pointers.

## Open specification work

1. Allocation authority, revision ordering and recovery under partition.
2. What evidence establishes no-deal if one party disappears or refuses to attest; a unilateral claim must not masquerade as mutual agreement.
3. How an accepted WORKING binding remains verifiable before resolution, so abandonment cannot erase it.
4. Disclosure and participant continuity needed to inspect ambient evidence across objects without creating a globally enumerable history.
5. Pool membership changes, excess demand and receipt boundaries for multiple recipients.
6. Validate the proposed Authorize / Bind / Resolve reduction against amendment, live revocation, loans, asymmetric exchange and partition; retain an additional operation if composition cannot preserve their semantics.

## Explicit V1 amendment targets

- §§9, 12 and 51: permit portion-level WORKING and continued availability under the same Has identity; remove automatic remainder creation as the default for this pattern.
- §§10–11, invariant 8 and Appendix A.4: extend canonical receipt semantics to deal/no-deal outcomes of accepted interactions.
- §23.1: clarify how authorized outcome evidence supports live inspection and personal filtering without a universal reputation score.
- §35 and related contract descriptions: document conditional participation and composable group receiving within existing community context.

Related expert review: [distributed systems #3](https://github.com/Has-Needs/docs/issues/3), [routing #6](https://github.com/Has-Needs/docs/issues/6), [accessible renderers #7](https://github.com/Has-Needs/docs/issues/7).
