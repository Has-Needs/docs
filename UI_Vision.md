# Has-Needs UI/UX Vision

**Status:** Current product direction aligned to [Specification V1](./Has-Needs-Spec-v1.md).

The interface goal is to reduce the human cost of entering the data universe without reducing the richness of the underlying data.

## 1. The globe as the primary rich interface

The default rich interface is globe/map-based because spatial relationships can communicate proximity, scale, movement, grouping, direction, and change with relatively little dependence on literacy or language.

The globe is not a conventional GIS database viewer and not a window onto globally enumerable data. It begins with the participant's own locally meaningful community contexts and shows broader possible relationships only when chosen or relevant. Has-Needs reverses the platform-first convention: the real social/geographic environment is primary, remote discovery an expansion rather than the starting point.

It is a **Data View over sovereign information**.

Depending on persona and permissions, it may show:
- the user's own Has, Need, and Working objects;
- candidate matches;
- receipts and lineage;
- local/community resources;
- hazards, routes, sensor fields, or environmental conditions;
- derived aggregate layers;
- Data Stories.

**Actual participant location is sacrosanct and must be unretrievable through Has-Needs.** Geography is a universal semantic dimension of a Has, Need, Working relationship, and relevant derived views; it can mean a broad service area, route, destination, mobile coverage, remote applicability, or withheld/unknown region. The globe displays permitted geographic context—not a global locator for people. A private location may be used transiently by its owner for proximity checking, but no map interface, shared record, query, or data layer gains a retrieval method for that position.

## 1.1 Geographic relevance without retrieving people

The spatial property that matching evaluates is an object's **sphere of possibility**: where a Has or Need can feasibly participate. Scopes can be regional, remote, mobile, corridor-shaped, discontinuous, or changing over time. Renting a truck can expand the pickup area of a refrigerator Need from local to regional without altering the owner's actual position or disclosing it.

A coarse-to-fine hierarchy of geographic areas, potentially inspired by multiresolution/wavelet representations, makes regional relevance easy to understand and compactly communicate. These are **applicability areas, not concentric rings centered on the person's actual coordinates**. A comparison of permitted scope overlap is the default; secret coordinate comparison is an optional specialized operation.


A person seeking a nearby resource can receive a consent-bounded compatibility result without publishing where they are. Matching owner-defined possibility regions is the normal baseline. Homomorphic encryption, potentially combined with MPC or related comparison methods, is a candidate only for specialized encrypted position evaluation; no V1 construction is selected or validated. Encrypted coordinates alone are not sufficient protection: repeated proximity questions, routing patterns, and metadata may allow location inference.

The interface makes the difference between **where a resource is useful** and **where its owner is located** explicit. It does not expose an exact-location search, a replayable private-position track, or an automatic coordinate disclosure upon match acceptance. If a safe comparison is unavailable, it degrades to broad authorized context or defers matching rather than sacrificing actual-location protection.

## 1.2 The first actionable moment

The participant's first view should make their own immediate sphere of awareness and capability actionable: express a Has, express a Need, and discover nearby compatible cooperation through participating peers within range. The interface should make a sent declaration and any actual acknowledgment distinguishable, so the possibility of being heard does not become a false claim of delivery. Supporting purposeful action before a reply is a human-factors design objective, including for the person beneath the rubble.

## 2. Data Views

A Data View is a projection over objects the participant owns or is authorized to see.

Changing a Data View changes representation and attention, not ownership.

Examples:
- My Needs
- My Has
- Working now
- Family resources
- Build House / Electrical
- Fire-status layer
- Cassava conditions
- Receipt history
- Research stream

List, map, timeline, Kanban, Gantt, chart, and agency-summary interfaces can all be alternative views over the same substrate.

## 3. Direct manipulation

The preferred interaction model is tangible and compositional:
- drag a Has toward a Need;
- group related objects;
- reveal or hide layers;
- change disclosure state;
- apply an operator to selected layers;
- save or share a useful expression.

The interface should make ownership, permission, and active relationship state visible without requiring users to understand the storage or cryptographic implementation.

## 3.1 Candidate shelves and participant control

The match-candidate display shows the available candidate count, active matching parameters, and current sorting criterion. Participants choose which attributes matter, add or remove tags and search parameters, and adjust dials where an attribute has a meaningful range. Suggested filter topics evolve with the Need, its added context, and the available candidates; their basis and effects are visible, and suggestions can be dismissed. Counts update with the selected scope and filters.

