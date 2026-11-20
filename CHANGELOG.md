# CHANGELOG

## [Unreleased]

### 变更

- 拆分 AGENTS 与 CONTRIBUTING：新增 `CONTRIBUTING.md` 收子模组操作流程与提交指针；`AGENTS.md` 删子模组表（正本在 README）与操作规范，只留领域认知与边界；`data/journal`、`data/profile`、`data/roadmap` 三子仓同步拆分，指针同步更新
- `AGENTS.md` 新增认知段：核心循环 session → 找偏离细节 → 修 harness；目标为创始人原话，三级判据（假设入档 / 暂时在位 / 证伪退位），五格落位与好坏标准
- `data/journal`、`data/profile`、`data/intention`、`data/insight`、`data/roadmap`、`data/brochure` 六仓 `AGENTS.md` 冷启动（profile、roadmap 为合并不覆盖），指针同步更新


## Unreleased

### 变更

- 实验室子模块改名：`examples/default` → `examples/quanttide-agent-lab`（仓 quanttide-laboratory-of-agent-engineering → quanttide-agent-lab）


### Added
- 更新 `apps/qtcloud-agent` 子模块：新增 `src/cli/docs/user-guide/session-audit.md`，写清 session audit 的用法、扫描范围、六类命中、退出码、实测数据与三个盲区
- 更新 `apps/qtcloud-agent` 子模块：`session list` 扩到 dsh / pi / opencode / hermes 四家存储，新增 `session show`（按 id 看会话详情）与 `session audit`（只读扫描敏感串，命中即退出码 1）；`registry status` 判据收紧——未知 agent 单列「无法比较」、文件名按 stem + 扩展名族对齐、本地自定义汇总一行；补 6 个单元测试
- 更新 `apps/qtcloud-agent` 子模块：CLI 命令面收敛——`status` → `registry status`，删 `dsh` 命令，新增 `session list`（按会话记录时的 cwd 判定归属，默认筛当前目录）；退出码立起来（0 有结果/一致、1 无匹配/有差异、2 用法错、3 数据源读不到）；注册中心默认路径修正为 `data/profile/default/agents`（CLI 与 provider 两处）
- 更新 `data/library` 子模块：新增 Clean Session Curate 会话脱敏调研（目标目录归属可证、Capsule 匿名化七项、路径残留清扫与打包，可考虑接入智能体云）
- 更新 `examples/quanttide-agent-lab` 子模块：新增 session-scrub 实验（clean-session-curate 全流程实测、七项匿名化效果、密钥漏网与二次自查）与脱敏产物数据 `data/session-scrub/`
- 更新 `examples/quanttide-agent-lab` 子模块：新增 pi-session-scrub 实验（pi 会话接入清洗流水线、Capsule 数组内路径盲区、第二道清扫拦下 1014 处身份与部署信息）与脱敏产物数据 `data/pi-session-scrub/`
- 更新 `data/context` 子模块：新增 `profile/STATUS.md`（14 份 SKILL 的分档清单、已知不一致与复核命令）
- 更新 `data/context` 子模块：新增 `profile/skills/`（14 份技能 68 文件，源自 hermes 备份，入仓前已脱敏）
- 更新 `data/profile` 子模块：Zed / Hermes 镜像本机运行时配置（MiMo 按量付费 API 与 Token Plan 分列为两个 provider，补 StepFun 接入）
- 更新 `data/library` 子模块：新增 Vicoa 介绍（开源 AI 编排器：多智能体并行编排、统一指挥台、多端协同与通知、BYO-key）
- 更新 `data/profile` 子模块：新增 `contexts/asset-init.jsonl`（裁剪后的资产初始化原始对话记录）
- 注册子模块：`docs/bylaw`（智能体工程章程，quanttide-bylaw-of-agent-engineering）
- 注册子模块：`docs/handbook`（智能体工程手册，quanttide-handbook-of-agent-engineering）
- 注册子模块：`docs/specification`（智能体工程标准，quanttide-specification-of-agent-engineering）
- 注册子模块：`docs/essay`（智能体工程札记，quanttide-essay-of-agent-engineering）
- 注册子模块：`docs/gallery`（智能体工程案例集，quanttide-gallery-of-agent-engineering）
- 注册子模块：`data/intention`（智能体工程意图，quanttide-intention-of-agent-engineering）
- 注册子模块：`data/insight`（智能体工程洞察，quanttide-insight-of-agent-engineering）
- 注册子模块：`data/brochure`（智能体工程宣传册，quanttide-brochure-of-agent-engineering）
- 注册子模块：`data/history`（智能体工程历史，quanttide-history-of-agent-engineering）
- 注册子模块：`data/archive`（智能体工程归档，quanttide-archive-of-agent-engineering）

## [v0.1.1] - 2026-05-23

### Added
- 添加 quanttide-roadmap-of-agent-engineering 子模块

## [v0.1.0] - 2026-05-22

### Added
- 项目初始化
- 添加 qtcloud-agent 应用子模块
- 添加 agent-toolkit 工具包子模块
