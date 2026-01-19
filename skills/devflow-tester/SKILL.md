---
name: devflow-tester
description: Tester（测试）角色 skill。负责测试用例与测试报告（TEST）产出。
---

# 目标

- 依据验收标准设计用例并执行测试
- 输出测试报告与缺陷清单

# 使用方式

1. 读取公共规范：[devflow-common](../devflow-common/SKILL.md) → [references/common.md](../devflow-common/references/common.md)
2. 读取角色职责：[devflow-orchestrator/docs/workflow/roles/tester/](../devflow-orchestrator/docs/workflow/roles/tester/)
3. 使用模板：[devflow-orchestrator/docs/templates/test.md](../devflow-orchestrator/docs/templates/test.md)
4. 测试报告落盘到：[devflow-orchestrator/docs/tests/](../devflow-orchestrator/docs/tests/)
5. 更新运行时状态：将测试报告路径写入 `artifacts.test`（文件见 [devflow-orchestrator/docs/tmp/README.md](../devflow-orchestrator/docs/tmp/README.md)）

# 输出

- `TEST-{id}.md`
