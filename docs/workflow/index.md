# 流程

## 流程总览

```
用户
  ↓
Orchestrator（主 Agent）
  ↓
PM → [PRD确认] → Architect → [方案确认] → Developer → Reviewer → Tester
```

## 阶段流转

```
[需求分析] → [PRD确认] → [技术设计] → [方案确认] → [编码] → [审查] → [测试] → [完成]
```

## 角色职责

- Orchestrator：协调流程、管理确认节点、推进阶段流转
- PM：需求澄清与 PRD 产出
- Architect：技术方案与架构设计
- Developer：按方案实现代码
- Reviewer：代码审查与改进建议
- Tester：测试用例与测试报告

## 产出物

- PRD：`docs/requirements/PRD-{id}-{name}.md`
- 技术方案：`docs/specs/SPEC-{id}-{name}.md`
- 审查/测试报告：按项目约定
