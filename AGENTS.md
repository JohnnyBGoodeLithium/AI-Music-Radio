# Agent 工程规则 / Agent Operating Rules

本文件参考 [Local-Video-Meeting-Minutes/AGENTS.md](https://github.com/JohnnyBGoodeLithium/Local-Video-Meeting-Minutes/blob/main/AGENTS.md) 的文档、验证与公开仓库治理原则，已适配 AI Music Radio。**不继承**会议转写、说话人、WeKnora、既有 CI 等不适用于本项目的细节。

## 项目目标及当前事实

- 项目：AI Music Radio — **Own Your Music. Discover Its Stories.**
- 基础是个人本地音乐服务器；差异化体验是有依据的 AI 音乐策展、自然主持语音和可播放的节目。
- 当前阶段：**Documentation / Concept only**。除非代码和测试证实，不得声称音乐服务器、TTS、播放器或推荐引擎已实现。
- 演示种子：**1992 年 Bob Dylan 录音生涯 30 周年纪念音乐会现场合唱版 My Back Pages**。不要误写成 20 周年；不要用 1964 年原版或 1967 年 The Byrds 版本替代种子录音。

## 默认阅读顺序与上下文预算

通常只读取：
1. `AGENTS.md`
2. `docs/STATUS.md`
3. `docs/INDEX.md`
4. 与任务直接相关的一份专项文档

目标控制在约 8,000 tokens；根据任务需要再增加。不要为了了解当前状态重复读取所有 README、历史文档和完整提交记录。当前实现以代码、测试、Git 为准；`STATUS` 是文档化状态的权威位置。

## 中文与英文 / Bilingual contract

- **项目说明同时维护中文和英文。** 英文使用 `README.md` 和 `docs/*.md`；对应简体中文使用 `README.zh-CN.md` 和同名 `docs/*.zh-CN.md`。
- README 顶部提供双向语言切换链接；各核心文档顶部也提供双向切换链接。
- **一项产品事实的修改必须在同一次变更中同步更新对应双语文档**，避免中文是新版、英文是旧版。两种语言不必逐字直译，但范围、数字、决策、风险和阶段状态必须一致。
- `AGENTS.md` 以中文为主；`docs/INDEX.md` 用双语导航；项目状态 `STATUS.md` 和 `STATUS.zh-CN.md` 成对维护。
- 报告或对外材料使用目标受众要求的语言，不因此改变产品合同。
- **权威位置（Canonical）依职责划分，不以语言划分。** 双语版本是同一事实的两份表达，不是两个独立产品决策来源。

## 文档唯一真源与更新矩阵

以 [docs/INDEX.md](docs/INDEX.md) 为准：

| 变更 | 必须同步更新 | 通常不改 |
| --- | --- | --- |
| 产品定位、Persona 或非目标 | `docs/01-product-overview*.md` | 架构，除非边界变化 |
| MVP 范围与验收 | `docs/02-mvp-and-requirements*.md` | README 详情 |
| 电台策划、节目曲目与主持词 | `docs/03-my-back-pages-demo*.md` | 架构，除非 schema 变化 |
| 元数据身份、数据结构、播放权限、AI 组件 | `docs/04-conceptual-architecture*.md` | Persona |
| 未决问题和已明确决策 | `docs/05-open-questions*.md` | README |
| 已实现功能、验证程度与近期重点 | `docs/STATUS*.md` | 不在 README 反复写版本历史 |
| 用户入口变化 | `README.md` + `README.zh-CN.md` | 不复制专项文档全文 |

## 内容证据、数据与版权

- 音乐的 **Work / Recording / Release / Track / PlayableSource** 必须区分；具体现场合唱版与原曲、翻唱版不可混淆。
- 把可核实的音乐事实、音频分析观察、主观听感和 AI 推断分开保存。模型输出不是事实真源；未经验证不编造创作背景、采样关系、演出阵容或意图。
- 重要音乐事件、年份、参与者和作品版本，优先引用官方发行方、音乐人官网及可靠数据库；文档中的明确事实尽量附来源。
- 仅使用合法取得或授权播放的音频。订阅权限不等于下载、解密、录制、切片、再编码或混音商业流媒体歌曲的许可。
- 口播和自有/授权 BGM 与歌曲保留独立逻辑时间轴；播放能力以真实来源接口为准。
- 用户私人曲库、试听历史、令牌和音乐文件不得提交到公开仓库。公开示例仅使用虚构数据、示意 track IDs、可公开的作品元数据和获得许可的音频。

## 本地优先与隐私

- 本地音乐服务器和授权的本地文件应在无流媒体订阅时可使用。
- AI 推理可先评测外部服务，但**不得静默上传本地音乐文件、收听历史或其他私人信息**；服务端接口与数据范围须经过显式配置与授权。
- 不将“无需流媒体订阅”表述为无硬件、电力、维护、模型、API 成本。
- Provider/资源/界面应以能力合同实现，避免初期绑定单一模型、显卡、操作系统或流媒体服务。

## 修改与验证

- 修改前重读目标文件、确认 Git 分支与 SHA；避免覆盖用户正在进行的改动。当前连接不能检查工作树时明确限制。
- 优先做最小的、与需求有关的改动；代码改动默认使用 feature branch + Pull Request；纯文档初始化/修订可按仓库当前治理直接提交。
- 任何编辑都应核对内部链接、语言配对、日期、时间线、版权边界与历史事实；真实音频时长以所用文件探测结果为准。
- 尚未配置 CI 时不得声称检查或 smoke 通过；文档验证应说明只验证了文本、链接或仓库回读。
- 对公开远端进行提交前，确认无私有人员、凭据、绝对路径、私人播放记录、未获许可的音频素材。
- 记录本次改动、验证范围和剩余未验证项。不要杜撰发布日期、演出时长或已完成能力。

## 不适用规则

不得直接复制 Meeting Minutes 仓库关于 ASR、speaker diarization、MeetingPack、WeKnora、真实会议数据、现有 Makefile/CI 和 release bundle 的专属约束；只有在 Local Radio 后续真正引入同类能力后，再定义对应规则。
