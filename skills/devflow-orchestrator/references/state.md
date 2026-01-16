# .cc-agent 状态结构

## index.yaml（轻量索引）

```yaml
current: "001"

tasks:
  - id: "001"
    name: "示例任务"
    stage: "技术设计"
```

## tasks/{id}.yaml（任务详情）

```yaml
id: "001"
name: "示例任务"
stage: "技术设计"
created_at: "2026-01-16"
prd: "docs/requirements/PRD-001-示例任务.md"
spec: "docs/specs/SPEC-001-示例任务.md"
commits: []
```

## 阶段枚举

- 需求分析
- PRD确认
- 技术设计
- 方案确认
- 编码
- 审查
- 测试
- 完成
