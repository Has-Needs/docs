# Has-Needs

**What do you have? What do you need? What can we accomplish together?**

Has-Needs is a way for people to find one another, exchange what they have and need, and organize useful work **without handing ownership of their identities, relationships, or information to a platform**.

It began with a simple observation from disaster response: the knowledge, tools, skills, and resources needed to help people are often already nearby. What is missing is a way for people to discover and act on those possibilities directly—on their own terms.

Has-Needs is designed for disaster and everyday life alike: neighbors helping neighbors, farmers finding transport, people organizing a project, businesses finding willing customers, and citizens obtaining accountable public services. The same small set of interactions serves them all.

## A simple interaction

Imagine a community needs drinking water and someone nearby has a way to provide it.

1. **Need:** A participant expresses the desired result and the conditions that would satisfy it.
2. **Has:** Another participant expresses a resource, capability, or useful piece of knowledge.
3. **Discover:** Has-Needs proposes a match, favoring relevant proximity communities, local experience, and permitted geographic scopes before searching farther afield.
4. **Agree:** The participants choose whether to proceed. Mutual acceptance creates a `WORKING` relationship.
5. **Do the work:** The agreement and its recorded progress remain **Pending** while the work is unfinished.
6. **Resolve:** When the required participants agree on what occurred, the system creates an identical canonical receipt for their personal histories.

No central authority needs to own a list of everyone's resources, and the system does not mistake an unaccepted offer for a commitment.

### A technical idea behind that simplicity

The **Need** draws on the **eUTXO model** of condition-governed contracts and authorized state transitions. The **Has** draws on the **NFT model** of unique identity and provenance. Together they form Has-Needs' own independent protocol, with no connection to existing blockchains.

## Pending: the useful part between agreement and outcome

**Pending is simple: record the agreement now; record the outcome when there is one.**

When parties accept a match into `WORKING`, the Need's append-only Pending journal preserves that accepted event and subsequent authorized progress. The final receipt has not been earned yet. There is no fourth Has-Needs relation state, no premature receipt, and no need to reorder anyone's history later.

A municipal service request illustrates the distinction. The municipality agrees to restore water service, so the accepted obligation enters Pending. The journal can retain the commitment, agreed deadline, and authorized progress. Residents can distinguish **promised** from **completed** work without being dependent on an internal agency ticket. Upon agreed resolution, the canonical receipt records what actually happened, with identical receipt hashes on both participants' chains.

If two agreements begin in one order but finish in another, receipts are appended in **resolution order**. If the parties mutually cancel, the receipt records the cancellation, any exchange that occurred, and the agreed release. If someone disappears or disputes the outcome, the accepted obligation stays unresolved in Pending until an authorized resolution.

### Vetting uses recorded events, not surveillance

This is another important consequence of Pending.

**Vetting is based on actual recorded interactions, not speculation about behavior.** Final receipts provide the reciprocal evidence for live chain-hop verification and consistency checks. Where participants authorize disclosure, Pending records show accepted commitments and their recorded progress or unresolved status. An unresolved journal entry is **not** a final receipt, a traversable completed-exchange link, or proof of bad conduct.

Browsing, being nearby, ignoring a proposal, declining an offer, and inferred intentions do not become a permanent behavioral history. There is **no stored numerical trust score**. The participant can inspect permitted evidence and make their own judgment. A mismatch between corresponding canonical receipt hashes is treated as tampering and invokes the grey-list integrity mechanism; an unfinished or disputed obligation alone does not.

## Start where people are, not where the servers are

Today's platform-centered experience generally begins with a global service and tries to locate human relevance inside it. **Has-Needs reverses that starting point.** It begins with sovereign people, their proximity communities, local knowledge, and successful exchanges. Discovery is strongly weighted toward useful local contexts and widens when the Need requires it.

Geography describes a **sphere of possibility**, not the current position of a person. A refrigerator Need may begin with a five-mile pickup area; access to a rental truck can expand it to fifty miles without anyone moving or disclosing where they are. A digital service may be useful anywhere. Coarse-to-fine geographic references and compact changes of scope are research and implementation directions.

**Actual personal location is sacrosanct and must be unretrievable through Has-Needs.** Matching ordinarily compares the geographic areas in which an exchange could work, not participants' private coordinates. People can even agree to meet at a third place without telling each other where they live. Homomorphic encryption and other privacy-preserving computations remain specialized candidates, not prerequisites for ordinary matching. Real-world privacy claims still require testing against inference and metadata leakage.

