# Demo 001 — Six Voices, One Song

English | [简体中文](03-my-back-pages-demo.zh-CN.md)

**Seed recording:** *My Back Pages*, performed by **Bob Dylan, Roger McGuinn, Tom Petty, Neil Young, Eric Clapton and George Harrison** at Madison Square Garden on **October 16, 1992**.

**Event:** *Bob Dylan: The 30th Anniversary Concert Celebration* — **30th anniversary of his recording career**, not 20th anniversary.

**Work:** *My Back Pages* written by Bob Dylan; first issued on *Another Side of Bob Dylan* (1964). The Byrds recorded a famous reinterpretation on *Younger Than Yesterday* (1967). These are **one composition and three different recordings**, not three unrelated songs.

**Status:** Proposed episode. The media assets, player and TTS have not been made yet.

## Editorial idea

An anniversary concert brings six different voices to the same composition. Why does a song written in 1964 still speak through musicians from multiple generations in 1992? Track the musical transformation in reverse chronology: an ensemble collaboration → Dylan's solitary original → The Byrds' folk-rock interpretation.

This is a **narrative about interpretation, authorship and musical relationships**, not a list of similar tracks. The concert gives additional possible branches via six artists, including the band/solo histories and collaborations, but the first episode should **not** invent causal links or turn into six biographies.

**Episode title:** *Six Voices, One Song* / 《一首歌，六种声音》

## Proposed 15-minute running order

The durations below assume representative versions: concert recording ~4:40, Dylan original ~4:22, The Byrds ~3:08, with ~2:50 for host narration and BGM. **Actual files and playback rights must be checked before generating an executable timeline.** Only use full lawful recordings; do not trim songs to meet 15:00.

| Target time | Mode | Content | Purpose |
| --- | --- | --- | --- |
| 00:00–00:40 | Host | Opening + original atmospheric BGM | Introduce six voices, one shared work |
| 00:40–05:20 | Music | **1992 live** — Dylan + McGuinn + Petty + Young + Clapton + Harrison | The seed: hear the collaboration in full |
| 05:20–06:15 | Host | Origin and the recording/work distinction | Go back from 1992 to 1964 |
| 06:15–10:37 | Music | **1964 original** — Bob Dylan | Hear the earlier acoustic, intimate interpretation |
| 10:37–11:32 | Host | How arrangement and voice change a work | Enter 1960s folk-rock |
| 11:32–14:40 | Music | **1967** — The Byrds | Compare the same writing in a band arrangement |
| 14:40–15:00 | Host | Closing + original/licensed BGM | Point to performer branches for the next episode |

The progression intentionally goes **1992 → 1964 → 1967**: start with the user's intriguing live recording, return to the source, then follow how it traveled. If this exact sequence is not available as lawful full-length recordings, replace or reschedule transparently. The target 15-minute structure is a demonstration, not an enforced cut.

## Original Mandarin host-script draft

All text below is newly written commentary. It contains no reproduced song lyrics. TTS pacing is indicative and should be calibrated to a real voice.

### 00:00 — Opening / 开场

> 想象这样一个画面：1992 年，纽约的麦迪逊广场花园，六位风格各异的音乐人，轮流唱着同一首歌。
>
> Bob Dylan、Roger McGuinn、Tom Petty、Neil Young、Eric Clapton，还有 George Harrison。
>
> 这首歌叫《My Back Pages》。它原本是 Dylan 将近三十年前写下的作品。
>
> 今天，我们从这场现场合唱出发，听听一首歌怎样穿过不同的年代，变成不同人的声音。

### 05:20 — Back to the source / 回到原点

> 刚才听到的，并不是六个人各唱各的代表作。他们围绕的是同一首《My Back Pages》。
>
> 这场演出发生在 Dylan 录音生涯三十周年的纪念音乐会上。歌曲本身则更早：1964 年，它出现在《Another Side of Bob Dylan》里。
>
> 现在我们先把舞台、乐队和众多明星暂时放到一边，回到 Dylan 自己的录音。
>
> 你可以留意，同样的旋律和词，换了演唱者、编曲与时代之后，给人的感受会有多大不同。

