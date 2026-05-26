# 设置报告 — 更新日志历史

## 状态图例

| 状态 | 含义 |
|------|------|
| ✅ `COMPLETE (reason)` | 已采取措施并成功解决 |
| ❌ `INVALID (reason)` | 发现结果不正确、不适用或有意为之 |
| ✋ `ON HOLD (reason)` | 操作延期 — 等待外部依赖或用户决定 |

---

## [2026-03-05 06:18 AM PKT] Claude Code v2.1.69

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 缺失设置 | 添加 13 个非钩子缺失设置键 (`$schema`, `availableModels`, `fastModePerSessionOptIn`, `teammateMode`, `prefersReducedMotion`, `sandbox.filesystem.*`, `sandbox.network.allowManagedDomainsOnly`, `sandbox.enableWeakerNetworkIsolation`, `allowManagedMcpServersOnly`, `blockedMarketplaces`, `includeGitInstructions`, `pluginTrustMessage`, `fileSuggestion` 表格条目) | ✅ COMPLETE (已添加到报告) |
| 2 | HIGH | 缺失环境变量 | 添加缺失的环境变量, 包括 `CLAUDE_CODE_DISABLE_ADAPTIVE_THINKING`, `CLAUDE_CODE_DISABLE_1M_CONTEXT`, `CLAUDE_CODE_ACCOUNT_UUID`, `CLAUDE_CODE_DISABLE_GIT_INSTRUCTIONS`, `ENABLE_CLAUDEAI_MCP_SERVERS` 等 | ✅ COMPLETE (已向报告添加 13 个缺失环境变量) |
| 3 | HIGH | 努力默认值 | 将努力级别默认值从"高"更新为"中" (针对 Max/Team 订阅用户); 添加 Sonnet 4.6 支持 (在 v2.1.68 中更改) | ✅ COMPLETE (默认值已更新, Sonnet 说明已添加) |
| 4 | MED | 设置层级 | 添加通过 macOS plist/Windows 注册表管理的设置 (v2.1.61/v2.1.69); 记录跨作用域的数组合并行为 | ✅ COMPLETE (plist/注册表及合并说明已添加) |
| 5 | MED | 沙箱文件系统 | 添加 `sandbox.filesystem.allowWrite`, `denyWrite`, `denyRead` 及路径前缀语义 (`//`, `~/`, `/`, `./`) | ✅ COMPLETE (已添加到沙箱表) |
| 6 | MED | 权限语法 | 添加 `Agent(name)` 权限模式; 记录 `MCP(server:tool)` 语法形式 | ✅ COMPLETE (已添加到工具语法表) |
| 7 | MED | 插件空白 | 添加 `blockedMarketplaces`, `pluginTrustMessage` | ✅ COMPLETE (已添加到插件表) |
| 8 | MED | 模型配置 | 添加 `availableModels` 设置 | ✅ COMPLETE (已添加到通用设置表) |
| 9 | MED | 可疑键 | 验证 `sandbox.network.deniedDomains`, `sandbox.ignoreViolations`, `pluginConfigs` — 存在于报告中但不在官方文档中 | ✋ ON HOLD (保留在报告中待验证) |
| 10 | LOW | 表头计数 | 将表头从"38 个设置和 84 个环境变量"更新为反映实际计数 (~55+ 设置, ~110+ 环境变量) | ✅ COMPLETE (表头已更新) |
| 11 | LOW | CLAUDE.md 同步 | 更新 CLAUDE.md 配置层级 (添加管理/CLI/用户级别) | ✋ ON HOLD (等待用户批准) |
| 12 | LOW | 示例更新 | 使用 `$schema`、沙箱文件系统、`Agent(*)` 更新快速参考示例, 移除钩子示例 | ✅ COMPLETE (示例已更新) |
| 13 | MED | 钩子重定向 | 将钩子部分替换为指向 claude-code-hooks 仓库的重定向 | ✅ COMPLETE (钩子已外部化到专用仓库) |

---

## [2026-03-07 02:17 PM PKT] Claude Code v2.1.71

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 行为变更 | 修复 `teammateMode`: 类型 `boolean` → `string`, 默认值 `false` → `"auto"`, 描述 → "代理团队显示: auto, in-process, tmux" | ✅ COMPLETE (类型、默认值和描述已更新) |
| 2 | HIGH | 新设置 | 在权限表中添加 `allowManagedPermissionRulesOnly` (布尔值, 仅管理) | ✅ COMPLETE (已添加到权限键表) |
| 3 | HIGH | 缺失环境变量 | 添加约 31 个缺失环境变量, 包括已确认的 (`CLAUDE_CODE_MAX_OUTPUT_TOKENS`, `CLAUDE_CODE_DISABLE_FAST_MODE`, `CLAUDE_CODE_DISABLE_AUTO_MEMORY`, `CLAUDE_CODE_USER_EMAIL`, `CLAUDE_CODE_ORGANIZATION_UUID`, `CLAUDE_CONFIG_DIR`) 和代理报告的 (Foundry, Bedrock, mTLS, shell 前缀等) | ✅ COMPLETE (已向表添加 31 个环境变量) |
| 4 | MED | 默认值变更 | 修复 `plansDirectory` 默认值从 `.claude/plans/` 到 `~/.claude/plans` | ✅ COMPLETE (默认值已更新) |
| 5 | MED | 描述变更 | 修复 `sandbox.enableWeakerNetworkIsolation` 描述为"(仅 macOS) 允许访问系统 TLS 信任; 降低安全性" | ✅ COMPLETE (描述已更新) |
| 6 | MED | 范围修复 | 修复 `extraKnownMarketplaces` 范围从"任意"到"项目" | ✅ COMPLETE (范围和描述已更新) |
| 7 | MED | 边界违规 | 将 `claude-cli-startup-flags.md` 中的 `CLAUDE_CODE_EFFORT_LEVEL` 替换为对设置报告的交叉引用 | ✅ COMPLETE (已替换为链接) |
| 8 | MED | 版本徽章 | 将报告版本从 v2.1.69 更新为 v2.1.71 | ✅ COMPLETE (徽章和表头已更新) |
| 9 | LOW | 可疑键 | 验证 `skipWebFetchPreflight`, `sandbox.ignoreViolations`, `sandbox.network.deniedDomains`, `skippedMarketplaces`, `skippedPlugins`, `pluginConfigs` | ✋ ON HOLD (保留在报告中待验证 — 从 2026-03-05 重复) |
| 10 | LOW | CLAUDE.md 同步 | 更新 CLAUDE.md 配置层级 (3 级 → 5+) | ✅ COMPLETE (已更新为包含管理层级的 5 级层级) |

---

## [2026-03-12 12:23 PM PKT] Claude Code v2.1.74

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 行为变更 | 修复 `dontAsk` 权限模式描述: "自动接受所有工具" → "自动拒绝工具, 除非通过 `/permissions` 或 `permissions.allow` 规则预先批准" | ✅ COMPLETE (描述已根据官方权限文档更正) |
| 2 | HIGH | 新设置 | 在模型配置部分添加 `modelOverrides` (对象, 将 Anthropic 模型 ID 映射到特定提供商的 ID, 如 Bedrock ARN) | ✅ COMPLETE (已添加示例和描述) |
| 3 | HIGH | 新设置 | 在仅管理设置列表中添加 `allow_remote_sessions` (布尔值, 默认 `true`, 控制远程控制/网络会话访问) | ✅ COMPLETE (已添加到权限键表) |
| 4 | HIGH | 默认值变更 | 根据官方文档修复 `$schema` URL 从 `https://www.schemastore.org/...` 到 `https://json.schemastore.org/...` | ✅ COMPLETE (已在描述、示例和来源中更新) |
| 5 | MED | 描述变更 | 修复 `ANTHROPIC_CUSTOM_HEADERS` 格式描述从"JSON 字符串"到"名称: 值格式, 换行分隔" | ✅ COMPLETE (描述已根据官方文档更新) |
| 6 | MED | 未验证模式 | `askEdits` 和 `viewOnly` 权限模式不在官方文档中 — 仅 5 种模式有文档记录 (default, acceptEdits, plan, dontAsk, bypassPermissions) | ✅ COMPLETE (已在表中标记为"不在官方文档中 — 未验证") |
| 7 | MED | 缺失环境变量 | 添加 `CLAUDE_CODE_SESSIONEND_HOOKS_TIMEOUT_MS`, `CLAUDE_CODE_DISABLE_FEEDBACK_SURVEY`, `CLAUDE_CODE_DISABLE_TERMINAL_TITLE`, `CLAUDE_CODE_IDE_SKIP_AUTO_INSTALL`, `CLAUDE_CODE_OTEL_HEADERS_HELPER_DEBOUNCE_MS` | ✅ COMPLETE (已添加 5 个环境变量及 `CLAUDE_CODE_OTEL_HEADERS_HELPER_DEBOUNCE_MS`) |
| 8 | MED | 新设置 | 在核心配置中添加 `autoMemoryDirectory` (字符串, 自定义自动记忆目录) — 版本不确定 (代理意见分歧: v2.1.68 vs v2.1.74), 不在设置页面上 | ✅ COMPLETE (已在 plansDirectory 附近添加 — 版本未解决) |
| 9 | LOW | 可疑键 | 验证 `skipWebFetchPreflight`, `sandbox.ignoreViolations`, `sandbox.network.deniedDomains`, `skippedMarketplaces`, `skippedPlugins`, `pluginConfigs` — 仍不在官方文档中 | ✋ ON HOLD (保留在报告中待验证 — 从 2026-03-05 重复) |
| 10 | LOW | 缺失环境变量 | 将 `CLAUDE_CODE_SUBAGENT_MODEL` 添加到环境变量表 (已在模型环境示例块中但表中缺失) | ✅ COMPLETE (已添加到环境变量表) |
| 11 | LOW | 示例更新 | 更新快速参考示例以包含 `modelOverrides` 和修正后的 `$schema` URL | ✅ COMPLETE (示例已更新两者) |

