# Agent 工程规则 / Agent Repository Rules

参考 [Local-Video-Meeting-Minutes/AGENTS.md](https://github.com/JohnnyBGoodeLithium/Local-Video-Meeting-Minutes/blob/main/AGENTS.md) 中可复用的文档、验证与公开仓库治理方法，按音乐项目的职责重新定义。**不要复制**其会议转写、人物核对、RAG、现有 Makefile/CI 等项目专属规则。

## 当前事实

- 这是**日常音乐数据 → 有证据的个人洞察 → 故事电台**项目，尚仅概念/文档；本地音乐/模型/NAS/联想硬件均非必要条件，不能声称已有实际集成。
- 核心是获授权的收藏/歌单、原始播放次数与添加日期、可解释 Music Report 和音乐关系、多选题策展、模块化口播及合法播放；声学可选。
- **具体歌曲、演出、发行和主持稿只出现在 Demo 专项文档**；不能写进 README、PRODUCT、ARCHITECTURE、MVP、STATUS、FUNCTIONS 或全局决策日志。
- Music Assistant + AI Radio 为优先实测/复用候选，其 Host/Show/Segment 等上游功能不算本仓库已实现；Smart Storage 非依赖。
- 本地和云端 TextLLM/TTS 均通过可配置 Provider 接口支持；无明确授权不得静默上云或上传私人音乐。

## 默认阅读顺序和上下文预算

普通工作默认阅读：
1. `AGENTS.md`
2. `docs/STATUS.md`（只看当前阶段）
3. `docs/INDEX.md`
4. 与任务直接对应的**一份**专项文档

默认目标不超过约 8,000 tokens，确实需要更多才增加。不要为查状态同时读一堆 README、历史日志和所有功能表。功能表只在盘点、发布核对和功能变更时读取。

## 双语文档维护

- `README.md` ↔ `README.zh-CN.md`；`docs/*.md` ↔ `docs/*.zh-CN.md`（核心产品文档）。
- 同一个事实的两份语言必须在**同一批修改**中同步，产品范围、数字、状态、隐私和版权边界一致，措辞可自然本地化。
- `AGENTS.md` 可中文为主；`docs/INDEX.md` 为双语导航，无须强行复制。
- 单个歌曲的演示文案可双语配对，但**不能当成产品定义**。

## 唯一真源 / 文档更新矩阵

| 修改主题 | 唯一维护位置（更新双语） | 其他文档 |
| --- | --- | --- |
| 产品定位、Persona、核心旅程 | `docs/01-product-overview*.md` | README 只保留摘要和链接 |
| MVP 需求、验收、非目标 | `docs/02-mvp-and-requirements*.md` | 不复制到功能库以外的文档 |
| 具体歌曲、演出、时间轴和主持稿 | `docs/03-my-back-pages-demo*.md` | **不进入通用项目文档** |
| 服务器责任、Smart Storage 评估、信息模型、分析与推荐、Provider 接口、隐私 | `docs/04-conceptual-architecture*.md` | 产品文档只简述边界 |
| 跨模块未决问题与已明确约束 | `docs/05-open-questions*.md` | 不放案例详情 |
| 当前完成度、测试边界、近期事项 | `docs/STATUS*.md` | 不把计划当成已实现 |
| 功能清单、稳定 ID、成熟度、上线版本和 Git 证据 | `docs/PRODUCT_FUNCTIONS*.md` | **只从这里读产品具备哪些能力** |
| 文档位置及职责 | `docs/INDEX.md` | README 只做入口 |

功能编号按四层命名（`模块.能力域.能力组.叶功能`），上线后不重排不复用。功能库“规划中”不能写成“已实现”；真实版本和 Git 证据只有在实际验证后回填。发布变化依靠 Git；不要重复写多份历史。

## 证据、隐私、版权

- 保持 Work / Recording / Release / Track / PlayableSource 的身份区别。作品关系来自可信元数据，声学相似是可带不确定性的算法观察，不能编造演奏者、影响关系和创作者意图。
- 个人曲库文件、播放历史、令牌、身份资料、授权外部服务详情、本地绝对路径不得进入公开仓库；测试和示例使用虚构元数据或合法可公开的信息。
- 不假设付费流媒体订阅就允许下载、解密、抓取 PCM、切片或重新混合商业歌曲。主持 TTS/BGM 与原始商业歌曲采用分离的播放编排。
- 本地或云端模型均可显式配置，数据出端需授权；不静默回退或上传。
- “可以播放用户合法拥有的文件而无需流媒体订阅”不代表所有模型服务、硬件、维护均免费。

## 范围、设计与 Git 提交

- 一次完整的产品文档变更（含中英文和文档索引）应汇总为**一个原子 Commit**，禁止每文件一个 Commit；不擅自重写历史。
- 黑白、Notion 式直线、块面及局部虚线的低保真草稿优先；不要 Axure 控件堆砌，Qira 后续再议。见 `docs/06-lowfi-wireframes*.md`。
- Home Assistant、NAS/Agentic Storage、家庭服务及 24×7 DT 是单独长期讨论，**不得污染音乐项目的 MVP、产品功能库**。

## 修改前、中、后

- 修改前先读取目标文件及最新 blob SHA，检查目标仓库和公开边界；避免覆盖与本任务无关的用户修改。能访问工作区时还应检查 `git status`、分支、相关测试。
- 诊断请求默认只读；获授权修改时尽量小范围修订。纯文档可以直接提交；代码改动默认 feature branch + PR。没有实际 CI 时不得假称已通过。
- 在对应的中英文文件中同时修改；检查链接可达、编号不重复、案例是否泄漏到通用文档、当前状态是否与代码一致。
- 能运行测试时运行相关专项测试；没有测试或真实素材时明确说明验证局限。
- 完成后报告变更范围、实际验证和仍未确定的技术边界。

## 不适用的 Meeting Minutes 规则

不要将 Meeting Minutes 的 ASR、VL、说话人、WeKnora、MeetingPack、预装模型及现有 CI/release 约束强行应用于音乐项目。
