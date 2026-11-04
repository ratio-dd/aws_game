# 协作约定

- 日常交流、issue 和 PR 描述使用中文，保持简短。
- `origin` 是自己的 fork：`ratio-dd/aws_game`；`upstream` 是原仓库：`cloudsmithy/aws_game`。
- `master`（本项目默认分支，相当于 main）保持与上游同步；`dev` 用于自己的集成和协作约定。
- 创建功能分支前，先同步上游和 fork 的 `master`，再从 `origin/master` 创建独立的 `codex/` 分支。
- 功能分支先推送到 `origin`，向 `upstream/master` 提 PR。提 PR 前检查 `git diff upstream/master...HEAD`，确认只有本次任务的改动。
- 功能代码通过合并功能分支进入 `dev`，保留提交关联；后续更新继续沿同一方向合入。
- `AGENTS.md` 只提交在 `dev`。功能分支不从 `dev` 创建，不将 `dev` 合入功能分支；`dev` 不向 `master` 或上游提 PR。
- 在功能分支工作时通过 `git show dev:AGENTS.md` 读取这些约定，保持该文件不进入功能分支的提交和上游 PR。
- 当前本地仓库安装了 pre-commit / pre-push 检查，限制约定文件只提交到 `dev`、只推送到自己的 `origin/dev`；保持检查启用。新克隆或新 worktree 开工前确认检查仍生效。
- 默认在自己的 fork 跟踪 issue。需要上游讨论的问题，逐个与用户确定是否在上游开 issue。
- fork 与上游的 issue、标签和状态各自独立；通过链接关联，避免重复维护。
- 修复先复现，再做最小改动，并验证原问题及相关行为。PR 写明原因、改动和验证结果。
- 项目入口和规则数据在 `index.html`；涉及规则或文档同步时先查 `README.md`，确认所需文件和工具实际存在。
