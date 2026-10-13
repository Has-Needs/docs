# Has-Needs

**What do you have? What do you need? What can we accomplish together?**

**Has-Needs exists to mitigate trauma by empowering people.** It helps people retain their voice, choices, relationships, and ability to act—capacities that can help them navigate traumatic experiences and recover more quickly. It does this by letting people discover one another, exchange what they have and need, and organize useful work **without handing ownership of their identities, relationships, or information to a platform**.

Has-Needs grew from several threads that came together during the 2010 Haiti earthquake response. Long before Haiti, its founder was following GIS-based disaster reporting, working on GIS fire-prediction tools in Idaho, and examining how geographic information could express individual Needs. **In 1996–97, while developing a handheld wind sail intended to make environmental awareness engaging, he proposed a satellite-imagery globe to aeronautics researcher Ilan Kroo, who had worked at NASA Ames.** He regards that exchange as the inspiration for NASA World Wind, the globe platform released in 2004. **In 2006–07, he built a World Wind plugin** to ingest CSV files and display information geographically through icons and color; he submitted the completed project, plugin, and a demonstration to the Millennium Development Goals-themed Imagine Cup. Childhood trauma and foster-care experience had taught something equally important: **having a voice and control over decisions affecting your life matters profoundly.** Meanwhile, cryptography and emerging blockchain concepts suggested that an individual's digital identity and history could be secured without placing an institution in charge of that person.

The Haiti response hackathons brought the turning point into focus. Humanitarian specialists, researchers, academics, and technologists had extraordinary expertise and resources—but **they were desperately short of information about what was happening on the ground**. The founder watched them struggle to find databases that might supply it. He suggested something simpler: let people in Haiti call and tell responders what they knew and needed.

**The room laughed.** He was told that human reports could not be trusted. This was presented not as a concern about one source or circumstance, but as an assumption running throughout humanitarian institutions and their reporting systems. Yet a call-in mechanism was later developed from that discussion: people's messages were translated, categorized, and added to the shared picture of Needs.

That revealed the distinction at the heart of Has-Needs. **Institutions could accept reports from people without accepting those people as trusted participants.** The larger idea—secure each individual, let people retain control of their information, and give them a direct role in matching Needs, offering capabilities, and resolving exchanges—was not pursued there. The founder continued to see this institutional assumption as widespread, with only limited local exceptions.

That realization galvanized Has-Needs: secure the individual first, then build cooperation outward. People should be able to speak, choose, contribute, and see what happens, rather than merely supplying information to someone else's system. As reports move up a hierarchy, local detail can be condensed away; Has-Needs preserves direct relationships and reciprocal evidence.

This was a sustained design effort, not a post-disaster idea developed in isolation. The founder took **emergency-management courses at Capella University in 2009**. After attending a post-Haiti earthquake forum at **UMass Boston**, he pursued **dual degrees in psychology and sociology**, graduating in **2013**. He deliberately focused the curriculum on **trauma, Indigenous studies, and epigenetics** to inform Has-Needs, which he has pursued in a dedicated way since 2010.

Over the following years, he examined cryptographic, **Web3**, blockchain, and interchain technologies for their suitability to Has-Needs. None of the external chain architectures he evaluated met the full sovereignty-first requirements in his assessment; their useful design principles informed Has-Needs' **independent protocol** instead. In **2022**, he began sustained work with **generative AI**. A pivotal exploration with **Perplexity** helped him discover the Has-Needs **`[entity, relation, context]` triplet**—its own minimal semantic grammar for different kinds of human interactions. The discovery followed decades of independent inquiry shaped by many experiences and intellectual influences; the full history is documented separately. AI can assist semantic exploration; people and protocol authorization retain control over agreements and state.

**Sovereignty is the foundation of resilience.** People and communities need meaningful authority over the circumstances that shape their lives. Has-Needs starts with sovereign individuals and supports voluntary collective action, while respecting the distinct cultural and political sovereignty of existing communities, including Indigenous peoples. **Sovereignty makes genuine interdependence possible: cooperation becomes a choice rather than a condition of submission.**

In everyday language, the aim is simple: **I can speak. I can choose. I can help. I can see what we agreed to and what happened.**

Trauma is not confined to earthquakes and emergencies. Everyday life can expose people to loss, instability, exclusion, coercion, and institutions that leave them unheard. **People should not have to wait for a disaster before the tools for regaining control and helping one another become available.** Has-Needs works through ordinary relationships and exchanges—neighbors helping neighbors, farmers finding transport, people organizing a project, businesses finding willing customers, and citizens obtaining accountable public services. Those everyday relationships are also what strengthen communities before the next crisis.

**The human outcomes came first.** Has-Needs was designed backward from a goal: **reduce the harm of traumatic experiences and support recovery by preserving people's ability to act.** What makes that possible? Having a voice, making meaningful choices, controlling one's information, retaining the dignity of having something to offer, seeing commitments honored, and finding others to work with. These are the human conditions the architecture is designed to support.

