# Decisions & Open Questions

English | [简体中文](05-open-questions.zh-CN.md)

**Baseline · 2026-11-18**

## Decisions established in product discussion

- Local personal music server is foundational; users' lawful files remain accessible without an ongoing streaming subscription.
- The three personas are **Music Owner, Music Explorer and Deep Listener**.
- A seed is **one complete identified recording/file**, even if part of a larger musical work.
- Essential metadata can be a prerequisite. Unknown identity may return an error; no compulsory fingerprint or within-track passage recovery in v0.
- Prioritize recordings with meaningful, credible stories; no requirement for viral short-form music coverage.
- **New Demo 001 seed:** 1992 live *My Back Pages* from **Bob Dylan's 30th Anniversary Concert Celebration**, not a 20th-anniversary show.
- First exploration thread: concert collaboration → Dylan's 1964 original → The Byrds' 1967 recording, with performer-based expansion in later iterations.
- Narration and original/licensed BGM remain logically separate from song playback; actual music rights constrain production.
- Core product documents and README are paired English/Simplified Chinese, with simultaneous updates; `AGENTS.md` defines rules.
- No implementation or model stack has been committed.

## Open product questions

1. Should MVP start with an indexed desktop directory or a running self-hosted music server?
2. Should the first client be a browser, desktop app or a home-network multi-device player?
3. What is the minimal evidence threshold to generate an episode without hallucinating?
4. How should a recommendation choose between **same-work versions** and other artists' related works?
5. How should the system handle tracks missing from the local library?
6. Which behaviors must work without internet connectivity, versus cloud model services?

## Open engineering questions

1. Which existing self-hosted server and playback APIs can be reused?
2. How should Music Context Pack store Work/Recording/Release identity and citations?
3. How can multi-artist credits and version relationships be verified?
4. Which Mandarin TTS handles six English-speaking artist names naturally?
5. Which lawful audio files/rights-cleared beds can be used for the actual demo?
6. What are real demo asset durations, audio levels, license limits and target hardware budgets?

## Immediate steps

1. Confirm legal copies of the 1992 live, 1964 original and 1967 Byrds recordings.
2. Validate minimum metadata and a deterministic library catalog.
3. Build the first evidence-based editorial plan.
4. Produce original Mandarin narration, licensed/original BGM and timeline player.
5. Test listening quality and source accuracy before expanding artist branches.

## Important limitations

No actual audio availability, duration on target assets, TTS model, streaming SDK or working server has been tested. Avoid presenting proposed capabilities as implemented facts.
