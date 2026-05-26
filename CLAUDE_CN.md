# CLAUDE.md

本文件为 Claude Code (claude.ai/code) 在此仓库中工作时提供指导。

## 仓库概述

这是一个 Claude Code 配置的最佳实践仓库，演示了技能(skills)、子代理(subagents)、钩子(hooks)和命令(commands)的使用模式。它作为参考实现，而非应用程序代码库。

## 关键组件

### 天气系统（示例工作流）
通过 **Command → Agent → Skill** 架构演示两种不同的技能模式：
- `/weather-orchestrator` 命令（`.claude/commands/weather-orchestrator.md`）：入口点 — 询问用户选择摄氏度/华氏度，调用代理，然后调用 SVG 技能
- `weather-agent` 代理（`.claude/agents/weather-agent.md`）：使用其预加载的 `weather-fetcher` 技能获取温度（代理技能模式）
- `weather-fetcher` 技能（`.claude/skills/weather-fetcher/SKILL.md`）：预加载到代理中 — 包含从 Open-Meteo 获取温度的指令
- `weather-svg-creator` 技能（`.claude/skills/weather-svg-creator/SKILL.md`）：独立技能 — 创建 SVG 天气卡片，写入 `orchestration-workflow/weather.svg` 和 `orchestration-workflow/output.md`

两种技能模式：代理技能（通过 `skills:` 字段预加载）与独立技能（通过 `Skill` 工具调用）。完整流程图见 `orchestration-workflow/orchestration-workflow.md`。

### 技能定义结构
`.claude/skills/<name>/SKILL.md` 中的技能使用 YAML 前置元数据：
- `name`：显示名称和 `/slash-command`（默认为目录名）
- `description`：何时调用（建议填写以支持自动发现）
- `argument-hint`：自动补全提示（例如 `[issue-number]`）
- `disable-model-invocation`：设为 `true` 可阻止自动调用
- `user-invocable`：设为 `false` 可从 `/` 菜单中隐藏（仅作为后台知识）
- `allowed-tools`：技能激活时无需权限提示即可使用的工具
- `model`：技能激活时使用的模型
- `context`：设为 `fork` 可在隔离的子代理上下文中运行
- `agent`：`context: fork` 时使用的子代理类型（默认：`general-purpose`）
- `hooks`：作用于此技能的生命周期钩子

### 演示系统
参见 `.claude/rules/presentation.md` — 演示工作按演示文稿委派给 `presentation-vibe-coding`（对应 `presentation/vibe-coding-to-agentic-engineering/`）或 `presentation-claude-gemini`（对应 `presentation/2026-04-25-gdg-kolachi-cli-claude-code-gemini/`）。

### 钩子系统
`.claude/hooks/` 中的跨平台声音通知系统：
- `scripts/hooks.py`：Claude Code 钩子事件的主处理程序
- `config/hooks-config.json`：团队共享配置
- `config/hooks-config.local.json`：个人覆盖配置（git 忽略）
- `sounds/`：按钩子事件组织的音频文件（通过 ElevenLabs TTS 生成）

`.claude/settings.json` 中配置的钩子事件：PreToolUse、PostToolUse、UserPromptSubmit、Notification、Stop、SubagentStart、SubagentStop、PreCompact、SessionStart、SessionEnd、Setup、PermissionRequest、TeammateIdle、TaskCompleted、ConfigChange。

特殊处理：git 提交触发 `pretooluse-git-committing` 声音。

## 关键模式

### 子代理编排
子代理**不能**通过 bash 命令调用其他子代理。请使用 Agent 工具（v2.1.63 中从 Task 重命名；`Task(...)` 仍可作为别名使用）：
```
Agent(subagent_type="agent-name", description="...", prompt="...", model="haiku")
```

在子代理定义中要明确说明工具使用方式。避免使用"launch"等可能被误解为 bash 命令的模糊术语。