That thinking shaped the architecture. Sovereign identities protect personal boundaries. Has and Need make everyone a potential contributor. Pending makes commitments visible; reciprocal receipts preserve what actually happened. Proximity communities help successful exchanges become lasting local connections. **These are intentional psychological and prosocial design choices, not incidental features of a matching system.**

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

## Designed to mitigate trauma and support recovery

Has-Needs is intentionally trauma-informed and prosocial. **Its aim is to help people move through traumatic experiences with more control, connection, and practical support—and recover more quickly.** A person can be helped and contribute in the same interaction. People form communities by mutual consent, without a social platform owning the group or its relationships. Everyday exchanges develop the same capacities that become essential during emergencies.

The **Persona Manager** protects the different facets of a person's life. **OCA** (Overlays Capture Architecture) controls what information becomes visible as an interaction progresses. The ontology grows from human-curated meaning and recorded evidence of what actually worked, rather than a central authority's permanent classification of people.

These choices are intended to encourage reciprocity, responsibility, trust informed by evidence, community efficacy, and dignity. Those are **designed emergent effects**, not claims of already measured psychological or clinical results.

## Explore the project

**[Specification V1](./Has-Needs-Spec-v1.md)** is the canonical architecture and protocol working draft, including technical invariants, threat boundaries, open questions, and tests. For an overview of individual mechanisms, see [Core Features](./Core_Features.md).

The [Development Roadmap](./ROADMAP.md) describes the reference-implementation path; [Contract Primitives](./CONTRACT_PRIMITIVES.md) explores composable agreements and optional Need subtypes; [UI Vision](./UI_Vision.md) describes the globe and Data Views; and [Technical Stack](./Tech_Stack.md) distinguishes the architecture from replaceable implementation technologies.

[Governance](./GOVERNANCE.md) and [Expert Review Process](./REVIEW_PROCESS.md) explain how decisions and challenges are handled.

[Origins and Development History](./HISTORY.md) documents the earlier environmental, geographic, community-sovereignty, emergency-management, and academic work behind the protocol.

**Specification V1 defines the architecture.** The separate [code repository](https://github.com/Has-Needs/code) contains experimental implementations. Usage terms appear in [LICENSE](./LICENSE).

---

## Executive summary — Has-Needs V1

**Purpose.** Has-Needs is a sovereign, local-first coordination architecture for discovering compatible Needs and capabilities, making voluntary agreements, recording actual outcomes, and enabling further cooperation without requiring a central platform to own identity, location, relationships, or resource inventories.

**Minimal grammar.** The core semantic triplet is `[entity, relation, context]`, with exactly three relation states: `HAS`, `NEED`, and `WORKING`. The **eUTXO blueprint** informs the Need's condition-governed contract; the **NFT blueprint** informs the Has's unique identity and provenance. Has-Needs implements both ideas independently of existing blockchains. Humans select matches, while a separate authorization-checking mechanism performs permitted transitions. Contract-specific features, such as quantity allocation, belong to optional Need subtypes rather than additional core states.

**Discovery.** Authorized proximity communities, local ontology, and recorded successful resolution paths are strongly favored, with broader search as circumstances permit. Geographic compatibility concerns each object's changing sphere of possibility. The protocol has no privileged operation for globally enumerating everyone's Has or Need objects or retrieving personal locations.

**Sovereignty.** The Persona Manager and OCA control identity facets, contextual participation, and progressive disclosure. Communities form by consent. Local-first transports and semantic Friend nodes can relay and assist coordination without becoming the owners of people or their objects.

**Commitment and evidence.** Mutual acceptance creates a `WORKING` binding. Accepted events and authorized progress are preserved in a Need-owned **Pending journal**. A mutually authorized resolution generates one canonical receipt whose identical contents are referenced from the participants' independent personal chains, in the order resolutions occur. Unfinished or disputed obligations stay distinguishable from completed exchanges.

**Trust and learning.** Vetting uses **recorded events only**. Reciprocal final receipts enable live chain-hop verification; authorized Pending records supply unresolved interaction context without becoming completed receipt links. There is no persistent reputation score, nor a behavioral record of rejected matches or unobserved intentions. Completed outcomes inform scoped, self-pruning ontology and locally useful resolution paths.

**Human purpose.** The central goal is trauma mitigation and faster recovery through practical empowerment: having a voice, retaining choice, contributing, and accessing reciprocal support in both everyday life and crises. The protocol deliberately makes these capacities easier to exercise through self-determination, verifiable commitments, voluntary grouping, direct citizen–governance interaction, and cooperation. The effects on recovery remain outcomes to evaluate.

**V1 status.** This is a canonical **working architectural specification**, not a production-ready or independently security-validated implementation. Cryptographic construction choices, persistence and recovery details, performance of semantic routing, and empirical human outcomes remain subjects for implementation, adversarial testing, and participatory research.
