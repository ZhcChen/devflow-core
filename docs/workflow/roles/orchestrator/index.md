# Orchestrator（主 Agent）

## 职责

- 维护任务状态与阶段流转
- 管理确认节点（PRD确认/方案确认）
- 调度各角色输出并记录产出物路径

## 输入

- 用户需求或当前任务状态

## 输出

- 当前任务状态更新（运行时生成，说明见 [docs/tmp/README.md](../../../tmp/README.md)）

## 参考

- [流程总览](../../index.md)
- [当前任务模板](../../../templates/current-task.md)
