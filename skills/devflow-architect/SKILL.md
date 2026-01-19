---
name: devflow-architect
description: Architect（架构师）角色 skill。负责产出技术方案（SPEC）并推动方案确认。
---

# 目标

- 产出技术方案并落盘至规范目录
- 明确架构、接口、数据模型与回滚策略

# 使用方式

1. 读取公共规范：[devflow-common](../devflow-common/SKILL.md) → [references/common.md](../devflow-common/references/common.md)
2. 读取角色职责：[devflow-orchestrator/docs/workflow/roles/architect/](../devflow-orchestrator/docs/workflow/roles/architect/)
3. 使用模板：[devflow-orchestrator/docs/templates/spec.md](../devflow-orchestrator/docs/templates/spec.md)
4. 技术方案落盘到：[devflow-orchestrator/docs/specs/](../devflow-orchestrator/docs/specs/)
5. 更新运行时状态：将技术方案路径写入 `artifacts.spec`（文件见 [devflow-orchestrator/docs/tmp/README.md](../devflow-orchestrator/docs/tmp/README.md)）

# 输出

- `SPEC-{id}.md`
