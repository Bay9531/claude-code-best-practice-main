# CLI 启动标志最佳实践

![Last Updated](https://img.shields.io/badge/Last_Updated-Mar%2002%2C%202026-white?style=flat&labelColor=555)

从终端启动 Claude Code 时，Claude Code 启动标志、顶级子命令和启动环境变量的参考文档。

<table width="100%">
<tr>
<td><a href="../">← 返回 Claude Code 最佳实践</a></td>
<td align="right"><img src="../!/claude-jumping.svg" alt="Claude" width="60" /></td>
</tr>
</table>

---

## 目录

1. [会话管理](#session-management)
2. [模型与配置](#model--configuration)
3. [权限与安全](#permissions--security)
4. [输出与格式](#output--format)
5. [系统提示词](#system-prompt)
6. [代理与子代理](#agent--subagent)
7. [MCP 与插件](#mcp--plugins)
8. [目录与工作区](#directory--workspace)
9. [预算与限制](#budget--limits)
10. [集成](#integration)
11. [初始化与维护](#initialization--maintenance)
12. [调试与诊断](#debug--diagnostics)
13. [设置覆盖](#settings-override)
14. [版本与帮助](#version--help)
15. [子命令](#subcommands)
16. [环境变量](#environment-variables)

---

## 会话管理

| Flag | Short | Description |
|------|-------|-------------|
| `--continue` | `-c` | 继续当前目录中最近的会话 |
| `--resume` | `-r` | 按 ID 或名称恢复指定会话，或显示交互式选择器 |
| `--from-pr <NUMBER\|URL>` | | 恢复与特定 GitHub PR 关联的会话 |
| `--fork-session` | | 在恢复时创建新会话 ID（与 `--resume` 或 `--continue` 配合使用） |
| `--session-id <UUID>` | | 使用指定的会话 ID（必须是有效 UUID） |
| `--no-session-persistence` | | 禁用会话持久化（仅打印模式） |
| `--remote` | | 在 claude.ai 上创建新的 Web 会话 |
| `--teleport` | | 在本地终端中恢复 Web 会话 |

---

## 模型与配置

| Flag | Short | Description |
|------|-------|-------------|
| `--model <NAME>` | | 使用别名（`sonnet`、`opus`、`haiku`）或完整模型 ID 设置模型 |
| `--fallback-model <NAME>` | | 默认模型过载时自动回退（仅打印模式） |
| `--betas <LIST>` | | 在 API 请求中包含的 Beta 标头（仅 API 密钥用户） |

---

## 权限与安全

| Flag | Short | Description |
|------|-------|-------------|
| `--dangerously-skip-permissions` | | 跳过所有权限提示。请极其谨慎使用 |
| `--allow-dangerously-skip-permissions` | | 启用权限绕过选项（但不激活它） |
| `--permission-mode <MODE>` | | 以指定权限模式启动：`default`、`plan`、`acceptEdits`、`bypassPermissions` |
| `--allowedTools <TOOLS>` | | 无需提示即可执行的工具（权限规则语法） |
| `--disallowedTools <TOOLS>` | | 从模型上下文中完全移除的工具 |
| `--tools <TOOLS>` | | 限制 Claude 可以使用的内置工具（使用 `""` 禁用所有工具） |
| `--permission-prompt-tool <TOOL>` | | 指定处理非交互模式下权限提示的 MCP 工具 |

---

## 输出与格式

| Flag | Short | Description |
|------|-------|-------------|
| `--print` | `-p` | 打印响应而不进入交互模式（无头/SDK 模式） |
| `--output-format <FORMAT>` | | 输出格式：`text`、`json`、`stream-json` |
| `--input-format <FORMAT>` | | 输入格式：`text`、`stream-json` |
| `--json-schema <SCHEMA>` | | 获取符合模式的验证 JSON（仅打印模式） |
| `--include-partial-messages` | | 包含部分流式事件（需要 `--print` 和 `--output-format=stream-json`） |
| `--verbose` | | 启用详细日志记录，包含完整的逐轮输出 |

---

## 系统提示词

| Flag | Short | Description |
|------|-------|-------------|
| `--system-prompt <TEXT>` | | 用自定义文本替换整个系统提示词 |
| `--system-prompt-file <PATH>` | | 从文件加载系统提示词，替换默认提示词（仅打印模式） |
| `--append-system-prompt <TEXT>` | | 将自定义文本附加到默认系统提示词之后 |
| `--append-system-prompt-file <PATH>` | | 将文件内容附加到默认提示词之后（仅打印模式） |

---

## 代理与子代理

| Flag | Short | Description |
|------|-------|-------------|
| `--agent <NAME>` | | 为当前会话指定代理 |
| `--agents <JSON>` | | 通过 JSON 动态定义自定义子代理 |
| `--teammate-mode <MODE>` | | 设置代理团队显示模式：`auto`、`in-process`、`tmux` |

---

## MCP 与插件

| Flag | Short | Description |
|------|-------|-------------|
| `--mcp-config <PATH\|JSON>` | | 从 JSON 文件或字符串加载 MCP 服务器 |
| `--strict-mcp-config` | | 仅使用来自 `--mcp-config` 的 MCP 服务器，忽略所有其他 |
| `--plugin-dir <PATH>` | | 从目录加载插件（仅限当前会话，可重复使用） |

---

## 目录与工作区

| Flag | Short | Description |
|------|-------|-------------|
| `--add-dir <PATH>` | | 添加额外的工作目录供 Claude 访问 |
| `--worktree` | `-w` | 在隔离的 git worktree 中启动 Claude（从 HEAD 分支） |

---

## 预算与限制

| Flag | Short | Description |
|------|-------|-------------|
| `--max-budget-usd <AMOUNT>` | | API 调用的最大美元金额，超出即停止（仅打印模式） |
| `--max-turns <NUMBER>` | | 限制代理轮次数量（仅打印模式） |

---

## 集成

| Flag | Short | Description |
|------|-------|-------------|
| `--chrome` | | 启用 Chrome 浏览器集成以实现 Web 自动化 |
| `--no-chrome` | | 禁用当前会话的 Chrome 浏览器集成 |
| `--ide` | | 启动时自动连接到 IDE（如果恰好有一个有效的 IDE 可用） |

---

## 初始化与维护

| Flag | Short | Description |
|------|-------|-------------|
| `--init` | | 运行初始化钩子并启动交互模式 |
| `--init-only` | | 运行初始化钩子后退出（不进入交互式会话） |
| `--maintenance` | | 运行维护钩子后退出 |

---

## 调试与诊断

| Flag | Short | Description |
|------|-------|-------------|
| `--debug <CATEGORIES>` | | 启用调试模式，可选的类别过滤（例如 `"api,hooks"`） |

---

## 设置覆盖

| Flag | Short | Description |
|------|-------|-------------|
| `--settings <PATH\|JSON>` | | 要加载的设置 JSON 文件路径或 JSON 字符串 |
| `--setting-sources <LIST>` | | 逗号分隔的加载来源列表：`user`、`project`、`local` |
| `--disable-slash-commands` | | 禁用当前会话的所有技能和斜杠命令 |

---

## 版本与帮助

| Flag | Short | Description |
|------|-------|-------------|
| `--version` | `-v` | 输出版本号 |
| `--help` | `-h` | 显示帮助信息 |

---

## 子命令

以下是以 `claude <subcommand>` 形式运行的顶级命令：

| Subcommand | Description |
|------------|-------------|
| `claude` | 启动交互式 REPL |
| `claude "query"` | 使用初始提示词启动 REPL |
| `claude agents` | 列出已配置的代理 |
| `claude auth` | 管理 Claude Code 身份验证 |
| `claude doctor` | 从命令行运行诊断 |
| `claude install` | 安装或切换 Claude Code 原生构建版本 |
| `claude mcp` | 配置 MCP 服务器（`add`、`remove`、`list`、`get`、`enable`） |
| `claude plugin` | 管理 Claude Code 插件 |
| `claude remote-control` | 管理远程控制会话 |
| `claude setup-token` | 创建用于订阅使用的长期令牌 |
| `claude update` / `claude upgrade` | 更新到最新版本 |

---

## 环境变量

以下仅在启动时使用的环境变量需在启动 Claude Code 之前在 Shell 中设置（它们不能通过 `settings.json` 配置）：

| Variable | Description |
|----------|-------------|
| `CLAUDE_CODE_EXPERIMENTAL_AGENT_TEAMS=1` | 启用实验性代理团队功能 |
| `CLAUDE_CODE_TMPDIR` | 覆盖内部文件的临时目录。也可通过 `env` 键配置——参见[设置参考](./claude-settings.md#environment-variables-via-env) |
| `CLAUDE_CODE_ADDITIONAL_DIRECTORIES_CLAUDE_MD=1` | 启用额外目录中的 CLAUDE.md 加载 |
| `DISABLE_AUTOUPDATER=1` | 禁用自动更新。也可通过 `env` 键配置——参见[设置参考](./claude-settings.md#environment-variables-via-env) |
| `CLAUDE_CODE_EFFORT_LEVEL` | 控制思考深度——参见[设置参考](./claude-settings.md#environment-variables-via-env) |
| `USE_BUILTIN_RIPGREP=0` | 使用系统 ripgrep 而非内置版本（Alpine Linux） |
| `CLAUDE_CODE_SIMPLE` | 启用简单模式（仅 Bash + 编辑工具）。也可通过 `env` 键配置——参见[设置参考](./claude-settings.md#environment-variables-via-env) |
| `CLAUDE_BASH_NO_LOGIN=1` | 跳过 BashTool 的登录 Shell |
| `CCR_FORCE_BUNDLE=1` | 使用 `claude --remote` 时强制打包/上传本地仓库。也可通过 `env` 键配置——参见[设置参考](./claude-settings.md#environment-variables-via-env) |

关于可通过 `settings.json` 中的 `"env"` 键配置的环境变量（包括 `MAX_THINKING_TOKENS`、`CLAUDE_CODE_SHELL`、`CLAUDE_CODE_ENABLE_TASKS`、`CLAUDE_CODE_DISABLE_BACKGROUND_TASKS`、`CLAUDE_CODE_DISABLE_EXPERIMENTAL_BETAS` 等），请参见[Claude 设置参考](./claude-settings.md#environment-variables-via-env)。

---

## 来源

- [Claude Code CLI 参考](https://code.claude.com/docs/en/cli-reference)
- [Claude Code 无头模式](https://code.claude.com/docs/en/headless)
- [Claude Code 设置](https://code.claude.com/docs/en/setup)
- [Claude Code 更新日志](https://github.com/anthropics/claude-code/blob/main/CHANGELOG.md)
- [Claude Code 常见工作流](https://code.claude.com/docs/en/common-workflows)
