# Decisions & Open Questions

English | [简体中文](05-open-questions.zh-CN.md)

**Scope:** cross-cutting product/architecture decisions and unresolved dependencies. Individual sample tracks, performer lists and episode running orders belong only in the [Demo](03-my-back-pages-demo.md). Stable feature states belong in [Product Functions](PRODUCT_FUNCTIONS.md).

## Agreed direction

- Product combines a **personal music storage/server foundation** with separate AI Music Radio intelligence and playback.
- Do **not** build a full backup, NAS or generic music-server replacement as a prerequisite for the radio MVP.
- Start with one full identifiable recording/file. Unknown essential identity can fail clearly; no sub-track alignment or automatic fingerprint rescue.
- Pair **metadata/verified music knowledge** with **optional whole-track acoustic analysis** when lawful and feasible.
- Retrieve candidate recordings from the **user's playable library first**. Explain the next-track selection with evidence and tagged subjective observations.
- Keep radio planning, scriptwriting, generated host assets, and authorized music playback separately represented.
- Local or cloud TextLLM/TTS is a **provider choice**, with explicit configuration and no silent data transfer or fallback.
- Maintain product, architecture, MVP, status, examples and inventory as separate documentation responsibilities, with paired English/Chinese versions.

## Open dependencies

| Area | Question | Practical next test |
| --- | --- | --- |
| Storage | Does **Lenovo Smart Storage** provide an authorized file/catalog/playback integration surface? | Inspect product/SDK documentation and test supported access; do not infer an API from music categorization |
| Library service | Should an external mature music server be reused, and what capabilities does it expose? | Compare adapters with local-folder baseline |
| Identity | What combination of tags, confidence and knowledge matching is sufficient to identify a Recording? | Curated file corpus with ambiguous titles/versions |
| Acoustic extraction | Which whole-track features are actually useful and legal to compute? | Small local DSP prototype and quality audit |
| Retrieval | How to balance verified cover/credit relations, sonic similarity, personal preference and program diversity? | Explainable candidate-ranking evaluation |
| Program | What makes a narrated sequence enjoyable rather than encyclopedic? | Listening review on varied recordings |
| Providers | What local/cloud text and TTS configurations can meet quality/cost/privacy targets? | Controlled provider comparison and explicit outbound-data audit |
| Playback | What complete-file interfaces, licensing and secure access does each backend support? | Verify actual playback with permitted files |
| User experience | Which of Owner, Explorer and Listener drives retention? | Test three different journeys, not genre stereotypes |

## Privacy & rights

Local storage avoids ongoing streaming subscriptions **for files owned and lawfully playable by the user**. It does not guarantee zero operating costs, unlimited cloud catalog access or rights to capture, cut or re-encode protected streaming. Do not publish real private libraries, listening histories, keys or uncleared media.

## Next decision checkpoint

After a small locally playable catalog and working episode path exist, choose between (a) deeper Lenovo Smart Storage integration, (b) a supported external music server, or (c) continued direct-file access. Preserve adapters so this choice does not rewrite the radio engine.
