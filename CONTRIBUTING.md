# CONTRIBUTING

本仓的子模组操作流程。领域认知与判断规矩见 [AGENTS](AGENTS.md)，子模组清单见 [README](README.md)。

## 子模组操作

- 初始化克隆：`git clone --recurse-submodules <repo-url>`
- 拉取更新：`git submodule update --remote <path>`
- 修改子模组：进入子模组目录提交后，回到主仓库更新引用

## 提交与指针

本仓与子模组是独立仓库。改动在子模组提交推送后，回到本仓更新指针再提交推送（顺序不能反：本仓记录的是子模组的提交哈希，先推本仓会指向远端尚不存在的提交）。提交后默认推送到远端，无需另行请示。