Candidates use three stable, shelf-dependent views. Moving between them rearranges and grows information rather than merely magnifying it:

| View | Emphasis |
|---|---|
| Full | Complete profile for the presented Persona, enriched by available authorized metadata |
| Medium | Extended candidate details and a small trust window |
| Small | Compact candidate information and a larger trust window for deciding whether to select |

The full profile is the authorized Persona projection, not the person's entire identity or private history. Participants traverse options, focus to inspect more, and return without losing filters, ordering, or candidate position. Equivalent controls and detail are available without visual zoom.

The trust display has its own visual language: a person outline progressively brings forward hop count, the Persona used for this transaction and its available details, grey-list status, and an annotation for each friendly chain encountered. Friendly means meeting the participant's chosen prior-interaction or relationship-proximity criteria; frequency and proximity remain inspectable. The participant can stop at their accepted verification depth or continue looking for familiar connections. Underlying chain examination is a background operation; the outside-facing display presents authorized findings. In local-only operation, unavailable remote evidence is distinguished from examined evidence with no friendly encounter. See §8 for event inspection.

Participant-configured filters can bring relevant events forward beyond grey-list status. Each flag identifies the recorded event and the criterion that triggered it, with supporting detail on focus. Claims, available records, and unavailable evidence remain distinguishable. These controls support selection within the presented Persona rather than assigning a universal judgment to its owner.

## 3.2 Refinement, waiting, and agency

