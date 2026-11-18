# MVP Requirements

English | [简体中文](02-mvp-and-requirements.zh-CN.md)

**Draft scope · 2026-11-18 · No implementation commitment**

## P0 — One end-to-end radio episode

| Capability | Minimal acceptance |
| --- | --- |
| One-track seed | Select a complete identified recording; v0 does not inspect in-file passages |
| Metadata gate | Required title, artist and sufficiently reliable recording identity; unknown identity yields an explicit error |
| Library playback | Use locally owned, lawfully playable audio; demonstrate a simple indexed library/queue |
| Source-backed research | Recover verifiable facts about composition, participants, event, recording and release |
| Recording-aware relations | Distinguish Dylan 1964, The Byrds 1967 and 1992 concert recordings of the **same work** |
| Editorial planner | Decide theme, sequence, why-next links and time budget before creating narration |
| Voice generation | Natural Mandarin TTS, correct English proper names, consistent pace/timbre |
| BGM and assembly | Original/licensed music beds, ducking and fades; no mixing of unauthorized recordings |
| Episode player | Timed narration and lawful full-track playback with pause/skip and transparent recommendations |
| Bilingual documentation | English and Simplified Chinese content parity in the same edit |

## P1 — Expansion

- Persistent desktop/NAS music indexing and cross-device access.
- Personal listening profile drawn from user-authorized libraries and history.
- Broader artist/recording relationship network: collaborators, interpretations, stylistic paths.
- Editable episode plans, source-aware listening queue and playback recovery.
- Acoustic analysis and embeddings when audio can be lawfully analyzed.
- Explicitly authorized streaming adapters; optional local model deployment.

## First-demo non-goals

- Automatic fingerprint rescue of completely unknown/unlabeled recordings.
- Detecting or aligning passages **inside** a musical recording.
- Universal viral-music, arbitrary recording or genre coverage.
- A full replacement for every streaming service or a promise of no ongoing cost.
- Using copyrighted song snippets unless specifically licensed; do not capture or decode DRM output for mixing.
- Full local-only inference, production NAS product, multi-user authentication or stable public API.

## Acceptance review

1. A valid 1992 concert recording produces an inspectable episode proposal.
2. Composition, release, event and performers are not mixed up; facts can be traced to sources.
3. The path from live collaboration to original to later interpretation is musically and historically defensible.
4. The approximately 15-minute plan adjusts to the **actual** legal audio assets and narration.
5. TTS is natural, factual narration clear and BGM does not overpower speech.
6. Missing metadata and unavailable audio produce honest, comprehensible failure states.

## Build order

A small lawful test catalog → identity validation → Music Context Pack & relationships → episode planner → Mandarin TTS/BGM → timeline player → deeper music-server and user-profile integrations.