---

## [2026-03-14 01:35 AM PKT] Claude Code v2.1.75

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 设置层级 | 重构以匹配官方 5 级层级: 管理 (#1) > CLI 参数 > 本地 > 项目 > 用户。移除 `~/.claude/settings.local.json` 行。添加管理层内部优先级 (服务器管理 > MDM > 文件 > HKCU)。注明管理"不能被任何其他级别覆盖, 包括 CLI 参数" | ✅ COMPLETE (表已重构为 5 级并将管理设为 #1, 添加了交付方法、内部优先级和文件路径) |
| 2 | HIGH | 行为变更 | 修复 `availableModels` 描述: 从复杂对象数组 (`title`/`modelId`/`effortOptions`) 改为简单字符串数组 `["sonnet", "haiku"]` (根据官方文档) | ✅ COMPLETE (描述已更新以匹配官方文档格式) |
| 3 | HIGH | 行为变更 | 添加 `cleanupPeriodDays` 的 `0` 值行为: "设置为 `0` 会在启动时删除所有现有转录并完全禁用会话持久化" | ✅ COMPLETE (0 值行为已添加到描述) |
| 4 | HIGH | 权限语法 | 在权限部分添加评估顺序说明: "规则按顺序评估: 拒绝规则优先, 然后询问, 然后允许。第一条匹配的规则获胜。" | ✅ COMPLETE (已在 Bash 通配符说明之前添加评估顺序) |
| 5 | MED | 描述变更 | 添加 `autoMemoryDirectory` 范围限制: "不接受在项目设置 (`.claude/settings.json`) 中。可从策略、本地和用户设置中接受。" | ✅ COMPLETE (范围限制已添加到描述) |
| 6 | MED | 描述变更 | 添加 `permissions.defaultMode` 的远程环境说明: 在远程环境中仅 `acceptEdits` 和 `plan` 受支持 (v2.1.70) | ✅ COMPLETE (远程限制已添加到描述) |
| 7 | MED | 模型配置 | 添加 Opus 4.6 1M 上下文默认说明: 自 v2.1.75 起, 1M 上下文是 Max/Team/Enterprise 计划的默认配置 | ✅ COMPLETE (已添加到努力级别说明) |
| 8 | MED | 设置层级 | 添加 Windows 管理路径说明: v2.1.75 移除了已弃用的 `C:\ProgramData\ClaudeCode\` 回退 — 使用 `C:\Program Files\ClaudeCode\managed-settings.json` | ✅ COMPLETE (已在层级部分添加弃用说明) |
| 9 | MED | 显示与用户体验 | 添加 `fileSuggestion` 标准输入 JSON 格式 (`{"query": "..."}`) 和 15 路径输出限制细节 | ✅ COMPLETE (标准输入格式和输出限制已添加到文件建议部分) |
| 10 | MED | 设置层级 | 根据官方文档将数组合并说明从"合并"更新为"连接并去重" | ✅ COMPLETE (层级重要部分的措辞已更新) |
| 11 | LOW | 可疑键 | `sandbox.ignoreViolations`, `sandbox.network.deniedDomains` 仍不在官方文档或 JSON 模式顶层 | ✋ ON HOLD (保留在报告中待验证 — 从 2026-03-05 重复) |
| 12 | LOW | 可疑键 | `skipWebFetchPreflight`, `skippedMarketplaces`, `skippedPlugins`, `pluginConfigs` — 在 JSON 模式中已确认但不在官方设置页面上 | ✋ ON HOLD (保留在报告中 — 根据模式有效, 从 2026-03-05 重复) |

---

## [2026-03-15 12:52 PM PKT] Claude Code v2.1.76

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 新设置 | 在通用设置或模型配置中添加 `effortLevel` — 跨会话持久化努力级别 (`"low"`, `"medium"`, `"high"`)。已在官方设置页面确认 | ✋ ON HOLD (等待用户批准) |
| 2 | HIGH | 新设置 | 添加工作树设置部分, 包含 `worktree.sparsePaths` (数组, 稀疏检出锥模式) 和 `worktree.symlinkDirectories` (数组, 符号链接目录以避免重复)。已在官方设置页面确认 | ✋ ON HOLD (等待用户批准) |
| 3 | HIGH | 新设置 | 在通用设置中添加 `feedbackSurveyRate` — 会话质量调查的概率 (0-1)。已在官方设置页面确认 | ✋ ON HOLD (等待用户批准) |
| 4 | HIGH | 缺失环境变量 | 向表添加 20 个缺失环境变量: `CLAUDE_CODE_AUTO_COMPACT_WINDOW`, `CLAUDE_CODE_ENABLE_PROMPT_SUGGESTION`, `CLAUDE_CODE_PLAN_MODE_REQUIRED`, `CLAUDE_CODE_TEAM_NAME`, `CLAUDE_CODE_TASK_LIST_ID`, `CLAUDE_ENV_FILE`, `FORCE_AUTOUPDATE_PLUGINS`, `HTTP_PROXY`, `HTTPS_PROXY`, `NO_PROXY`, `MCP_TOOL_TIMEOUT`, `MCP_CLIENT_SECRET`, `MCP_OAUTH_CALLBACK_PORT`, `IS_DEMO`, `SLASH_COMMAND_TOOL_CHAR_BUDGET`, `VERTEX_REGION_CLAUDE_3_5_HAIKU`, `VERTEX_REGION_CLAUDE_3_7_SONNET`, `VERTEX_REGION_CLAUDE_4_0_OPUS`, `VERTEX_REGION_CLAUDE_4_0_SONNET`, `VERTEX_REGION_CLAUDE_4_1_OPUS`。已在官方 /en/env-vars 页面确认 | ✋ ON HOLD (等待用户批准) |
| 5 | HIGH | 缺失环境变量 | 将 `ANTHROPIC_DEFAULT_OPUS_MODEL`, `ANTHROPIC_DEFAULT_SONNET_MODEL`, `MAX_THINKING_TOKENS` 从仅代码块移至通用环境变量表 | ✋ ON HOLD (等待用户批准) |
| 6 | HIGH | 损坏链接 | 修复 `https://claudelog.com/configuration/` — 返回 ECONNREFUSED。删除或替换为可用的来源 | ✋ ON HOLD (等待用户批准) |
| 7 | MED | 描述变更 | 更新 `cleanupPeriodDays` 描述以添加: 设置为 0 时"钩子接收空的 `transcript_path`"。根据官方文档 | ✋ ON HOLD (等待用户批准) |
| 8 | MED | 未验证环境变量 | 将报告中但不在官方文档中的 7 个环境变量标记为未验证: `CLAUDE_CODE_DISABLE_MCP`, `CLAUDE_CODE_DISABLE_TOOLS`, `CLAUDE_CODE_HIDE_ACCOUNT_INFO`, `CLAUDE_CODE_MAX_TURNS`, `CLAUDE_CODE_PROMPT_CACHING_ENABLED`, `CLAUDE_CODE_SKIP_SETTINGS_SETUP`, `DISABLE_NON_ESSENTIAL_MODEL_CALLS` | ✋ ON HOLD (等待用户批准) |
| 9 | MED | 新来源 | 将 `https://code.claude.com/docs/en/env-vars` 添加到来源部分 — 官方环境变量参考页面 | ✋ ON HOLD (等待用户批准) |
| 10 | MED | 示例更新 | 更新快速参考示例以包含 `effortLevel` 和 `worktree` 设置 | ✋ ON HOLD (等待用户批准) |
| 11 | LOW | 可疑键 | `sandbox.ignoreViolations`, `sandbox.network.deniedDomains` 仍不在官方文档沙箱表中 | ✋ ON HOLD (保留在报告中待验证 — 从 2026-03-05 重复) |
| 12 | LOW | 可疑键 | `skipWebFetchPreflight`, `skippedMarketplaces`, `skippedPlugins`, `pluginConfigs` — 仍在 JSON 模式中但不在官方设置页面上 | ✋ ON HOLD (保留在报告中 — 根据模式有效, 从 2026-03-05 重复) |

---

## [2026-03-15 01:10 PM PKT] Claude Code v2.1.76

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 新设置 | 在模型配置中添加 `effortLevel` — 跨会话持久化努力级别 (`"low"`, `"medium"`, `"high"`)。同时将 `/effort` 命令添加到有用命令并更新努力级别操作指南部分 | ✅ COMPLETE (已添加到模型覆盖表, 更新了操作指南, 添加了 /effort 命令) |
| 2 | HIGH | 新设置 | 添加工作树设置部分, 包含 `worktree.sparsePaths` (数组, 稀疏检出锥模式) 和 `worktree.symlinkDirectories` (数组, 符号链接目录以避免重复) | ✅ COMPLETE (核心配置中新增工作树设置子部分, 包含表和示例) |
| 3 | HIGH | 新设置 | 在通用设置中添加 `feedbackSurveyRate` — 会话质量调查的概率 (0-1) | ✅ COMPLETE (已添加到通用设置表) |
| 4 | HIGH | 缺失环境变量 | 向表添加 23 个缺失环境变量 (20 个全新 + 3 个来自仅代码块) | ✅ COMPLETE (所有 23 个环境变量已添加到通用环境变量表) |
| 5 | HIGH | 损坏链接 | 先前运行标记 `https://claudelog.com/configuration/` 为 ECONNREFUSED — 现在成功加载 | ✅ COMPLETE (链接已恢复, 无需操作) |
| 6 | MED | 权限语法 | 添加读取/编辑 gitignore 风格路径模式 (`//path`, `~/path`, `/path`, `./path`), 词边界通配符细节, 和遗留 `:*` 弃用说明 | ✅ COMPLETE (路径模式表、词边界说明和 `:*` 弃用已添加) |
| 7 | MED | 描述变更 | 更新 `cleanupPeriodDays` 以添加设置为 0 时"钩子接收空的 `transcript_path`" | ✅ COMPLETE (已添加到描述) |
| 8 | MED | 未验证环境变量 | 将不在官方文档中的 7 个环境变量标记为未验证 | ✅ COMPLETE (已添加"不在官方文档中 — 未验证"标记) |
| 9 | MED | 新来源 | 将 `https://code.claude.com/docs/en/env-vars` 和 `https://code.claude.com/docs/en/permissions` 添加到来源部分 | ✅ COMPLETE (两个 URL 已添加) |
| 10 | MED | 示例更新 | 更新快速参考示例以包含 `effortLevel` 和 `worktree` 设置 | ✅ COMPLETE (effortLevel 和 worktree 块已添加到示例) |
| 11 | LOW | 可疑键 | `sandbox.ignoreViolations`, `sandbox.network.deniedDomains` 仍不在官方文档沙箱表中 | ✋ ON HOLD (保留在报告中待验证 — 从 2026-03-05 重复) |
| 12 | LOW | 可疑键 | `skipWebFetchPreflight`, `skippedMarketplaces`, `skippedPlugins`, `pluginConfigs` — 仍在 JSON 模式中但不在官方设置页面上 | ✋ ON HOLD (保留在报告中 — 根据模式有效, 从 2026-03-05 重复) |

---

## [2026-03-17 12:54 PM PKT] Claude Code v2.1.77

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 新设置 | 在沙箱设置表中添加 `sandbox.filesystem.allowRead` — 在 `denyRead` 区域内重新允许读取访问 (数组, 默认 `[]`)。在 v2.1.77 更新日志中确认 | ✅ COMPLETE (已在沙箱设置表中添加于 denyRead 行之后) |
| 2 | HIGH | 描述变更 | 更新 `CLAUDE_CODE_MAX_OUTPUT_TOKENS` 描述: Opus 4.6 默认值增加到 64k, Opus 4.6 和 Sonnet 4.6 的上限增加到 128k (v2.1.77 更新日志) | ✅ COMPLETE (描述已更新, 包含模型特定默认值和边界) |
| 3 | HIGH | 缺失环境变量 | 在通用环境变量表中添加 `CLAUDECODE` — 在生成的 shell 环境中设置为 `1`。已在官方 /en/env-vars 页面确认 | ✅ COMPLETE (已添加到环境变量表) |
| 4 | HIGH | 缺失环境变量 | 在通用环境变量表中添加 `CLAUDE_CODE_SKIP_FAST_MODE_NETWORK_ERRORS` — 允许在组织状态检查失败时使用快速模式。已在官方 /en/env-vars 页面确认 | ✅ COMPLETE (已添加到环境变量表) |
| 5 | MED | 环境变量表 | 将 `ANTHROPIC_MODEL` 和 `ANTHROPIC_DEFAULT_HAIKU_MODEL` 从仅代码块移至通用环境变量表。两者均在官方 /en/env-vars 页面确认 | ✅ COMPLETE (两者已添加到其他 ANTHROPIC_ 变量附近的环境变量表) |
| 6 | MED | 可疑键升级 | `sandbox.network.deniedDomains` — 连续 8 次 ON HOLD 运行 (自 2026-03-05)。不在官方文档页面或 JSON 模式中。根据规则 10B: 标记为"不在官方文档中 — 未验证" | ✅ COMPLETE (未验证标注已添加到描述) |
| 7 | MED | 可疑键升级 | `allow_remote_sessions` — 不在官方文档页面或 JSON 模式中。标记为"不在官方文档中 — 未验证" | ✅ COMPLETE (未验证标注已添加到描述) |
| 8 | LOW | 可疑键解决 | `sandbox.ignoreViolations` — 连续 8 次 ON HOLD 运行。在 JSON 模式中确认。标注: "在 JSON 模式中, 不在官方设置页面上" | ✅ COMPLETE (模式标注已添加到描述) |
| 9 | LOW | 可疑键解决 | `skipWebFetchPreflight`, `skippedMarketplaces`, `skippedPlugins`, `pluginConfigs` — 连续 8 次 ON HOLD 运行。均在 JSON 模式中确认。标注: "在 JSON 模式中, 不在官方设置页面上" | ✅ COMPLETE (模式标注已添加到所有 4 个描述) |
| 10 | LOW | 表头计数 | 更新表头环境变量计数从"160+"到"100+" — 实际表中有 97 个环境变量 | ✅ COMPLETE (表头已更新为"100+ 环境变量", 版本为 v2.1.77) |

---

## [2026-03-18 11:53 PM PKT] Claude Code v2.1.78

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 缺失设置 | 在通用设置表中添加 `voiceEnabled` — 启用即按即说语音听写 (布尔值, 由 `/voice` 写入, 需要 Claude.ai 账户)。已在官方设置页面确认 | ✅ COMPLETE (已在通用设置表中添加于 feedbackSurveyRate 之前) |
| 2 | HIGH | 缺失设置 | 在沙箱设置表中添加 `filesystem.allowManagedReadPathsOnly` — 仅管理, 仅受管的 `allowRead` 路径被尊重 (布尔值, 默认 false)。已在官方设置页面确认 | ✅ COMPLETE (已在沙箱设置表中添加于 enableWeakerNetworkIsolation 之前) |
| 3 | HIGH | 显示位置 | 将 `showTurnDuration` 和 `terminalProgressBarEnabled` 从显示设置表移至单独的"全局配置设置 (~/.claude.json)"子部分。官方文档说明:"将它们添加到 settings.json 会触发模式验证错误" | ✅ COMPLETE (已创建新的子部分及表; 从 settings.json 显示设置表和示例中移除) |
| 4 | HIGH | 默认值变更 | 修复 `MAX_MCP_OUTPUT_TOKENS` 默认值从 50000 到 25000。官方 /en/env-vars 页面确认默认值: 25000 | ✅ COMPLETE (默认值已更新, 添加了警告阈值说明) |
| 5 | HIGH | 缺失环境变量 | 向环境变量表添加 `CLAUDE_CODE_NEW_INIT`, `CLAUDE_CODE_PLUGIN_SEED_DIR`, `DISABLE_FEEDBACK_COMMAND`。均在官方 /en/env-vars 页面确认 | ✅ COMPLETE (所有 3 个环境变量已添加到表) |
| 6 | MED | 验证修复 | 从 `allow_remote_sessions` 移除"未验证"标注 — 现在在官方权限页面上确认为仅管理设置。先前运行 (v2.1.77 #7) 错误地标记为未验证 | ✅ COMPLETE ("未验证"标注已移除) |
| 7 | MED | 环境变量重命名 | 更新 `DISABLE_BUG_COMMAND` 为 `DISABLE_FEEDBACK_COMMAND` — 官方文档说 `DISABLE_FEEDBACK_COMMAND` 是当前名称, `DISABLE_BUG_COMMAND` 是"旧名称" | ✅ COMPLETE (已重命名并添加别名说明) |
| 8 | MED | 描述变更 | 更新 `CLAUDE_CODE_EFFORT_LEVEL` 以包含 `max` (仅 Opus 4.6) 和 `auto` 值。官方 /en/env-vars 页面确认:"值: low, medium, high, max (仅 Opus 4.6), 或 auto" | ✅ COMPLETE (描述已更新, 包含所有值和优先级说明) |
| 9 | MED | 描述变更 | 修复 `CLAUDE_CODE_ENABLE_TASKS` 描述 — 官方:"设置为 true 以在非交互模式 (-p 标志) 下启用任务跟踪。任务在交互模式下默认启用。"报告当前显示"设置为 false 以禁用" | ✅ COMPLETE (描述已更正以匹配官方文档) |
| 10 | MED | 描述变更 | 更新 `CLAUDE_CODE_DISABLE_NONESSENTIAL_TRAFFIC` 以注明:"等同于设置 DISABLE_AUTOUPDATER, DISABLE_FEEDBACK_COMMAND, DISABLE_ERROR_REPORTING 和 DISABLE_TELEMETRY" | ✅ COMPLETE (描述已更新, 包含等效变量列表) |
| 11 | MED | 示例更新 | 从快速参考示例中移除 `showTurnDuration` — 根据官方文档不属于 settings.json | ✅ COMPLETE (已从快速参考示例和显示与用户体验示例中移除) |
| 12 | LOW | 环境变量默认值 | 验证 `MCP_TIMEOUT` 默认值 (报告说 10000) — 官方文档未指定默认值 | ✅ COMPLETE (未验证的默认值已移除 — 官方文档省略了它) |

---

## [2026-03-19 12:38 PM PKT] Claude Code v2.1.79

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 缺失环境变量 | 在通用环境变量表中添加 `ANTHROPIC_CUSTOM_MODEL_OPTION`, `ANTHROPIC_CUSTOM_MODEL_OPTION_NAME`, `ANTHROPIC_CUSTOM_MODEL_OPTION_DESCRIPTION` — 用于向 `/model` 选择器添加自定义条目的模型配置变量。已在官方 /en/env-vars 页面确认 | ✅ COMPLETE (3 个环境变量已在表中添加于 ANTHROPIC_BASE_URL 之后) |
| 2 | HIGH | 描述变更 | 更新 `CLAUDE_CODE_PLUGIN_SEED_DIR` 从单数到复数:"指向一个或多个只读插件种子目录的路径, 在 Unix 上以 `:` 分隔, 在 Windows 上以 `;` 分隔"。在 v2.1.79 更新日志中更改。已在官方 /en/env-vars 页面确认 | ✅ COMPLETE (描述已更新为多目录支持) |
| 3 | HIGH | 沙箱路径前缀 | 修复 sandbox.filesystem 路径前缀文档: `/` = 绝对路径 (标准 Unix), `./` = 项目相对路径, `//` = 旧版仍可工作。报告当前显示相反的约定。官方文档明确说明:"此语法不同于读取和编辑权限规则" | ✅ COMPLETE (所有 4 个 sandbox.filesystem 条目已更新为正确的前缀约定, 添加了对读取/编辑权限规则的交叉引用说明, 添加了跨作用域合并细节) |
| 4 | MED | 描述变更 | 扩展 `CLAUDE_CODE_AUTO_COMPACT_WINDOW` 描述 — 当前"自动压缩窗口行为配置"过于简略。官方文档描述了: 令牌容量、默认值 (200K 标准 / 1M 扩展)、与 `CLAUDE_AUTOCOMPACT_PCT_OVERRIDE` 的交互、状态行解耦 | ✅ COMPLETE (描述已扩展, 包含令牌容量、模型默认值、AUTOCOMPACT_PCT 交互和状态行解耦) |

---

## [2026-03-20 08:41 AM PKT] Claude Code v2.1.80

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 新设置 | 在 MCP 设置表中添加 `channelsEnabled` — 仅管理布尔值, 控制团队和企业用户的消息渠道传递。已在官方设置页面确认 | ✅ COMPLETE (已在 MCP 设置表中添加于 allowManagedMcpServersOnly 之后) |
| 2 | MED | 版本徽章 | 将报告版本从 v2.1.79 更新为 v2.1.80 | ✅ COMPLETE (徽章和表头已更新) |

---

## [2026-03-21 09:17 PM PKT] Claude Code v2.1.81

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 缺失设置 (~/.claude.json) | 在全局配置设置表中添加 `autoConnectIde` (布尔值, 默认 `false`) 和 `autoInstallIdeExtension` (布尔值, 默认 `true`)。已在官方设置页面"全局配置设置"下确认 | ✅ COMPLETE (两个键已添加到 ~/.claude.json 表中 showTurnDuration 之前) |
| 2 | HIGH | 错误设置 | `allow_remote_sessions` 在权限键表中列为仅管理布尔值, 但官方权限页面说明:"远程控制和网络会话的访问不由管理设置键控制。"标记为未验证或移除 | ✅ COMPLETE (已重新添加未验证标注, 包含官方文档引用和管理 UI 链接) |
| 3 | MED | 版本升级 | 将报告版本徽章从 v2.1.80 更新为 v2.1.81 | ✅ COMPLETE (徽章、表头版本和表头文本已更新) |
| 4 | MED | 新设置 | 添加 `showClearContextOnPlanAccept` — 在 v2.1.81 更新日志中确认。当为 `true` 时, 恢复计划接受上的"清除上下文"选项 (默认隐藏)。尚未在官方设置页面上 — 可能是一个 `~/.claude.json` 键 | ✅ COMPLETE (已添加到全局配置设置表, 附带更新日志来源说明) |
| 5 | MED | 插件文档 | 在插件设置部分记录 `source: 'settings'` 作为市场来源类型。官方设置页面将其列为 `extraKnownMarkets` 的 7 种来源类型之一 | ✅ COMPLETE (所有 7 种来源类型列表已添加, 内联市场示例) |
| 6 | MED | 状态行字段 | 在状态行输入字段表中添加 `rate_limits` 字段组 — 包括 `five_hour.used_percentage`, `five_hour.resets_at`, `seven_day.used_percentage`, `seven_day.resets_at`。在 v2.1.80 中添加 | ✅ COMPLETE (4 个 rate_limits 字段已添加到状态行输入字段表) |

---

## [2026-03-23 10:02 PM PKT] Claude Code v2.1.81

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 缺失设置 (~/.claude.json) | 在全局配置设置表中添加 `editorMode` (字符串, 默认 `"normal"`, 值: `"normal"` 或 `"vim"`)。运行 `/vim` 时自动写入。已在官方设置页面确认 | ✅ COMPLETE (已在全局配置设置表中添加于 autoInstallIdeExtension 之后) |
| 2 | HIGH | 文件范围修复 | 将 `showClearContextOnPlanAccept` 从全局配置设置 (~/.claude.json) 移至通用设置 (settings.json)。官方文档现在将其列在主可用设置表中, 而非全局配置表中。移除过时的"尚未在官方设置页面上"标注 | ✅ COMPLETE (已移至通用设置表中 feedbackSurveyRate 之前, 移除了过时标注) |
| 3 | MED | 描述变更 | 修复 `terminalProgressBarEnabled` 受支持的终端从"Windows 终端、iTerm2"到"ConEmu、Ghostty 1.2.0+ 和 iTerm2 3.6.6+" (根据官方文档) | ✅ COMPLETE (终端列表已更新) |
| 4 | MED | 描述变更 | 在 `availableModels` 描述中添加"配置工具" — 官方文档说"通过 `/model`、`--model`、配置工具或 `ANTHROPIC_MODEL`"。报告当前省略了"配置工具" | ✅ COMPLETE ("配置工具"已添加到描述) |

---

## [2026-03-25 08:16 PM PKT] Claude Code v2.1.83

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 新设置 | 在权限部分添加 `autoMode` — 包含 `environment`、`allow`、`soft_deny` 数组的对象, 用于配置自动模式分类器。不从共享项目设置 (`.claude/settings.json`) 读取。在用户、本地和管理设置中可用。已在官方设置 + 权限页面确认 | ✅ COMPLETE (已添加到权限键表, 包含完整描述、范围限制和 `claude auto-mode defaults` 说明) |
| 2 | HIGH | 新设置 | 在权限部分添加 `disableAutoMode` — 字符串, 设置为 `"disable"` 以防止自动模式激活。从 Shift+Tab 循环中移除 `auto`。可在任何设置级别设置, 在管理设置中最有用。已在官方设置 + 权限页面确认 | ✅ COMPLETE (已在权限键表中添加于 `autoMode` 之后) |
| 3 | HIGH | 新权限模式 | 在权限模式表中添加 `auto` — 后台分类器取代手动提示。研究预览。需要 Team 计划 + Sonnet/Opus 4.6。已在官方权限模式页面确认 | ✅ COMPLETE (已添加到权限模式表, 包含分类器细节和回退行为) |
| 4 | HIGH | 新设置 | 在沙箱设置表中添加 `sandbox.failIfUnavailable` — 布尔值, 默认 `false`, 在沙箱已启用但无法启动时退出并显示错误, 而不是在无沙箱情况下运行。在 v2.1.83 更新日志中确认 | ✅ COMPLETE (已在沙箱设置表中添加于 `sandbox.enabled` 之后) |
| 5 | HIGH | 新设置 | 在通用设置表中添加 `disableDeepLinkRegistration` — 布尔值, 阻止 `claude-cli://` 协议处理器注册。在 v2.1.83 更新日志中确认 | ✅ COMPLETE (已在通用设置表中添加于 `feedbackSurveyRate` 之前) |
| 6 | HIGH | 缺失环境变量 | 在通用环境变量表中添加 `CLAUDE_CODE_SUBPROCESS_ENV_SCRUB` — 设置为 `1` 以从子进程环境 (Bash 工具、钩子、MCP stdio 服务器) 中剥离 Anthropic 和云提供商凭据。在 v2.1.83 更新日志中确认 | ✅ COMPLETE (已添加于 `CLAUDE_CODE_SUBAGENT_MODEL` 之后的环境变量表) |
| 7 | HIGH | 设置层级 | 在管理设置部分添加 `managed-settings.d/` 放置目录 — 与 `managed-settings.json` 并列的独立策略片段, 按字母顺序合并。在 v2.1.83 更新日志中确认 | ✅ COMPLETE (已作为管理设置交付方法下的项目符号添加) |
| 8 | HIGH | 损坏链接 | 修复来源中的 `https://claudelog.com/configuration/` — 返回 403 禁止访问。删除或替换为可用的来源 | ✅ COMPLETE (已替换为 `https://claudelog.com/claude-code-changelog/`, 经验证有效) |
| 9 | MED | 版本徽章 | 将报告版本从 v2.1.81 更新为 v2.1.83 | ✅ COMPLETE (徽章和表头已在阶段 2.6 中更新) |
| 10 | MED | 示例更新 | 在快速参考示例中添加 `autoMode` 以演示自动模式分类器配置 | ✅ COMPLETE (已在 `permissions` 块之前添加 `autoMode` 块及 `environment` 数组) |
| 11 | MED | 路径变更 | 修复 Windows 注册表路径从 `Software\Anthropic\ClaudeCode` 到 `SOFTWARE\Policies\ClaudeCode` (HKLM 和 HKCU)。官方文档已更新为使用 `Policies` 子键 | ✅ COMPLETE (已更新为 `HKLM\SOFTWARE\Policies\ClaudeCode` 和 `HKCU\SOFTWARE\Policies\ClaudeCode`, 附带优先级说明) |
| 12 | LOW | 缺失别名 | 在模型别名表中添加 `opus[1m]` — Opus 4.6 带 1M 上下文, 自 v2.1.75 起在 Max/Team/Enterprise 上默认可用 | ✅ COMPLETE (已在 `sonnet[1m]` 之后的模型别名表中添加) |

---

## [2026-03-26 01:04 PM PKT] Claude Code v2.1.84

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 新设置 | 在通用设置中添加 `defaultShell` — 字符串, 默认 `"bash"`, 接受 `"bash"` 或 `"powershell"`。在 Windows 上通过 PowerShell 路由交互式 `!` 命令。需要 `CLAUDE_CODE_USE_POWERSHELL_TOOL=1`。已在官方设置页面确认 | ✅ COMPLETE (已在通用设置表中添加于 teammateMode 之后) |
| 2 | HIGH | 新设置 | 在 MCP 设置中添加 `allowedChannelPlugins` — 数组, 仅管理。可推送消息的渠道插件的允许列表。设置后替换默认的 Anthropic 允许列表。需要 `channelsEnabled: true`。已在官方设置页面确认 | ✅ COMPLETE (已在 MCP 设置表中添加于 channelsEnabled 之后) |
| 3 | HIGH | 新设置 | 在权限键中添加 `useAutoModeDuringPlan` — 布尔值, 默认 `true`。当自动模式可用时, 计划模式使用自动模式语义。不从共享项目设置读取。已在官方设置页面确认 | ✅ COMPLETE (已在权限键表中添加于 disableAutoMode 之后) |
| 4 | HIGH | 缺失环境变量 | 添加 9 个模型自定义环境变量: `ANTHROPIC_DEFAULT_{OPUS,SONNET,HAIKU}_MODEL_{NAME,DESCRIPTION,SUPPORTED_CAPABILITIES}` 用于 Bedrock/Vertex/Foundry 上的 `/model` 选择器自定义。已在官方 /en/env-vars 页面确认 | ✅ COMPLETE (每个基础模型变量后添加了 3 个变量: Haiku, Opus, Sonnet) |
| 5 | HIGH | 缺失环境变量 | 添加 `CLAUDE_CODE_DISABLE_NONSTREAMING_FALLBACK` — 在流式传输失败时禁用非流式回退。防止通过代理重复执行工具。已在官方 /en/env-vars 页面确认 (在 v2.1.83 中添加, 先前运行中遗漏) | ✅ COMPLETE (已添加于 CLAUDE_CODE_DISABLE_FAST_MODE 之后) |
| 6 | HIGH | 缺失环境变量 | 添加 `CLAUDE_CODE_USE_POWERSHELL_TOOL` — 在 Windows 上启用 PowerShell 工具 (选择加入预览)。仅限原生 Windows, 非 WSL。已在官方 /en/env-vars 页面确认 | ✅ COMPLETE (已添加于 CLAUDE_CODE_USE_FOUNDRY 之后) |
| 7 | HIGH | 损坏链接 | 修复来源中的 `https://claudelog.com/claude-code-changelog/` — 返回 403 禁止访问。替换为官方 GitHub 更新日志 URL | ✅ COMPLETE (已替换为 github.com/anthropics/claude-code/blob/main/CHANGELOG.md) |
| 8 | MED | 设置层级 | 更新管理层优先级:"基于文件 (`managed-settings.d/*.json` + `managed-settings.json`)"并添加"跨层级"限定语。根据官方文档添加层级内合并说明 | ✅ COMPLETE (优先级描述已更新, 包含基于文件的层级和跨层级限定语) |
| 9 | MED | 设置层级 | 扩展放置目录合并语义: systemd 约定、标量覆盖、数组连接并去重、深度合并、隐藏文件排除、数字前缀提示。根据官方设置页面 | ✅ COMPLETE (已扩展, 包含完整的 systemd 约定细节和数字前缀提示) |
| 10 | MED | 标注 | 根据规则 1F 逆向完整性检查, 为 `disableDeepLinkRegistration` 添加"在更新日志中, 不在官方设置页面上"标注 | ✅ COMPLETE (标注已添加到描述) |
| 11 | MED | 示例更新 | 在快速参考示例中添加 `defaultShell` 以演示 PowerShell 配置 | ✅ COMPLETE (已向示例添加 "defaultShell": "bash") |

---

## [2026-03-27 06:32 PM PKT] Claude Code v2.1.85

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 缺失环境变量 | 在通用环境变量表中添加 `CLAUDE_STREAM_IDLE_TIMEOUT_MS` — 空闲看门狗关闭停滞连接前超时毫秒数 (默认: 90000)。已在官方 /en/env-vars 页面确认。在 v2.1.84 中添加但在先前运行中遗漏 | ✅ COMPLETE (已在 CLAUDE_CODE_OTEL_HEADERS_HELPER_DEBOUNCE_MS 之后的环境变量表中添加) |
| 2 | HIGH | 版本升级 | 将报告版本徽章从 v2.1.84 更新为 v2.1.85 | ✅ COMPLETE (徽章、表头版本和表头文本已在阶段 2.6 中更新) |
| 3 | MED | 新环境变量 | 向环境变量表添加 `OTEL_LOG_TOOL_DETAILS` — 控制 OpenTelemetry 事件中的 `tool_parameters`。仅 v2.1.85 更新日志 (尚未在官方 env-vars 页面上)。附带更新日志来源标注添加 | ✅ COMPLETE (已添加, 附带"在 v2.1.85 更新日志中, 尚未在官方 env-vars 页面上"标注) |
| 4 | MED | 新环境变量 (归属) | 决定 `CLAUDE_CODE_MCP_SERVER_NAME` 和 `CLAUDE_CODE_MCP_SERVER_URL` 的归属 — 传递给 MCP `headersHelper` 脚本的环境变量 (v2.1.85 更新日志)。可能属于钩子仓库而非设置报告 | ✅ COMPLETE (已添加到设置报告, 附带更新日志标注 — 这些变量可通过 `env` 键进行环境配置, 非仅限钩子) |

---

## [2026-03-28 06:10 PM PKT] Claude Code v2.1.86

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 文件范围 | 将 `teammateMode` 从通用设置 (settings.json) 移至全局配置设置 (~/.claude.json)。官方设置页面将其列在"全局配置设置"下 — 添加到 settings.json 会触发模式验证错误 (规则 1H)。与 v2.1.78 `showTurnDuration` 修复相同模式 | ✅ COMPLETE (已从通用设置表移除, 添加到全局配置设置表中 terminalProgressBarEnabled 之后, 附带代理团队文档链接) |
| 2 | HIGH | 类型 + 标注 | 修复 `disableDeepLinkRegistration`: 将类型从 `boolean` 改为 `string` (值: `"disable"`), 更新描述以匹配官方文档, 移除过时的"(在更新日志中, 不在官方设置页面上)"标注。现在在官方设置页面 (第 169 行) 确认 | ✅ COMPLETE (类型已改为字符串, 描述已更新以匹配官方文档, 更新日志标注已移除) |
| 3 | HIGH | 版本升级 | 将报告版本徽章从 v2.1.85 更新为 v2.1.86 | ✅ COMPLETE (徽章和表头已在阶段 2.6 中更新) |

---

## [2026-03-31 07:02 PM PKT] Claude Code v2.1.88

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 缺失环境变量 | 在通用环境变量表中添加 `CLAUDE_CODE_NO_FLICKER` — 启用无闪烁备屏渲染 (v2.1.88)。已在官方 /en/env-vars 页面确认 | ✅ COMPLETE (已添加于 CLAUDE_CODE_DISABLE_TERMINAL_TITLE 之后) |
| 2 | HIGH | 缺失环境变量 | 在通用环境变量表中添加 `CLAUDE_CODE_SCROLL_SPEED` 和 `CLAUDE_CODE_DISABLE_MOUSE` — 全屏 UI 控制。已在官方 /en/env-vars 页面确认 | ✅ COMPLETE (已添加于 CLAUDE_CODE_NO_FLICKER 之后) |
| 3 | HIGH | 版本升级 | 将报告版本徽章从 v2.1.86 更新为 v2.1.88 | ✅ COMPLETE (徽章、表头版本和表头文本已在阶段 2.6 中更新) |
| 4 | HIGH | 损坏链接 | 修复来源中的 `https://www.eesel.ai/blog/settings-json-claude-code` — 返回仅 CSS 内容, 无可读博客文章 | ✅ COMPLETE (已从来源部分移除损坏链接) |
| 5 | MED | 设置层级 | 向基于文件的管理交付方法添加 `managed-mcp.json` — 官方设置页面将其与 `managed-settings.json` 并列列出, 用于 MCP 服务器配置 | ✅ COMPLETE (已添加到设置层级中文件交付方法项目符号) |
| 6 | MED | 插件来源类型 | 将 `url`, `npm`, `file` 市场来源类型标注为"不在官方文档中 — 未验证" (仅 `github`, `git`, `directory`, `hostPattern`, `settings` 已确认) | ✅ COMPLETE (未验证标注已添加到所有 3 个来源类型) |
| 7 | LOW | 表头计数 | 更新表头从"60+ 设置"以匹配任何添加后的实际表计数 | ❌ INVALID (计数准确 — 60+ 设置和 125 个环境变量, 均在所述范围内) |

---

## [2026-04-01 12:32 PM PKT] Claude Code v2.1.89

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 缺失设置 | 在权限键表中添加 `skipDangerousModePermissionPrompt` — 布尔值, 跳过绕过模式确认提示。在项目设置中被忽略。已在官方设置页面确认 | ✅ COMPLETE (已在权限键表中添加于 disableBypassPermissionsMode 之后) |
| 2 | HIGH | 新设置 | 在通用设置中添加 `showThinkingSummaries` — 布尔值, 默认 `false`。思考摘要默认不再生成; 设置为 `true` 以恢复。v2.1.89 更新日志 — 尚未在官方设置页面上 | ✅ COMPLETE (已在 feedbackSurveyRate 之前添加, 附带更新日志标注) |
| 3 | HIGH | 行为变更 | 更新 `cleanupPeriodDays` 描述 — v2.1.89 更新日志说 `0` 现在被拒绝, 并显示验证错误。矛盾: 官方设置页面仍将 `0` 描述为有效。向用户标记 | ✅ COMPLETE (描述已更新, 附带更新日志与文档页面之间的矛盾说明) |
| 4 | HIGH | 缺失环境变量 | 添加在官方 /en/env-vars 页面确认的约 46 个缺失环境变量: `ANTHROPIC_BEDROCK_BASE_URL`, `ANTHROPIC_VERTEX_BASE_URL`, `ANTHROPIC_BETAS`, `ANTHROPIC_VERTEX_PROJECT_ID`, `CLAUDE_CODE_DISABLE_THINKING`, `DISABLE_INTERLEAVED_THINKING`, `ENABLE_PROMPT_CACHING_1H_BEDROCK`, `DISABLE_AUTO_COMPACT`, `DISABLE_COMPACT`, `CLAUDE_CODE_DISABLE_FILE_CHECKPOINTING`, `CLAUDE_CODE_DISABLE_ATTACHMENTS`, `CLAUDE_CODE_DISABLE_CLAUDE_MDS`, `CLAUDE_CODE_GLOB_HIDDEN`, `CLAUDE_CODE_GLOB_NO_IGNORE`, `CLAUDE_CODE_GLOB_TIMEOUT_SECONDS`, `CLAUDE_CODE_DISABLE_OFFICIAL_MARKETPLACE_AUTOINSTALL`, `CLAUDE_CODE_SYNC_PLUGIN_INSTALL`, `CLAUDE_CODE_SYNC_PLUGIN_INSTALL_TIMEOUT_MS`, `CLAUDE_CODE_AUTO_CONNECT_IDE`, `CLAUDE_CODE_IDE_HOST_OVERRIDE`, `CLAUDE_CODE_IDE_SKIP_VALID_CHECK`, `CLAUDE_CODE_MAX_RETRIES`, `API_TIMEOUT_MS`, `CLAUDE_CODE_OTEL_FLUSH_TIMEOUT_MS`, `CLAUDE_CODE_OTEL_SHUTDOWN_TIMEOUT_MS`, `CLAUDE_ENABLE_STREAM_WATCHDOG`, `CLAUDE_CODE_ENABLE_FINE_GRAINED_TOOL_STREAMING`, `CLAUDE_CODE_DEBUG_LOGS_DIR`, `CLAUDE_CODE_DEBUG_LOG_LEVEL`, `CLAUDE_CODE_ACCESSIBILITY`, `CLAUDE_CODE_SYNTAX_HIGHLIGHT`, `CLAUDE_CODE_RESUME_INTERRUPTED_TURN`, `CLAUDE_CODE_MAX_TOOL_USE_CONCURRENCY`, `CLAUDE_CODE_DISABLE_LEGACY_MODEL_REMAP`, `FALLBACK_FOR_ALL_PRIMARY_MODELS`, `CLAUDE_CODE_GIT_BASH_PATH`, `CLAUDE_AUTO_BACKGROUND_TASKS`, `CLAUDE_AGENT_SDK_DISABLE_BUILTIN_AGENTS`, `CLAUDE_AGENT_SDK_MCP_NO_PREFIX`, `DISABLE_DOCTOR_COMMAND`, `DISABLE_LOGIN_COMMAND`, `DISABLE_LOGOUT_COMMAND`, `DISABLE_UPGRADE_COMMAND`, `DISABLE_EXTRA_USAGE_COMMAND`, `DISABLE_INSTALL_GITHUB_APP_COMMAND`, `CLAUDE_CODE_PLUGIN_CACHE_DIR`, `CLAUDE_CODE_SIMPLE` | ✅ COMPLETE (所有 46 个环境变量已添加到表中相关变量附近) |
| 5 | HIGH | 版本升级 | 将报告版本徽章从 v2.1.88 更新为 v2.1.89 | ✅ COMPLETE (徽章和表头已在阶段 2.6 中更新) |
| 6 | MED | 新环境变量 | 向环境变量表添加 `MCP_CONNECTION_NONBLOCKING` — 在 `-p` 模式下设置为 `true` 以跳过 MCP 连接等待。仅 v2.1.89 更新日志, 尚未在官方 /en/env-vars 页面上 | ✅ COMPLETE (已添加于 CLAUDE_AGENT_SDK_MCP_NO_PREFIX 之后, 附带更新日志标注) |
| 7 | MED | 归属边界 | `CLAUDE_CODE_SIMPLE` 在 CLI 启动标志文件中作为仅启动项, 但官方 /en/env-vars 页面将其列为可配置。协调归属 | ✅ COMPLETE (已添加到设置报告环境表; CLI 文件已更新以交叉引用设置报告) |
| 8 | MED | 示例更新 | 如果添加了 `showThinkingSummaries`, 更新快速参考示例以包含 | ✅ COMPLETE (已向示例添加 showThinkingSummaries: true) |

---

## [2026-04-02 09:24 PM PKT] Claude Code v2.1.90

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 类型+描述变更 | 修复 `forceLoginOrgUUID`: 类型从 `string` 改为 `string \| string[]`。扩展描述以包含数组行为 (任何列出的组织无需预选即可接受)、管理设置执行 (如果不属于列出的组织则登录失败) 和空数组失败关闭行为 | ✅ COMPLETE (类型已更新为 string \| array, 描述已扩展包含数组行为、管理执行、失败关闭语义, 示例已更新) |
| 2 | HIGH | 缺失环境变量 | 在通用环境变量表中添加 `CLAUDE_CODE_OAUTH_TOKEN`, `CLAUDE_CODE_OAUTH_REFRESH_TOKEN`, `CLAUDE_CODE_OAUTH_SCOPES`。均在官方 /en/env-vars 页面确认 | ✅ COMPLETE (3 个 OAuth 环境变量已添加于 ANTHROPIC_AUTH_TOKEN 之后) |
| 3 | HIGH | 描述+标注变更 | 更新 `showThinkingSummaries`: 移除"(在 v2.1.89 更新日志中, 尚未在官方设置页面上)"标注 — 现在在官方设置页面上确认。更新描述以匹配官方:"当未设置或为 false (交互模式下的默认值) 时, 思考块被 API 编辑并显示为折叠的存根。编辑仅改变您看到的内容, 而非模型生成的内容" | ✅ COMPLETE (标注已移除, 描述已更新以匹配官方文档) |
| 4 | HIGH | 沙箱交叉合并 | 更新 `sandbox.filesystem.allowWrite` 描述以添加"还与来自 `Edit(...)` 允许权限规则的路径合并"。更新 `denyWrite` 以添加"还与来自 `Edit(...)` 拒绝权限规则的路径合并"。更新 `denyRead` 以添加"还与来自 `Read(...)` 拒绝权限规则的路径合并"。已在官方设置页面确认 | ✅ COMPLETE (交叉合并行为已添加到所有 3 个文件系统条目) |
| 5 | HIGH | 描述变更 | 简化 `cleanupPeriodDays` 描述: 移除矛盾说明, 与官方文档对齐, 现在官方说"最小值为 1, 设置为 0 会被拒绝并显示验证错误"。旧行为不再在官方页面上记录 | ✅ COMPLETE (矛盾说明已移除, 描述已与官方文档对齐, 添加了 --no-session-persistence 替代方案) |
| 6 | HIGH | 版本升级 | 将报告版本徽章从 v2.1.89 更新为 v2.1.90 | ✅ COMPLETE (徽章、表头版本和表头文本已更新) |
| 7 | MED | 新环境变量 | 向环境变量表添加 `CLAUDE_CODE_PLUGIN_KEEP_MARKETPLACE_ON_FAILURE` — 在 git 拉取失败时保留市场缓存 (v2.1.90 更新日志, 尚未在官方 /en/env-vars 页面上) | ✅ COMPLETE (已添加于 CLAUDE_CODE_SYNC_PLUGIN_INSTALL_TIMEOUT_MS 之后, 附带更新日志标注) |
| 8 | MED | 钩子重定向计数 | 根据官方钩子页面计数, 将重定向文本从"所有 19 个钩子事件"更新为"所有 25 个钩子事件" | ✅ COMPLETE (钩子重定向部分中的计数已更新) |
| 9 | MED | 归属边界 | `CLAUDE_CODE_TMPDIR` 在官方 /en/env-vars 页面上列为可通过 `env` 键配置, 但 CLI 启动标志报告将其列为仅启动项。协调归属 | ✅ COMPLETE (已添加到设置报告环境表; CLI 标志文件已更新以交叉引用设置报告) |

---

## [2026-04-03 08:44 PM PKT] Claude Code v2.1.91

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 新设置 | 在通用设置表中添加 `disableSkillShellExecution` — 布尔值, 禁用技能、自定义斜杠命令和插件命令中的内联 shell 执行。在 v2.1.91 更新日志中确认。尚未在官方设置页面或 JSON 模式中 | ✅ COMPLETE (已在 showThinkingSummaries 之后添加, 附带更新日志标注) |
| 2 | HIGH | 版本升级 | 将报告版本徽章从 v2.1.90 更新为 v2.1.91 | ✅ COMPLETE (徽章和表头已在阶段 2.6 中更新) |

---

## [2026-04-04 10:48 PM PKT] Claude Code v2.1.92

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 新设置 | 在通用设置中添加 `forceRemoteSettingsRefresh` — 布尔值, 仅管理, 阻止 CLI 启动直到远程管理设置被新鲜获取 (失败关闭)。已在官方设置页面确认 | ✅ COMPLETE (已在通用设置表中添加于 feedbackSurveyRate 之前) |
| 2 | HIGH | 缺失环境变量 | 在通用环境变量表中添加 `CLAUDE_REMOTE_CONTROL_SESSION_NAME_PREFIX` — 自动生成的远程控制会话名称的前缀, 默认为机器主机名。已在官方 /en/env-vars 页面确认 | ✅ COMPLETE (已添加于 CLAUDE_CODE_ENABLE_TELEMETRY 之前) |
| 3 | MED | 描述变更 | 更新 `disableSkillShellExecution` — 移除"(在 v2.1.91 更新日志中, 尚未在官方设置页面上)"标注。现在在官方设置页面上确认, 描述已扩展 | ✅ COMPLETE (标注已移除, 描述已根据官方文档扩展) |
| 4 | MED | 描述变更 | 从市场来源类型 `url`, `npm` 和 `file` 中移除"不在官方文档中 — 未验证"标签。官方设置页面现在记录了所有 8 种来源类型 | ✅ COMPLETE (未验证标注已移除 — 从 2026-03-31 重复, 现已解决) |
| 5 | MED | 描述变更 | 丰富 `cleanupPeriodDays` — 添加"同时控制启动时自动移除孤立子代理工作树的年龄截止值" (根据官方设置页面) | ✅ COMPLETE (工作树清理细节已添加) |
| 6 | MED | 描述变更 | 丰富 `disableDeepLinkRegistration` — 根据官方设置页面添加通过 `%0A` 的多行提示支持 | ✅ COMPLETE (多行提示细节已添加) |
| 7 | MED | 描述变更 | 丰富 `includeGitInstructions` — 更新以包含 git 状态快照和环境变量优先级 (根据官方设置页面) | ✅ COMPLETE (描述已扩展, 包含 git 状态快照和 CLAUDE_CODE_DISABLE_GIT_INSTRUCTIONS 优先级) |
| 8 | MED | 描述变更 | 丰富 `language` — 根据官方设置页面添加"也设置语音听写语言" | ✅ COMPLETE (语音听写细节已添加) |
| 9 | MED | 描述变更 | 丰富 `allowUnsandboxedCommands` — 根据官方设置页面添加企业策略细节 | ✅ COMPLETE (已扩展, 包含失败关闭行为和企业用例) |

---

## [2026-04-08 09:51 PM PKT] Claude Code v2.1.96

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 缺失环境变量 | 在通用环境变量表中添加 `CLAUDE_CODE_USE_MANTLE`, `ANTHROPIC_BEDROCK_MANTLE_BASE_URL`, `CLAUDE_CODE_SKIP_MANTLE_AUTH` — Bedrock Mantle 端点支持 (v2.1.94)。均在官方 /en/env-vars 页面确认 | ✅ COMPLETE (已添加在相关云提供商变量附近) |
| 2 | HIGH | 默认值变更 | 更新努力级别部分 — 默认值从中改为高, 适用于 API 密钥、Bedrock/Vertex/Foundry、Team 和企业用户 (v2.1.94)。更新表默认标记和历史说明 | ✅ COMPLETE (表已更新高为默认值, 历史说明已扩展包含 v2.1.94 更改) |
| 3 | HIGH | 版本升级 | 将报告版本徽章从 v2.1.92 更新为 v2.1.96 | ✅ COMPLETE (徽章、表头版本和表头文本已在阶段 2.6 中更新) |
| 4 | MED | 过时标注 | 从 `CLAUDE_CODE_PLUGIN_KEEP_MARKETPLACE_ON_FAILURE` 移除"(在 v2.1.90 更新日志中, 尚未在官方 env-vars 页面上)" — 现在在官方 /en/env-vars 页面上确认。更新描述以匹配官方措辞 | ✅ COMPLETE (标注已移除, 描述已根据官方文档更新) |
| 5 | MED | 描述变更 | 更新 `CLAUDE_CODE_GLOB_HIDDEN` 描述以匹配官方:"设置为 `false` 以从 Glob 结果中排除点文件。默认包含。不影响 `@` 文件自动补全、`ls`、Grep 或 Read" | ✅ COMPLETE (描述已根据官方 env-vars 页面重写) |

---

## [2026-04-09 11:39 PM PKT] Claude Code v2.1.97

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 新设置 | 在沙箱设置表中添加 `sandbox.network.allowMachLookup` — 数组, 仅 macOS, XPC/Mach 服务名支持尾部 `*` 通配符。已在官方设置页面确认 | ✅ COMPLETE (已在沙箱网络子键中添加于 allowManagedDomainsOnly 之后) |
| 2 | HIGH | 显示与用户体验 | 在状态行配置部分添加 `refreshInterval` 字段 — 可选, 每 N 秒重新运行命令, 最小 1 (v2.1.97)。已在官方状态行文档确认 | ✅ COMPLETE (已与 `padding` 字段一起添加到配置表, JSON 示例已更新) |
| 3 | HIGH | 显示与用户体验 | 将状态行输入字段表从 9 个扩展到 30+ 个字段以匹配官方状态行文档。添加 `model.*`, `workspace.*`, `cost.*`, `session_id`, `session_name`, `transcript_path`, `version`, `output_style.name`, `vim.mode`, `agent.name`, `worktree.*` 字段 | ✅ COMPLETE (已根据官方状态行文档从 9 个扩展到 30 个字段) |
| 4 | HIGH | 版本升级 | 将报告版本徽章从 v2.1.96 更新为 v2.1.97 | ✅ COMPLETE (徽章和表头已在阶段 2.6 中更新) |
| 5 | MED | 字段命名 | 在状态行输入字段表中修复 `current_usage` → `context_window.current_usage` | ✅ COMPLETE (已重命名, 包含完整路径和扩展描述) |
| 6 | MED | 归属边界 | 将 `CCR_FORCE_BUNDLE` 添加到 `claude-cli-startup-flags.md` — 用于 `claude --remote` 捆绑的仅启动变量。在官方 /en/env-vars 页面上但不在任一文件中 | ✅ COMPLETE (已添加到 CLI 启动标志环境变量表) |
| 7 | MED | 描述变更 | 更新 `CLAUDE_CODE_GLOB_NO_IGNORE` 描述以匹配官方:"设置为 `false` 以使 Glob 工具尊重 `.gitignore` 模式。默认情况下, Glob 返回所有匹配文件, 包括被 git 忽略的文件。不影响 `@` 文件自动补全" | ✅ COMPLETE (描述已根据官方 env-vars 页面重写) |
| 8 | MED | 描述变更 | 更新 `editorMode` 描述 — 移除过时的 `/vim` 引用 (在 v2.1.94 中移除), 将配置标签从"键绑定模式"改为"编辑器模式" (根据官方文档) | ✅ COMPLETE (/vim 引用已移除, 配置标签已更新) |

---

## [2026-04-13 08:10 PM PKT] Claude Code v2.1.101

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 缺失环境变量 | 在通用环境变量表中添加 `CLAUDE_CODE_CERT_STORE` — 逗号分隔的 CA 证书来源, 用于 TLS (`bundled`, `system`)。默认值: `bundled,system`。需要原生二进制才能使用系统存储。v2.1.101。已在官方 /en/env-vars 页面确认 | ✅ COMPLETE (已添加于 CLAUDE_CODE_CLIENT_KEY_PASSPHRASE 之后) |
| 2 | HIGH | 缺失环境变量 | 在通用环境变量表中添加 `CLAUDE_CODE_PERFORCE_MODE` — 设置为 `1` 以启用 Perforce 感知的写入保护。如果目标文件缺少所有者写入位, Edit/Write/NotebookEdit 会失败并显示 `p4 edit` 提示。v2.1.98。已在官方 /en/env-vars 页面确认 | ✅ COMPLETE (已添加于 CLAUDE_CODE_SCRIPT_CAPS 之后) |
| 3 | HIGH | 缺失环境变量 | 在通用环境变量表中添加 `CLAUDE_CODE_SCRIPT_CAPS` — JSON 对象, 限制当 `CLAUDE_CODE_SUBPROCESS_ENV_SCRUB` 已设置时每个会话的脚本调用计数。键是与命令文本匹配的子字符串; 值是整数调用限制。已在官方 /en/env-vars 页面确认 | ✅ COMPLETE (已添加于 CLAUDE_CODE_SUBPROCESS_ENV_SCRUB 之后) |
| 4 | HIGH | 版本升级 | 将报告版本徽章从 v2.1.97 更新为 v2.1.101 | ✅ COMPLETE (徽章、表头版本和表头文本已在阶段 2.6 中更新) |
| 5 | MED | 描述变更 | 更新 `disableSkillShellExecution` — 添加 ` ```! ` (三重反引号 shell) 块语法和"来自用户、项目、插件或额外目录来源"限定语 (根据官方设置页面) | ✅ COMPLETE (描述已根据官方文档扩展) |
| 6 | MED | 归属边界 | 将 `DISABLE_AUTOUPDATER` 添加到设置报告环境变量表 — 在官方 /en/env-vars 页面上列为可通过 `env` 键配置, 当前仅在 CLI 启动标志文件中。添加对 CLI 标志文件的交叉引用 | ✅ COMPLETE (已添加到设置报告 DISABLE_TELEMETRY 之前; CLI 标志文件已更新交叉引用) |

---

## [2026-04-14 11:22 PM PKT] Claude Code v2.1.107

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 新设置 | 在通用设置表中添加 `viewMode` — 字符串, 值 `"default"`, `"verbose"`, `"focus"`。启动时的默认转录视图模式, 覆盖粘性 Ctrl+O 选择。已在官方设置页面确认 | ✅ COMPLETE (已在通用设置中添加于 showClearContextOnPlanAccept 之后) |
| 2 | HIGH | 缺失环境变量 | 添加 5 个在官方 /en/env-vars 页面确认的缺失环境变量: `ANTHROPIC_CUSTOM_MODEL_OPTION_SUPPORTED_CAPABILITIES`, `CLAUDE_CODE_DISABLE_VIRTUAL_SCROLL`, `CLAUDE_ENABLE_BYTE_WATCHDOG`, `CLAUDE_CODE_MAX_CONTEXT_TOKENS`, `CLAUDE_CODE_SKIP_PROMPT_HISTORY` | ✅ COMPLETE (已添加在环境表中相关变量附近) |
| 3 | HIGH | 描述变更 | 更新 `disableAllHooks` 描述 — 根据官方设置页面第 180 行添加"和任何自定义状态行" | ✅ COMPLETE (已在钩子重定向部分内联更新) |
| 4 | HIGH | 默认值变更 | 在全局配置设置表中修复 `teammateMode` 默认值从 `"in-process"` 到 `"auto"`。官方文档将 `auto` 描述为主要行为。在 v2.1.86 文件范围移动期间发生回归 | ✅ COMPLETE (默认值已更新为 "auto" — 从 2026-03-07 重复, 自 v2.1.86 移动回归) |
| 5 | MED | 描述变更 | 更新 `CLAUDE_STREAM_IDLE_TIMEOUT_MS` 描述 — 区分字节看门狗 (默认/最小 300000ms) 和事件看门狗 (默认 90000ms)。根据官方 /en/env-vars 页面 | ✅ COMPLETE (描述已扩展, 包含双重看门狗细节和 CLAUDE_ENABLE_BYTE_WATCHDOG 交叉引用) |
| 6 | MED | 标注修复 | 从 `CLAUDE_CODE_GIT_BASH_PATH` 移除"(仅启动)" — 官方 /en/env-vars 页面将其列为可环境配置 | ✅ COMPLETE (描述已根据官方文档重写, 仅启动标注已移除) |
| 7 | MED | 示例更新 | 在 `showThinkingSummaries` 之后向快速参考示例添加 `viewMode` | ✅ COMPLETE (已向示例添加 "viewMode": "default") |
| 8 | MED | 过时标注 | `OTEL_LOG_TOOL_DETAILS` 仍标记为"在 v2.1.85 更新日志中, 尚未在官方 env-vars 页面上" — 经 10+ 版本和 7 次连续运行确认仍不在官方页面上 | ✋ ON HOLD (标注准确 — 保持现状, 等待官方文档更新) |
| 7 | MED | 归属边界 | 将 `CCR_FORCE_BUNDLE` 添加到设置报告环境变量表 — 在官方 /en/env-vars 页面上列为可通过 `env` 键配置, 当前仅在 CLI 启动标志文件中。添加对 CLI 标志文件的交叉引用 | ✅ COMPLETE (已添加到设置报告 CLAUDE_CODE_GIT_BASH_PATH 之前; CLI 标志文件已更新交叉引用) |

---

## [2026-04-16 08:25 PM PKT] Claude Code v2.1.110

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 缺失设置 | 在通用设置表中添加 `minimumVersion` — 字符串, 阻止自动更新器降级到特定版本以下。已在官方设置页面确认 | ✅ COMPLETE (已在通用设置表中添加于 autoUpdatesChannel 之后) |
| 2 | HIGH | 缺失环境变量 | 在通用环境变量表中添加 `CLAUDE_CODE_TMUX_TRUECOLOR` — 设置为 `1` 以允许 tmux 内的 24 位真彩色输出。已在官方 /en/env-vars 页面确认 | ✅ COMPLETE (已添加于 CLAUDE_CODE_NO_FLICKER 之前) |
| 3 | HIGH | 缺失环境变量 | 在通用环境变量表中添加 `CLAUDE_CODE_REMOTE` — 只读, 在云会话中设置为 `true`。已在官方 /en/env-vars 页面确认 | ✅ COMPLETE (已添加于 CLAUDE_REMOTE_CONTROL_SESSION_NAME_PREFIX 之前) |
| 4 | HIGH | 缺失环境变量 | 在通用环境变量表中添加 `CLAUDE_CODE_REMOTE_SESSION_ID` — 只读, 云会话 ID。已在官方 /en/env-vars 页面确认 | ✅ COMPLETE (已添加于 CLAUDE_REMOTE_CONTROL_SESSION_NAME_PREFIX 之前) |
| 5 | HIGH | 逆向环境变量检查 | 将 `ENABLE_PROMPT_CACHING_1H_BEDROCK` 标记为"不在官方文档中 — 未验证"。不再在官方 /en/env-vars 页面上。根据规则 5D | ✅ COMPLETE (已添加未验证标注和弃用说明) |
| 6 | MED | 新设置 (更新日志) | 在通用设置中添加 `autoScrollEnabled` — 布尔值, 在全屏模式下禁用对话自动滚动。仅 v2.1.110 更新日志, 尚未在官方设置页面上 | ✅ COMPLETE (已在 feedbackSurveyRate 之前添加, 附带更新日志标注) |
| 7 | MED | 新设置 (更新日志) | 在通用设置中添加 `tui` — 无闪烁渲染模式的设置 (`/tui fullscreen`)。仅 v2.1.110 更新日志, 尚未在官方设置页面上 | ✅ COMPLETE (已在 feedbackSurveyRate 之前添加, 附带更新日志标注) |
| 8 | MED | 新环境变量 (更新日志) | 向环境变量表添加 `ENABLE_PROMPT_CACHING_1H` — 1 小时提示缓存 TTL (替换已弃用的 `ENABLE_PROMPT_CACHING_1H_BEDROCK`)。仅 v2.1.108 更新日志, 尚未在官方 /en/env-vars 页面上 | ✅ COMPLETE (已在 DISABLE_PROMPT_CACHING 之前添加, 附带更新日志标注) |
| 9 | MED | 新环境变量 (更新日志) | 向环境变量表添加 `FORCE_PROMPT_CACHING_5M` — 强制 5 分钟 TTL。仅 v2.1.108 更新日志, 尚未在官方 /en/env-vars 页面上 | ✅ COMPLETE (已在 DISABLE_PROMPT_CACHING 之前添加, 附带更新日志标注) |
| 10 | MED | 努力级别表 | 向努力级别表添加 `Max` 行 — 仅 Opus 4.6, 在环境变量中有记录但表里缺失 | ✅ COMPLETE (已作为努力级别表第一行添加) |
| 11 | MED | 沙箱描述 | 添加平台特定说明: `allowUnixSockets` (仅 macOS), `allowAllUnixSockets` (Linux/WSL2 细节), `enableWeakerNestedSandbox` (仅 Linux/WSL2) | ✅ COMPLETE (所有 3 个描述已根据官方文档更新, 附带平台特定说明) |
| 12 | LOW | 仅更新日志环境变量 | 考虑添加 `CLAUDE_CODE_ENABLE_AWAY_SUMMARY` (v2.1.108), `OTEL_LOG_USER_PROMPTS` (v2.1.101), `OTEL_LOG_TOOL_CONTENT` (v2.1.101) — 均为仅更新日志, 不在官方 env-vars 页面上。根据规则 8A 推迟, 直到官方文档确认 | ✋ ON HOLD (已推迟 — 仅更新日志, 未获官方文档确认) |

---

## [2026-04-18 07:56 PM PKT] Claude Code v2.1.114

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 版本升级 | 将报告版本徽章从 v2.1.110 更新为 v2.1.114, 表头"截至 v2.1.110" → "截至 v2.1.114" | ✅ COMPLETE (徽章和表头文本已更新) |
| 2 | HIGH | 新设置 | 在通用设置表中添加 `awaySummaryEnabled` — 布尔值, 控制是否生成空闲会话回顾 ("离开摘要")。已在官方设置页面确认。与 `CLAUDE_CODE_ENABLE_AWAY_SUMMARY` 环境变量配对 | ✅ COMPLETE (已在通用设置表中添加于 `tui` 和 `feedbackSurveyRate` 之间, 附带配对说明) |
| 3 | HIGH | 缺失环境变量 | 在通用环境变量表中添加 `CLAUDE_CODE_ENABLE_AWAY_SUMMARY` — 退出选择加入离开摘要/会话回顾。已在官方 /en/env-vars 页面确认 | ✅ COMPLETE (已添加于 `FORCE_PROMPT_CACHING_5M` 之后 — 周期性解决, 首次出现于 2026-04-16) |
| 4 | HIGH | 缺失值 | 在 `effortLevel` 有效值 (第 497 行) 中添加 `xhigh` — v2.1.111 为 Opus 4.7 引入了 `xhigh`。当前仅列出 `"low"`, `"medium"`, `"high"` | ✅ COMPLETE (描述已更新, 包含 `"xhigh"` 值、Opus 4.7 支持和回退行为) |
| 5 | HIGH | 努力级别表 | 在努力级别表中添加 `xhigh` 行 (位于 Max 和 High 之间) — 仅 Opus 4.7, 在 v2.1.111 中引入 | ✅ COMPLETE (XHigh 行已添加; 默认标记已更新为"Opus 4.6/Sonnet 4.6 上的默认值"; 说明部分已扩展, 包含 v2.1.111 中 Opus 4.7 上 xhigh 的默认设置) |
| 6 | HIGH | 文件范围移动 | 将 `autoScrollEnabled` 从通用设置 (第 88 行) 移至全局配置设置 (`~/.claude.json`) 表 — 官方文档将其列为 `~/.claude.json` 键, 非 `settings.json`。默认 `true`。根据规则 1H。添加到 settings.json 可能触发模式验证错误 | ✅ COMPLETE (已从通用设置中移除, 添加到全局配置设置表中 `autoInstallIdeExtension` 和 `editorMode` 之间, 默认值 `true`) |
| 7 | HIGH | 过时标注 | 从 `tui` 描述 (第 89 行) 移除"(在 v2.1.110 更新日志中, 尚未在官方设置页面上)" — 现在有官方文档记录。根据官方文档更新描述: `"fullscreen"` 或 `"default"` | ✅ COMPLETE (标注已移除, 描述已更新, 包含值和 v2.1.110 引用) |
| 8 | HIGH | 新设置 | 在全局配置设置 (`~/.claude.json`) 表中添加 `externalEditorContext` — 在官方设置页面"全局配置设置"部分确认。根据规则 1A | ✅ COMPLETE (已在全局配置设置表中添加于 `editorMode` 之后, 默认值 `true`) |
| 9 | HIGH | 过时标注 | 从 `sandbox.network.deniedDomains` (第 388 行) 移除"(不在官方文档中 — 未验证)" — 在 v2.1.113 更新日志中正式添加。根据官方文档更新描述 (优先于 `allowedDomains`)。根据规则 10B, 连续 11 次 ON HOLD 运行后解除阻塞 | ✅ COMPLETE (标注已移除, 描述已重写, 包含优先级和 glob 支持说明 — 周期性解决, 首次出现于 2026-03-05) |
| 10 | MED | 示例更新 | 更新快速参考示例 (第 938–1023 行) 以包含 `awaySummaryEnabled`, `tui: "fullscreen"` 和 `effortLevel: "xhigh"`, 以展示 v2.1.111–v2.1.114 的添加内容 | ✅ COMPLETE (所有 3 个键已添加到示例; `effortLevel` 从 `"medium"` 提升到 `"xhigh"`) |
