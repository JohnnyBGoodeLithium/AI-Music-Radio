# Open Questions & Decision Log

**Baseline: 2026-11-18**

## Agreed concept decisions

- Local music-server capabilities are **foundational**, not just an optional source adapter.
- Three target goals: **ownership**, **discovery** and **deep listening**.
- Input unit: **one identifiable full track or audio file**. Files may be chapters/movements of longer compositions.
- Missing necessary track identity may **fail clearly**. No requirement to recover via fingerprints or detect passages inside a file.
- Prioritize music worth interpreting with verifiable facts; do not test universality with every possible meme audio.
- First showcase: Radiohead’s *Weird Fishes / Arpeggi*, an approximately 15-minute scripted, TTS-narrated radio program.
- Narration and original/licensed BGM are separate from actual music playback.
- Music copyright and streaming source restrictions are part of the product model.
- Code and technical documents live in the GitHub repository. Architecture remains exploratory.

## Product questions

1. How much of an actual NAS/music-server UX must the first demo include, versus a small indexed local folder?
2. Should the first player be a web UI on the home network, a desktop application, or both?
3. What precise metadata/evidence threshold makes a track eligible for program generation?
4. How should user favorites and history shape familiar-vs-new discovery?
5. When a recommended song is missing locally, should we replace it, provide an external link, or let the episode branch?

## Engineering questions

1. Which existing self-hosted music server or protocol provides the best foundation?
2. Which metadata services and audio analysis methods produce credible music relations with provenance?
3. Which Mandarin TTS is natural with English musician/track names?
4. How should the editable radio episode and its evidence structure be persisted?
5. Which local recordings and BGM assets have sufficient rights for a real demo?
6. What are appropriate privacy, access and remote streaming security boundaries?

## Proposed next milestones

1. Finish and review product/docs baseline.
2. Index 20–50 lawful known recordings and validate metadata error handling.
3. Implement a reviewable Music Context Pack / Editorial Planner.
4. Connect TTS, BGM and a working timeline player.
5. Add persistent music-server operations and optional authorized streaming sources.

**Cost caveat:** avoiding a streaming subscription for user-owned audio does not mean free hardware, electricity, AI inference or maintenance.
