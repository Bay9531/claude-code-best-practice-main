# CLAUDE.md

本文件为 Claude Code (claude.ai/code) 在此仓库中工作时提供指导。

## 仓库概述

这是一个 Claude Code 配置的最佳实践参考仓库，演示了技能(skills)、子代理(subagents)、钩子(hooks)和命令(commands)的使用模式。它是一个文档和示例仓库 — 而非可运行的应用程序。

## 关键组件

### 天气系统（示例工作流）
演示 Command → Agent → Skill 架构：
- `/weather-orchestrator` 命令（`.claude/commands/weather-orchestrator.md`）— 入口点，先调用代理，再调用技能
- `weather-agent` 代理（`.claude/agents/weather-agent.md`）— 预加载 `weather-fetcher` 技能，Sonnet 模型，5 轮次
- `weather-fetcher` 技能（`.claude/skills/weather-fetcher/SKILL.md`）— 仅代理使用，从 Open-Meteo 获取迪拜温度
- `weather-svg-creator` 技能（`.claude/skills/weather-svg-creator/SKILL.md`）— 创建 SVG 卡片，写入输出文件
完整流程图见 `orchestration-workflow/orchestration-workflow.md`。

### 代理团队系统（实验性）
`agent-teams/` 中的独立演示，展示实验性的代理团队(agent teams)功能，包含并行的时间编排工作流。启动提示见 `agent-teams/agent-teams-prompt.md`。

### 开发工作流
- `development-workflows/rpi/` — 研究(Research) → 规划(Plan) → 实施(Implement) 模式，配备 8 个专用子代理（PM、UX、CTO、需求解析器、高级工程师、代码审查员、文档分析师、合规验证器）和 3 个命令（`/rpi:research`、`/rpi:plan`、`/rpi:implement`）
- `development-workflows/cross-model-workflow/` — Claude Code + Codex 双模型工作流：规划(Claude) → QA 审查(Codex) → 实施(Claude) → 验证(Codex)。记录了 4 种桥接机制（插件、MCP、路由）

### 技能定义结构
`.claude/skills/<name>/SKILL.md` 中的技能使用 YAML 前置元数据：
- `name`、`description`（用于自动发现）、`argument-hint`、`disable-model-invocation`、`user-invocable`
- `allowed-tools`、`model`、`context`（设为 `fork` 可隔离为子代理）、`agent`、`hooks`

两种技能模式：**代理技能**（通过代理的 `skills:` 字段预加载，`user-invocable: false`）与**独立技能**（通过 `Skill` 工具或 `/` 菜单调用）。

### 子代理定义结构
`.claude/agents/*.md` 中的子代理使用 YAML 前置元数据：
- `name`、`description`（使用 "PROACTIVELY" 表示自动调用）、`tools`、`disallowedTools`
- `model`（haiku/sonnet/opus/inherit）、`permissionMode`（如 `acceptEdits`、`bypassPermissions`）、`maxTurns`
- `skills`（预加载的代理技能）、`mcpServers`、`hooks`、`memory`（user/project/local）
- `background`、`effort`（low/medium/high/max）、`isolation`（worktree）、`color`

### 演示系统
每个演示文稿由专用代理处理（参见 `.claude/rules/presentation.md`）：
- `presentation-vibe-coding` → `presentation/vibe-coding-to-agentic-engineering/`
- `presentation-claude-gemini` → `presentation/2026-04-25-gdg-kolachi-cli-claude-code-gemini/`
- `presentation-claude-code` → `presentation/claude-code-best-practice/`

### 钩子系统
`.claude/hooks/` 中的跨平台声音通知系统：
- `scripts/hooks.py` — 处理全部 27 个钩子事件的 Python 处理程序，支持代理特定音效
- `config/hooks-config.json` — 团队共享配置（按钩子启用/禁用）；`hooks-config.local.json` 用于个人覆盖
- `sounds/` — 每个事件的 .mp3/.wav 文件对（ElevenLabs TTS 生成）
- 已注册 27 个钩子：PreToolUse、PostToolUse、UserPromptSubmit、Notification、Stop、SubagentStart、SubagentStop、PreCompact、SessionStart、SessionEnd、Setup、PermissionRequest、TeammateIdle、TaskCompleted、ConfigChange 等
- 特殊处理：git 提交触发 `pretooluse-git-committing` 音效
- 完整文档：`.claude/hooks/HOOKS-README.md`

## 配置

