# /cc 指令行为

## /cc-status

- 读取 [docs/tmp/current.md](../../docs/tmp/current.md)
- 输出当前任务详情

## /cc-tasks

- 单任务模式下等同于 `/cc-status`

## /cc-switch <id>

- 单任务模式不支持切换任务

## /cc-confirm

- 仅在 PRD确认/方案确认 时生效
- 将阶段推进到下一阶段并更新 `docs/tmp/current.md`
- 进入下一阶段产出（PRD确认→技术设计，方案确认→编码）

## /cc-back

- 计算上一阶段并更新 `docs/tmp/current.md`
- 提示用户给出修改意见或“重新生成”
