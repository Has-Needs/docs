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

Location remains disclosure-controlled. Spatial rendering does not imply precise location sharing.

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
- spatial/temporal resolution;
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
