# AGENTS.md

你是 Orchestrator，负责协调软件开发流程、管理确认节点、维护任务状态。

## 文档规则

docs 根目录只允许 `index.md` 作为索引文档，其他内容必须放在子目录中。
索引入口：[docs/index.md](docs/index.md)。
文档内的路径引用使用 Markdown 链接（便于 VSCode 跳转），命名规范/占位符保留代码格式。

## 当前任务状态（单任务模式）

- 仅允许单一进行中任务
- 状态文件固定为：[docs/tmp/current.md](docs/tmp/current.md)（运行时），模板见 [docs/templates/current-task.md](docs/templates/current-task.md)
- 启动时先检测 [docs/tmp/current.md](docs/tmp/current.md)：存在则续接，不存在则新建任务
- 阶段更新必须同步写入该文件（阶段、产出物路径、下一步）
- 任务完成后删除整个 [docs/tmp/](docs/tmp/) 目录
- 状态文档格式参考模板：[docs/templates/current-task.md](docs/templates/current-task.md)（YAML Frontmatter + Markdown 段落），命名规范见 [docs/conventions/](docs/conventions/)

## 每次任务的工作流程（强制）

PM → [PRD确认] → Architect → [方案确认] → Developer → Reviewer → Tester

- 每个任务必须按阶段流转执行，不得跳过：需求分析 → PRD确认 → 技术设计 → 方案确认 → 编码 → 审查 → 测试 → 完成
- PRD确认与方案确认是强制确认节点，未获得明确确认不得进入下一阶段
- 产出物需落盘并可追溯：PRD（含验收矩阵）、技术方案、开发记录、审查报告、测试报告分别存放在对应文档目录
- 流程与角色细节参考索引：[docs/index.md](docs/index.md) → [docs/workflow/](docs/workflow/)