## Designed for human agency

Has-Needs is intentionally trauma-informed and prosocial. A person can be helped and contribute in the same interaction. People form communities by mutual consent, without a social platform owning the group or its relationships.

The **Persona Manager** protects the different facets of a person's life. **OCA** (Overlays Capture Architecture) controls what information becomes visible as an interaction progresses. The ontology grows from human-curated meaning and recorded evidence of what actually worked, rather than a central authority's permanent classification of people.

These choices are intended to encourage reciprocity, responsibility, trust informed by evidence, community efficacy, and dignity. Those are **designed emergent effects**, not claims of already measured psychological or clinical results.

## Explore the project

**[Specification V1](./Has-Needs-Spec-v1.md)** is the canonical architecture and protocol working draft, including technical invariants, threat boundaries, open questions, and tests. For an overview of individual mechanisms, see [Core Features](./Core_Features.md).

The [Development Roadmap](./ROADMAP.md) describes the reference-implementation path; [Contract Primitives](./CONTRACT_PRIMITIVES.md) explores composable agreements and optional Need subtypes; [UI Vision](./UI_Vision.md) describes the globe and Data Views; and [Technical Stack](./Tech_Stack.md) distinguishes the architecture from replaceable implementation technologies.

[Governance](./GOVERNANCE.md) and [Expert Review Process](./REVIEW_PROCESS.md) explain how decisions and challenges are handled.

**Specification V1 defines the architecture.** The separate [code repository](https://github.com/Has-Needs/code) contains experimental implementations. Usage terms appear in [LICENSE](./LICENSE).

---

## Executive summary — Has-Needs V1

**Purpose.** Has-Needs is a sovereign, local-first coordination architecture for discovering compatible Needs and capabilities, making voluntary agreements, recording actual outcomes, and enabling further cooperation without requiring a central platform to own identity, location, relationships, or resource inventories.

**Minimal grammar.** The core semantic triplet is `[entity, relation, context]`, with exactly three relation states: `HAS`, `NEED`, and `WORKING`. The **eUTXO blueprint** informs the Need's condition-governed contract; the **NFT blueprint** informs the Has's unique identity and provenance. Has-Needs implements both ideas independently of existing blockchains. Humans select matches, while a separate authorization-checking mechanism performs permitted transitions. Contract-specific features, such as quantity allocation, belong to optional Need subtypes rather than additional core states.

**Discovery.** Authorized proximity communities, local ontology, and recorded successful resolution paths are strongly favored, with broader search as circumstances permit. Geographic compatibility concerns each object's changing sphere of possibility. The protocol has no privileged operation for globally enumerating everyone's Has or Need objects or retrieving personal locations.

**Sovereignty.** The Persona Manager and OCA control identity facets, contextual participation, and progressive disclosure. Communities form by consent. Local-first transports and semantic Friend nodes can relay and assist coordination without becoming the owners of people or their objects.

**Commitment and evidence.** Mutual acceptance creates a `WORKING` binding. Accepted events and authorized progress are preserved in a Need-owned **Pending journal**. A mutually authorized resolution generates one canonical receipt whose identical contents are referenced from the participants' independent personal chains, in the order resolutions occur. Unfinished or disputed obligations stay distinguishable from completed exchanges.

**Trust and learning.** Vetting uses **recorded events only**. Reciprocal final receipts enable live chain-hop verification; authorized Pending records supply unresolved interaction context without becoming completed receipt links. There is no persistent reputation score, nor a behavioral record of rejected matches or unobserved intentions. Completed outcomes inform scoped, self-pruning ontology and locally useful resolution paths.

**Human purpose.** The protocol deliberately makes reciprocity, self-determination, verifiable commitments, voluntary grouping, direct citizen–governance interaction, and practical cooperation easier to exercise. Its prosocial and trauma-informed effects are intended outcomes to evaluate, not asserted guarantees.

**V1 status.** This is a canonical **working architectural specification**, not a production-ready or independently security-validated implementation. Cryptographic construction choices, persistence and recovery details, performance of semantic routing, and empirical human outcomes remain subjects for implementation, adversarial testing, and participatory research.
