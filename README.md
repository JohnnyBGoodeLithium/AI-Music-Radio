# AI Music Radio

English | [简体中文](README.zh-CN.md)

**Own Your Music. Discover Its Stories.**

> A local-first personal music server paired with an AI radio producer that tells the stories behind the recordings you choose.

**Maturity:** Concept and documentation only as of 2026-11-18. No working music server, player or audio generation has been built in this repository. See [Current Status](docs/STATUS.md).

## Why

Cloud streaming offers convenience but brings recurring subscriptions, shifting catalogs and fragmented personal collections. Listeners who own legally acquired music deserve a stable private library that remains useful without renting access indefinitely.

Traditional personal music servers preserve files and enable playback. **AI Music Radio adds intelligent, evidence-grounded music exploration**: select one identified complete recording, research it, choose meaningful musical connections, and generate a narrated episode with natural TTS, original/licensed BGM and authorized music playback.

Local-first does not mean every AI feature is free or offline. Hardware, maintenance and optional model services can still cost money.

## Three personas

- **Music Owner:** owns a long-lived local collection and wants durable, cross-device access independent of ongoing streaming subscriptions.
- **Music Explorer:** wants music recommendations with *explainable connections*, spanning their existing library and new discoveries.
- **Deep Listener:** enjoys musical history, performance context, arrangements and a listening experience with thoughtful commentary.

[Product positioning and three personas](docs/01-product-overview.md)

## One-click experience

**Pick a recording → Validate metadata → Research its story → Curate related recordings → Generate narration → Listen and discover.**

One full track/file is the input unit, even when it is part of a larger composition. Unknown essential metadata may return a clear error in v0; no automatic fingerprint recovery or sub-track passage analysis is required.

## Showcase: Six Voices, One Song

**Seed:** the six-artist performance of **Bob Dylan's “My Back Pages”** at the *30th Anniversary Concert Celebration* on **October 16, 1992**, Madison Square Garden. It marked Dylan's 30 years as a recording artist, **not his 20th anniversary**.

The proposed ~15-minute program moves from the **1992 concert recording** back to Dylan's **1964 original** (*Another Side of Bob Dylan*) and The Byrds' **1967 interpretation** (*Younger Than Yesterday*). From there, the music relation graph can branch into Roger McGuinn/The Byrds, Tom Petty, Neil Young, Eric Clapton, George Harrison and Dylan's broader work.

This illustrates **one composition, multiple recordings, many musical histories**, without needing to detect passages inside a track.

[Read the episode brief](docs/03-my-back-pages-demo.md).

## Documentation

See the [bilingual documentation index](docs/INDEX.md) and [agent contribution rules](AGENTS.md).

| Document | English | 简体中文 |
| --- | --- | --- |
| Product and personas | [Product](docs/01-product-overview.md) | [产品说明](docs/01-product-overview.zh-CN.md) |
| Requirements | [MVP](docs/02-mvp-and-requirements.md) | [MVP 需求](docs/02-mvp-and-requirements.zh-CN.md) |
| Episode demo | [My Back Pages](docs/03-my-back-pages-demo.md) | [节目演示](docs/03-my-back-pages-demo.zh-CN.md) |
| Architecture | [Architecture](docs/04-conceptual-architecture.md) | [架构说明](docs/04-conceptual-architecture.zh-CN.md) |
| Decisions / risks | [Questions](docs/05-open-questions.md) | [待决策事项](docs/05-open-questions.zh-CN.md) |
| Current status | [Status](docs/STATUS.md) | [项目状态](docs/STATUS.zh-CN.md) |

Bilingual pairs must be updated together. Each topic has one canonical document responsibility; implementation truth belongs to code and tests.

## Product boundaries

- Local music files and the personal server remain useful without AI radio generation or a streaming subscription.
- Streaming sources are optional and only integrated where actual APIs and rights allow playback.
- The episode planner distinguishes **work**, **recording**, **release** and **playable source**; it does not conflate an original with a cover or a live collaboration.
- Historical facts require evidence; subjective musical observations must not be presented as verified artist intent.
- The radio timeline orchestrates host audio and lawful recordings as separate items; no presumption of DRM capture, extraction, clipping or remixing rights.
- Public demos never commit private libraries, listening history, credentials or uncleared music.

## Sources for the new seed

- [Bob Dylan official album notes](https://www.bobdylan.com/albums/30th-anniversary-concert-celebration-deluxe-edition/)
- [Legacy Recordings concert track credits](https://www.legacyrecordings.com/releases/30th-anniversary-concert-celebration-deluxe-edition-2-cd/)
- [Bob Dylan — Another Side of Bob Dylan (1964)](https://www.bobdylan.com/albums/another-side-of-bob-dylan/)
- [MusicBrainz — 1992 concert live recording](https://musicbrainz.org/release/94fb18c0-610e-41e2-853f-32a442427a90)
- [MusicBrainz — The Byrds, Younger Than Yesterday](https://musicbrainz.org/release/85311619-b29f-4157-ae45-718cee659681)

## License

No open-source license selected. Do not assume permission to redistribute code, music or BGM.
