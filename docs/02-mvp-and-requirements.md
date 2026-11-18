# MVP: Verifying the Personal Music Data → Radio Loop

English | [简体中文](02-mvp-and-requirements.zh-CN.md)

[README](../README.md) owns the full product narrative. [Feature Inventory](PRODUCT_FUNCTIONS.md) owns stable IDs and maturity. This document defines **the experiment that proves real personal music data improves the listening experience**.

## P0 acceptance

| Order | Capability | Observable acceptance |
| --- | --- | --- |
| 1 | **Import real music data** | At least one consented library export with tracks, artists, albums, playlists and available original play counts/dates added |
| 2 | **Identity and quality** | Source, missingness and count semantics shown; Work/Recording/Release/Track distinguished; imported date is not silently substituted for original added date |
| 3 | **Personal Music Report** | At least three inspectable, source-backed findings: longer-term patterns, recent spikes and music relationships |
| 4 | **Verified context** | Retrieve relevant catalog and sourced music-history evidence for a topic; do not invent performers, credits or historical links |
| 5 | **Editorial options** | At least two genuinely different story outlines, song/theme entry, target ~15–20 minutes, segment plan and availability |
| 6 | **Modular production** | Independent intro/bridges/songs/outro; rendered TTS; user-directed revision preserves unaffected assets when feasible |
| 7 | **Real playback or transparent preview** | Play only with verified source permission; otherwise clearly label metadata-only episode plans and host previews |
| 8 | **Music Assistant audit** | Run existing library/API, AI Radio Host/Show/Segment/queue, check actual data fields and classify reuse/adaptation/build |
| 9 | **Configurable providers** | User-chosen local or cloud LLM/TTS and explicit outbound data/error behavior, without silent private-data transmission |

## Evaluation design

**Editorial A/B test:** create the same topic using generic music knowledge and then using authentic personal catalog signals. Judge verifiable facts, real personal relevance, narrative flow and new discoveries, plus willingness to finish.

**Data audit:** compare source UI and import for a sample of tracks, including Play Count, original Date Added, artist, title and album. Keep provider total counts separate from counts computed from play events. Never fill missing counts with invented zeros.

**Segment audit:** ask the editor to shift from version comparison to an artist-relationship story, then observe which scripts/TTS segments changed and which were reused. Some neighboring transitions may require rerendering.

**Rights audit:** separately check catalog readability, full-track playback, audio access/mixing for each provider. Provider presence or account login is not proof of each ability.

## P1 after validated utility

More platform imports; a richer personal music network/report; optional interviews and acoustic analysis; longer editorial memory, saved shows and fuller UI. Prioritize according to evidence.

## Execution order

Audit Apple Music Windows catalog data and original statistics → generate report/editorial options → test unmodified Music Assistant AI Radio → extend only demonstrated gaps. Use monochrome low-fi UI first.

As of 2026-11-18 none of these tests have been passed **in this repository**. [Actual status](STATUS.md).
