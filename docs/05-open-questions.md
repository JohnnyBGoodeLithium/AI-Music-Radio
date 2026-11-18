# Decisions & Open Questions

English | [简体中文](05-open-questions.zh-CN.md)

**Product scope:** Daily music data → source-backed Personal Music Report → personally curated narrated radio. **Not** Home Assistant, generic NAS/Agentic Storage, household services or 24×7 DT; those are separate future explorations.

Agreed: original play count/date-added and coverage matter; local files/local inference optional; evidence not mysticism; multiple ~15–20-minute program choices; optional interviews; modular clips and feedback, with possible story continuation. Music Assistant is a reuse-first *candidate*, not integrated. Monochrome Notion-like low-fi UI comes before Qira branding.

## Unknowns to test

| Area | Test |
| --- | --- |
| Data export | Compare Apple Music Windows play count/date-added/playlist data with exported file |
| Music Assistant | Inspect catalog/API behavioral fields; run Host/Show/Segment/queue and measure partial editing |
| Experience | Compare generic AI DJ with grounded personal music story and report |
| Rights | Separate metadata import, subscription login, lawful playback and remixing |
| UI | Validate [wireframe concepts](06-lowfi-wireframes.md) before choosing full frontend rewrite |

Named song examples remain [Demo-only](03-my-back-pages-demo.md); maturity belongs to [Functions](PRODUCT_FUNCTIONS.md).
