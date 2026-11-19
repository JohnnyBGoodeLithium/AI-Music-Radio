# AI Music Radio — Product Requirements Document

**Version:** v0.5 · 2026-11-19  
**Status:** product discussion and interactive prototype, not a working music integration  
**Prototype:** [2025 personal-listening data H5](../prototype/index.html) · **Dataset:** [98 ranked tracks](../prototype/data/2025-top-songs.json)  
[中文版完整 PRD](PRD.zh-CN.md)

## Goal and scope

AI Music Radio turns existing daily music data into an explainable **Personal Music Report**, a grounded **Music Graph**, and personalized, narrated **radio show proposals**. This PRD specifies what users do, what each screen must show, how data must remain linked, what happens when data is missing, and how to verify a demonstration. The README remains the standalone product overview, and the function inventory remains the source of stable feature IDs.

The current prototype uses **real track titles, artists, ranks and 2025 play counts transcribed from user-supplied Apple Music “2025 favorite songs” screenshots**. Ranks **1–98** are visible. The sum of those displayed plays is **1,733**, not a claim about the user's complete annual or lifetime listening. Original date added, individual play timestamps, verified album identities, track durations and commercial audio rights are not available. Truncated screenshot labels are kept partial rather than fabricated.

The repository publishes metadata only for this demonstration; it does not publish source screenshots, Apple credentials or commercial audio files.

## Information architecture and workflows

The five interactive product screens are **Home / Radio**, **My Music**, **Music Report**, **Music Graph**, and **Show / Player**. A single track ID must refer to the same record in lists, insights, graph nodes and shows. Editorial changes may affect script sections but must never silently rewrite the original user-listening observations.

| Requirement | User experience | Acceptance criteria |
| --- | --- | --- |
| **FR-01 Home** | Show relevant data-backed insights and multiple show ideas without requiring a prompt | Insight totals and episode links match the shared dataset |
| **FR-02 My Music** | Browse/search 98 ranked tracks; view original 2025 play count, source and missing-field information in track detail | Rank/artist/count faithfully reflect screenshot transcriptions; no invented dates |
| **FR-03 Music Report** | Explain repeated artists, work-series clusters and recent vs long-term uncertainty | At least three factual findings; aggregated group values recompute from track IDs |
| **FR-04 Music Graph** | Select an artist/work-series group, view graph edges and inspect a connected track | Every edge has a defined semantic and evidence; mobile graph and static SVG fallback available |
| **FR-05 Editorial Planner** | Choose between distinct programs grounded in observed favorites | At least three proposals, each with traceable referenced tracks and a structured show outline |
| **FR-06 Show / Player** | Inspect Intro/Music/Narration/Bridge/Outro and leave an editorial comment | A sample comment selectively revises narration without changing track IDs or play counts |

### Data contract

A song record has an immutable `id`, observed `rank`, `title`, `artist`, `plays2025`, `playCountScope`, `source` and `partial` flag. `dateAdded`, `album`, and `durationSeconds` are null when the screenshots do not supply those fields. `audioAvailable=false` makes clear there is no authorized recorded audio in the prototype.

The graph currently supports `same_primary_artist` (songs attributed to the same named primary artist), `curated_series` (tracks recognizable as belonging to the same musical-theatre series), and `editorial_uses` (a show proposal references a track). **These links do not prove musician collaboration or historical influence.** Such relationships require separate sourced research.

### Demonstration examples and evidence

- **Red Velvet:** six visible tracks, a sum of 150 displayed 2025 plays.
- **Hamilton:** eight recognizable musical-theatre-series tracks, 169 displayed 2025 plays; grouping is editorial/series identity, not performer collaboration.
- **孙燕姿:** five visible tracks, sum 70; **Queen:** four tracks, sum 47; **方大同:** three tracks, sum 47.

Program examples are **“From What'd I Miss to Broadway”**, **“Six Faces of Red Velvet”**, and **“From 克卜勒 to Under Pressure”**. The last is explicitly an editorial juxtaposition, not a claim of artistic collaboration.

### Error and safety states

