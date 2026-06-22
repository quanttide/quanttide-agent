# AGENTS.md

## 子模组

本项目使用 Git 子模组管理关联仓库：

| 子模组 | 路径 | 用途 |
|--------|------|------|
| qtcloud-agent | `apps/qtcloud-agent` | 智能体云平台应用 |
| agent-toolkit | `packages/toolkit` | 智能体工程工具包 SDK |
| roadmap | `data/roadmap` | 智能体工程蓝图 |
| default-example | `examples/default` | 智能体工程实验室默认示例 |
| journal | `data/journal` | 智能体工程日志 |
| report | `data/report` | 智能体工程报告 |
| profile | `data/profile` | 智能体工程工作档案 |

**子模组操作规范：**
- 拉取更新：`git submodule update --remote <path>`
- 修改子模组：进入子模组目录提交后，回到主仓库更新引用
- 初始化克隆：`git clone --recurse-submodules <repo-url>`
