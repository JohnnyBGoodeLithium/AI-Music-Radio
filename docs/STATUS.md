# Current Project Status

English | [简体中文](STATUS.zh-CN.md)

**As of 2026-11-19: a tested low-fidelity interactive prototype exists, but the product is not integrated with real music platforms or AI audio.**

**Delivered:** User-supplied Apple Music 2025 favorites screenshots were transcribed into ranks 1–98 (visible displayed plays sum to 1,733). The same dataset powers Home, My Music, Music Report, Music Graph, and Show / Player, including linked track details and a demo of selective host-segment edits. Desktop, mobile and JavaScript-disabled static fallback were checked.

**Data limits:** Screenshot transcription is not a live Apple Music API import. These are screenshot-visible 2025 annual plays, not lifetime history. Date Added, event timestamps, verified full album/version IDs and track durations are unavailable. Graph edges include only observed same-artist, recognizable-series and editorial-reference relationships.

**Not yet implemented:** Live library sync, playback rights/actual audio, Music Assistant or AI Radio integration, sourced historical music-relationship research, real LLM/TTS, duration-accurate program production.

[PRD v0.3](PRD.md) · [Interactive prototype](../prototype/index.html) · [Data JSON](../prototype/data/2025-top-songs.json) · [MVP](02-mvp-and-requirements.md).
