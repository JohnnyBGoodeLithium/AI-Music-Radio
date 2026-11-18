# AI Music Radio

**Own Your Music. Discover Its Stories.**

> A personal music server and AI-curated radio experience, starting from a track you own.

**Status:** concept / documentation-first, 2026-11-18. No player or AI service has been implemented yet.

## Vision

Streaming makes music easy to access, but long-term listeners can face recurring subscriptions, disappearing catalog entries, service lock-in, and fragmented collections. AI Music Radio puts a **personal music library** at the center and makes it explorable with narrated, evidence-grounded radio episodes.

The system can ultimately use music stored on a desktop, home server or NAS, alongside supported, authorized streaming integrations. Locally owned audio stays playable independently of a streaming subscription. AI features may still need compute or paid services; local-first does **not** mean zero cost or unconditional offline operation.

## One-line experience

**Pick a track → Understand its context → Curate related music → Produce a narrated radio show → Listen and discover.**

## Who it serves

- **Music Owner** — controls a durable local music collection and wants cross-device access without depending on a recurring streaming subscription.
- **Music Explorer** — wants understandable connections between familiar music and new discoveries, not opaque similarity scores.
- **Deep Listener** — wants informed commentary, music history and interpretive listening integrated into playback.

See [Product positioning and personas](docs/01-product-overview.md).

## First demo

Select **Radiohead — Weird Fishes / Arpeggi** (from *In Rainbows*, 2007) and create an approximately **15-minute** narrated program: opening, seed track, musical explanation, related track(s), contextual transitions, new discovery and outro. Host narration is created with TTS and mixed with licensed or original background music. Music playback remains separately orchestrated to respect source rights.

See [Demo brief](docs/03-radiohead-demo.md).

## Current product boundaries

1. **Track or complete audio file** as the starting unit. A file may be one part of a larger work; no within-file segment detection is required.
2. Reliable **track identity and minimum metadata** are prerequisites. Unidentifiable audio returns an explicit error in v0; no automatic fingerprint-based rescue.
3. Prioritize music with meaningful, verifiable interpretation material, not universal genre coverage.
4. Local music server is foundational. Cloud streaming is optional and subject to actual integration rights.
5. Episode structures remain editable timelines rather than one immutable, mixed commercial-song audio export.

## Documentation

- [Product overview](docs/01-product-overview.md) — positioning, problems, three personas, value proposition.
- [MVP requirements](docs/02-mvp-and-requirements.md) — scope, priorities, acceptance criteria, non-goals.
- [Radiohead demo](docs/03-radiohead-demo.md) — 15-minute episode outline, music pathway, audio design, UI story.
- [Conceptual architecture](docs/04-conceptual-architecture.md) — services, inputs, metadata validation, episode schema, playback rights.
- [Open questions](docs/05-open-questions.md) — unresolved product and engineering questions.

## Development approach

Documentation first → curated, legally playable local test library → verifiable recommendation graph and episode planner → TTS/BGM and timeline player → personal profile and music-server integration → optional authorized streaming sources.

## Rights and provenance

Music files must be owned or lawfully accessible. Streaming authorization does not automatically grant rights to download, analyze PCM, clip, capture, remix or export audio. Editorial claims should retain sources and uncertainty; interpretations are not presented as documented artist intent.

## License

Not yet selected. Do not assume permission to redistribute code or example audio.
