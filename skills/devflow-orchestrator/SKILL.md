---
name: devflow-orchestrator
description: 多角色软件开发流程编排与任务状态管理。适用于需要按“需求分析→PRD确认→技术设计→方案确认→编码→审查→测试→完成”推进的任务；用于建立文档驱动开发、确认节点控制与运行时状态文档管理。
---

# 目标

- 作为 Orchestrator（主 Agent）统筹 PM（产品负责人）/Architect（架构师）/Developer（开发）/Reviewer（审查）/Tester（测试） 的交付顺序
- 使用运行时状态文档实现跨会话任务续接与确认节点控制
- 通过固定产出物（PRD/SPEC/报告）驱动流程推进

# 使用方式

1. 读取 `docs/tmp/current.md` 作为唯一状态源（说明见 [docs/tmp/README.md](../../docs/tmp/README.md)）
2. 当运行时状态不存在时，从 [docs/templates/current-task.md](../../docs/templates/current-task.md) 初始化
3. 按 [references/workflow.md](references/workflow.md) 的流程推进阶段，遇到确认节点停止等待用户输入
4. 产出物统一落盘并记录在任务状态中

# 产出物约定

- PRD：`PRD-{id}.md`（含验收矩阵，见 [docs/requirements/](../../docs/requirements/)）
- 技术方案：`SPEC-{id}.md`（见 [docs/specs/](../../docs/specs/)）
- 开发记录：`DEV-{id}.md`（见 [docs/development/](../../docs/development/)）
- 审查报告：`REVIEW-{id}.md`（见 [docs/reviews/](../../docs/reviews/)）
- 测试报告：`TEST-{id}.md`（见 [docs/tests/](../../docs/tests/)）

# 当前任务状态（单任务模式）

- 仅允许单一进行中任务
- 状态文件固定为：`docs/tmp/current.md`（运行时，说明见 [docs/tmp/README.md](../../docs/tmp/README.md)）
- 启动时先检测该文件：存在则续接，不存在则新建任务
- 阶段更新必须同步写入该文件（阶段、产出物路径、下一步）
- 任务完成后删除该文件（保留 [docs/tmp/README.md](../../docs/tmp/README.md)）
- 状态文档格式参考模板：[docs/templates/current-task.md](../../docs/templates/current-task.md)，命名规范见 [docs/conventions/](../../docs/conventions/)

# 资源索引（按需读取）

- [references/workflow.md](references/workflow.md)：角色分工、阶段流转、确认节点
- [references/state.md](references/state.md)：任务状态文档结构
- [assets/AGENTS.md](assets/AGENTS.md)：可复制的入口文件模板

# 协作技能（可选）

- 公共规范索引：[devflow-common](../devflow-common/SKILL.md)
- PM：[devflow-pm](../devflow-pm/SKILL.md)
- Architect：[devflow-architect](../devflow-architect/SKILL.md)
- Developer：[devflow-developer](../devflow-developer/SKILL.md)
- Reviewer：[devflow-reviewer](../devflow-reviewer/SKILL.md)
- Tester：[devflow-tester](../devflow-tester/SKILL.md)
