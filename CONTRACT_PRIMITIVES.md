# Contract primitives — working list

Status: design draft, v0.1  
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
6. Whether P1–P8 can be reduced further into a smaller selectable contract vocabulary.

## Explicit V1 amendment targets

- §§9, 12 and 51: permit portion-level WORKING and continued availability under the same Has identity; remove automatic remainder creation as the default for this pattern.
- §§10–11, invariant 8 and Appendix A.4: extend canonical receipt semantics to deal/no-deal outcomes of accepted interactions.
- §23.1: clarify how authorized outcome evidence supports live inspection and personal filtering without a universal reputation score.
- §35 and related contract descriptions: document conditional participation and composable group receiving within existing community context.

Related expert review: [distributed systems #3](https://github.com/Has-Needs/docs/issues/3), [routing #6](https://github.com/Has-Needs/docs/issues/6), [accessible renderers #7](https://github.com/Has-Needs/docs/issues/7).
