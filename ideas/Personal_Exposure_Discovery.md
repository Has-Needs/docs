# Personal Exposure Discovery — interactive companion concept

**Status:** Future educational/market idea. Not implemented; not a requirement of the Has-Needs V1 architecture.

## The experience

A reader explores the Has-Needs introduction or specification while a small optional corner widget offers to demonstrate how digital interactions reveal information about a person.

The first stage is a **Jupyter-style executable notebook**. The reader types into a field and sees locally generated event traces alongside a clear distinction between what the page *could* transmit and what it *actually* transmits. The code is intentionally small enough to understand by reading it. A network inspector should report real transmissions; a simulated example must be labeled as simulated.

This matters because a keystroke is **not automatically sent to the network**. Sending individual characters requires page code or another mechanism that transmits them. The demonstration should show how such collection can be deliberately built into software, rather than imply that all websites necessarily do it.

The second stage, with **separate explicit authorization**, checks an email address against eligible public-index or breach-notification sources. A silhouette or constellation of identity facets accumulates small pins as verified observations appear. Each pin carries its source, discovery method, date if available, sensitivity, uncertainty, and the limits of what was actually established. Unverified or merely illustrative examples must be visually distinct from real findings.

The third stage presents the Has-Needs reframe: what changes when a person can declare meanings, grant narrow access to live data, separate personas, and preserve proof of agreed exchange without a platform becoming the owner of the relationship?

**Teaching sequence:** Experience exposure → inspect its mechanism → discover sovereign alternatives.

## Boundaries that make the lesson credible

- **Consent first.** No real third-party lookup, collection, or transmission before a clear opt-in. Keep local typing local by default.
- **Authorization.** Confirm control of an email address before queries that might reveal sensitive exposure about its owner. Do not let the widget become a tool for enumerating other people's information.
- **Data minimization.** No hidden telemetry, advertising pixels, silent analytics, or server-side retention of queried addresses or discoveries. Explain third-party terms before transmitting anything.
- **Evidence integrity.** Differentiate exposed content, service membership, possible association, breach notification, and inference. A public hit does not necessarily prove an account exists or that a person authored the data.
- **Human presentation.** Allow dismissal, pause, deletion of local state, screen-reader navigation, and an equivalent text-first experience. Avoid fear-based nudging.
- **Practical limits.** The public web cannot produce a complete personal-data inventory, and live-access revocation cannot recall existing copies.

## Placement

Treat this as an **optional interactive education experience linked from [Has-Needs and AI](../AI_INTERACTION.md)**. It belongs alongside future communications and product concepts, not inside normative V1 state machines or the protocol's core claims.

No actual exposure scanner, executable notebook, or production UI is provided by this document.
