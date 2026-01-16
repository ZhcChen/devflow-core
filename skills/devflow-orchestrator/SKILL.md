---
name: devflow-orchestrator
description: 多角色软件开发流程编排与任务状态管理。适用于需要按“需求分析→PRD确认→技术设计→方案确认→编码→审查→测试→完成”推进的任务，或需要 /cc-status、/cc-tasks、/cc-switch、/cc-confirm、/cc-back 指令的场景；用于建立文档驱动开发、确认节点控制与 .cc-agent 状态机。
---

# 目标

- 作为 Orchestrator 统筹 PM/Architect/Developer/Reviewer/Tester 的交付顺序
- 使用 .cc-agent 状态机实现跨会话任务续接与确认节点控制
- 通过固定产出物（PRD/SPEC/报告）驱动流程推进

# 使用方式

1. 读取 `.cc-agent/index.yaml` 与 `.cc-agent/tasks/*.yaml` 作为唯一状态源
2. 当 `.cc-agent/` 不存在时，使用 `assets/.cc-agent/` 初始化
3. 按 `references/workflow.md` 的流程推进阶段，遇到确认节点停止等待用户输入
4. 根据 `references/commands.md` 响应 `/cc-*` 指令
5. 产出物统一落盘并记录在任务状态中

# 产出物约定

- PRD：`docs/requirements/PRD-{id}.md`（含验收矩阵）
- 技术方案：`docs/specs/SPEC-{id}.md`
- 开发记录：`docs/development/DEV-{id}.md`
- 审查报告：`docs/reviews/REVIEW-{id}.md`
- 测试报告：`docs/tests/TEST-{id}.md`

# 当前任务状态（单任务模式）

- 仅允许单一进行中任务
- 状态文件固定为：`docs/tmp/current.md`
- 启动时先检测 `docs/tmp/current.md`：存在则续接，不存在则新建任务
- 阶段更新必须同步写入该文件（阶段、产出物路径、下一步）
- 任务完成后删除整个 `docs/tmp/` 目录
- 状态文档格式参考模板：`docs/templates/current-task.md`，任务 ID 使用 6 位自增数字（例如 `000001`）

# 资源索引（按需读取）

- `references/workflow.md`：角色分工、阶段流转、确认节点
- `references/state.md`：`.cc-agent` 状态文件结构
- `references/commands.md`：`/cc-*` 指令行为
- `assets/AGENTS.md`：可复制的入口文件模板
- `assets/.cc-agent/`：状态机初始化模板
