# The WORKING state: contracts, delegation, streams, and outcomes

This guide records the architecture clarified on 21 October 2026. The [V1 specification](./Has-Needs-Spec-v1.md) defines the protocol; the examples here explain the same mechanics without adding categories or primitives.

## One contract mechanism

A **Need is a smart contract, using standard templates and custom options**. **The WORKING state connects all involved Has and Needs while the Need/smart contract executes.** Participants choose a candidate pairing and mutually authorize it; the committed objects leave ordinary matching. The Need-owned append-only journal preserves the agreement, communications, progress, delegation, and handoffs.

Purpose, participant count, duration, governance policies, responsibilities, and outcome conditions are contract terms. A Community can form around a Need for collective space to interact for a chosen purpose under a chosen DAO's governance policies. That Need can support an open-ended, one-to-many match in the WORKING state. It uses the same mechanism as any other accepted Need.

## Outcomes, release, and expiry

The parties decide an outcome under the Need's terms. Fulfillment, partial fulfillment, and a decision not to proceed use the same receipt mechanism. A standard template may include an agreed expiry that releases the associated WORKING objects and records the expiry as an on-chain outcome. Release follows the actual resource disposition: it does not make a delivered item available again.

An agreed contract expiry is different from an unexplained absence or a failed communication timer. The expiry terms must identify the authorized decision, evidence, release effects, and receipt participants. Simultaneous receipt writing still requires the necessary peer interaction; an interrupted write is not a completed reciprocal record. Without an applicable agreed resolution rule, an unresolved commitment remains in the journal.

Recorded no-deal outcomes can affect personal filters seeking relevant participants for clean, easy value exchanges, reducing exposure to available matches. This uses authorized outcome evidence, not a universal reputation score. Declining an unaccepted candidate is not a no-deal outcome of a WORKING contract.

## Composable APIs and personal data streams

An entity can provide data within its control to another entity through a composable API mechanism. The Need defines recipients, purpose, scope, duration, permissions, and responsibilities. Personal data streams, a bounded data projection, and a Community's stream of communications to secure storage use that same mechanism.

If the originator's resources become overwhelmed, the Community can arrange a secure storage channel for its communications. The Community determines the responsible parties and the permissions needed to execute that Need. Existing contributor and subgroup permissions remain in force; holding the stream does not grant the storage provider permission to read, disclose, or act beyond its agreement. Storage placement changes capacity, not authority.

## Delegation and delivery

Delegation is available within the WORKING state under the Need's terms. It records who may act for whom, for which actions, and within which limits.

A truck driver scans and accepts package A onto the truck. The handing-over entity is also part of the exchange and records the handoff. The agreed departure time can hold whether or not every expected shipment is aboard. The journal distinguishes accepted packages from absent ones.

At delivery, a representative authorized by a Community pooled Need can receive and scan the pooled items. For individually negotiated items, each recipient must appear or delegate receiving permission to another entity. Transport custody alone does not grant acceptance authority. Every handoff and delegation remains part of the recorded exchange.

## The self-pruning tree

An organizational request can follow the org chart through authorized delegation until it reaches the worker who fulfills the Need. That final contributor becomes preeminent in the value exchange's resolution evidence. The completed outcome informs the local ontology, making the most recent effective route available for subsequent requests.

The organizational hierarchy remains available to examine when the effective endpoint is absent or unsuitable. This **self-pruning tree** improves paths to resolution through actual fulfillment while preserving the authority and fallback relationships needed to act. A useful route does not itself confer permission to bypass required authorization.

## Simultaneous receipts and selective disclosure

At resolution, the complete exchange—including its contract-relevant communications, delegation steps, and delivery handoffs—is encapsulated in one canonical receipt. Participants choose the authorized public/plaintext and encrypted portions. Their Persona Managers write the **identical receipt simultaneously to each required participant's personal chain**, as one coordinated direct peer-to-peer operation, and mutually verify it. Participant-local chain pointers remain private and can differ.

Corroboration checks that corresponding canonical entries agree even when all their contents are encrypted. It does not require decrypting the contents or exposing the core chains. Facets provide the chosen purpose and context of interaction. Participants can remain anonymous to outsiders, accepting or deliberately choosing the resulting limits on interaction.

For example, customer name, address, and costs can remain encrypted while “deck,” “recycled wood,” “very happy with the job,” and “accurate quote” are disclosed through **Bob the woodworker**. Jim can also disclose evidence that he pays on time, gives clear directions, and respects a craftsperson's input. The same reciprocal exchange supports each participant's selected facet without exposing unrelated personal history.

Immediately after completion, each participant independently initiates random verification hops outward from the exchange. These resemble ongoing background Jitterbug traffic; resemblance is not a guarantee against traffic analysis. Jitterbug is the adaptive transport topology; chain-hopping corroborates records carried through that topology.

## Civic accountability and protected details

Publicly funded operations need an accountable view of who did what with public resources. Contract records can connect commitments, delegation, fulfillment, and expenditure, supporting budget reconciliation and revealing administrative or organizational bottlenecks. Sensitive whereabouts and operational details can be obscured for citizen safety while authorized role and contribution evidence remains available.

The choice between a standard lightweight encryption profile for civic interactions and a mandatory transparency policy for publicly funded operations remains open. An implementation must state its chosen disclosure policy, audiences, safety protections, and authorized access; this discussion does not select a cipher, publish private citizen chains, or establish a universal public-disclosure rule.

## Related reading

- [Introduction](./INTRODUCTION.md)
- [Contract templates and operations](./CONTRACT_PRIMITIVES.md)
- [Data layers and composable access](./DXOS_OCA_ARCHITECTURE.md)
- [Paradigm Delta](./Has-Needs_Paradigm_Delta_Review_2026-10-14.md)
- [Persona scenarios](./Persona%20Files/README.md)
