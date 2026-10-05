> **Status: Pre-V1 internal comparison — non-normative.**  
> Historical design research, not independent technical due diligence. It includes earlier assumed components and security claims that are not V1 requirements. See [Specification V1](./Has-Needs-Spec-v1.md) and [Reference Implementation Candidates](./Tech_Stack.md).

# Due Diligence Report
  
| **Subsystem / Component**                                  | **Purpose in Has-Needs**                                                                                                        | **Nearest Analog(s)**                                                                                      | **Overlap / Derivation**                   | **Distinct / Novel Aspects**                                                                                                                      |
| ---------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| **1. Persona Manager (PM)**                                | Core sovereign agent controlling identity, data, access contracts, and communication.                                           | *SSI Agents (e.g., Aries, KILT), Solid Pods, DIDComm Agents.*                                              | Similar principle of user-controlled data. | Multi-protocol integration (DXOS + Matrix + SSB); acts as an active firewall and API composer; supports ZKPs + homomorphic proofs.                |
| **2. DXOS (as Data & Sync Layer)**                         | Local-first data engine, managing CRDT documents and state replication between peers.                                           | *Automerge, Gun.js, OrbitDB, Y.js.*                                                                        | Shares CRDT-based sync.                    | Integrated tightly with persona semantics and chain notary; no central relay; tied to verifiable receipt structure.                               |
| **3. Chain Notary + Trust Kernel (with HOKKAIDO)**         | Formal, cryptographically verified core that notarizes every “Has/Need/Working” event and provides ZKP + encryption operations. | *Hyperledger Indy’s ledger*, *zk-SNARK identity proofs*, *TEE/microkernel security research (seL4, Tock)*. | Uses existing cryptographic primitives.    | Combines microkernel security verification with ZKP and homomorphic computation at edge device—uncommon in SSI.                                   |
| **4. Node Marshall + Jitterbug Network**                   | Biomimetic mesh topology enabling dynamic peer discovery, partial connectivity, censorship-resistant routing.                   | *Scuttlebutt gossip layer, IPFS pubsub, Briar, Delay-Tolerant Networking (DTN).*                           | Shares resilient P2P communication traits. | Introduces adaptive, organism-like topology (“biomimetic”) with self-healing nodes; supports encrypted computation on message flow.               |
| **5. Communication Layer (DXOS, Matrix, SSB, NATS, MQTT)** | Multi-transport communication supporting everything from local mesh to IoT integration.                                         | *Matrix, SSB, MQTT brokers, WebRTC.*                                                                       | Uses existing standards.                   | Multi-layer redundancy across contexts (offline, constrained, or full net); unified message schema for “Has/Need” context.                        |
| **6. Overlays Capture Architecture (OCA)**                 | Defines verifiable schema for `[Persona, Has, Need, Working]` relationships and data contracts.                                 | *Verifiable Credentials JSON-LD, Schema.org, RDF Ontologies.*                                              | Conceptually similar schema frameworks.    | Uses a semantic triad model `[entity-relation-context]` that captures dynamic roles without static identity; human-centric linguistic neutrality. |
| **7. Agregoire UI / Resource Map**                         | Peer-to-peer browser with local IPFS embedding; language-agnostic visual interface.                                             | *Beaker Browser, Agregore, IPFS Companion, Holochain UIs.*                                                 | Derived from Agregore concepts.            | Treats UI as a decentralized “resource ecosystem map,” adaptable to local dialects; no global language dependency.                                |
| **8. IPFS Storage Layer**                                  | Large-object decentralized storage (ontologies, grey lists, receipts).                                                          | *IPFS, Filecoin, Arweave.*                                                                                 | Similar in mechanism.                      | Employed purely as optional shared persistence; core operation works offline.                                                                     |
| **9. Containerized Node Deployment**                       | Allows personal chain backup, low-power or feature phone access (SMS/voice/photo).                                              | *Home cloud pods, Solid containers, HoloPorts.*                                                            | Shares self-hosting idea.                  | Adds telecom integration (SMS/voice interface), enabling inclusion beyond smartphones.                                                            |
| **10. Third-Party Service Ecosystem**                      | Framework for external verifiers, escrows, or validators to plug in via contracts.                                              | *Web5 verifiers, Hyperledger Aries Trust Frameworks.*                                                      | Inspired by existing agent ecosystems.     | Adds decentralized “proof-as-a-service” economy with on-demand chain validation and physical escrow options.                                      |
  
  
## Novelty Analysis  
  
| **Dimension**                                         | **Novelty Level**        | **Commentary**                                                                                         |
| ----------------------------------------------------- | ------------------------ | ------------------------------------------------------------------------------------------------------ |
| Cryptographic microkernel (Trust Kernel)              | 🔬 **High**              | Applying seL4/Tock-level verification to user agents is rare outside research OSes.                    |
| Persona semantics (`Has/Need/Working`)                | 💡 **High**              | Social grammar with verifiable data ontology is unique; no known direct precedent.                     |
| Multi-protocol resilience (Jitterbug + Node Marshall) | 🌐 **Moderate-High**     | Integrative approach across DXOS/SSB/Matrix/NATS is novel in its redundancy and censorship-resistance. |
| Chain Notary receipts                                 | 🔏 **High**              | Embedding receipts into a local-first CRDT chain introduces new cryptographic design space.            |
| Feature phone inclusion                               | 📱 **Moderate**          | Rare but not wholly novel; however, combined with local-first sovereignty, unique.                     |
| Ecosystem / Verification market                       | ⚙️ **Moderate**          | Analogous to “trust frameworks,” but implemented in P2P environment.                                   |
  
  
## 🧭 Final Assessment
  
Has-Needs represents a first-of-kind synthesis of:

- Cryptographically verified personal microkernels

- Local-first, sovereign P2P data chains

- Human-centric emergent ontology
  
- Machine readable context for disaster logistics

- 'Safe' AI reliant on human intelligence layer for knowledge
  
- Multi-transport resilient networking

- Inclusive, device-agnostic access

  
# Conclusion
  
No extant SSI, Web5, or decentralized OS project currently implements this complete stack or philosophy.  
In the Humanitarian Sector, no solution provides trauma-mitigating logistics, and parallel but asynchronous recovery.
