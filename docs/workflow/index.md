# 流程

## 流程总览

```
用户
  ↓
Orchestrator（主 Agent）
  ↓
PM（产品负责人） → [PRD确认] → Architect（架构师） → [方案确认] → Developer（开发） → Reviewer（审查） → Tester（测试）
```

## 阶段流转

```
[需求分析] → [PRD确认] → [技术设计] → [方案确认] → [编码] → [审查] → [测试] → [完成]
```

## 角色职责

- Orchestrator（主 Agent）：协调流程、管理确认节点、推进阶段流转（见 [orchestrator/](roles/orchestrator/)）
- PM（产品负责人）：需求澄清与 PRD 产出
- Architect（架构师）：技术方案与架构设计
- Developer（开发）：按方案实现代码与开发记录
- Reviewer（审查）：代码审查与审查报告
- Tester（测试）：测试用例与测试报告

## 角色文档

| 角色 | 文档 |
|------|------|
| Orchestrator（主 Agent） | [orchestrator/](roles/orchestrator/) |
| PM（产品负责人） | [pm/](roles/pm/) |
| Architect（架构师） | [architect/](roles/architect/) |
| Developer（开发） | [developer/](roles/developer/) |
| Reviewer（审查） | [reviewer/](roles/reviewer/) |
| Tester（测试） | [tester/](roles/tester/) |

## 产出物

- PRD：`PRD-{id}.md`（见 [requirements/](../requirements/)）
- 技术方案：`SPEC-{id}.md`（见 [specs/](../specs/)）
- 开发记录：`DEV-{id}.md`（见 [development/](../development/)）
- 审查报告：`REVIEW-{id}.md`（见 [reviews/](../reviews/)）
- 测试报告：`TEST-{id}.md`（见 [tests/](../tests/)）

## 确认节点要求

- PRD确认：必须已有 PRD 文档并包含验收矩阵，需用户确认后进入技术设计
- 方案确认：必须已有技术方案文档且满足必备内容（见 [specs/](../specs/)），需用户确认后进入编码
- 确认未通过则回退到上一阶段并携带修改意见

## 审查与测试门槛

- 审查通过后进入测试
- 测试通过后进入完成
- 审查/测试不通过则回到编码阶段并携带问题清单
