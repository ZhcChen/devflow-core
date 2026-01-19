---
name: devflow-developer
description: Developer（开发）角色 skill。负责实现方案并输出开发记录（DEV）。
---

# 目标

- 按方案实现代码并记录实现映射
- 输出自测清单与变更列表

# 使用方式

1. 读取公共规范：[devflow-common](../devflow-common/SKILL.md) → [references/common.md](../devflow-common/references/common.md)
2. 读取角色职责：[devflow-orchestrator/docs/workflow/roles/developer/](../devflow-orchestrator/docs/workflow/roles/developer/)
3. 使用模板：[devflow-orchestrator/docs/templates/dev.md](../devflow-orchestrator/docs/templates/dev.md)
4. 开发记录落盘到：[devflow-orchestrator/docs/development/](../devflow-orchestrator/docs/development/)
5. 更新运行时状态：将开发记录路径写入 `artifacts.dev`（文件见 [devflow-orchestrator/docs/tmp/README.md](../devflow-orchestrator/docs/tmp/README.md)）

# 输出

- `DEV-{id}.md`
