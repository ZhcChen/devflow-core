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
- Developer：按方案实现代码与开发记录
- Reviewer：代码审查与审查报告
- Tester：测试用例与测试报告

## 角色文档

| 角色 | 文档 |
|------|------|
| PM | [pm/](roles/pm/) |
| Architect | [architect/](roles/architect/) |
| Developer | [developer/](roles/developer/) |
| Reviewer | [reviewer/](roles/reviewer/) |
| Tester | [tester/](roles/tester/) |

## 产出物

- PRD：`PRD-{id}.md`（见 [requirements/](../requirements/)）
- 技术方案：`SPEC-{id}.md`（见 [specs/](../specs/)）
- 开发记录：`DEV-{id}.md`（见 [development/](../development/)）
- 审查报告：`REVIEW-{id}.md`（见 [reviews/](../reviews/)）
- 测试报告：`TEST-{id}.md`（见 [tests/](../tests/)）

## 确认节点要求

- PRD确认：必须已有 PRD 文档并包含验收矩阵
- 方案确认：必须已有技术方案文档且满足必备内容（见 [specs/](../specs/)）
