# AI Music Radio

[English](README.md) | 简体中文

**Own Your Music. Discover Its Stories.**

> 以私人音乐服务器为基础，让 AI 为你选中的一首录音讲述故事，策划真正值得聆听的个人音乐电台。

**项目成熟度：** 截至 2026-11-18，处于概念与文档阶段。仓库尚未实现可运行的音乐服务器、播放器或音频生成管线。详见[当前状态](docs/STATUS.zh-CN.md)。

## 为什么做这个项目

流媒体解决了音乐获取的便利性，却让长期听众面对持续订阅、曲库版权变化、平台依赖和收藏分散的问题。拥有合法获取的本地音乐文件，意味着用户可以长期保存和使用自己的音乐，而不是必须持续支付流媒体订阅费用。

传统的私人音乐服务器擅长存储、管理与播放文件。**AI Music Radio 则在此之上提供有依据的音乐解读和个性化策展**：从一首可识别的完整录音出发，研究背景、连接相关作品，制作带有自然 TTS 主持、原创/授权 BGM 及可交互播放的节目。

本地优先不等于所有 AI 功能都完全离线或免费；硬件、维护和可选云端模型服务仍可能有成本。

## 三类目标用户

- **Music Owner｜音乐拥有者：** 希望持久保存、跨设备访问本地音乐，不再依赖持续的流媒体订阅。
- **Music Explorer｜音乐探索者：** 希望理解推荐背后的联系，而不是接受一个不透明的相似度分数。
- **Deep Listener｜深度聆听者：** 希望在聆听中理解创作历史、音乐人、编曲与演奏版本。

详见[产品定位与三个 Persona](docs/01-product-overview.zh-CN.md)。

## 一键电台体验

**选择录音 → 校验元数据 → 研究音乐故事 → 策划关联推荐 → 生成主持语音 → 聆听与继续探索。**

输入单位是一首完整歌曲/录音文件，即使它在更大作品中只是一章。v0 允许在无法确定必要身份时明确报错，不要求音频指纹补全或文件内部乐段识别。

## 主演示：一首歌，六种声音

**种子录音：** 1992 年 10 月 16 日，Bob Dylan 在纽约麦迪逊广场花园**录音生涯 30 周年纪念演唱会**上，与 Roger McGuinn、Tom Petty、Neil Young、Eric Clapton、George Harrison 合唱的《My Back Pages》。是 **30 周年，并非 20 周年**。

拟定约 15 分钟节目将从 **1992 年现场合唱**追溯到 *Another Side of Bob Dylan* 中 **1964 年原版**，再聆听 The Byrds 在 *Younger Than Yesterday* 中的 **1967 年版本**。后续可以沿 Roger McGuinn/The Byrds、Tom Petty、Neil Young、Eric Clapton、George Harrison 和 Dylan 自身的作品继续延伸。

它体现的是：**一首作品、多份录音、多个年代、许多音乐人故事**，不需要切割歌曲内部的片段。

[阅读《一首歌，六种声音》节目方案](docs/03-my-back-pages-demo.zh-CN.md)。

## 项目文档

见[双语文档导航](docs/INDEX.md)及 [AGENTS.md](AGENTS.md) 中的贡献规则。

| 文档 | 中文 | English |
| --- | --- | --- |
| 产品与用户 | [产品说明](docs/01-product-overview.zh-CN.md) | [Product](docs/01-product-overview.md) |
| 需求与优先级 | [MVP 需求](docs/02-mvp-and-requirements.zh-CN.md) | [MVP](docs/02-mvp-and-requirements.md) |
| 旗舰演示 | [My Back Pages 节目](docs/03-my-back-pages-demo.zh-CN.md) | [Demo](docs/03-my-back-pages-demo.md) |
| 系统架构 | [架构说明](docs/04-conceptual-architecture.zh-CN.md) | [Architecture](docs/04-conceptual-architecture.md) |
| 决策与风险 | [待决策事项](docs/05-open-questions.zh-CN.md) | [Questions](docs/05-open-questions.md) |
| 当前状态 | [状态](docs/STATUS.zh-CN.md) | [Status](docs/STATUS.md) |

中文和英文对应文档必须同步更新。每类事实有唯一的专项文档负责，真正实现状态以代码和测试为准。

## 产品边界

- 用户自己的合法本地音频文件，无需开启 AI 功能或持续流媒体订阅也能播放。
- 云音乐服务只作为可选来源，实际能力由官方接口与许可决定。
- 必须区分 **Work（作品）/ Recording（具体录音）/ Release（发行）/ PlayableSource（可播放来源）**，不能混淆原版、翻唱和现场合唱。
- 音乐历史事实必须保留证据，主观听感不能伪装成已证实的音乐人创作意图。
- 节目将口播和音乐组织为独立时间轴，不默认拥有商业 DRM 音乐的抓取、裁切或再混音权限。
- 公开仓库不提交个人曲库、收听历史、凭据或未经授权的商业音频。

## 新种子的事实参考

- [Bob Dylan 官方演唱会介绍](https://www.bobdylan.com/albums/30th-anniversary-concert-celebration-deluxe-edition/)
- [Legacy Recordings 演唱会曲目和演出阵容](https://www.legacyrecordings.com/releases/30th-anniversary-concert-celebration-deluxe-edition-2-cd/)
- [Bob Dylan 官方 1964 年专辑页](https://www.bobdylan.com/albums/another-side-of-bob-dylan/)
- [MusicBrainz：1992 年现场录音](https://musicbrainz.org/release/94fb18c0-610e-41e2-853f-32a442427a90)
- [MusicBrainz：The Byrds《Younger Than Yesterday》](https://musicbrainz.org/release/85311619-b29f-4157-ae45-718cee659681)

## 许可

目前尚未选择开源许可证。不要自行假定代码、商业歌曲或 BGM 可以被重新分发。