### 子代理定义结构
`.claude/agents/*.md` 中的子代理使用 YAML 前置元数据：
- `name`：子代理标识符
- `description`：何时调用（使用 "PROACTIVELY" 表示自动调用）
- `tools`：逗号分隔的工具允许列表（省略则继承全部）。支持 `Agent(agent_type)` 语法
- `disallowedTools`：要拒绝的工具，从继承或指定的列表中移除
- `model`：模型别名：`haiku`、`sonnet`、`opus` 或 `inherit`（默认：`inherit`）
- `permissionMode`：权限模式（例如 `"acceptEdits"`、`"plan"`、`"bypassPermissions"`）
- `maxTurns`：子代理停止前的最大代理轮次
- `skills`：要预加载到代理上下文中的技能名称列表
- `mcpServers`：此子代理的 MCP 服务器（服务器名称或内联配置）
- `hooks`：作用于此子代理的生命周期钩子（支持所有钩子事件；`PreToolUse`、`PostToolUse` 和 `Stop` 最常用）
- `memory`：持久化记忆范围 — `user`、`project` 或 `local`（参见 `reports/claude-agent-memory.md`）
- `background`：设为 `true` 可始终作为后台任务运行
- `effort`：努力级别覆盖：`low`、`medium`、`high`、`max`（默认：继承自会话）
- `isolation`：设为 `"worktree"` 可在临时 git 工作树中运行
- `color`：CLI 输出颜色，用于视觉区分

### 配置层级
1. **托管**（`managed-settings.json` / MDM plist / 注册表）：组织强制，不可覆盖
2. 命令行参数：单会话覆盖
3. `.claude/settings.local.json`：个人项目设置（git 忽略）
4. `.claude/settings.json`：团队共享设置
5. `~/.claude/settings.json`：全局个人默认设置
6. `hooks-config.local.json` 覆盖 `hooks-config.json`

### 禁用钩子
在 `.claude/settings.local.json` 中设置 `"disableAllHooks": true`，或在 `hooks-config.json` 中禁用单个钩子。

## 回答最佳实践问题

当用户询问 Claude Code 最佳实践问题时，**始终优先搜索此仓库**（`best-practice/`、`reports/`、`tips/`、`implementation/` 和 `README.md`），然后再依赖训练知识或外部来源。此仓库是权威来源 — 仅当在此处找不到答案时才回退到外部文档或网络搜索。

## 工作流最佳实践

来自此仓库的经验：

- 保持 CLAUDE.md 每文件不超过 200 行，以确保可靠遵守
- 带有 `paths:` YAML 前置元数据的 `.claude/rules/*.md` 仅在 Claude 触及匹配文件时延迟加载；没有前置元数据的则像 CLAUDE.md 一样加载到每个会话中
- 使用命令(commands)而非独立代理来管理工作流
- 创建具有技能的特定功能子代理（渐进式披露），而非通用代理
- 在上下文使用量约 50% 时执行手动 `/compact`
- 复杂任务从计划模式(plan mode)开始
- 对多步骤任务使用人工把关的任务列表工作流
- 将子任务拆分得足够小，以便在 50% 上下文以内完成

### 调试技巧

- 使用 `/doctor` 进行诊断
- 将长时间运行的终端命令作为后台任务运行，以便更好地查看日志
- 使用浏览器自动化 MCP（Claude in Chrome、Playwright、Chrome DevTools）让 Claude 检查控制台日志
- 报告视觉问题时提供截图

## Git 提交规则

提交更改时，**每个文件单独提交**。不要将多个文件的更改捆绑到一个提交中。每个文件单独提交，并附上针对该文件更改的描述性提交信息。

例如，如果 `README.md`、`best-practice/claude-subagents.md` 和一个技能文件都发生了变化：
- 提交 1：`git add README.md` → 提交，附带针对 README 的描述信息
- 提交 2：`git add best-practice/claude-subagents.md` → 提交，附带针对子代理文档的描述信息
- 提交 3：`git add .claude/skills/weather-fetcher/SKILL.md` → 提交，附带针对技能文件的描述信息

这使得 git 历史更清晰，更易于审查、回滚或挑选单个更改。

## 文档

参见 `.claude/rules/markdown-docs.md` 了解文档标准。关键文档：
- `best-practice/claude-subagents.md`：子代理前置元数据、钩子和仓库代理
- `best-practice/claude-commands.md`：斜杠命令模式和内置命令参考
- `orchestration-workflow/orchestration-workflow.md`：天气系统流程图
