# 当前任务状态结构（单任务模式）

## docs/tmp/current.md（任务详情）

```yaml
---
id: "000001"
name: "示例任务"
stage: "技术设计"
created_at: "2026-01-16"
updated_at: "2026-01-16"
pending_confirmation: false
next_action: "输出技术方案"
artifacts:
  prd: "docs/requirements/PRD-000001.md"
  spec: "docs/specs/SPEC-000001.md"
  dev: "docs/development/DEV-000001.md"
  review: "docs/reviews/REVIEW-000001.md"
  test: "docs/tests/TEST-000001.md"
---
```

正文部分按 [docs/templates/current-task.md](../../docs/templates/current-task.md) 执行（Markdown 段落）。

## 阶段枚举

- 需求分析
- PRD确认
- 技术设计
- 方案确认
- 编码
- 审查
- 测试
- 完成