### 10:37 — From folk to folk-rock / 从民谣到民谣摇滚

> 听完 Dylan 的原版，再回想 1992 年那场合唱，最明显的变化，是同一首歌可以容纳多少种不同的演唱方式。
>
> 但中间还有重要的一站。
>
> The Byrds 在 1967 年把《My Back Pages》录进了《Younger Than Yesterday》。他们的版本把这首歌带进更鲜明的乐队声音里。
>
> 留意 Roger McGuinn 的声音。等你想起刚才的现场表演，这条跨越二十多年的联系就会出现。

### 14:40 — Outro / 收尾

> 一首歌，三个年代的录音，六个人同台的回声。
>
> 下一次，我们可以沿着其中任何一位音乐人继续走下去。
>
> 这就是今天的《一首歌，六种声音》。

## Why-next evidence plan

| Step | Relationship | Evidence needed | Editorial interpretation |
| --- | --- | --- | --- |
| 1992 live → Dylan 1964 | **Same work; distinct recording** | Official Dylan discography and concert credits | What changes when six voices give way to the writer's earlier solo version? |
| Dylan 1964 → The Byrds 1967 | **Cover/interpretation of same work** | Album credits and release/recording metadata | What changes when a folk song becomes a band recording? |
| The Byrds → future branch | **Roger McGuinn performs both 1967 and 1992 versions** | Recording credits for both | Follow a performer through decades |
| Concert → future branches | **Live collaboration of six credited artists** | Label and MusicBrainz performer credits | Explore their other music and verified connections |

Do not claim that a performer felt or intended something unless a reputable source establishes it. A listener-oriented observation about sound is an interpretation, not a historical fact.

## Music server and AI system responsibilities

- **Local music server:** each version is a distinct `Recording` with a separate locally accessible file and duration, all linked to one `Work`.
- **Music Context Pack:** verified event date, credits, 1964 work origin, 1967 arrangement/version, album identities, user-permitted collection availability and citations.
- **Editorial planner:** choose a meaningful thread through these relationships and decide time budget.
- **TTS:** natural Mandarin narration with accurate names; one consistent host voice, room for silence.
- **BGM:** original/licensed minimal acoustic/ambient transitions; speech ducking; music plays separately and in full.
- **Playback:** show current recording, progress, why-next evidence, source status, save and branch.

## Rights & feasibility

The official concert video or YouTube link is **not** a license to download or extract audio. For demo execution, supply legally controlled/authorized local copies, or integrate a provider that explicitly supports the required playback. No unauthorized audio samples in Git; use metadata-only placeholders until cleared.

## Verified reference materials

1. [Bob Dylan official concert notes](https://www.bobdylan.com/albums/30th-anniversary-concert-celebration-deluxe-edition/) — October 16, 1992, anniversary purpose, singer lineup and 1964 origin.
2. [Legacy Recordings track list](https://www.legacyrecordings.com/releases/30th-anniversary-concert-celebration-deluxe-edition-2-cd/) — six artists credited to `My Back Pages`.
3. [Bob Dylan — Another Side of Bob Dylan](https://www.bobdylan.com/albums/another-side-of-bob-dylan/) — 1964 release/work context.
4. [MusicBrainz concert release](https://musicbrainz.org/release/94fb18c0-610e-41e2-853f-32a442427a90) — recording and performer metadata, representative ~4:40 duration.
5. [MusicBrainz — Younger Than Yesterday](https://musicbrainz.org/release/85311619-b29f-4157-ae45-718cee659681) — The Byrds' 1967 interpretation.
6. [MusicBrainz — My Back Pages work](https://musicbrainz.org/work/b85b3a85-b955-3a99-99e8-168027489954) — original recording context.

These links support facts only; they do not establish audio use rights.
