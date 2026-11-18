# Product Function Inventory

English | [简体中文](PRODUCT_FUNCTIONS.zh-CN.md)

**This is the one stable inventory of product capabilities**, modeled on the four-level IDs and maturity/evidence discipline used by [Meeting Minutes](https://github.com/JohnnyBGoodeLithium/Local-Video-Meeting-Minutes/blob/main/docs/PRODUCT_FUNCTIONS.md). This is not a user story, demo script, release log or plan for this week's work.

- **Stable ID:** `module.domain.group.function` (four levels). Once shipped, never renumber or reuse IDs.
- **Priority:** P0 = core contract/security; P1 = main experience; P2 = operational improvement; P3 = polish.
- **Maturity:** Planned / Implemented, unverified / Experimenting / Validated. All functions are **Planned** at this documentation-only baseline; descriptions do not assert that code exists.
- **First release / Major update / Git:** `—` means **not released / no implementation evidence yet**. Add a real version and commit only when verified.
- **Evidence:** implementation and validation truth belongs to code, tests and Git; [Status](STATUS.md) summarizes current reality. Proposed product scope belongs to [MVP](02-mvp-and-requirements.md).
- Read the full table only when doing a capability review, release audit, or changing a function. Normal agents use AGENTS → STATUS → INDEX → one relevant document.

## Capability overview

| Module | Responsibility | First path |
| --- | --- | --- |
| 1. Library & sources | Connect existing storage; identify recordings and playable sources | Local folder, not a new NAS |
| 2. Music intelligence | Metadata, sourced knowledge, optional acoustic features and personal context | Metadata/verified relationships first |
| 3. Radio producer | Select narratable links in the available collection and create a program | Plan before script |
| 4. Model & audio providers | Local/cloud text models, TTS, BGM, explicit data boundaries | Replaceable providers |
| 5. Player & continuity | Executable timeline, explanation, interaction and failure recovery | Full tracks + original host assets |

## Functions

| ID | Feature | Contract / boundary | First release | Last major enhancement | Key Git | Priority | Maturity |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1.1.1.1 | Local folder adapter | Index user-authorized complete audio files without building backup/NAS services. | — | — | — | P0 | Planned |
| 1.1.1.2 | Lenovo Smart Storage adapter | Integrate only after authenticated list/read/play interfaces and permissions are confirmed. | — | — | — | P1 | Planned |
| 1.1.1.3 | External music-server adapter | Optional supported media-server catalog/stream adapters; not required for first demo. | — | — | — | P1 | Planned |
| 1.2.1.1 | File tags & identity gate | Read tags; establish recording identity, or return a clear unknown-metadata error. | — | — | — | P0 | Planned |
| 1.2.1.2 | Work/recording identity | Keep compositions, performances, releases, artists and versions distinct. | — | — | — | P0 | Planned |
| 1.2.1.3 | Source resolver | Resolve available authorized local playback and explicit unsupported-source states. | — | — | — | P0 | Planned |
| 2.1.1.1 | Source-backed music knowledge | Enrich metadata/relationships with provenance and uncertainty, never guessed intent. | — | — | — | P0 | Planned |
| 2.1.1.2 | Whole-track acoustic features | Optional lawful tempo/rhythm/timbre/harmonic summaries and embeddings, no passage detection. | — | — | — | P1 | Planned |
| 2.1.1.3 | Personal music profile | Permissioned favorites, playlists and play history; distinguish collected/released/played dates. | — | — | — | P1 | Planned |
| 2.1.1.4 | Music Context Pack | Combine verified identities, research, acoustic evidence, personal context and playability. | — | — | — | P0 | Planned |
| 3.1.1.1 | Library-first candidate retrieval | Find candidates inside owned playable library before external discovery suggestions. | — | — | — | P0 | Planned |
| 3.1.1.2 | Narratable why-next relations | Each candidate carries typed relation, evidence, confidence and editorial explanation. | — | — | — | P0 | Planned |
| 3.1.1.3 | Editorial episode planner | Select theme, track order, transitions and duration based on actual playable sources. | — | — | — | P0 | Planned |
| 3.1.1.4 | Grounded narration scripts | Write intro, transitions and outro from cited facts; keep observations subjective. | — | — | — | P0 | Planned |
| 4.1.1.1 | Local/cloud TextLLM | Explicit configurable local and cloud interfaces; no silent external fallback. | — | — | — | P0 | Planned |
| 4.1.1.2 | Replaceable TTS provider | Generate natural host speech via locally or remotely configured TTS, with audio metadata. | — | — | — | P0 | Planned |
| 4.1.1.3 | Licensed BGM & ducking | Mix original/licensed background music under host speech only; protected music remains separate. | — | — | — | P0 | Planned |
| 4.2.1.1 | Explicit provider privacy | Show outbound data/permission; no silent raw-audio or private-history uploads. | — | — | — | P0 | Planned |
| 5.1.1.1 | Episode timeline player | Play independent full recordings and host assets with real duration, pause/skip. | — | — | — | P0 | Planned |
| 5.1.1.2 | Recommendation explanation | Show why each next recording belongs, with a link back to evidence where practical. | — | — | — | P0 | Planned |
| 5.1.1.3 | Save & branch | Save program and start a new journey from a related recording. | — | — | — | P1 | Planned |
| 5.2.1.1 | Honest errors and recovery | Distinguish metadata, missing source, rights and provider errors; no fabricated completion. | — | — | — | P0 | Planned |

## Updating the inventory

1. Changes to feature scope update this row and the paired Chinese row in the **same change**.
2. A feature becomes Implemented only after real code exists; becomes Validated only after specific tests/usage evidence exists.
3. When released, fill the true release version, commit and important enhancement references. Never backfill fictional evidence.
4. Do not duplicate complete function rows in README, Status or sample demo; use links.