### 层级
1. **托管配置**（`managed-settings.json` / MDM plist / Windows 注册表）— 组织强制，不可覆盖
2. 命令行参数 — 单会话覆盖
3. `.claude/settings.local.json` — 个人项目设置（git 忽略）
4. `.claude/settings.json` — 团队共享项目设置
5. `~/.claude/settings.json` — 全局个人默认设置
6. `hooks-config.local.json` 覆盖 `hooks-config.json`

### 关键项目设置
- `CLAUDE_AUTOCOMPACT_PCT_OVERRIDE=80` — 上下文达到 80% 时自动压缩
- `plansDirectory: "./reports"` — 计划文件存储在 reports 目录
- `outputStyle: "Explanatory"` — 详细教程风格输出
- 所有提交附带 `Co-Authored-By: Claude`
- 自定义旋转提示词(spinner verbs)和提示覆盖内置默认值
- 状态栏显示模型、分支、上下文百分比、费用
- `enableAllProjectMcpServers: true`

### MCP 服务器（`.mcp.json`）
- `playwright` — 浏览器自动化（`npx @playwright/mcp@0.0.70`）
- `context7` — 文档查询（`npx @upstash/context7-mcp@2.1.8`）
- `deepwiki` — Wiki 搜索（`npx deepwiki-mcp@0.0.6`）

## 内容目录

- `best-practice/` — 权威参考文档：子代理、命令、技能、设置、记忆、MCP、CLI 启动参数、强化功能(power-ups)
- `reports/` — 13 篇深度分析报告：代理记忆、高级工具使用、SDK vs CLI、LLM 退化、Harness 重要性、旋转提示词、浏览器 MCP 对比、设置作用域等
- `tips/` — 8 篇精选技巧合集，来自 Boris Cherny（Claude Code 创建者）和 Thariq（Anthropic），按日期整理
- `videos/` — 8 篇视频/播客转录（Karpathy、Matt Pocock、Boris Cherny 等），含时间戳
- `tutorial/` — 初学者课程：day0（Windows/Linux/macOS 安装），day1（提示词 → 代理 → 技能）
- `implementation/` — 展示每个概念在此仓库中如何实现的工作示例
- `changelog/` — 按类别追踪版本变更

## 关键模式

### 子代理编排
子代理**不能**通过 bash 调用其他子代理。请使用 Agent 工具：
```
Agent(subagent_type="agent-name", description="...", prompt="...", model="haiku")
```
在子代理定义中要明确说明工具使用方式 — 避免使用"launch"等模糊术语。

### README 表格维护
`.claude/commands/workflows/` 中的命令用于更新 README 中的开发工作流、代理合集和技能合集表格。最佳实践变更追踪工作流位于 `.claude/commands/workflows/best-practice/`。

## 回答最佳实践问题

始终优先搜索此仓库（`best-practice/`、`reports/`、`tips/`、`implementation/`、`README.md`），然后再依赖训练知识或外部来源。此仓库是权威来源。

## 工作流最佳实践

- 保持 CLAUDE.md 每文件不超过 200 行，以确保可靠遵守
- 带有 `paths:` 前置元数据的 `.claude/rules/*.md` 仅在 Claude 触及匹配文件时延迟加载；没有前置元数据的则像 CLAUDE.md 一样加载到每个会话中
- 使用命令(commands)而非独立代理来管理工作流
- 创建具有技能的特定功能子代理（渐进式披露），而非通用代理
- 当上下文接近自动压缩阈值时（本项目为 80%）执行手动 `/compact`
- 复杂任务从计划模式(plan mode)开始
- 对多步骤任务使用人工把关的任务列表工作流
- 将子任务拆分得足够小，以便在远低于压缩阈值前完成

### 调试
- 使用 `/doctor` 进行诊断
- 将长时间运行的终端命令作为后台任务运行，以便更好地查看日志
- 使用浏览器自动化 MCP（Playwright、Chrome DevTools）让 Claude 检查控制台日志
- 报告视觉问题时提供截图

## Git 提交规则

**每个文件单独提交** — 不要将多个文件的更改捆绑到一个提交中。每个文件单独提交，并附上针对该文件更改的描述性提交信息。

## 文档

参见 `.claude/rules/markdown-docs.md` 了解文档标准：
- 保持文件聚焦 — 一个文件一个主题
- 使用文档之间的相对链接，而非绝对 GitHub URL
- 在最佳实践和报告文档顶部包含返回导航链接
- 添加新概念或报告时，更新 README.md 中相应的表格
