# 当前项目状态

[English](STATUS.md) | 简体中文

**截至 2026-11-19：有一套基于真实截图转录的可交互低保真原型，但仍不是可接入平台的 AI 音乐产品。**

**已经完成并验证：** 根据用户提供的 Apple Music「2025年度最爱歌曲」截图，转录排名第 1–98 的曲目名称、音乐人及年度播放次数（可见条目合计 1,733 次）；以同一个数据文件驱动 Home、My Music、Personal Music Report、Music Graph 和 Show / Player；可从洞察跳到图谱、从节点到曲目与节目，并通过评论模拟一个主持 Segment 的定向修改。黑白 H5 在桌面、手机及禁用 JavaScript 的只读预览中完成基本验证。

**重要数据边界：** 这是用户截图转录，不是 Apple Music API 导入；播放次数是 2025 年榜单的展示次数而非全部历史累计值。Date Added、逐次收听事件、实际专辑版本和歌曲时长尚未取得；图谱只声明同音乐人、同可辨认系列、节目引用等可追溯关系，不编造合作史。

**仍待开发和验证：** 自动/持续曲库导入、真实音源播放、Music Assistant 和 AI Radio 实际集成、音乐史关系证据检索、LLM/TTS 制作、节目真实时长与音轨授权。

[PRD v0.3](PRD.zh-CN.md) · [交互式 2025 原型](../prototype/index.html) · [榜单 JSON](../prototype/data/2025-top-songs.json) · [MVP](02-mvp-and-requirements.zh-CN.md)。
