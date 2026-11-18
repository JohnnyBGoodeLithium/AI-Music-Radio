# Positioning, Personas and User Journeys

English | [简体中文](01-product-overview.zh-CN.md)

This document expands **who the listener is, why this matters and what the complete experience feels like**. Read [README](../README.md) for a standalone product definition and [Architecture](04-conceptual-architecture.md) for modules and reuse. Named recordings belong only in the [Demo](03-my-back-pages-demo.md).

## Product promise

The listener already has abundant ways to play music and discover similar tracks. What is rarer is an editor that **understands the listener's accumulated music experience** and makes new history and artist connections compelling. The product combines the emotional resonance of a personal listening report with the research and storytelling quality of a good music program—without unsupported personality labels or AI invention.

It should connect existing data, make the collection and listening patterns understandable, and turn credible links into radio episodes the user can simply enjoy.

## Three user jobs

| Persona | Job to be done | Typical journey | Success |
| --- | --- | --- | --- |
| **Music Owner / Collection Curator** | Make an existing catalog interpretable and reusable | Import authorized favorites/playlists, inspect play counts, dates and coverage | Sees real changes without rebuilding a library |
| **Music Explorer** | Follow music relationships actively | Start from a song/artist, navigate sourced performers, works and history | Understands why each relation matters |
| **Radio Listener** | Get a complete lean-back experience | Pick from curated topics or delegate; listen, save and comment | Wants the next editorially strong show |

One person can move between all three roles. Classical guided listening, artist biographies and music-history journeys are **show formats**, not additional personas.

## Connect: familiar data first

Import authorized catalogs and playlist metadata, preserving original track IDs, plays, collection dates and source coverage. Show what was successfully imported and what is missing. Full per-play timelines are valuable but not prerequisites.

The optional question “which song changed your musical taste?” can supplement observed behavior, but should never gate setup. Listening frequency is evidence of preference; it does not establish a subjective life-changing meaning.

## Explore: cross from familiar to unfamiliar

Start from recently repeated songs, long-term collection hubs, favorite musicians or a requested topic. A relationship graph is grounded in documented performances, covers, collaborations and musical history, not raw node degree alone. Source-specific listening and collection behavior helps distinguish temporary spikes from stable tastes.

Explain not just *what follows*, but *why*: a shared performer, an era or stylistic transition, a credible historical link, or a new recording connected to familiar favorites. Allow inspection of provenance and correction.

## Listen: a personal editorial team

Offer several distinct program concepts—an unfinished thread, recent interests, an unexpected connection—or an explicitly supplied song/topic. About 15–20 minutes is a starting target, adjustable for real song durations.

Plan **host sections, song slots, transitions and endings** separately. Feedback feels like a short comment to an editor; replan affected blocks and keep valid clips where possible. Episodes can be saved, and unfinished stories can inform future shows, without requiring sequential listening.

## Experience principles

- **Explain rather than mystify:** allow evidence to be inspected; distinguish facts from interpretations.
- **Use behavior intelligently:** play count and date added matter, but do not prove private emotional significance.
- **Offer editorial agency with choice:** two or three real options; no mandatory prompt every morning.
- **Content before chat:** home shows music insights and episodes, not a full-screen chatbot.
- **Continuity without obligation:** current interests may supersede unfinished stories; make the next episode attractive.

Use [monochrome low-fi wireframes](06-lowfi-wireframes.md) to validate the information hierarchy. [MVP](02-mvp-and-requirements.md) owns first-release acceptance.
