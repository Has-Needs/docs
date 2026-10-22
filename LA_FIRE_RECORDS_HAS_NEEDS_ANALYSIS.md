# Los Angeles Fire Records Through the Current Has-Needs Workflow

**A records-based operational replay of the January 2025 Eaton and Palisades fires**

## Purpose

This analysis compares official Los Angeles County fire records with the current Has-Needs workflow and its implemented prototypes. It asks what the system would have represented, connected, and preserved if people and participating organizations had been using it during the incident.

Has-Needs was not deployed at these fires. This is a retrospective workflow replay, not a claim that the system changed the response or its outcomes. The comparison is useful because the County’s own reviews describe information and coordination conditions that Has-Needs was designed to address.

## What the fire records show

The County’s after-action review found no single point of failure. It identified a series of weaknesses, including outdated policies, inconsistent practices, and communications vulnerabilities. It also found that field personnel and command staff had inconsistent access to real-time information because of unreliable cellular connectivity, inconsistent field-reporting methods, and disparate, non-integrated systems. ([McChrystal Group after-action review](https://file.lacounty.gov/SDSInter/bos/supdocs/207915.pdf), [County review collection](https://lacounty.gov/aar/))

Citygate’s independently cross-verified investigation adds a detailed timeline for the Eaton Fire:

- From about **1:00 to 2:00 a.m. on January 8**, field resources were handling approximately 30 separate structure fires—about one new fire-response request every two minutes—while available resources were being triaged.
- At about **2:18 a.m.**, Incident Command heard critical radio reports of the fire moving through the mountains and toward northwestern Altadena. The process of evaluating expanded evacuation orders and warnings west of Lake Avenue began.
- At **2:33 a.m.**, Pasadena police reported a street on fire west of Lake Avenue. At **2:43 a.m.**, sheriff’s personnel reported significant fire activity on both sides of Lake Avenue and fire approaching residences.
- The County EOC issued evacuation orders for western Altadena zones by about **3:25 a.m.**

Citygate concluded that Incident Command did not fail to request earlier evacuation orders west of Lake Avenue: the order process began when the fire’s westward spread became known to command at approximately 2:18 a.m. It also documents the conditions behind that decision, including no real-time aerial view of fire spread, extreme winds, darkness, and scarce response resources. This analysis therefore examines information flow and coordination; it does not allege that command ignored known information or that Has-Needs would have changed the timing of an order. ([Citygate investigation, revised May 19, 2026](https://file.lacounty.gov/SDSInter/lac/1208708_InvestigationReportoftheEatonFireEvacuationAlerts_05-18-26_.pdf))

## How the current Has-Needs workflow fits those records

Has-Needs starts with a sovereign person who can originate a **Need** or a **Has**. A Need expresses an outcome and its terms; a Has identifies a capability, observation, resource, or other contribution. Local-first discovery lets participating devices find possible cooperation nearby and relay authorized information outward. A proposal becomes **WORKING** only when the relevant participants accept it. The Need-owned pending journal preserves accepted commitments and authorized progress. When participants resolve the exchange, reciprocal receipts preserve the agreed outcome on their separate personal chains.

The current prototypes and components support this workflow through the Persona Manager, eUTXO-based Need contracts, Has NFTs, DXOS local-first collaboration, OCA context, and Jitterbug discovery and routing. The exact route used for any specific report depends on participating devices, connectivity, permissions, and who accepts responsibility.

| Fire-record condition | Has-Needs representation | Operational value |
| --- | --- | --- |
| A person or responder observes fire, a blocked route, a vulnerable person, or a changing condition | The originator expresses a contextual Has of observed information, or a Need for help or verification | Keeps the observation attached to its source, time, and declared context |
| Many separate fire calls arrive in a short period | Distinct Needs and Hases retain their owners and states; related items can be viewed together without erasing their independent origins | Lets authorized participants distinguish new work, accepted work, and unresolved work |
| Cellular access and reporting systems are inconsistent | Nearby participating devices can discover and relay authorized messages locally; Jitterbug supports routing across peers as paths become available | Provides another communication path when central platforms or cellular service are unavailable |
| A report is relayed, acknowledged, accepted, or acted on | Each transition remains distinct; acceptance starts WORKING and progress enters the Need’s pending journal | Prevents an attempted message from being mistaken for a received or completed response |
| The exchange is resolved | Required participants preserve identical canonical receipts on their separate chains | Leaves durable evidence of who contributed, what was agreed, and how the exchange ended |

This is why the durable chain record is a reciprocal value exchange. Reciprocity makes a person’s contribution count: they are a participant whose information and choices receive a response. That recognition strengthens agency. The receipt proves their part in the agreement and records the outcome. Secure provenance keeps that contribution traceable as it moves through the response chain, instead of letting it disappear into message traffic.

## Reading the timeline through Has-Needs

The overnight increase in separate fire-response requests is a concrete test of the difference between **message volume** and **actionable coordination**. Has-Needs would not treat every incoming report as a new, undifferentiated item in one queue. Each person’s Need would remain linked to its originator, while authorized views could show related observations, available Hases, accepted work, and unresolved Needs.

Distinct records also matter when reports concern the same place or event. A retransmission of one person’s Need can remain linked to that Need, while independent observations from different people remain separately attributed and available to corroborate one another. The protocol can preserve this distinction; deciding whether separate reports describe the same fire or require independent verification remains a contextual human and operational judgment.

The **2:18 a.m.** command decision illustrates the boundary between information flow and authority. Has-Needs could have provided an additional route for residents or field personnel to originate observations and could have preserved their source, relay path, acknowledgment, and status. An authorized official would still decide whether the information warranted an evacuation action. The system records and connects contributions; it does not issue public warnings or replace incident command.

The **2:33 and 2:43 a.m.** reports show why secure provenance and status matter. An observation can carry its origin and handoffs as it moves from the field toward people making decisions. A recipient can distinguish a message that was sent from one that was received, acknowledged, accepted as an obligation, and resolved. A later receipt can preserve the reciprocal outcome. This creates an auditable path through the decision chain without turning an unverified observation into an official finding.

Local-first discovery also changes who can participate. A person under rubble, a resident walking past a fire, a responder outside their assigned information system, or a neighboring organization can contribute relevant knowledge through a nearby participating device. The person closest to an event may have information the institution cannot generate itself. The system gives that person a way to act, choose what to disclose, and remain attached to the outcome.

## What this comparison establishes

The fire records document fragmented communication, inconsistent field reporting, uneven real-time access, and a high volume of time-critical requests. The current Has-Needs workflow has specific structures for those conditions: sovereign origin, local discovery and relay, explicit acceptance, persistent Need identity, authorized progress history, and reciprocal receipts.

This comparison supports a concrete architectural claim: Has-Needs can represent the path from a ground-level observation or Need through relay, acknowledgment, accepted work, and recorded resolution as connected participant-controlled events. It can preserve independent corroborating reports and distinguish them from retransmissions. It can keep an unresolved request attached to its owner and status instead of reducing it to a transient message.

The records do **not** establish that Has-Needs would have produced an earlier evacuation order, prevented property loss, created additional crews, supplied aerial intelligence, or guaranteed delivery. They also do not establish that duplicate verification was a specific documented failure in this incident. The analysis identifies duplicate confusion as a problem the record structure is designed to prevent and a measure to test in exercises.

The direct next evaluation is an incident replay using the official timestamps and the current implementation: model each documented observation, call, and decision as a distinct event; trace which participant could originate it, which peers could receive it, what acknowledgments or commitments would follow, and where authority remains. A controlled exercise can then measure delivery and acknowledgment time, duplicate dispatches per unique issue, unresolved Need duration, responder hours spent repeating verification, and whether participants can accurately reconstruct what happened from the receipts.

The central finding is not that Has-Needs would have solved the fires. It is that the official record shows a break between valuable local information and coordinated action, while Has-Needs is designed to keep the person, the information, the commitment, and the outcome connected.

## Primary records

1. [Los Angeles County: Eaton & Palisades Fires After-Action Reviews and Reports](https://lacounty.gov/aar/) — official collection of County reviews and investigations.
2. [McChrystal Group: After-Action Review of Alert Notification Systems and Evacuation Policies](https://file.lacounty.gov/SDSInter/bos/supdocs/207915.pdf) — County review of alerts, evacuation policies, communications, and interdepartmental coordination.
3. [Citygate Associates: Investigation Report of the Eaton Fire Evacuation Alerts](https://file.lacounty.gov/SDSInter/lac/1208708_InvestigationReportoftheEatonFireEvacuationAlerts_05-18-26_.pdf) — independently cross-verified timeline and findings, updated May 19, 2026.
4. [Eaton Fire Timeline Overview](https://file.lacounty.gov/SDSInter/lac/1191567_EatonFireTimelineOverview.pdf) — County timeline summary.
