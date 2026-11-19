# 2025 Listening Data Prototype (v0.4)

[Open interactive prototype](index.html) · [Dataset JSON](data/2025-top-songs.json) · [Chinese PRD](../docs/PRD.zh-CN.md)

This is a **single-file, dependency-free HTML prototype** with embedded song records. It shows five pages: Home, My Music, Report, Music Graph, and Show / Player. All interactive pages use the same 98-record dataset derived from the user's Apple Music 2025 favorites screenshots. The JSON file is the inspectable source; the HTML embeds the same snapshot to work as a local file without a server.

Start by opening `index.html` in a browser. On restrictive iPhone file previews, **static HTML and a real SVG relationship graphic are still visible**; interactive controls need JavaScript enabled. There is no actual music, TTS, online account access or Music Assistant API integration. Play is a transparent state simulation only.

**Provenance:** Screenshot-visible ranks 1–98 and 2025 play counts. Sum of displayed play counts: 1,733. `dateAdded`, `album`, and `durationSeconds` intentionally remain null. Titles or credits truncated in source images are marked `partial`. `plays2025` is not a lifetime play count, and the screenshot sequence is not claimed to be the user's complete annual history. Raw user screenshots and credentials are intentionally not stored in this public repository.

**Graph semantics:** `same_primary_artist` and `curated_series` are observed/grouped metadata; `editorial_uses` is a proposed programming connection. No historical artist-collaboration edges are invented.

This is a UX/PRD validation artifact. Upstream Music Assistant reuse remains to be tested separately.


## v0.5 · 真实跨音乐人知识网络

默认 Music Graph 现在同时展示四条有外部资料支持的关系：Queen—David Bowie—Lou Reed、Bob Dylan—Johnny Cash、Red Velvet—aespa、Sting—The Police。每条关系边可查看证据，未入榜的专辑/合作曲目明确标注外部知识；图谱可跳至相应的**模拟**节目策划。

原有按音乐人展开歌曲的星形图保留为辅助“榜单聚合”，不是知识图谱的默认视图。iPhone 纵向 SVG 与禁用 JavaScript 的静态图均可阅读。外部出处随数据保存在 `data/2025-top-songs.json` 的 `knowledgeGraph` 中。


## v0.6 · 全部 98 首歌曲进入一张可探索的知识图谱

全量图谱不再只显示选中歌手或四条精选路线，而是从全部 98 条榜单 Track 生成节点，连接截图原样署名的音乐人/演奏者、Hamilton 作品系列和已核实的外部音乐知识。可全局浏览、缩放拖动、按歌名或音乐人定位，查看边的来源；四条故事线只用于**聚焦视野**，不删除其他歌曲。原按歌手聚合图保留为辅助视图。

数据结构保存在 `knowledgeGraph.nodes`、`edges`、`layout` 和 `coverage`；HTML 中的静态 SVG 也由同一份数据生成，避免 iPhone 文件预览无脚本时只显示一小组歌曲。
