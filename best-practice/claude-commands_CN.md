# Commands Best Practice

![最后更新](https://img.shields.io/badge/Last_Updated-May%2021%2C%202026%2012%3A06%20AM%20PKT-white?style=flat&labelColor=555) ![版本](https://img.shields.io/badge/Claude_Code-v2.1.145-blue?style=flat&labelColor=555)<br>
[![已实现](https://img.shields.io/badge/Implemented-2ea44f?style=flat)](../implementation/claude-commands-implementation.md)

Claude Code 命令——元数据字段和官方内置斜杠命令。

<table width="100%">
<tr>
<td><a href="../">← 返回 Claude Code 最佳实践</a></td>
<td align="right"><img src="../!/claude-jumping.svg" alt="Claude" width="60" /></td>
</tr>
</table>

---

## 元数据字段（15 个）

| 字段 | 类型 | 必填 | 描述 |
|-------|------|----------|-------------|
| `name` | string | 否 | 显示名称和 `/斜杠命令` 标识符。省略时默认为目录名 |
| `description` | string | 推荐 | 命令的功能描述。在自动补全中显示，供 Claude 进行自动发现 |
| `when_to_use` | string | 否 | 关于 Claude 何时应调用该技能的额外上下文——触发短语或示例请求。追加到 `description` 后的列表项中，计入 1,536 字符上限 |
| `argument-hint` | string | 否 | 自动补全时显示的提示（例如 `[issue-number]`、`[filename]`） |
| `arguments` | string/list | 否 | 命令内容中 `$name` 替换的命名位置参数。接受空格分隔的字符串或 YAML 列表——名称按顺序映射到参数位置 |
| `disable-model-invocation` | boolean | 否 | 设置为 `true` 可防止 Claude 自动调用此命令 |
| `user-invocable` | boolean | 否 | 设置为 `false` 可从 `/` 菜单中隐藏——命令仅作为背景知识使用 |
| `paths` | string/list | 否 | 限制该技能何时被激活的 glob 模式。接受逗号分隔的字符串或 YAML 列表。设置后，Claude 仅在处理匹配模式的文件时自动加载该技能 |
| `allowed-tools` | string | 否 | 此命令激活时无需权限提示即可使用的工具 |
| `model` | string | 否 | 此命令运行时要使用的模型（例如 `haiku`、`sonnet`、`opus`） |
| `effort` | string | 否 | 调用时覆盖模型的 effort 级别（`low`、`medium`、`high`、`xhigh`、`max`） |
| `context` | string | 否 | 设置为 `fork` 可在隔离的子代理上下文中运行该命令 |
| `agent` | string | 否 | 当设置了 `context: fork` 时的子代理类型（默认：`general-purpose`） |
| `shell` | string | 否 | `` !`command` `` 代码块的 shell——接受 `bash`（默认）或 `powershell`。需要设置 `CLAUDE_CODE_USE_POWERSHELL_TOOL=1` |
| `hooks` | object | 否 | 作用于该命令的生命周期钩子 |

---

## ![官方](../!/tags/official.svg) **（80 个）**

| # | 命令 | 标签 | 描述 |
|---|---------|-----|-------------|
| 1 | `/login` | ![认证](https://img.shields.io/badge/Auth-2980B9?style=flat) | 登录您的 Anthropic 账户 |
| 2 | `/logout` | ![认证](https://img.shields.io/badge/Auth-2980B9?style=flat) | 退出您的 Anthropic 账户 |
| 3 | `/setup-bedrock` | ![认证](https://img.shields.io/badge/Auth-2980B9?style=flat) | 通过交互式向导配置 Amazon Bedrock 认证、区域和模型锁定。仅在设置了 `CLAUDE_CODE_USE_BEDROCK=1` 时可见。首次使用 Bedrock 的用户也可以从登录界面访问此向导 |
| 4 | `/setup-vertex` | ![认证](https://img.shields.io/badge/Auth-2980B9?style=flat) | 通过交互式向导配置 Google Vertex AI 认证、项目、区域和模型锁定。仅在设置了 `CLAUDE_CODE_USE_VERTEX=1` 时可见。首次使用 Vertex AI 的用户也可以从登录界面访问此向导 |
| 5 | `/upgrade` | ![认证](https://img.shields.io/badge/Auth-2980B9?style=flat) | 打开升级页面以切换到更高计划层级 |
| 6 | `/color [color\|default]` | ![配置](https://img.shields.io/badge/Config-F39C12?style=flat) | 设置当前会话的提示栏颜色。可选颜色：`red`、`blue`、`green`、`yellow`、`purple`、`orange`、`pink`、`cyan`。使用 `default` 重置 |
| 7 | `/config` | ![配置](https://img.shields.io/badge/Config-F39C12?style=flat) | 打开设置界面以调整主题、模型、输出样式和其他偏好设置。别名：`/settings` |
| 8 | `/focus` | ![配置](https://img.shields.io/badge/Config-F39C12?style=flat) | 切换聚焦视图，仅显示上一个提示、工具调用摘要和最终响应。有助于减少长时间会话中的视觉干扰。仅在全屏渲染模式下可用 |
| 9 | `/keybindings` | ![配置](https://img.shields.io/badge/Config-F39C12?style=flat) | 打开或创建您的按键绑定配置文件 |
| 10 | `/permissions` | ![配置](https://img.shields.io/badge/Config-F39C12?style=flat) | 管理工具的允许、询问和拒绝规则。打开交互式对话框，您可以按作用域查看规则、添加或删除规则、管理工作目录以及查看最近的自动模式拒绝记录。别名：`/allowed-tools` |
| 11 | `/privacy-settings` | ![配置](https://img.shields.io/badge/Config-F39C12?style=flat) | 查看和更新您的隐私设置。仅适用于 Pro 和 Max 计划订阅用户 |
| 12 | `/radio` | ![配置](https://img.shields.io/badge/Config-F39C12?style=flat) | 在浏览器中打开 Claude FM 低保真电台 |
| 13 | `/sandbox` | ![配置](https://img.shields.io/badge/Config-F39C12?style=flat) | 切换沙箱模式。仅在支持的平台上可用 |
| 14 | `/scroll-speed` | ![配置](https://img.shields.io/badge/Config-F39C12?style=flat) | 交互式调整鼠标滚轮滚动速度 |
| 15 | `/statusline` | ![配置](https://img.shields.io/badge/Config-F39C12?style=flat) | 配置 Claude Code 的状态栏。描述您想要的样式，或不带参数运行以根据您的 shell 提示自动配置 |
| 16 | `/stickers` | ![配置](https://img.shields.io/badge/Config-F39C12?style=flat) | 订购 Claude Code 贴纸 |
| 17 | `/terminal-setup` | ![配置](https://img.shields.io/badge/Config-F39C12?style=flat) | 配置 Shift+Enter 等快捷键的终端按键绑定。仅在需要此功能的终端中可见，如 VS Code、Cursor、Windsurf、Alacritty 或 Zed |
| 18 | `/theme` | ![配置](https://img.shields.io/badge/Config-F39C12?style=flat) | 更改颜色主题。包括浅色和深色变体、色盲友好（道尔顿化）主题、使用终端调色板的 ANSI 主题、跟随终端浅色/深色模式的"自动（匹配终端）"选项，以及从 `~/.claude/themes/` 或插件加载的自定义主题。选择"新建自定义主题…"以创建您自己的主题 |
| 19 | `/tui [default\|fullscreen]` | ![配置](https://img.shields.io/badge/Config-F39C12?style=flat) | 设置终端 UI 渲染器并重新启动 Claude Code，保持当前对话不变。`default` 使用内联渲染；`fullscreen` 使用备屏 TUI |
| 20 | `/voice [hold\|tap\|off]` | ![配置](https://img.shields.io/badge/Config-F39C12?style=flat) | 切换语音听写，或在特定模式下启用。需要 Claude.ai 账户 |
| 21 | `/context` | ![上下文](https://img.shields.io/badge/Context-8E44AD?style=flat) | 以彩色网格形式可视化当前上下文使用情况。显示针对上下文密集型工具、内存膨胀和容量警告的优化建议 |
| 22 | `/cost` | ![上下文](https://img.shields.io/badge/Context-8E44AD?style=flat) | `/usage` 的别名 |
| 23 | `/insights` | ![上下文](https://img.shields.io/badge/Context-8E44AD?style=flat) | 生成分析您的 Claude Code 会话的报告，包括项目领域、交互模式和摩擦点 |
| 24 | `/stats` | ![上下文](https://img.shields.io/badge/Context-8E44AD?style=flat) | `/usage` 的别名。在"统计"标签页中打开 |
| 25 | `/status` | ![上下文](https://img.shields.io/badge/Context-8E44AD?style=flat) | 打开设置界面（状态标签页），显示版本、模型、账户和连接状态。在 Claude 响应期间即可使用，无需等待当前响应完成 |
| 26 | `/usage` | ![上下文](https://img.shields.io/badge/Context-8E44AD?style=flat) | 显示会话费用、计划使用限制和活动统计。`/cost` 和 `/stats` 是别名 |
| 27 | `/usage-credits` | ![上下文](https://img.shields.io/badge/Context-8E44AD?style=flat) | 配置使用额度，以便在达到限制时继续工作。以前称为 `/extra-usage` |
| 28 | `/doctor` | ![调试](https://img.shields.io/badge/Debug-E74C3C?style=flat) | 诊断并验证您的 Claude Code 安装和设置。结果以状态图标显示。按 `f` 让 Claude 修复任何报告的问题 |
| 29 | `/feedback [report]` | ![调试](https://img.shields.io/badge/Debug-E74C3C?style=flat) | 提交反馈、报告错误或分享您的对话。别名：`/bug`、`/share` |
| 30 | `/heapdump` | ![调试](https://img.shields.io/badge/Debug-E74C3C?style=flat) | 将 JavaScript 堆快照和内存分析写入 `~/Desktop`，用于诊断高内存使用情况。在提交有关内存增长的错误报告时很有用 |
| 31 | `/help` | ![调试](https://img.shields.io/badge/Debug-E74C3C?style=flat) | 显示帮助信息和可用命令 |
| 32 | `/powerup` | ![调试](https://img.shields.io/badge/Debug-E74C3C?style=flat) | 通过带有动画演示的快速交互式课程探索 Claude Code 功能 |
| 33 | `/release-notes` | ![调试](https://img.shields.io/badge/Debug-E74C3C?style=flat) | 在交互式版本选择器中查看变更日志。选择特定版本查看其发布说明，或选择显示所有版本 |
| 34 | `/tasks` | ![调试](https://img.shields.io/badge/Debug-E74C3C?style=flat) | 列出和管理后台任务。别名：`/bashes` |
| 35 | `/copy [N]` | ![导出](https://img.shields.io/badge/Export-7F8C8D?style=flat) | 将最后一条助手响应复制到剪贴板。传入数字 `N` 可复制倒数第 N 条响应：`/copy 2` 复制倒数第二条。当存在代码块时，显示交互式选择器以选择单个块或完整响应。在选择器中按 `w` 可将所选内容写入文件而不是剪贴板，在 SSH 环境下很有用 |
| 36 | `/export [filename]` | ![导出](https://img.shields.io/badge/Export-7F8C8D?style=flat) | 将当前对话导出为纯文本。提供文件名则直接写入该文件。不提供文件名则打开对话框，可选择复制到剪贴板或保存到文件 |
| 37 | `/agents` | ![扩展](https://img.shields.io/badge/Extensions-16A085?style=flat) | 管理代理配置 |
| 38 | `/chrome` | ![扩展](https://img.shields.io/badge/Extensions-16A085?style=flat) | 配置 Claude in Chrome 设置 |
| 39 | `/hooks` | ![扩展](https://img.shields.io/badge/Extensions-16A085?style=flat) | 查看工具事件的钩子配置 |
| 40 | `/ide` | ![扩展](https://img.shields.io/badge/Extensions-16A085?style=flat) | 管理 IDE 集成并显示状态 |
| 41 | `/mcp` | ![扩展](https://img.shields.io/badge/Extensions-16A085?style=flat) | 管理 MCP 服务器连接和 OAuth 认证 |
| 42 | `/plugin` | ![扩展](https://img.shields.io/badge/Extensions-16A085?style=flat) | 管理 Claude Code 插件 |
| 43 | `/reload-plugins` | ![扩展](https://img.shields.io/badge/Extensions-16A085?style=flat) | 重新加载所有活动插件以应用待定更改，无需重启。报告每个已重新加载组件的计数，并标记任何加载错误 |
| 44 | `/skills` | ![扩展](https://img.shields.io/badge/Extensions-16A085?style=flat) | 列出可用技能。按 `t` 可按 token 数量排序 |
| 45 | `/memory` | ![记忆](https://img.shields.io/badge/Memory-3498DB?style=flat) | 编辑 `CLAUDE.md` 记忆文件，启用或禁用自动记忆，以及查看自动记忆条目 |
| 46 | `/effort [low\|medium\|high\|xhigh\|max\|auto]` | ![模型](https://img.shields.io/badge/Model-E67E22?style=flat) | 设置模型的 effort 级别。可用级别取决于模型，包括 `low`、`medium`、`high`、`xhigh` 和 `max`（仅会话内）。不带参数时，打开交互式滑块以选择级别。`auto` 重置为模型默认值。立即生效，无需等待当前响应完成 |
| 47 | `/fast [on\|off]` | ![模型](https://img.shields.io/badge/Model-E67E22?style=flat) | 切换快速模式的开启或关闭 |
| 48 | `/model [model]` | ![模型](https://img.shields.io/badge/Model-E67E22?style=flat) | 选择或更改 AI 模型。对于支持此功能的模型，使用左/右箭头调整 effort 级别。更改立即生效，无需等待当前响应完成。在已有历史输出的对话中间切换时，Claude 会在应用更改前发出警告 |
| 49 | `/passes` | ![模型](https://img.shields.io/badge/Model-E67E22?style=flat) | 与朋友分享 Claude Code 免费一周。仅当您的账户符合条件时可见 |
| 50 | `/plan [description]` | ![模型](https://img.shields.io/badge/Model-E67E22?style=flat) | 直接从提示进入计划模式。传入可选的描述以进入计划模式并立即开始处理该任务，例如 `/plan fix the auth bug` |
| 51 | `/ultraplan <prompt>` | ![模型](https://img.shields.io/badge/Model-E67E22?style=flat) | 在超级计划会话中起草计划，在浏览器中审阅，然后远程执行或将其发送回您的终端 |
| 52 | `/add-dir <path>` | ![项目](https://img.shields.io/badge/Project-27AE60?style=flat) | 在当前会话中添加一个工作目录以访问文件。添加的目录不会发现大多数 `.claude/` 配置 |
| 53 | `/diff` | ![项目](https://img.shields.io/badge/Project-27AE60?style=flat) | 打开交互式差异查看器，显示未提交的更改和每轮差异。使用左/右箭头在当前的 git diff 和各个 Claude 轮次之间切换，使用上/下箭头浏览文件 |
| 54 | `/init` | ![项目](https://img.shields.io/badge/Project-27AE60?style=flat) | 使用 `CLAUDE.md` 指南初始化项目。设置 `CLAUDE_CODE_NEW_INIT=1` 可使用交互式流程，同时引导您完成技能、钩子和个人记忆文件的设置 |
| 55 | `/review` | ![项目](https://img.shields.io/badge/Project-27AE60?style=flat) | 在当前会话中本地审查拉取请求。如需更深入的基于云的审查，请参见 `/ultrareview` |
| 56 | `/security-review` | ![项目](https://img.shields.io/badge/Project-27AE60?style=flat) | 分析当前分支上的待定更改以查找安全漏洞。审查 git diff 并识别注入、认证问题和数据暴露等风险 |
| 57 | `/team-onboarding` | ![项目](https://img.shields.io/badge/Project-27AE60?style=flat) | 根据您的 Claude Code 使用历史生成团队入职指南。分析过去 30 天的会话、命令和 MCP 服务器使用情况 |
| 58 | `/ultrareview [PR]` | ![项目](https://img.shields.io/badge/Project-27AE60?style=flat) | 在云沙箱中对给定拉取请求进行深入的多代理代码审查。生成带有优先级排序发现的结构化审查报告；补充本地的 `/review` 命令 |
| 59 | `/autofix-pr [prompt]` | ![远程](https://img.shields.io/badge/Remote-5D6D7E?style=flat) | 生成一个在 Web 会话上的 Claude Code，监视当前分支的 PR，并在 CI 失败或审阅者留下评论时推送修复。通过 `gh pr view` 从您检出的分支检测打开的 PR；如需监视不同的 PR，请先检出其分支。需要 `gh` CLI 和对 Claude Code on the web 的访问权限 |
| 60 | `/desktop` | ![远程](https://img.shields.io/badge/Remote-5D6D7E?style=flat) | 在 Claude Code 桌面应用中继续当前会话。仅限 macOS 和 Windows。别名：`/app` |
| 61 | `/install-github-app` | ![远程](https://img.shields.io/badge/Remote-5D6D7E?style=flat) | 为仓库设置 Claude GitHub Actions 应用。引导您选择仓库并配置集成 |
| 62 | `/install-slack-app` | ![远程](https://img.shields.io/badge/Remote-5D6D7E?style=flat) | 安装 Claude Slack 应用。打开浏览器完成 OAuth 流程 |
| 63 | `/mobile` | ![远程](https://img.shields.io/badge/Remote-5D6D7E?style=flat) | 显示二维码以下载 Claude 移动应用。别名：`/ios`、`/android` |
| 64 | `/remote-control` | ![远程](https://img.shields.io/badge/Remote-5D6D7E?style=flat) | 使此会话可从 claude.ai 进行远程控制。别名：`/rc` |
| 65 | `/remote-env` | ![远程](https://img.shields.io/badge/Remote-5D6D7E?style=flat) | 配置使用 `--remote` 启动的 Web 会话的默认远程环境 |
| 66 | `/schedule [description]` | ![远程](https://img.shields.io/badge/Remote-5D6D7E?style=flat) | 创建、更新、列出或运行例行任务。Claude 以对话方式引导您完成设置。别名：`/routines` |
| 67 | `/teleport` | ![远程](https://img.shields.io/badge/Remote-5D6D7E?style=flat) | 将 Web 会话上的 Claude Code 拉入当前终端：打开选择器，然后获取分支和对话。也可使用 `/tp`。需要 claude.ai 订阅 |
| 68 | `/web-setup` | ![远程](https://img.shields.io/badge/Remote-5D6D7E?style=flat) | 使用您本地的 `gh` CLI 凭据将您的 GitHub 账户连接到 Claude Code on the web。如果 GitHub 未连接，`/schedule` 会自动提示此操作 |
| 69 | `/background [prompt]` | ![会话](https://img.shields.io/badge/Session-4A90D9?style=flat) | 分离当前会话以作为后台代理运行，释放此终端。别名：`/bg` |
| 70 | `/branch [name]` | ![会话](https://img.shields.io/badge/Session-4A90D9?style=flat) | 在此时间点创建当前对话的分支。别名：`/fork`。当设置了 `CLAUDE_CODE_FORK_SUBAGENT` 时，`/fork` 改为生成一个分支子代理，不再作为此命令的别名 |
| 71 | `/btw <question>` | ![会话](https://img.shields.io/badge/Session-4A90D9?style=flat) | 快速提出一个旁侧问题，不添加到对话中 |
| 72 | `/clear` | ![会话](https://img.shields.io/badge/Session-4A90D9?style=flat) | 以空上下文开始新对话。之前的对话可在 `/resume` 中找到。如需在继续同一对话的同时释放上下文，请使用 `/compact`。别名：`/reset`、`/new` |
| 73 | `/compact [instructions]` | ![会话](https://img.shields.io/badge/Session-4A90D9?style=flat) | 压缩对话，附带可选的聚焦指令 |
| 74 | `/exit` | ![会话](https://img.shields.io/badge/Session-4A90D9?style=flat) | 退出 CLI。别名：`/quit` |
| 75 | `/goal [condition\|clear]` | ![会话](https://img.shields.io/badge/Session-4A90D9?style=flat) | 设置一个目标——Claude 会持续工作多轮，直到条件满足。传入 `clear` 可移除现有目标 |
| 76 | `/recap` | ![会话](https://img.shields.io/badge/Session-4A90D9?style=flat) | 按需生成当前会话的一行摘要，不影响正在进行的对话 |
| 77 | `/rename [name]` | ![会话](https://img.shields.io/badge/Session-4A90D9?style=flat) | 重命名当前会话并在提示栏上显示名称。不提供名称时，根据对话历史自动生成一个 |
| 78 | `/resume [session]` | ![会话](https://img.shields.io/badge/Session-4A90D9?style=flat) | 按 ID 或名称恢复会话，或打开会话选择器。别名：`/continue` |
| 79 | `/rewind` | ![会话](https://img.shields.io/badge/Session-4A90D9?style=flat) | 将对话和/或代码回退到之前的时间点，或从选中的消息进行摘要。请参见检查点。别名：`/checkpoint`、`/undo` |
| 80 | `/stop` | ![会话](https://img.shields.io/badge/Session-4A90D9?style=flat) | 停止当前后台会话。保留对话记录和工作树 |

诸如 `/debug` 等捆绑技能也会出现在斜杠命令菜单中，但它们不是内置命令。

---

## 来源

- [Claude Code 斜杠命令](https://code.claude.com/docs/en/slash-commands)
- [Claude Code 交互模式](https://code.claude.com/docs/en/interactive-mode)
- [Claude Code 变更日志](https://github.com/anthropics/claude-code/blob/main/CHANGELOG.md)
