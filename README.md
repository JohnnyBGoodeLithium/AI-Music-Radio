# AI Music Radio

English | [简体中文](README.zh-CN.md)

**Your Music. More to Discover.**

AI Music Radio uses **existing everyday music data**—playlists, favorites, play counts, original dates added, and optionally owned music—to create an evidence-backed **Personal Music Report** and personalized narrated programs. **No local audio files, home server, Lenovo DT or on-device model is mandatory.**

**State: concept/docs only.** No personal import, Music Assistant integration or playable program has yet been implemented here. [Status](docs/STATUS.md).

## Three checkpoints

1. **Collection:** import authorized music catalog and behavior data, with source/coverage.
2. **Understanding:** distinguish lasting interests from recent listening spikes; connect familiar music to credible music history and explain why.
3. **Radio:** offer a few curated ~15–20-minute story ideas or a user-selected theme. Build modular host segments plus lawfully playable song items. Let user feedback influence the next story or affected clips.

Catalog metadata can support analysis and episode planning **without granting the rights to play or remix the original recording**.

## Reuse before reinventing

[Music Assistant](https://www.music-assistant.io/) + its [AI Radio plugin](https://www.music-assistant.io/plugins/ai-radio/) already provide music catalog aggregation, player/queue, Hosts, Shows, spoken segments and TTS. These are **upstream capabilities**, not implemented by this repository. Review [server](https://github.com/music-assistant/server) and [frontend](https://github.com/music-assistant/frontend) before building duplicates.

**Hypothesized differences:** source-aware personal music statistics, an inspectable music report and relationship graph, sourced multi-artist storytelling, several episode choices, feedback memory and selective segment revisions. Local and cloud LLM/TTS are both supported *design options*, not validated implementations.

## Documents

[Product](docs/01-product-overview.md) · [MVP](docs/02-mvp-and-requirements.md) · [Architecture / Music Assistant assessment](docs/04-conceptual-architecture.md) · [Functions](docs/PRODUCT_FUNCTIONS.md) · [Status](docs/STATUS.md) · [Open questions](docs/05-open-questions.md) · [Black/white wireframes](docs/06-lowfi-wireframes.md) · [Illustrative demo](docs/03-my-back-pages-demo.md) · [Index](docs/INDEX.md) · [Agent rules](AGENTS.md).

**Scope firewall:** Home Assistant, generalized NAS/Agentic Storage, 24×7 DT and household service ecosystems are **separate long-term explorations**, not this music project. Smart Storage is an optional future integration. **UI first:** monochrome Notion-like low-fi line/block sketches with selective dashed borders; Qira styling deferred.

No private listening data, credentials or uncleared recordings in this public repository. Commercial streaming subscriptions do not grant DRM capture/remix rights. Project license not yet selected; Music Assistant and providers retain their terms.
