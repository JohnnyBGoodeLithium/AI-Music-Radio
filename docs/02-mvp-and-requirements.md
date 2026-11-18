# MVP Requirements and Acceptance

English | [简体中文](02-mvp-and-requirements.zh-CN.md)

This document defines **what the first product must do**, not the implementation details or an individual demo track. Feature IDs and maturity belong only to [Product Functions](PRODUCT_FUNCTIONS.md); current actual progress belongs to [Status](STATUS.md).

## P0 — Vertical slice

1. **Connect an existing library:** Index a user-authorized local directory and safely read lawful complete audio files. No requirement to build new NAS storage/backup infrastructure.
2. **Metadata gate:** Parse known artist, title and available release/recording/version identifiers. Block truly unidentified recordings with a clear error. Missing cover, year or optional acoustic data alone must not block.
3. **Distinct recording identity:** Model Work / Recording / Release / PlayableSource and credits separately; do not merge versions just because titles match.
4. **Context Pack:** Assemble provenance-aware metadata, music knowledge, user-library availability and *optional* whole-track acoustic features. Annotate certainty and missingness.
5. **Relationship retrieval:** Generate candidates from **the user's own library first**, using explicit music relations and optionally audio similarity. Preserve a specific reason and source for each relationship.
6. **Editorial planning:** Choose a theme, sequence, transitions, length budget and playable source for each proposed track before writing the script.
7. **Model-provider abstraction:** Support explicit **local or cloud** text-LLM configuration through a consistent interface. No silent remote fallback or private-file upload. Test configuration and error behavior even if only one real provider is used in an early demo.
8. **Narration and BGM:** Generate original speech with a replaceable TTS provider, add lawful BGM with ducking, and preserve the music as separate authorized playback items.
9. **Radio player:** Execute the planned host/music timeline with real durations, play/pause/skip, track identity and explainable next-track information.
10. **Clear errors:** Report unidentifiable metadata, absent playable tracks, restricted sources and provider failures without inventing results.

## P1 — Personal media experience

- Evaluate Lenovo Smart Storage's **actual** file, identity, permission and playback APIs; build an adapter only if supported.
- Optionally integrate an existing music server; do not reimplement a mature server just to generate radio.
- Persistent background indexing, metadata repair, cross-device access and secure remote access.
- Personal music profile from permitted collection history, saved playlists and listening data.
- Robust acoustic analysis (tempo, timbre, harmony, embeddings) on lawfully analyzable local files.
- Discovery beyond local library, with explicit availability and user authorization.
- Episode saving, alternative editorial themes, recuration and partial regeneration.
- Validate at least one local LLM and one cloud LLM end-to-end; compare quality, latency, resource and privacy boundaries.

## Not in the first version

- Detecting arbitrary sub-track moments or score/audio alignment.
- Fingerprint-based rescue of files with no usable identity.
- Building a full independent NAS, backup, file-sharing or multi-user platform.
- Guaranteed Spotify/Apple Music/NetEase DRM capture, extraction or unlicensed blending.
- Treating a mood label or a similarity score as a factual artistic relationship.
- Claiming all AI inference is offline or free, or that local models match cloud quality without testing.

## Acceptance: core user story

Given a playable, clearly identified recording in an authorized personal music library:

1. Show its canonical metadata and available source.
2. Offer a theme and two or more *actually playable* related recordings from the user's collection, with evidence or clearly labeled subjective acoustic reasoning.
3. Allow the user to inspect the sequence, then generate natural narration.
4. Play a coherent radio show with independent host/BGM and full tracks, adapting to real track lengths.
5. Show meaningful error states for missing metadata and unavailable tracks.

Evaluation must cover **editorial coherence**, **metadata correctness**, **musical relation evidence**, **audio listening quality**, **privacy/configuration behavior**, and **successful real playback**. Exact model choice and hardware are not yet committed.
