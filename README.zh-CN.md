# AI Music Radio

[English](README.md) | 简体中文

**Your Music. More to Discover.**

AI Music Radio 利用已有的**日常音乐数据**——收藏、歌单、播放次数、原始添加日期及可选的自有音频——生成有依据的 **Personal Music Report** 和个人故事电台。**不要求本地音乐文件、家庭服务器、联想台式机或本地大模型。**

**当前仅有概念和文档。** 本仓库尚未完成真实导入、Music Assistant 集成或可播放节目。[状态](docs/STATUS.zh-CN.md)。

## 三个 Checkpoint

1. **连接：** 导入获授权的曲库、歌单、行为统计，记录来源和覆盖范围。
2. **理解：** 区分长期审美与近期洗脑循环，从熟悉的音乐延伸到可靠音乐史，并解释为什么。
3. **节目：** AI 准备几个约 15–20 分钟的策展主题，也可以指定歌曲。主持稿/TTS 与合法歌曲模块化编排；评论影响后续节目或相关段落。

**曲库元数据可以用于报告和策划，但不等于有播放或重混原始录音的许可。**

## 优先复用

[Music Assistant](https://www.music-assistant.io/) + [AI Radio](https://www.music-assistant.io/plugins/ai-radio/) 已有多来源曲库、播放队列、Host/Show、分段口播及 TTS。这些是**上游能力，不是本仓库成果**。先看[服务端](https://github.com/music-assistant/server)、[前端](https://github.com/music-assistant/frontend)，不要重造基础播放器。

**待验证的区别：** 用户原始行为数据、可解释音乐报告和关系图谱、跨音乐人的可信故事、多候选选题、编辑反馈与局部修改。LLM/TTS 可以选本地或云端，必须有明确数据授权。

## 文档

[产品](docs/01-product-overview.zh-CN.md) · [MVP](docs/02-mvp-and-requirements.zh-CN.md) · [架构/Music Assistant 评估](docs/04-conceptual-architecture.zh-CN.md) · [功能库](docs/PRODUCT_FUNCTIONS.zh-CN.md) · [状态](docs/STATUS.zh-CN.md) · [待决策](docs/05-open-questions.zh-CN.md) · [黑白线框](docs/06-lowfi-wireframes.zh-CN.md) · [独立 Demo](docs/03-my-back-pages-demo.zh-CN.md) · [导航](docs/INDEX.md) · [Agent 规则](AGENTS.md)。

**范围防火墙：** Home Assistant、通用 NAS/Agentic Storage、24×7 DT、家庭服务属于**独立长期讨论**，不写进音乐项目。Smart Storage 仅是可选未来适配。**UI 先做**黑白、Notion 式直线/块面与局部虚线草稿，Qira 风格往后再说。

公开仓库不存私人听歌记录、凭据或无授权音频。订阅不意味着可以抓取/混音 DRM 音轨。项目许可证未定，上游及 Provider 各自遵守其条款。
