# devflow-core

面向 Codex CLI 的 skill 集合仓库，用于沉淀可复用的 AI 开发流程与规范。

## 使用方式

- 直接从 GitHub 读取仓库，并按需加载 `skills/` 下的 skill
- 每个 skill 都是独立目录，包含 `SKILL.md`（触发与执行说明）及相关资源

## Skills

| 名称 | 作用 | 简介 |
|------|------|------|
| devflow-orchestrator | 开发流程编排 | 多角色流程与确认节点的单任务状态机，提供 Orchestrator（主 Agent）级别的流程驱动与文档落盘规范。 |
| devflow-common | 公共规范索引 | 统一提供命名规范、验收矩阵与 SQL 规范等公共规则入口。 |
| devflow-pm | PM 角色 | 产出 PRD（含验收矩阵）并推动 PRD 确认。 |
| devflow-architect | 架构师角色 | 产出技术方案（SPEC）并推动方案确认。 |
| devflow-developer | 开发角色 | 按方案实现并输出开发记录（DEV）。 |
| devflow-reviewer | 审查角色 | 输出审查报告（REVIEW）并给出结论。 |
| devflow-tester | 测试角色 | 输出测试报告（TEST）与缺陷清单。 |

## 目录结构

```
skills/
  devflow-orchestrator/
    SKILL.md
    references/
    assets/
```

## 文档索引

- [skills/devflow-orchestrator/docs/](skills/devflow-orchestrator/docs/)
