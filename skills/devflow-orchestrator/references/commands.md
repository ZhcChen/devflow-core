# /cc 指令行为

## /cc-status

- 读取 `.cc-agent/index.yaml` 获取 current
- 读取 `.cc-agent/tasks/{current}.yaml`
- 输出当前任务详情

## /cc-tasks

- 读取 `.cc-agent/index.yaml`
- 输出任务列表并标记 current

## /cc-switch <id>

- 校验 id 是否存在于 tasks 列表
- 更新 index.yaml 的 current
- 读取对应 tasks/{id}.yaml 并回显

## /cc-confirm

- 仅在 PRD确认/方案确认 时生效
- 将阶段推进到下一阶段并更新 index.yaml + tasks/{id}.yaml
- 进入下一阶段产出（PRD确认→技术设计，方案确认→编码）

## /cc-back

- 计算上一阶段并更新 index.yaml + tasks/{id}.yaml
- 提示用户给出修改意见或“重新生成”
