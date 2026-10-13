# Has-Needs UI/UX Vision

**Status:** Current product direction aligned to [Specification V1](./Has-Needs-Spec-v1.md).

The interface goal is to reduce the human cost of entering the data universe without reducing the richness of the underlying data.

## 1. The globe as the primary rich interface

The default rich interface is globe/map-based because spatial relationships can communicate proximity, scale, movement, grouping, direction, and change with relatively little dependence on literacy or language.

The globe is not a conventional GIS database viewer and not a window onto globally enumerable data.

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

A person seeking a nearby resource can receive a consent-bounded compatibility result without publishing where they are. Owner-local checking is a baseline. Homomorphic encryption, potentially combined with MPC or related comparison methods, is a candidate for encrypted proximity evaluation; no V1 construction is selected or validated. Encrypted coordinates alone are not sufficient protection: repeated proximity questions, routing patterns, and metadata may allow location inference.

The interface makes the difference between **where a resource is useful** and **where its owner is located** explicit. It does not expose an exact-location search, a replayable private-position track, or an automatic coordinate disclosure upon match acceptance. If a safe comparison is unavailable, it degrades to broad authorized context or defers matching rather than sacrificing actual-location protection.

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

The renderer must never redefine the protocol.

## 8. Working, cancellation, and relationship inspection

Show accepted obligations and progress from the pending journal separately from
final personal-chain receipts. A cancellation request remains pending until the
required agreement exists. Mutual cancellation records the actual resolution;
the interface must not imply delivery or launch an automatic reverse exchange.

Render disclosed event links between somewhat parallel chains. A disputed event
can be enlarged and brought forward for touch selection, then followed into the
counterpart's authorized context. This can reveal a repeated pattern or restore
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
