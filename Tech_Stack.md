# Has-Needs Technology Stack

*This document outlines the chosen technology stack for the Has-Needs prototype, organized by architectural layer and purpose.*

***

### Primary Language

- **Rust:** Chosen for its performance, memory safety, and suitability for building secure, concurrent systems.

***

### Presentation Layer (UI)

- **Agregoire:** The Agregoire browser delivers peer-to-peer IPFS and self-contained browsing features. It is well-suited for hosting Has-Needs' resource map interface, which is designed to be linguistically and culturally agnostic.
- **React + TypeScript:** These web technologies power Agregoire’s UI components, supporting interactive and resilient user experiences.

***

### Communication & Networking Layer

- **Node Marshall:** Handles core network operations, including node management, state retention, and secure communication across the network.
- **Jitterbug Network:** Features a biomimetic, message-centric networking topology to enhance resilience and censorship-resistance.
- **Peer-to-Peer Messaging:**
  - **DXOS:** Facilitates peer-to-peer connections and identity management through its Persona Manager.
  - **Secure Scuttlebutt (SSB):** Provides secure, decentralized gossip-based messaging for peer and group interaction.
  - **Matrix:** Enables interoperable, decentralized, real-time communications for group and community needs.
- **Transport Protocols:**
  - **NATS:** High-performance, lightweight messaging system.
  - **MQTT:** Optimized for efficient messaging, especially with IoT device contexts.

***

### Data, Identity & API Layer

- **Persona Manager (PM):** Serves as the sovereign agent, managing identities, personal data contracts, and acting as a firewall. It leverages DXOS, SSB, and Matrix for its communication functions.
- **Overlays Capture Architecture (OCA):** Provides verifiable, extensible schema for Persona attributes and entity-relation-context triplets (`Has`, `Need`, `Working`).
- **Dynamic API Management:** The PM, Node Marshall, and OCA collaborate to compose and provide secure, on-demand APIs for personal data sharing, IoT streaming, and external integrations.

***

### Security & Verification Layer

- **Trust Kernel:** Provides a secure, verifiable microkernel for core cryptographic operations, message integrity, financial passthrough functions, and more.
  - **Microkernel Tech:** Employs principles from seL4 and Tock for formal security verification.
- **Chain Notary:** Handles the writing of transactions to personal chains using custom cryptographic logic.
  - **HOKKAIDO:** A dedicated cryptographic component within the Chain Notary, built using Tokio (for async operations), Ristretto (for secure cryptography), and HACL* (for verified primitives).
- **Encryption & Privacy:**
  - **Homomorphic Encryption:** Used in Node Marshall to enable computations on encrypted data without decryption.
  - **Zero-Knowledge Proofs (ZKPs):** Allow statements (such as age confirmation) to be verified without exposing underlying sensitive data.

***

### Decentralized Storage Layer

- **IPFS:** Content-addressed, decentralized storage for large data objects, including shared ontologies, public Grey Lists, and personal records that do not fit on core chains.

***

### Deployment & Ecosystem

- **Containerized Instances:**
  - **Personal Backup:** Users can deploy containerized node instances for secure backup on personal servers or cloud providers.
  - **Feature Phone Accessibility:** The backend supports feature phone users, enabling interaction via SMS, voice, or photo through dedicated numbers.
- **Third-Party Service Ecosystem:**
  - Protocol supports integration by external third-party providers for added functionalities.
  - **Examples:** Trusted physical escrow agents for contactless exchanges and specialized rapid chain validity verification services for transactions.

***

This architecture is purpose-built for sovereign, resilient, and privacy-preserving coordination across diverse contexts, reflecting a strong commitment to social robustness and reliability in extreme conditions.


