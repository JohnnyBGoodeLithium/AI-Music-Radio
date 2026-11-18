# 2025 Listening Data Prototype (v0.4)

[Open interactive prototype](index.html) · [Dataset JSON](data/2025-top-songs.json) · [Chinese PRD](../docs/PRD.zh-CN.md)

This is a **single-file, dependency-free HTML prototype** with embedded song records. It shows five pages: Home, My Music, Report, Music Graph, and Show / Player. All interactive pages use the same 98-record dataset derived from the user's Apple Music 2025 favorites screenshots. The JSON file is the inspectable source; the HTML embeds the same snapshot to work as a local file without a server.

Start by opening `index.html` in a browser. On restrictive iPhone file previews, **static HTML and a real SVG relationship graphic are still visible**; interactive controls need JavaScript enabled. There is no actual music, TTS, online account access or Music Assistant API integration. Play is a transparent state simulation only.

**Provenance:** Screenshot-visible ranks 1–98 and 2025 play counts. Sum of displayed play counts: 1,733. `dateAdded`, `album`, and `durationSeconds` intentionally remain null. Titles or credits truncated in source images are marked `partial`. `plays2025` is not a lifetime play count, and the screenshot sequence is not claimed to be the user's complete annual history. Raw user screenshots and credentials are intentionally not stored in this public repository.

**Graph semantics:** `same_primary_artist` and `curated_series` are observed/grouped metadata; `editorial_uses` is a proposed programming connection. No historical artist-collaboration edges are invented.

This is a UX/PRD validation artifact. Upstream Music Assistant reuse remains to be tested separately.
