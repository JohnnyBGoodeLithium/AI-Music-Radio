# MVP 需求与验收

[English](02-mvp-and-requirements.md) | 简体中文

**目的：证明个人音乐数据能产生更好的洞察和故事电台。** 稳定 ID 见[功能库](PRODUCT_FUNCTIONS.zh-CN.md)，真实状态见[STATUS](STATUS.zh-CN.md)。

1. 获授权导入 Apple Music Windows 或其他曲库/歌单元数据，优先**原始播放次数与添加日期**，保留来源和缺失项；不强制音频文件。
2. 保留平台 ID、统计口径/覆盖、原始添加日期与导入日期、匹配不确定性；不把不同平台次数直接相加。
3. 生成有证据的 Personal Music Report：长期主线、近期热度、音乐人关系与音乐史解释。
4. 每期仅提取相关的 Music Context Pack，不把整库塞进 LLM；区分数据推断和真实史实。
5. 至少提出两个不同的约 15–20 分钟节目方案，也可从单曲/主题出发，并检查每首歌实际播放许可。
6. 分段生成主持稿/TTS 和歌曲项，验证评论后的局部修改；只能通过授权音源播放。
7. **先测试 Music Assistant + AI Radio：** 曲库/队列/API、Host/Show、Segment、统计字段、版权限制。
8. LLM/TTS 可明确选本地**或**云端；缺失数据、错误和授权限制要诚实呈现。

**P1：** 更多平台、可选本地歌曲/声学、节目记忆、音乐报告/图谱、可选采访、节目收藏、[黑白线框](06-lowfi-wireframes.zh-CN.md)、可选 Smart Storage。Qira 后续等内部正式规范。

**不做：** 通用 NAS/Agentic Storage、Home Assistant、24×7 DT、强制本地模型、DRM 抓取混音或不经测试重造 Music Assistant。

**验收：** 真实导入并核对次数/日期；报告和两个节目方案；比较普通与个人化质量；分段主持音频；确认播放许可；记录上游已实现与真实缺口。**目前均未通过。**