- Treat unavailable Date Added, album and duration as unknown—not zero or today's date.
- Mark truncated titles and performer credits as incomplete.
- Keep screenshot-scope 2025 plays distinct from lifetime plays or timestamped event history; never infer listening hour/month from totals.
- Permit insight/report/show planning without playback rights; **do not simulate real commercial audio** or misrepresent a 15–20-minute target as an actual produced timeline.
- Preserve source descriptions for data-backed findings. Do not fabricate credit or influence edges to make the graph visually richer.
- Show a meaningful static, no-JavaScript HTML experience in restrictive iOS file previewers.

## Music Assistant reuse decision

**Reuse-first candidate:** source providers and `controllers/music` for catalog access; `controllers/player_queues` and `controllers/streams` for actual licensed playback; `providers/ai_radio` Host/Show/Segment/Queue DJ and TTS for narration; optional statistics, Smart Playlist and sonic analysis. The **project-specific increment** is original external behavioral-data provenance, an explainable report and sourced music relationship semantics, genuine multi-option editorial planning, and feedback-conditioned segment edits.

None of these Music Assistant integrations has been run or verified in this repository. Whether the existing frontend can be restyled or requires a separate UI should be decided after an API and interaction test, not assumed upfront. Local/cloud inference and external music sources are permitted implementation options, subject to user consent and provider rights.

## Definition of done for this prototype

Verify 98 consecutive unique ranks, aggregate count 1,733, report/group totals, shared ID navigation across screens, segment-level comment changes, desktop/mobile responsive layout, static no-JS fallback and no commercially playable audio. These tests verify a **prototype**, not a finished product. Subsequent milestones include real Apple Music metadata ingestion, sourced artist relationship research, Music Assistant integration, actual TTS, licensed playback and true duration scheduling.


## v0.4 — Cross-artist knowledge network (FR-04 correction)

The earlier one-artist star (MusicGroup → Tracks) is merely a **collection grouping**, not a sufficient Music Graph. The default graph must visualize multiple real-world people and works connected by sourced, typed relationships, while keeping ranked songs and externally researched entities distinct.

Four grounded example paths: (1) Queen → **Under Pressure** (#64) → David Bowie → **Transformer** → **Perfect Day** (#20) → Lou Reed; (2) Bob Dylan (#85) → **Girl from the North Country** → Johnny Cash (#82); (3) Red Velvet (#3) → **Beautiful Christmas** → aespa (#2); (4) Sting (#90) → The Police (#63).

Each node has a stable ID, entity type, and `inRanking` or external indicator. Each edge has a type, written claim, provenance and optional external `sourceUrl`. Screenshot-based attribution is distinct from published history; **never force unsupported links or imply external tracks were in the user's library**.

On click: ranked songs open the existing track drawer, external music entities show their identity and edges, and edges open evidence and the source link. Each grounded path leads to a distinct editorial show plan. Default network view shows all cross-artist paths; the older song-collection star view remains secondary. On iPhone display vertical SVG paths; without JS show equivalent static SVG and source links.

Acceptance: four verifiable cross-artist paths visible and interactive, consistent track IDs, and evidence for every nontrivial history edge. Neither actual AI inference nor playback is claimed.


## v0.5 — Full-library knowledge network (correction to FR-04)

**The default Graph must contain every one of the 98 ranked songs as a node in ONE global network**, not a handful of cherry-picked cross-artist paths or one artist's star. Source-credit entities are created from the exact observed attribution strings (including truncated labels), linked to each ranked Track. Recognizable Hamilton series items are explicitly labeled curated grouping with unverified version detail. Existing fact-checked external artists/works/albums and typed music-history relations belong in the same graph but are clearly distinct from the listener's collection.

Disconnected components are expected when evidence is sparse. Do not fabricate relationships to force connectivity. The network is scalable and pannable, searchable by song and source credit, supports zoom/fit and evidence on edge click. Preset artist-history paths change the viewport only—no other track disappears from the DOM. A visible 98-song index is a navigation aid, not a replacement for in-graph nodes. The legacy artist-star visualization is secondary.

**Acceptance:** 98 unique ranked Track nodes; each appears in the global SVG and has at least one attributable edge; original ranks/counts unchanged; verified external facts and source links retained. iPhone/JavaScript-disabled static fallback renders the SAME complete graph, not a small sample. This is a prototype; real playback and history imports remain unimplemented.
