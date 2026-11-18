# MVP Requirements

**Proposed scope · 2026-11-18 · Not a committed stack**

## P0 — Demo requirements

| Feature | Required behavior |
| --- | --- |
| Single-track input | Select a complete audio file / identified track, not an arbitrary excerpt |
| Metadata validation | Establish artist/title and sufficient identity; show error if unidentified; optional cover/year absent need not fail |
| Music research | Reliable, cited facts and musical-context evidence |
| Relation / recommendation | Choose relevant follow-up music and provide concrete why-next reasoning |
| Editorial planner | Reviewable theme, running order and duration estimate before script generation |
| TTS | Natural Mandarin host, tested for English music names |
| BGM / sound | Original/licensed ambient beds, natural fades and speech ducking |
| Timeline player | Sequential host/music playback with pause, skip and recommendation explanation |

## P1

Persistent desktop/NAS library scanning; metadata cleanup; music embeddings and acoustic analysis; personal music profile; saved editable episodes; cross-device access; optional authorized streaming adapters.

## Outside first-demo scope

Unlabeled-audio fingerprint identification, within-file passage analysis, automatic orchestral score alignment, full streaming-platform synchronization, universal short-video-music coverage and mandatory fully local LLM/TTS deployment.

## Acceptance criteria

- One click on a known recording yields an intentionally curated show.
- Listeners can articulate *why* a recording follows the previous one.
- Facts have provenance; subjective sonic interpretations are not misrepresented as documented artist intent.
- Host sounds natural and handles mixed Mandarin/English.
- BGM remains subordinate to speech.
- Missing identity or unplayable source produces an honest user-visible state.
- Approximate 15-minute program target is adapted to actual audio durations and usage rights.

## Demo development order

20–50 legally playable test tracks → minimum metadata index → evidence-backed music relation examples → editorial episode planner → generated TTS/BGM → timeline playback → personal profile and music-server integrations.
