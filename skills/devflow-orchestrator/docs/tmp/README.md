# tmp 运行时目录

用于存放运行时任务状态文件：`tmp/current.md`。

- 该文件由流程运行时生成，不纳入版本控制。
- 任务完成后删除 `tmp/current.md`（保留本说明文件）。
- 状态文档格式参考 [templates/current-task.md](../templates/current-task.md)。

## 字段说明（摘要）

- id：6 位任务编号，例如 `000001`（规则见 [conventions/](../conventions/)）
- name：任务名称
- stage：当前阶段（见 [workflow/](../workflow/)）
- created_at / updated_at：创建与更新时间
- pending_confirmation：是否等待确认节点
- next_action：下一步动作描述
- artifacts：产出物路径（PRD/SPEC/DEV/REVIEW/TEST）

## 更新规则（摘要）

- 进入新阶段时更新 stage 与 updated_at
- 进入确认节点时将 pending_confirmation 置为 true
- 确认通过后更新 pending_confirmation 与 next_action
- 产出物落盘后更新 artifacts 对应路径
