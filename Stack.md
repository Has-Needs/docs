# Has-Needs Technology Stack

*This document outlines the chosen technology stack for the Has-Needs prototype, organized by architectural layer.*

---

### Primary Language

- **[Rust](https://www.rust-lang.org/):** Chosen for its performance, memory safety, and suitability for building secure, concurrent systems.

---

### Presentation Layer (UI)

- **Agregoire:** The primary, purpose-built user interface designed to be linguistically and culturally agnostic, providing an emergent resource map.
- **[React](https://react.dev/) + [TypeScript](https://www.typescriptlang.org/):** The underlying web technologies for building the Agregoire UI components.

---

### Communication & Networking Layer

- **Node Marshall:** The core component that manages all network operations, including node creation, state retention, and secure communication.
- **Jitterbug Network:** A biomimetic, message-centric networking topology for resilience and censorship-resistance.
- **Peer-to-Peer Messaging:**
  - **[DXOS](https://dxos.org/):** Used for establishing peer-to-peer connections and managing identity within the Persona Manager.
  - **[Secure Scuttlebutt (SSB)](https://scuttlebutt.nz/):** Provides a secure, decentralized gossip protocol for peer and community interactions.
  - **[Matrix](https://matrix.org/):** Offers interoperable, decentralized, real-time communication for groups and communities.
- **Transport Protocols:**
  - **[NATS](https://nats.io/):** Used for high-performance, lightweight messaging.
  - **[MQTT](https://mqtt.org/):** Used for efficient messaging, particularly with IoT devices.

---

### Data, Identity & API Layer

- **Persona Manager (PM):** The sovereign agent that manages the user's identities, data contracts, and acts as a high-level firewall. It leverages DXOS, SSB, and Matrix for its communication functions.
- **[NextGraph](https://nextgraph.org/):** The core data platform, using DAG-based repositories for the immutable Personal Chains and CRDTs for local-first synchronization.
- **[Overlays Capture Architecture (OCA)](https://oca.colossi.network/):** The verifiable data schema layer used to define `Persona` attributes and the `[entity-relation-context]` triplets (`Has`, `Need`, `Working`).
- **Dynamic API Management:** The PM, Node Marshall, OCA, and NextGraph work in concert to compose and manage secure, on-demand APIs for data sharing, IoT streaming, and third-party interactions.

---

### Security & Verification Layer

- **Trust Kernel:** A verifiable, secure micro-kernel that handles all core cryptographic operations, ensures message integrity, and manages the financial passthrough mechanism.
  - **Microkernel Tech:** Leverages **[seL4](https://sel4.systems/)** and **[Tock](https://www.tockos.org/)** principles for formal verification and security.
- **Chain Notary:** The component responsible for writing transactions to the personal chain.
  - **HOKKAIDO:** A custom cryptographic component within the Chain Notary.
  - **Crypto Libraries:** HOKKAIDO is built with **[Tokio](https://tokio.rs/)** (for async operations), **[Ristretto](https://ristretto.group/)** (for cryptography), and **[HACL*](https://hacl-star.github.io/)** (for verified cryptographic primitives).
- **Encryption & Privacy:**
  - **Homomorphic Encryption:** Used within the Node Marshall to allow computation on encrypted data without decrypting it.
  - **Zero-Knowledge Proofs (ZKPs):** Used to prove the validity of a statement (e.g., "I am over 18") without revealing the underlying data (the user's birthdate).

---

### Decentralized Storage Layer

- **[IPFS (InterPlanetary File System)](https://ipfs.tech/):** Used for content-addressed, decentralized storage of larger data objects such as the shared ontology, the public Grey List, and other personal records that do not fit on the core chain.

---

### Deployment & Ecosystem

- **Containerized Instances:**
  - **Personal Backup:** Users can run a containerized instance of their node on a home server or cloud provider to act as a secure, personal backup.
  - **Feature Phone Accessibility:** The containerized version provides the backend for feature phone users, allowing them to interact with the protocol via SMS, voice, or photo through a dedicated number.
- **Third-Party Service Ecosystem:**
  - The protocol is open for external, third-party providers to offer value-added services.
  - **Example - Physical Escrow:** A trusted third party could act as a physical escrow agent for contactless exchanges of goods between users.
  - **Example - On-Demand Verification:** A specialized service could be paid to perform a rapid, deep-chain validity assessment for high-stakes transactions, providing instant verification as a service.