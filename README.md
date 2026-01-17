# devflow-core

面向 Codex CLI 的 skill 集合仓库，用于沉淀可复用的 AI 开发流程与规范。

## 使用方式

- 直接从 GitHub 读取仓库，并按需加载 `skills/` 下的 skill
- 每个 skill 都是独立目录，包含 `SKILL.md`（触发与执行说明）及相关资源

## Skills

| 名称 | 作用 | 简介 |
|------|------|------|
| devflow-orchestrator | 开发流程编排 | 多角色流程与确认节点的单任务状态机，提供 Orchestrator 级别的流程驱动与文档落盘规范。 |

## 目录结构

```
skills/
  devflow-orchestrator/
    SKILL.md
    references/
    assets/
```

## 文档索引

- [docs/index.md](docs/index.md)
