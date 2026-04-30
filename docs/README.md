# Busy Bee Documentation

Busy Bee 是一个面向团队协作的 AI 工作助手。产品入口是飞书/Lark 群，控制台是 macOS App，执行核心是 Agent Runner，研发闭环通过 GitHub PR 完成。

## 核心产品闭环

```text
飞书/Lark 群 @AI
  -> 解析消息和上下文
  -> 创建或更新任务
  -> Agent Runner 执行任务
  -> 需要时访问 GitHub 仓库
  -> 修改代码、运行测试、创建 PR
  -> 通过飞书/Lark 通知结果
  -> 在 Mac App 中查看任务、日志、审批和审计
```

## 文档地图

### 产品文档

- `product/product-vision.md`：产品定位、目标用户、核心价值和边界。
- `product/core-workflows.md`：核心业务流程，包括问答、任务、自动开发、通知和定时计划。
- `product/feature-map.md`：完整功能清单和优先级。
- `product/mvp-scope.md`：MVP 范围、非目标和验收标准。
- `product/roadmap.md`：阶段性路线图。

### 架构文档

- `architecture/system-architecture.md`：整体架构、模块职责和部署形态。
- `architecture/data-model.md`：核心领域模型和数据表。
- `architecture/security-model.md`：权限、安全、审计和密钥管理。

### Agent 文档

- `agent/agent-protocol.md`：Agent 执行协议、状态机和工具调用规范。
- `agent/tool-registry.md`：工具注册表和权限分级。
- `agent/coding-agent-flow.md`：自动开发并创建 PR 的完整流程。

### 设计文档

- `design/design-principles.md`：UI/UX 设计原则。
- `design/information-architecture.md`：Mac App 信息架构。
- `design/design-system.md`：视觉规范、组件规范和状态系统。

### 页面文档

- `screens/dashboard.md`：首页 Dashboard。
- `screens/task-center.md`：任务中心。
- `screens/agent-run-detail.md`：Agent 执行详情。
- `screens/development-center.md`：开发中心。

### 任务文档

- `tasks/task-index.md`：开发任务总索引。
- `tasks/TASK-001-project-foundation.md`：工程骨架。
- `tasks/TASK-002-lark-bot-entry.md`：飞书/Lark Bot 入口。
- `tasks/TASK-003-task-system.md`：任务系统。
- `tasks/TASK-004-github-integration.md`：GitHub 集成。
- `tasks/TASK-005-agent-runner.md`：Agent Runner。
- `tasks/TASK-006-auto-pr-flow.md`：自动开发并创建 PR。
- `tasks/TASK-007-mac-app-mvp.md`：Mac App MVP。

## 使用方式

1. 先阅读 `product/product-vision.md` 和 `product/core-workflows.md`。
2. 再阅读 `architecture/system-architecture.md`。
3. 如果让 AI Agent 开发，按 `tasks/task-index.md` 的顺序逐个执行任务。
4. 如果让 AI Agent 做 UI，先读取 `design/*`，再执行 `screens/*`。
5. 每个任务执行前必须确认目标、非目标、验收标准和风险点。

## 开发原则

- 不从“大而全”开始，先打通一个端到端核心闭环。
- 不让 AI 直接操作主分支，只允许创建分支和 PR。
- 不跳过权限、审计和执行日志。
- 长任务必须可暂停、可恢复、可审查。
- UI 不是聊天窗口，而是任务、执行、PR、审批和审计的控制台。
