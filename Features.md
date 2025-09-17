# Core Features & Interaction Flows

## 1. Anonymous Matching & Three-Step Handshake

1.  **Discovery:** The system presents anonymous match-candidates to the user.
2.  **Initial Approval:** User A approves a candidate for their `Need`.
3.  **Reciprocal Approval:** The anonymous party (User B) is notified and must also approve the match for their `Has`.
4.  **Connection:** Only after mutual approval are communication channels opened to arrange the final value exchange.

## 2. Transaction State: "Accepted Responsibility"

This is an intermediate state for a `Has`/`Need` pair that is critical for accountability.

- **Purpose:** To prevent double-spending of resources and create a public record of commitments before a transaction is finalized.
- **Mechanism:** When two parties agree to a match, the corresponding `Has` and `Need` enter an "Accepted" state. They are temporarily locked and cannot be matched with other items.
- **Public Service Indicator:** For public entities (e.g., government agencies), the ratio of "Accepted" to "Completed" transactions serves as a real-time, verifiable metric of their performance and responsiveness.

## 3. Chain Hopping for Trust Verification

- A user can trigger a "chain hop" to verify the integrity of a potential partner's transactional history.
- The system traverses the partner's chain, checking for hash mismatches or unresolved disputes.
- This provides a trust score based on computationally verifiable evidence.

## 5. Persona Manager as a Verifiable Kernel

- The Persona Manager is the core, stable, and auditable foundation of the system, analogous to the Linux kernel.
- All users run the same verifiable code, ensuring a secure and consistent interaction layer.
- A discrepancy between chains is not treated as an error but as definitive foolproof of a fraudulent transaction, triggering immediate grey-listing.

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

## 11. Incentivized Contribution

- The system fosters a circular economy where users are incentivized to contribute resources (e.g., running nodes, hosting data, providing relay services).
- Contributions are verifiable and recorded as immutable transactions on Personal Chains.
- Benefits can include enhanced matching priority, access to premium features, and improved community standing, creating a self-sustaining value system.
