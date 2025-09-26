# Core Features & Interaction Flows

## 1. Anonymous Matching & Three-Step Handshake

1.  **Discovery:** The system presents anonymous match-candidates to the user.
2.  **Initial Approval:** User A approves a candidate for their `Need`.
3.  **Reciprocal Approval:** The anonymous party (User B) is notified and must also approve the match for their `Has`.
4.  **Connection:** Only after mutual approval are communication channels opened to arrange the final value exchange.

## 2. Transaction State

Object States are `HAS`, `NEED`, or `WORKING`. Whether matched with an individual, Agency, or Organization etc., the `WORKING` state equates to a "claim" on that resource and provides user controlled provenance of the request.

- **Purpose:** To prevent double-spending of resources and create a public record of commitments as the transaction is finalized.
- **Mechanism:** When two parties agree to a match, the corresponding `HAS` and `NEED` enter `WORKING` state. They are temporarily locked and cannot be matched with other items while the `NEED` (eUTXO Smart Contract) executes.
- **Public Service Indicator:** Since user controls all aspects of their data, exposing the `count`:`NEEDS:WORKING` is a simple UI checkbox. For public entities (e.g., government agencies), the ratio of requests to accomplishments becomes a real-time, verifiable metric of 'responsiveness'.

## 3. Chain Hopping for Trust Verification

- A user can trigger a "chain hop" to verify the integrity of a potential partner's transactional history.
- The system traverses the partner's chain, checking for hash mismatches or unresolved disputes.
- This provides a trust score based on computationally verifiable evidence.
- Following a number of value exchange entries from chain to chain validates the entire system randomly, and generates provable authenticity nearing 100% within 8 hops.
- If any discrepancy between recorded hash is discovered, all parties are retroactively excluded from trust. New entries begin the trust cycle - forcing social consequences and filter triggers, diminishing match options.
- Trust factors are merely suggestion because human systems require situational flexibility.

## 5. Persona Manager as a Verifiable Core

- The Persona Manager is the core, stable, and auditable foundation of the system.
- All users run the same verifiable code, ensuring a secure and consistent interaction layer.
- Any discrepancy between chains is treated as a trust error triggering immediate grey-listing.
- A discrepancy between data entering and exiting any node, however, is an instant Red List, prompting the next interaction to force a download of a validated Trust Kernel to restore node function.

## 8. Communities as Privacy Abstractions

- Users join "Communities" to interact within a specific geographic or logical context.
- A Community acts as a privacy zone, allowing members to signal their general location or affiliation without revealing specific, sensitive data.
- Resources can be pooled at the Community level, enabling collective action.
- **IP Address Protection:** NextGraph's overlay networks will utilize relay mechanisms (e.g., TURN servers, dedicated relay nodes) to ensure that direct IP addresses are not exposed to other peers, even during peer-to-peer communication. All communication is end-to-end encrypted.

## 10. The Personal API for Data Control

- **Mechanism:** All data created by a user originates on their Personal Chain. Access to this data is granted via a revocable, cryptographically signed API key, not by sharing the data itself.
- **Functionality:**
  - **Copyright & Authenticity:** The Personal API acts as a verification oracle. Any content can be checked against the immutable original on the Personal Chain, instantly identifying deepfakes or unauthorized copies.
  - **GDPR/HIPAA Compliance:** The "right to be forgotten" is enforced by revoking an API key. Access to sensitive data (like health records) is inherently auditable and controllable.
  - **Negotiated Access:** The terms of data access are themselves a contract on the Has-Needs network, making data rights explicit and enforceable.
  - **Verifiable Claims (via OCA):** Personal claims (e.g., skills, certifications) are defined using Overlays Capture Architecture (OCA) schemas. Certification is handled by the dual-chain recording of the transaction (user's and institution's chains), providing inherent, verifiable proof without external certifying bodies. Users maintain full control over the visibility of these certifications.
 
## 11. Jitterbug network Topology

- Nodes are autonomous and exist in a low power ground-state, passing messages transparently.
- The Persona Manager intercepts messages destined for any of its operating Personas.
- Nodes can 'expand' connections upon receipt of a header object `open_n` that gets decremented `open_n-1`.
- The reducing count number forces expanded state for a finite number of transmissions before returning to ground.
- Nodes only need know the state of their peer and the message header count to respond to surges.
- Open capacity nodes timeout last, ensuring that gound-state has high availability.
- Certain nodes can be dedicated to persistent connection.
- Expansion and contraction are known geometric states, facilitating network awareness in the local context. 

## 12. Incentivized Contribution

- The system fosters a circular economy where users are incentivized to contribute resources (e.g., running nodes, hosting data, providing relay services).
- Contributions are verifiable and recorded as immutable transactions on Personal Chains.
- Benefits can include enhanced matching priority, access to premium features, and improved community standing, creating a self-sustaining value system.
