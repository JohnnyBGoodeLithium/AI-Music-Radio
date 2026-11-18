# Product Overview & Personas

English | [简体中文](01-product-overview.zh-CN.md)

**Purpose:** product positioning, customer needs and user journeys only. Architecture belongs to [Architecture](04-conceptual-architecture.md); individual demo recordings belong only to [Demo](03-my-back-pages-demo.md).

## Product promise

Turn a **personally controlled music library** into a place for rediscovery and listening. A dedicated AI radio layer chooses an identified complete recording, researches credible context, finds narratable connections to available music, and produces an editorially coherent, naturally voiced program.

The personal music server and the radio layer are separable: the library and lawful playback must remain useful without AI generation.

## Three clearly distinct user jobs

| Persona | Main job | Behavior | What success looks like |
| --- | --- | --- | --- |
| **1. Music Owner — Collector / Curator** | **Keep & control** a durable personal collection | Maintains local files and server; wants reliability and cost predictability | Own files accessible, organized, and rediscovered without streaming subscription dependence |
| **2. Music Explorer — Active Discoverer** | **Find & choose** what to listen to next | Lean-forward: starts from a seed, explores connections, evaluates recommendations and saves discoveries | Finds previously unknown, relevant recordings with credible *why-next* reasons |
| **3. Radio Listener — Lean-back Audience** | **Listen without managing the queue** | Lean-back: wants a compelling host, strong pacing and continuous context while working, resting or commuting | Finishes programs, enjoys natural voice/transitions and needs few manual skips |

These roles can overlap within one person, but their **jobs and interactions are different**. A deep historical/compositional listening theme is a **program mode**, not an additional, nearly identical discovery persona.

## Core journeys

### The Owner

Connect a local collection → inspect/repair known metadata → play across supported devices → allow the radio engine to rediscover an overlooked recording. Ownership and basic playback work even if AI is unavailable.

### The Explorer

Choose a familiar recording → review a theme and explainable relationship path → follow related music from the personal collection → optionally branch to new music where lawful playback/discovery exists → save what was found.

### The Listener

Choose a track, theme or saved episode → press **Create Radio / Play** → enjoy original host narration, BGM and full recordings as one continuous queue → skip or save without navigating a complex relation graph.

## What makes it different?

1. **Local music is a first-class asset**, not a cache of leased tracks.
2. **Music understanding blends metadata/knowledge and acoustic evidence**; personal collection availability constrains the actual program.
3. **The episode is curated**, with a defensible reason for each transition.
4. **Provider-neutral models** permit local or explicitly configured cloud generation.
5. **Full-track input** and rights-aware playback keep the first version tractable.

## Positioning boundaries

Not an alternative commercial subscription catalog; not a generic AI audio transcription/segmentation tool; not a guarantee of fully offline or zero-cost inference. The first version favors recordings with reliable identity and interpretable musical context, and can reject insufficient metadata.

Primary launch priority: **Owner + Listener** for a tangible utility and a compelling radio demo; Explorer provides the sustained discovery loop. This is a proposal to validate rather than a finalized business segmentation.
