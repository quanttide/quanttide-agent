# AGENTS.md

## 理解：这个领域是什么

**量潮智能体领域。核心循环：session → 找偏离细节 → 修 harness。**与客服域同是两段，分量不同：创始人自述记录已完善，第一段不是瓶颈，重心压在第二段——把 AI 偏离预期的细节变成 harness 结构，让同类偏离不再发生、或发生时被拉回。

- **目标（创始人原话，2026-11-01）**：「就我自己而言，我的记录总体做的还是比较完善的，所以更多不是挖掘知识经验，而是找到那些AI容易偏离的细节，建立更反脆弱的harness。」
- **session**——一段智能体会话的原始记录（pi 为主，另有 opencode、hermes）。事件侧，原料。
- **偏离**——AI 实际行为与预期的落差，写成「预期 X，实际 Y」的可比对形状。第二段唯一选料入口。
- **harness 修正**——loops、skills、prompts、agents 配置里的一处修订。结果侧：跟场景走，适用范围绑偏离模式不绑目录。
- **修正没有终态**：落地＝假设入档；不再偏＝暂时在位；再现偏离＝怀疑旧规则，证伪就退位。人写的 harness 规则本身不可信，怀疑是日常状态。
- **同任务形态不事前定义**：按工作目录机械筛，再比对偏离描述，对得上才算同一个。
- **落位**：记录段落 `data/journal`（只增不改、标偏离），修正落 `data/profile`（快照替换），方向落 `data/intention`（创始人给定），判断落 `data/insight`（可错、带证伪条件），步骤落 `data/roadmap`（一步一格、顺序由洞察撑着、验收用意图），对外口径落 `data/brochure`。各资产位规矩见对应子仓 `AGENTS.md`。
- **好坏标准**：不看修了多少条规则，看再现偏离触发了几次怀疑与退位——规则在位待证伪的数量与退位速度。
- **设计范式三段**：第一段自用（量潮自己用智能体干活）；第二段找演化规律（偏离 → 修正 → 结构更强）；第三段推己及人（售卖口径占位，前两段站住再立）。

### 领域边界

- 机器上的工作配置（`~/.pi`、`~/.hermes` 等）是采集源，仓是正本；
- 范畴不补领域判断：偏离的粒度、意图的表述必须人给，落位再对也枉然。

## 子模组

本项目使用 Git 子模组管理关联仓库：

| 子模组 | 路径 | 用途 |
|--------|------|------|
| qtcloud-agent | `apps/qtcloud-agent` | 智能体云平台应用 |
| agent-toolkit | `packages/toolkit` | 智能体工程工具包 SDK |
| roadmap | `data/roadmap` | 智能体工程蓝图 |
| default-example | `examples/quanttide-agent-lab` | 智能体工程实验室默认示例 |
| journal | `data/journal` | 智能体工程日志 |
| report | `data/report` | 智能体工程报告 |
| profile | `data/profile` | 智能体工程工作档案 |
| library | `data/library` | 智能体工程配置库 |
| context | `data/context` | 智能体工程语境 |

**子模组操作规范：**
- 拉取更新：`git submodule update --remote <path>`
- 修改子模组：进入子模组目录提交后，回到主仓库更新引用
- 初始化克隆：`git clone --recurse-submodules <repo-url>`
