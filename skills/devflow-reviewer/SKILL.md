---
name: devflow-reviewer
description: Reviewer（审查）角色 skill。负责代码审查并输出审查报告（REVIEW）。
---

# 目标

- 审查实现与方案一致性
- 输出问题清单与结论

# 使用方式

1. 读取公共规范：[devflow-common](../devflow-common/SKILL.md) → [references/common.md](../devflow-common/references/common.md)
2. 读取角色职责：[devflow-orchestrator/docs/workflow/roles/reviewer/](../devflow-orchestrator/docs/workflow/roles/reviewer/)
3. 使用模板：[devflow-orchestrator/docs/templates/review.md](../devflow-orchestrator/docs/templates/review.md)
4. 审查报告落盘到：[devflow-orchestrator/docs/reviews/](../devflow-orchestrator/docs/reviews/)
5. 更新运行时状态：将审查报告路径写入 `artifacts.review`（文件见 [devflow-orchestrator/docs/tmp/README.md](../devflow-orchestrator/docs/tmp/README.md)）

# 输出

- `REVIEW-{id}.md`