A participant can choose among current matches, say “These do not fit,” refine the Need, or keep it waiting. Adding context over time—such as an image of a desired chair—can refine matching; the participant can identify which properties of the reference matter. The personal relevance engine assists this dialogue; see [Core Features §8](./Core_Features.md#8-local-ontology-and-resolution-evidence).

An unmatched Need remains a valid expression of intention. It may stay active, be refined, be saved for later outside active matching, or be removed through an explicit choice. Saved Needs can help the owner recognize recurring interests or dream topics without the system judging the aspiration unrealistic. Creation and last-refinement dates provide a quiet invitation to keep, revise, save, or let go, without escalating urgency or treating age as failure. These are presentation and discovery choices, not additional protocol relation states.

Agency comes from understandable consequences: visible ordering, reversible filter changes, inspectable suggestions, and control over attention. Candidate selection has no chance-based award, shuffle-to-win, mystery reveal, suspense animation, artificial countdown, or winner/loser framing. After agreement, unsolicited comparisons with supposedly better alternatives should not provoke “what you could have won.” Background random verification remains an evidence-sampling process.

Research on [counterfactual outcome processing](https://doi.org/10.1016/j.neuroimage.2026.122303) motivates examining how comparison changes emotional evaluation. These interface choices are design guidance to evaluate, not findings established by that gambling experiment. Greater neural activation alone does not establish satisfaction, fuller participation, or a gambling response.

## 4. RGB as the visual lingua franca

RGB is the common rendered composition surface.

It is **not** the canonical data encoding and does not pretend that arbitrary data can be uniquely compressed into one 24-bit color value.

Instead, each authorized source can be rendered as a color field, gradient, intensity, pattern, or RGB layer while retaining provenance to its underlying data.

This gives heterogeneous sources a shared human-facing surface.

## 5. Data Stories

A Data Story exists when layers are related by an operator.

For example:

`rainfall_24h + (dew_point_today × cassava_crop)`

The expression itself is already a story. It need not be saved or named first.

Possible operators include:
- addition;
- subtraction / difference;
- multiplication;
- intersection;
- threshold;
- mask;
- normalization;
- temporal comparison.

The source data remains unchanged. The expression creates a derived semantic relationship.

If useful, a story can be:
- named;
- saved;
- reused as another layer;
- shared;
- streamed;
- offered as a Has.

## 6. Streaming and value exchange

A Data Story may be a live, bounded stream derived from changing inputs.

A buyer, researcher, agency, neighbor, or other participant can express a Need for a specific derived product. The owner may answer with a Has whose contract defines:
- permitted inputs;
- transformation;
- permitted geographic applicability and temporal resolution (not retrievable participant coordinates);
- update frequency;
- duration;
- compensation or reciprocal value;
- disclosure conditions.

The derived story can leave the Persona boundary while the underlying raw data remains private.

## 7. Literacy and accessibility

**The graphical environment is supplied by Has-Needs; users do not author it.** Its prepared icons, visual controls, and a bounded vocabulary of official basic contract primitives make ordinary giving, receiving, and exchange accessible without literacy. Participants use these controls to express their own Has, Need, and local meanings; they are not expected to design a UI, invent standard contracts, or learn a predetermined ontology. Optional text, speech, signs, or assistance may support the same actions. Advanced custom contracts are extensions, not new official primitives.

The rich UI should favor:
- icons;
- spatial relationships;
- direct manipulation;
- visual layers;
- locally meaningful symbols;
- simple gestures.

Equivalent semantics must remain available through:
- text;
- speech;
- screen readers;
- terminal interfaces;
- SMS / feature phones;
- human intermediaries.

The renderer must never redefine the protocol. **Core interface flow:** use the provided graphical actions to create a Has or Need, select an official basic contract type, work with relevant counterparties, and confirm completion. Participants provide the content and local meaning. There is no additional adaptation layer or separate test of whether the application conforms to a user-authored visual world.

## 8. Working, independent disclosure, and relationship inspection

**The Persona Manager is the concierge for all user-created personas; no interface exposes the underlying private chain to an outside party.** After a job is finished, the vendor and customer each independently mark it complete. Both can review the transaction and communications, optionally add their own free-form comments, and decide what to leave plaintext or encrypted. Each sees the other's contribution and exposure settings **before committing**, but cannot edit, delete, or suppress the other's statement. Show **Not ready / Ready to commit** for each participant. A change in the proposed record resets readiness for the changed version. Once all required parties are ready, Persona Managers coordinate simultaneous writing of identical canonical receipts. Valid on-chain receipts themselves establish completed exchange; do not show a redundant “verified completed exchange” label.

Show accepted obligations and progress from the pending journal separately from
final personal-chain receipts. An agreed template expiry can also authorize release with an on-chain outcome. Otherwise, a cancellation request remains pending until the
required agreement exists. Mutual cancellation records the actual resolution;
the interface must not imply delivery or launch an automatic reverse exchange.

Render authorized receipt-derived event links without showing or traversing underlying private personal chains. A disputed event can be enlarged and brought forward for selection, then followed only into specifically permitted counterpart context. This can reveal a repeated pattern or restore
confidence in someone affected by a problematic counterpart. Do not assign a
virus icon or stored reputation number to the person.

Distinguish mutual cancellation, unresolved Working, dispute, and verified
canonical hash discrepancy. Short history indicates limited evidence. A declined
unaccepted invitation is not automatically a permanent interaction record; its
possible display and disclosure rules remain open. Provide equivalent text and
screen-reader access to every event and relationship.

## 9. Collective choice and timing

Sharing makes an object visible; pooling entrusts fulfillment under explicit
delegation; clustering retains required individual authorization. A drop entering
a pool versus joining a cluster of distinct drops is a visual direction to test.
The authority choice, cutoff, readiness, and departure window must be understandable
without contract terminology. Missing readiness must not appear as shipment.

Communities and subcommunities retain separate conversation contexts. Sharing a
selected status with the parent does not merge their discussions. Successful
cooperation may make future participation feel safer; that is an intended effect
to evaluate, not a guaranteed psychological outcome.

## Contract execution, delegation, and outcome views

Present a Need as a smart contract with standard templates and custom options. Use **the WORKING state** for the connected Has and Needs while it executes. Show the authorized responsible party, delegate, handoff evidence, outcome conditions, and any agreed expiry. A no-deal outcome uses the same record flow; a proposed candidate that was never accepted does not acquire one.

For shipping, let the sender and driver record their handoff and the agreed departure cutoff. Receiving controls distinguish a delegated pooled-resource representative from an individual recipient or their delegate. For an organizational request, show the actual fulfilling worker and authorized fallback path from the self-pruning tree.

Stream controls use the composable API's existing permissions: who provides which data, to whom, for what purpose, and for how long. A Community can route its communications to secure storage without giving the provider new reading rights. Facet previews distinguish public/plaintext evidence from encrypted details; encrypted equality remains corroborable. Civic views should show accountable contribution and expenditure within the selected policy, with safety-sensitive detail protected. See [the WORKING state, delegation, and streams](./WORKING_CONTRACTS_AND_DELEGATION.md).
