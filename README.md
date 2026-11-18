# AI Music Radio

English | [简体中文](README.zh-CN.md)

**Own Your Music. Discover Its Stories.**

AI Music Radio is a **local-first, AI-powered music radio experience** built around the music a user already owns. A music server or storage backend keeps recordings accessible; a separate intelligence layer understands the collection and produces coherent, narrated programs with explainable music transitions.

**Status: concept / documentation only.** No server integration, analysis engine, audio generator, or player has been built or verified. See [Status](docs/STATUS.md).

## What problem does it solve?

- **Ownership:** keep a durable library of lawfully acquired files without depending on recurring streaming subscriptions or shifting catalogs.
- **Discovery:** turn existing collections into paths through related and unfamiliar music, with understandable reasons.
- **Listening:** enjoy a lean-back, editorially paced radio experience instead of managing every track or searching for background information.

These are distinct user jobs, not three music genres. See [Product & personas](docs/01-product-overview.md).

## One-click experience

**Choose an identified complete recording → Understand its context → Find playable connections in the user's library → Plan the show → Generate host speech + BGM → Play a radio timeline.**

The engine analyzes two complementary information layers:

- **Music metadata and knowledge:** artist, work, recording, release, version, credits, time and sourced relationships.
- **Audio features (when permitted):** whole-track tempo, rhythm, timbre, energy, texture, harmonic descriptors and embeddings. These are estimates, not documented artist intentions.

It then retrieves candidates from the **user's own library first**, explains why each follows the previous track, and assembles an episode. Optional external discovery can be added where authorized.

## System boundaries

| Responsibility | Proposed owner |
| --- | --- |
| File storage, backup, sharing, access rights | Existing user infrastructure: local folders, NAS or a storage platform; **Lenovo Smart Storage is a preferred integration candidate, not a confirmed dependency** |
| Music-specific index, identity, enriched context, search | **AI Music Radio** library/intelligence layer |
| Editorial planning and narration | **AI Music Radio**, using configurable text-LLM and TTS providers |
| AI inference runtime | **Local or cloud**, explicitly selected/configured; no silent transfer of private files |
| Audio playback and episode timeline | **AI Music Radio player/orchestrator** atop permitted local/server/streaming sources |

Lenovo's public Smart Storage documentation establishes local PC-backed file storage and music categorization, **not yet a verified third-party music streaming/metadata API**. Implementation depends on capability and interface validation; local-folder integration is the MVP fallback.

Read the [architecture and provider boundaries](docs/04-conceptual-architecture.md).

## Project documentation

The [Documentation Index](docs/INDEX.md) identifies one canonical responsibility per document. English/Chinese pairs are updated together.

- [Product & personas](docs/01-product-overview.md) — who, why, and product boundaries.
- [MVP requirements](docs/02-mvp-and-requirements.md) — scope and acceptance criteria.
- [Architecture](docs/04-conceptual-architecture.md) — server adapters, metadata + audio understanding, recommendation and model providers.
- [Product function inventory](docs/PRODUCT_FUNCTIONS.md) — stable capability IDs, priorities, maturity and validation evidence.
- [Current status](docs/STATUS.md) — what is actually implemented.
- [Decisions and unknowns](docs/05-open-questions.md) — unresolved dependencies.
- [Illustrative radio demo](docs/03-my-back-pages-demo.md) — **a case study only**, not the product definition.

[Repository rules](AGENTS.md) govern editing and evidence.

## Product boundaries

The initial input is **one identified complete recording/file**. Missing essential music identity can produce a visible error. Within-track passage detection, mandatory fingerprint recovery and blanket genre coverage are out of scope. Music playback remains separately authorized from generated TTS/BGM; access to DRM streams is not assumed. Owning files avoids streaming subscription requirements for those files but does not eliminate hardware, maintenance or AI-service costs.

## License

No open-source license has been selected. No privately owned recordings, user histories or unlicensed music assets belong in this public repository.
