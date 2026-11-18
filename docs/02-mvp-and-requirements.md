# MVP Requirements and Acceptance

English | [简体中文](02-mvp-and-requirements.zh-CN.md)

**Goal: show that personal music data creates better insights and narrated programs.** Stable IDs: [Functions](PRODUCT_FUNCTIONS.md). Actual state: [Status](STATUS.md).

1. Import authorized Apple Music Windows or other music library/playlist metadata, especially original **play count and date added**, source and missingness. Audio file optional.
2. Preserve platform IDs, counting semantics/period, original versus imported date, matching uncertainty. Never add incompatible provider counts.
3. Create an evidence-backed Personal Music Report: long-term interests, recent spikes, artist relationships and grounded musical history.
4. Use a small, relevant Music Context Pack, not a raw full-library LLM prompt. Distinguish inferred patterns from verified facts.
5. Propose at least two distinct ~15–20-minute editorial journeys, or accept a song/theme, with a plan and lawful source availability.
6. Produce modular script/TTS/music items and demonstrate a targeted feedback/segment revision; only play tracks through permitted sources.
7. **Test Music Assistant + AI Radio first:** catalog/queue/API, Hosts, Shows, segment rendering, personal stats and playback restrictions.
8. Permit explicit local **or** cloud LLM/TTS; show errors, missing data and rights restrictions honestly.

**P1:** broader platforms, optional owned songs/acoustic analysis, editorial memory, reports/graph detail, optional interviews, saved episodes, [low-fi UI](06-lowfi-wireframes.md), potential later Smart Storage. Qira requires internal design approval.

**Out of scope:** general NAS/Agentic Storage, Home Assistant, 24×7 DT, mandatory local AI, DRM capture/remix or rewriting Music Assistant without a measured gap.

**Acceptance:** validate real import/count/date coverage; produce a sourced report and two episode plans; compare generic and personally grounded quality; render a modular spoken draft; verify playback entitlement; document upstream reuse vs gaps. **None passed yet.**
