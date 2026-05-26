# 更新日志 — README CONCEPTS 章节

追踪 README CONCEPTS 表与官方 Claude Code 文档之间的差异。

## 状态图例

| 状态 | 含义 |
|--------|---------|
| ✅ `COMPLETE (reason)` | 已采取措施并成功解决 |
| ❌ `INVALID (reason)` | 发现不正确、不适用或有意为之 |
| ✋ `ON HOLD (reason)` | 操作已推迟 — 等待外部依赖或用户决定 |

---

## [2026-03-02 11:14 PKT] Claude Code v2.1.63

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | URL 失效 | 修复权限 URL 从 `/iam` 到 `/permissions` | ✅ COMPLETE（URL 已更新为 /permissions） |
| 2 | 高 | 缺失概念 | 向 CONCEPTS 表添加代理团队行 | ✅ COMPLETE（已添加行，位置为 ~\/\.claude\/teams\/） |
| 3 | 高 | 缺失概念 | 向 CONCEPTS 表添加键绑定行 | ✅ COMPLETE（已添加行，位置为 ~\/\.claude\/keybindings\.json） |
| 4 | 高 | 缺失概念 | 向 CONCEPTS 表添加模型配置行 | ✅ COMPLETE（已添加行，位置为 \.claude\/settings\.json） |
| 5 | 高 | 缺失概念 | 向 CONCEPTS 表添加自动记忆行 | ✅ COMPLETE（已添加行，位置为 ~\/\.claude\/projects\/<project>\/memory\/） |
| 6 | 高 | 锚点过时 | 修复规则 URL 锚点从 `#modular-rules-with-clauderules` 到 `#organize-rules-with-clauderules` | ✅ COMPLETE（锚点已更新） |
| 7 | 中 | 缺失概念 | 向 CONCEPTS 表添加检查点行 | ✅ COMPLETE（已添加行，位置为自动的基于 git 的） |
| 8 | 中 | 缺失概念 | 向 CONCEPTS 表添加状态行行 | ✅ COMPLETE（已添加行，位置为 ~\/\.claude\/settings\.json） |
| 9 | 中 | 缺失概念 | 向 CONCEPTS 表添加远程控制行 | ✅ COMPLETE（已添加行，位置为 CLI \/ claude\.ai） |
| 10 | 中 | 缺失概念 | 向 CONCEPTS 表添加快速模式行 | ✅ COMPLETE（已添加行，位置为 \.claude\/settings\.json） |
| 11 | 中 | 缺失概念 | 向 CONCEPTS 表添加无头模式行 | ✅ COMPLETE（已添加行，位置为 CLI 标志 -p） |
| 12 | 低 | 描述变更 | 更新记忆描述以提及自动记忆 | ✅ COMPLETE（描述和位置已更新） |
| 13 | 低 | 位置变更 | 更新 MCP 服务器位置以包含 `.mcp.json` | ✅ COMPLETE（位置已更新以包含 .mcp.json） |
| 14 | 低 | 缺失徽章 | 向钩子行添加已实现徽章 | ✅ COMPLETE（已添加指向 .claude/hooks/ 的已实现徽章） |

---

## [2026-03-02 11:57 PKT] Claude Code v2.1.63

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 表整合 | 将 CONCEPTS 表从 22 行整合为 10 行 — 将相关概念折叠为内联文档链接 | ✅ COMPLETE（22 → 10 行） |
| 2 | 中 | 合并概念 | 将市场折叠到插件行作为内联链接 | ✅ COMPLETE（已链接到 /discover-plugins） |
| 3 | 中 | 合并概念 | 将代理团队折叠到子代理行作为内联链接 | ✅ COMPLETE（已链接到 /agent-teams） |
| 4 | 中 | 合并概念 | 将权限、模型配置、输出样式、沙箱、键绑定、状态行、快速模式折叠到设置行作为内联链接 | ✅ COMPLETE（7 个概念已折叠并附文档链接） |
| 5 | 中 | 合并概念 | 将自动记忆和规则折叠到记忆行作为内联链接 | ✅ COMPLETE（已链接到 /memory 和 /memory#organize-rules-with-clauderules） |
| 6 | 中 | 合并概念 | 将无头模式折叠到远程控制行作为内联链接 | ✅ COMPLETE（已链接到 /headless） |
| 7 | 低 | 重新排序 | 按逻辑分组重新排序表：构建块 → 扩展 → 配置 → 上下文 → 运行时 | ✅ COMPLETE（按关注领域分组，而非时间顺序） |

---

## [2026-03-07 08:40 PKT] Claude Code v2.1.71

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | URL 失效 | 修复 TIPS 中的 `context-management` → `interactive-mode`（第 112、115、135 行） | ✅ COMPLETE（已替换 3 处为 interactive-mode） |
| 2 | 高 | URL 失效 | 修复 TIPS 中的 `model-configuration` → `model-config`（第 115、116、135 行） | ✅ COMPLETE（已替换 3 处为 model-config） |
| 3 | 高 | URL 失效 | 修复 TIPS 中的 `usage-billing` → `costs`（第 115 行） | ✅ COMPLETE（已替换为 costs） |
| 4 | 高 | URL 失效 | 移除 STARTUPS 中的 `cowork` URL（第 167 行）— 页面不存在 | ✅ COMPLETE（超链接已移除，纯文本保留） |
| 5 | 高 | 缺失概念 | 向 CONCEPTS 和 Hot 章节添加计划任务行（`/loop`、cron 工具） | ✅ COMPLETE（用户已添加到两个表 + /loop 提示 + Boris 推文） |
| 6 | 中 | 位置变更 | 更新代理团队位置从 `.claude/agents/<name>.md` 为 `built-in (env var)` | ✅ COMPLETE（位置已更新为内置环境变量） |

---

## [2026-03-10 13:18 PKT] Claude Code v2.1.72

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | URL 失效 | 修复 CONCEPTS 表中的命令 URL 从 `/slash-commands` 到 `/skills`（第 24 行）— `/slash-commands` 提供技能页面内容；文档说"命令已合并到技能中" | ❌ INVALID（URL 仍可解析；用户选择保持原样） |
| 2 | 高 | URL 失效 | 修复 TIPS 章节中的命令 URL 从 `/slash-commands` 到 `/skills`（第 108 行）— 相同的过时 URL | ❌ INVALID（URL 仍可解析；用户选择保持原样） |
| 3 | 中 | 缺失内联链接 | 向 CLI 启动标志行添加交互模式（`/interactive-mode`）作为内联链接 — 涵盖 /compact、/clear、/context、/extra-usage | ✅ COMPLETE（内联链接已添加到 CLI 启动标志描述） |
| 4 | 中 | 缺失内联链接 | 向设置行添加成本（`/costs`）作为内联链接 — 涵盖 /usage、计费、按量付费 | ❌ INVALID（用户选择跳过） |
| 5 | 低 | 缺失概念 | 考虑添加 IDE 集成行（VS Code、JetBrains、桌面应用、Web）或内联链接到最佳实践 | ❌ INVALID（用户选择跳过 — 平台界面，非配置概念） |
| 6 | 高 | 缺失概念 | 向 Hot 表添加代码审查行 — 多代理 PR 分析（研究预览，团队和企业版） | ✅ COMPLETE（已添加为第一个 Hot 条目，含博客链接和最佳实践推文） |
| 7 | 中 | 新徽章 | 创建 `!/tags/beta.svg` 标签（黄色，38x20px）并添加到 Hot 表中的代码审查和代理团队 | ✅ COMPLETE（beta.svg 已创建；已添加到代码审查和代理团队行） |
| 8 | 中 | 重新排序 | 按发布日期对 Hot 表排序（最近优先）：代码审查 → 计划任务 → 语音模式 → 代理团队 → 远程控制 → Git Worktrees → Ralph Wiggum | ✅ COMPLETE（语音模式和代理团队已交换以匹配时间顺序） |

---

## [2026-03-12 12:22 PKT] Claude Code v2.1.74

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | URL 失效 | 修复 CONCEPTS 表中的命令 URL 从 `/slash-commands` 到 `/skills`（第 24 行）— `/slash-commands` 重定向到 `/skills` 页面 | ❌ INVALID（自 2026-03-10 起重复出现；URL 仍可解析；用户选择保持原样） |
| 2 | 低 | 验证 | 所有外部文档 URL 已验证 — 未发现损坏链接 | ✅ COMPLETE（所有 20+ 个 URL 返回有效页面） |
| 3 | 低 | 验证 | 所有本地徽章文件路径已验证 — 无缺失文件 | ✅ COMPLETE（所有徽章目标在文件系统上存在） |
| 4 | 低 | 验证 | 记忆锚点 `#organize-rules-with-clauderules` 已在目标页面上验证 | ✅ COMPLETE（标题在 /memory 页面上存在） |
| 5 | 低 | 验证 | 所有 CONCEPTS 描述已对照官方文档检查 | ✅ COMPLETE（未检测到描述漂移） |

---

## [2026-03-15 12:48 PKT] Claude Code v2.1.76

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | URL 过时 | 命令 URL `/slash-commands` 提供技能页面 — 文档说"命令已合并到技能中" | ❌ INVALID（自 2026-03-10 起重复出现；URL 仍可解析；用户选择保持原样） |
| 2 | 中 | 缺失徽章 | 远程控制（Hot）没有徽章 — 唯一没有 BP 或 Impl 徽章的 Hot 条目 | ✅ COMPLETE（BP 徽章已添加，链接到官方文档页面） |
| 3 | 低 | 命名 | README 中的"Sub-Agents"与官方文档中的"subagents"（一个词）— 外观上的不一致 | ✅ COMPLETE（已在 CONCEPTS 表中重命名为"Subagents"） |
| 4 | 低 | 验证 | 所有 27 个外部文档 URL 已验证 — 未发现损坏链接 | ✅ COMPLETE（所有 URL 返回有效页面） |
| 5 | 低 | 验证 | 所有本地徽章文件路径已验证 — 无缺失文件 | ✅ COMPLETE（所有徽章目标在文件系统上存在） |
| 6 | 低 | 验证 | 记忆锚点 `#organize-rules-with-clauderules` 已在 /memory 页面确认 | ✅ COMPLETE（章节标题存在） |
| 7 | 低 | 验证 | 所有 CONCEPTS 描述已对照官方文档检查 — 未检测到漂移 | ✅ COMPLETE（所有 13 个 CONCEPTS + 9 个 Hot 行的描述准确） |

---

## [2026-03-17 12:46 PKT] Claude Code v2.1.77

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | URL 过时 | 命令 URL `/slash-commands` 提供技能页面 — 文档说"命令已合并到技能中" | ❌ INVALID（自 2026-03-10 起重复出现；URL 仍可解析；用户选择保持原样） |
| 2 | 高 | 描述变更 | 钩子描述说"确定性脚本"但钩子现在包含 4 种类型：命令、HTTP、提示和代理 — 只有命令钩子是确定性的 | ✅ COMPLETE（已在 CONCEPTS 表中更新为"用户定义的处理程序（脚本、HTTP、提示、代理）"） |
| 3 | 中 | 缺失概念 | 桌面应用有专用文档页面在 `/desktop` — 不在 CONCEPTS 或 Hot 表中 | ❌ INVALID（用户选择跳过 — 桌面是平台界面，非配置概念） |
| 4 | 中 | URL 变更 | 钩子文档现已分为指南（`/hooks-guide`）和参考（`/hooks`）— CONCEPTS 仅链接到参考 | ✅ COMPLETE（指南链接已作为内联链接添加到钩子行描述中） |
| 5 | 低 | 验证 | 所有 28 个外部文档 URL 已验证 — 未发现损坏链接 | ✅ COMPLETE（所有 URL 返回有效页面，包括 /slash-commands 重定向） |
| 6 | 低 | 验证 | 所有本地徽章文件路径已验证 — 无缺失文件 | ✅ COMPLETE（所有 20 个徽章目标在文件系统上存在） |
| 7 | 低 | 验证 | 记忆锚点 `#organize-rules-with-clauderules` 已在 /memory 页面确认 | ✅ COMPLETE（章节标题存在） |
| 8 | 低 | 验证 | 所有 CONCEPTS 描述已对照官方文档检查 | ✅ COMPLETE（钩子描述漂移已检测到 — 见 #2） |

---

## [2026-03-18 23:43 PKT] Claude Code v2.1.78

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | URL 过时 | 命令 URL `/slash-commands` 提供技能页面 — 文档说"命令已合并到技能中" | ❌ INVALID（自 2026-03-10 起重复出现；URL 仍可解析；用户选择保持原样） |
| 2 | 高 | URL+名称变更 | Hot 表中的语音模式链接到推文而非官方文档 `/voice-dictation`；官方名称为"语音听写" | ✅ COMPLETE（已重命名为"语音听写"，链接到 /voice-dictation，描述已更新；BP 徽章保持链接到推文；也在 STARTUPS 表中更新） |
| 3 | 低 | 验证 | 所有 29 个外部文档 URL 已验证 — 未发现损坏链接 | ✅ COMPLETE（所有 URL 返回有效页面，包括 /slash-commands 重定向） |
| 4 | 低 | 验证 | 所有本地徽章文件路径已验证 — 无缺失文件 | ✅ COMPLETE（所有 20+ 个徽章目标在文件系统上存在） |
| 5 | 低 | 验证 | 记忆锚点 `#organize-rules-with-clauderules` 已在 /memory 页面确认 | ✅ COMPLETE（章节标题存在） |
| 6 | 低 | 验证 | 所有 CONCEPTS 描述已对照官方文档检查 — 未检测到漂移 | ✅ COMPLETE（所有描述准确） |

---

## [2026-03-19 11:59 PKT] Claude Code v2.1.79

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | URL 过时 | 命令 URL `/slash-commands` 提供技能页面 — 文档说"命令已合并到技能中" | ❌ INVALID（自 2026-03-10 起重复出现；URL 仍可解析；用户选择保持原样） |
| 2 | 低 | 验证 | 所有 30 个外部文档 URL 已验证 — 未发现损坏链接 | ✅ COMPLETE（所有 URL 返回有效页面，包括 /slash-commands 重定向） |
| 3 | 低 | 验证 | 所有本地徽章文件路径已验证 — 无缺失文件 | ✅ COMPLETE（所有 20+ 个徽章目标在文件系统上存在） |
| 4 | 低 | 验证 | 记忆锚点 `#organize-rules-with-clauderules` 已在 /memory 页面确认 | ✅ COMPLETE（章节标题存在） |
| 5 | 低 | 验证 | 所有 CONCEPTS 描述已对照官方文档检查 — 未检测到漂移 | ✅ COMPLETE（所有描述准确） |

---

## [2026-03-20 08:38 PKT] Claude Code v2.1.80

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 缺失概念 | 向 Hot 表添加频道行 — 从 Telegram/Discord/webhook 推送事件到正在运行的会话（研究预览，v2.1.80） | ✅ COMPLETE（已添加为第一个 Hot 条目，带 beta 徽章和参考链接） |
| 2 | 高 | URL 过时 | 命令 URL `/slash-commands` 提供技能页面 — 文档说"命令已合并到技能中" | ❌ INVALID（自 2026-03-10 起重复出现；URL 仍可解析；用户选择保持原样） |
| 3 | 中 | 缺失深度链接 | Git Worktrees URL 应锚定到 `#run-parallel-claude-code-sessions-with-git-worktrees` | ✅ COMPLETE（锚点已添加到 Hot 表中的 Git Worktrees URL） |
| 4 | 低 | 缺失内联链接 | 插件行可以添加 `[Marketplaces](https://code.claude.com/docs/en/plugin-marketplaces)` 子链接 | ✅ COMPLETE（创建市场内联链接已添加到插件行） |
| 5 | 低 | 验证 | 所有 31 个外部文档 URL 已验证 — 未发现损坏链接 | ✅ COMPLETE（所有 URL 返回有效页面，包括 /slash-commands 重定向） |
| 6 | 低 | 验证 | 所有本地徽章文件路径已验证 — 无缺失文件 | ✅ COMPLETE（所有 20+ 个徽章目标在文件系统上存在） |
| 7 | 低 | 验证 | 记忆锚点 `#organize-rules-with-clauderules` 已在 /memory 页面确认 | ✅ COMPLETE（章节标题存在） |
| 8 | 低 | 验证 | 所有 CONCEPTS 描述已对照官方文档检查 — 未检测到漂移 | ✅ COMPLETE（所有描述准确） |

---

## [2026-03-21 21:12 PKT] Claude Code v2.1.81

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | URL 过时 | 命令 URL `/slash-commands` 提供技能页面 — 文档说"命令已合并到技能中" | ❌ INVALID（自 2026-03-10 起重复出现；URL 仍可解析；用户选择保持原样） |
| 2 | 低 | 验证 | 所有 32 个外部文档 URL 已验证 — 未发现损坏链接 | ✅ COMPLETE（所有 URL 返回有效页面，包括 /slash-commands 重定向） |
| 3 | 低 | 验证 | 所有本地徽章文件路径已验证 — 无缺失文件 | ✅ COMPLETE（所有 20+ 个徽章目标在文件系统上存在） |
| 4 | 低 | 验证 | 记忆锚点 `#organize-rules-with-clauderules` 已在 /memory 页面确认 | ✅ COMPLETE（章节标题存在） |
| 5 | 低 | 验证 | Git Worktrees 锚点 `#run-parallel-claude-code-sessions-with-git-worktrees` 已在 /common-workflows 页面确认 | ✅ COMPLETE（章节标题存在） |
| 6 | 低 | 验证 | 所有 CONCEPTS 描述已对照官方文档检查 — 未检测到漂移 | ✅ COMPLETE（所有描述准确） |

---

## [2026-03-23 21:53 PKT] Claude Code v2.1.81

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | URL 过时 | 命令 URL `/slash-commands` 提供技能页面 — 文档说"命令已合并到技能中" | ❌ INVALID（自 2026-03-10 起重复出现；URL 仍可解析；用户选择保持原样） |
| 2 | 低 | 验证 | 所有 33 个外部文档 URL 已验证 — 未发现损坏链接 | ✅ COMPLETE（所有 URL 返回有效页面，包括 /slash-commands 重定向） |
| 3 | 低 | 验证 | 所有本地徽章文件路径已验证 — 无缺失文件 | ✅ COMPLETE（所有 20+ 个徽章目标在文件系统上存在） |
| 4 | 低 | 验证 | 记忆锚点 `#organize-rules-with-clauderules` 已在 /memory 页面确认 | ✅ COMPLETE（章节标题存在） |
| 5 | 低 | 验证 | Git Worktrees 锚点 `#run-parallel-claude-code-sessions-with-git-worktrees` 已在 /common-workflows 页面确认 | ✅ COMPLETE（章节标题存在） |
| 6 | 低 | 验证 | 所有 CONCEPTS 描述已对照官方文档检查 — 未检测到漂移 | ✅ COMPLETE（所有描述准确） |

---

## [2026-03-25 20:12 PKT] Claude Code v2.1.83

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | URL 过时 | 命令 URL `/slash-commands` 提供技能页面 — 文档说"命令已合并到技能中" | ❌ INVALID（自 2026-03-10 起重复出现；URL 仍可解析；用户选择保持原样） |
| 2 | 中 | URL 变更 | Simplify & Batch 的主链接指向推文而非官方文档 `/skills#bundled-skills` — 现已正式成为捆绑技能 | ✅ COMPLETE（主链接已更新为 /skills#bundled-skills；BP 徽章保持链接到 Boris 的推文） |
| 3 | 低 | 验证 | 所有 34 个外部文档 URL 已验证 — 未发现损坏链接 | ✅ COMPLETE（所有 URL 返回有效页面，包括 /slash-commands 重定向） |
| 4 | 低 | 验证 | 所有本地徽章文件路径已验证 — 无缺失文件 | ✅ COMPLETE（所有 20+ 个徽章目标在文件系统上存在） |
| 5 | 低 | 验证 | 记忆锚点 `#organize-rules-with-clauderules` 已在 /memory 页面确认 | ✅ COMPLETE（章节标题存在） |
| 6 | 低 | 验证 | Git Worktrees 锚点 `#run-parallel-claude-code-sessions-with-git-worktrees` 已在 /common-workflows 页面确认 | ✅ COMPLETE（章节标题存在） |
| 7 | 低 | 验证 | 所有 CONCEPTS 描述已对照官方文档检查 — 未检测到漂移 | ✅ COMPLETE（所有描述准确） |
| 8 | 高 | 缺失概念 | 向 Hot 表添加自动模式行 — 后台安全分类器替代权限提示（研究预览，团队/企业版） | ✅ COMPLETE（已添加为第一个 Hot 条目，带 beta 徽章、链接到 @claudeai 推文的 BP 徽章和博客链接） |

---

## [2026-03-26 13:05 PKT] Claude Code v2.1.84

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | URL 过时 | 命令 URL `/slash-commands` 提供技能页面 — 文档说"命令已合并到技能中" | ❌ INVALID（自 2026-03-10 起重复出现；URL 仍可解析；用户选择保持原样） |
| 2 | 中 | 缺失概念 | 向 Hot 表添加 Slack 集成 — 在 Slack 中 @Claude 将编码任务路由到 Claude Code Web 会话 | ✅ COMPLETE（已在频道后添加行，位置为 @Claude，并有 Web 会话描述） |
| 3 | 中 | 缺失概念 | 向 Hot 表添加 GitHub Actions / CI-CD — 在 CI/CD 流水线中自动化 PR 审查、问题分类和代码生成 | ✅ COMPLETE（已在代码审查后添加行，位置为 .github/workflows/，并有 GitLab CI/CD 内联链接） |
| 4 | 低 | 验证 | 所有 35 个外部文档 URL 已验证 — 未发现损坏链接 | ✅ COMPLETE（所有 URL 返回有效页面，包括 /slash-commands 重定向） |
| 5 | 低 | 验证 | 所有本地徽章文件路径已验证 — 无缺失文件 | ✅ COMPLETE（所有 20+ 个徽章目标在文件系统上存在） |
| 6 | 低 | 验证 | 记忆锚点 `#organize-rules-with-clauderules` 已在 /memory 页面确认 | ✅ COMPLETE（章节标题存在） |
| 7 | 低 | 验证 | Git Worktrees 锚点 `#run-parallel-claude-code-sessions-with-git-worktrees` 已在 /common-workflows 页面确认 | ✅ COMPLETE（章节标题存在） |
| 8 | 低 | 验证 | 自动模式锚点 `#eliminate-prompts-with-auto-mode` 已在 /permission-modes 页面确认 | ✅ COMPLETE（章节标题存在） |
| 9 | 低 | 验证 | 捆绑技能锚点 `#bundled-skills` 已在 /skills 页面确认 | ✅ COMPLETE（章节标题存在） |
| 10 | 低 | 验证 | 所有 CONCEPTS 描述已对照官方文档检查 — 未检测到漂移 | ✅ COMPLETE（所有描述准确） |

---

## [2026-03-27 18:37 PKT] Claude Code v2.1.85

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | URL 过时 | 命令 URL `/slash-commands` 提供技能页面 — 文档说"命令已合并到技能中" | ❌ INVALID（自 2026-03-10 起重复出现；URL 仍可解析；用户选择保持原样） |
| 2 | 中 | 缺失概念 | 向 Hot 表添加 Chrome 集成 — 通过 Claude in Chrome 扩展进行浏览器自动化（beta，专用文档在 `/chrome`） | ✅ COMPLETE（已在 GitHub Actions 后添加行，位置为 --chrome，带 beta 徽章） |
| 3 | 低 | 验证 | 所有 36 个外部文档 URL 已验证 — 未发现损坏链接 | ✅ COMPLETE（所有 URL 返回有效页面，包括 /slash-commands 重定向） |
| 4 | 低 | 验证 | 所有本地徽章文件路径已验证 — 无缺失文件 | ✅ COMPLETE（所有 20+ 个徽章目标在文件系统上存在） |
| 5 | 低 | 验证 | 记忆锚点 `#organize-rules-with-clauderules` 已在 /memory 页面确认 | ✅ COMPLETE（章节标题存在） |
| 6 | 低 | 验证 | Git Worktrees 锚点 `#run-parallel-claude-code-sessions-with-git-worktrees` 已在 /common-workflows 页面确认 | ✅ COMPLETE（章节标题存在） |
| 7 | 低 | 验证 | 自动模式锚点 `#eliminate-prompts-with-auto-mode` 已在 /permission-modes 页面确认 | ✅ COMPLETE（章节标题存在） |
| 8 | 低 | 验证 | 捆绑技能锚点 `#bundled-skills` 已在 /skills 页面确认 | ✅ COMPLETE（章节标题存在） |
| 9 | 低 | 验证 | 所有 CONCEPTS 描述已对照官方文档检查 — 未检测到漂移 | ✅ COMPLETE（所有描述准确） |

---

## [2026-03-28 18:04 PKT] Claude Code v2.1.86

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | URL 过时 | 命令 URL `/slash-commands` 提供技能页面 — 文档说"命令已合并到技能中" | ❌ INVALID（自 2026-03-10 起重复出现；URL 仍可解析；用户选择保持原样） |
| 2 | 中 | 缺失徽章 | Hot 表中的 Chrome 行没有 BP 徽章 — 报告存在于 `reports/claude-in-chrome-v-chrome-devtools-mcp.md` | ✅ COMPLETE（BP 徽章已添加，链接到 reports/claude-in-chrome-v-chrome-devtools-mcp.md） |
| 3 | 低 | 描述变更 | 插件描述缺少 LSP 服务器 — 官方文档将 `.lsp.json` 列为插件组件 | ✅ COMPLETE（已在插件描述中添加"和 LSP 服务器"） |
| 4 | 低 | 验证 | 所有 37 个外部文档 URL 已验证 — 未发现损坏链接 | ✅ COMPLETE（所有 URL 返回有效页面，包括 /slash-commands 重定向） |
| 5 | 低 | 验证 | 所有本地徽章文件路径已验证 — 无缺失文件 | ✅ COMPLETE（所有 20+ 个徽章目标在文件系统上存在） |
| 6 | 低 | 验证 | 记忆锚点 `#organize-rules-with-clauderules` 已在 /memory 页面确认 | ✅ COMPLETE（章节标题 `.claude/rules/` 存在） |
| 7 | 低 | 验证 | Git Worktrees 锚点 `#run-parallel-claude-code-sessions-with-git-worktrees` 已在 /common-workflows 页面确认 | ✅ COMPLETE（章节标题存在） |
| 8 | 低 | 验证 | 自动模式锚点 `#eliminate-prompts-with-auto-mode` 已在 /permission-modes 页面确认 | ✅ COMPLETE（章节标题存在） |
| 9 | 低 | 验证 | 捆绑技能锚点 `#bundled-skills` 已在 /skills 页面确认 | ✅ COMPLETE（章节标题存在） |
| 10 | 低 | 验证 | 所有 CONCEPTS 描述已对照官方文档检查 — 未检测到漂移 | ✅ COMPLETE（除插件 LSP 说明外所有描述准确 — 见 #3） |

---

## [2026-04-01 12:33 PKT] Claude Code v2.1.89

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 缺失概念 | 向 Hot 表添加计算机使用行 — 通过内置 MCP 服务器在 macOS 上进行屏幕控制（研究预览，v2.1.85+） | ✅ COMPLETE（已在全屏渲染后添加行，带 beta 徽章和桌面内联链接） |
| 2 | 高 | URL 过时 | 命令 URL `/slash-commands` 提供技能页面 — 文档说"命令已合并到技能中" | ❌ INVALID（自 2026-03-10 起重复出现；URL 仍可解析；用户选择保持原样） |
| 3 | 中 | 缺失概念 | 向 Hot 表添加全屏渲染行 — 无闪烁备用屏幕渲染，支持鼠标（研究预览，v2.1.88+） | ✅ COMPLETE（已添加为第一个 Hot 条目，位置为 CLAUDE_CODE_NO_FLICKER=1） |
| 4 | 低 | 验证 | 所有 38 个外部文档 URL 已验证 — 未发现损坏链接 | ✅ COMPLETE（所有 URL 返回有效页面，包括 /slash-commands 重定向） |
| 5 | 低 | 验证 | 所有本地徽章文件路径已验证 — 无缺失文件 | ✅ COMPLETE（所有 20+ 个徽章目标在文件系统上存在） |
| 6 | 低 | 验证 | 记忆锚点 `#organize-rules-with-clauderules` 已在 /memory 页面确认 | ✅ COMPLETE（章节标题存在） |
| 7 | 低 | 验证 | Git Worktrees 锚点 `#run-parallel-claude-code-sessions-with-git-worktrees` 已在 /common-workflows 页面确认 | ✅ COMPLETE（章节标题存在） |
| 8 | 低 | 验证 | 自动模式锚点 `#eliminate-prompts-with-auto-mode` 已在 /permission-modes 页面确认 | ✅ COMPLETE（章节标题存在） |
| 9 | 低 | 验证 | 捆绑技能锚点 `#bundled-skills` 已在 /skills 页面确认 | ✅ COMPLETE（章节标题存在） |
| 10 | 低 | 验证 | 所有 CONCEPTS 描述已对照官方文档检查 — 未检测到漂移 | ✅ COMPLETE（所有描述准确） |

---

## [2026-04-02 21:17 PKT] Claude Code v2.1.90

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | URL 过时 | 命令 URL `/slash-commands` 提供技能页面 — 文档说"命令已合并到技能中" | ❌ INVALID（自 2026-03-10 起重复出现；URL 仍可解析；用户选择保持原样） |
| 2 | 低 | 验证 | 所有 39 个外部文档 URL 已验证 — 未发现损坏链接 | ✅ COMPLETE（所有 URL 返回有效页面，包括 /slash-commands 重定向） |
| 3 | 低 | 验证 | 所有本地徽章文件路径已验证 — 无缺失文件 | ✅ COMPLETE（所有 20+ 个徽章目标在文件系统上存在） |
| 4 | 低 | 验证 | 记忆锚点 `#organize-rules-with-clauderules` 已在 /memory 页面确认 | ✅ COMPLETE（章节标题"使用 `.claude/rules/` 组织规则"存在） |
| 5 | 低 | 验证 | Git Worktrees 锚点 `#run-parallel-claude-code-sessions-with-git-worktrees` 已在 /common-workflows 页面确认 | ✅ COMPLETE（章节标题存在） |
| 6 | 低 | 验证 | 自动模式锚点 `#eliminate-prompts-with-auto-mode` 已在 /permission-modes 页面确认 | ✅ COMPLETE（章节标题存在） |
| 7 | 低 | 验证 | 捆绑技能锚点 `#bundled-skills` 已在 /skills 页面确认 | ✅ COMPLETE（章节标题存在） |
| 8 | 低 | 验证 | 所有 CONCEPTS 描述已对照官方文档检查 — 未检测到漂移 | ✅ COMPLETE（所有描述准确） |

---

## [2026-04-03 20:35 PKT] Claude Code v2.1.91

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | URL 过时 | 命令 URL `/slash-commands` 不在官方站点地图（llms.txt）中 — 重定向到 `/skills` 页面；文档说"命令已合并到技能中" | ❌ INVALID（自 2026-03-10 起重复出现；URL 仍可通过重定向解析；用户选择保持原样） |
| 2 | 低 | 验证 | 所有 40 个外部文档 URL 已对照 llms.txt 站点地图（80 页）验证 — 未发现损坏链接 | ✅ COMPLETE（所有 URL 返回有效页面，包括 /slash-commands 重定向） |
| 3 | 低 | 验证 | 所有本地徽章文件路径已验证 — 无缺失文件（已检查 17 个本地目标） | ✅ COMPLETE（所有徽章目标在文件系统上存在） |
| 4 | 低 | 验证 | 记忆锚点 `#organize-rules-with-clauderules` 已在 /memory 页面确认 | ✅ COMPLETE（章节标题"使用 `.claude/rules/` 组织规则"存在） |
| 5 | 低 | 验证 | Git Worktrees 锚点 `#run-parallel-claude-code-sessions-with-git-worktrees` 已在 /common-workflows 页面确认 | ✅ COMPLETE（章节标题存在） |
| 6 | 低 | 验证 | 自动模式锚点 `#eliminate-prompts-with-auto-mode` 已在 /permission-modes 页面确认 | ✅ COMPLETE（章节标题存在） |
| 7 | 低 | 验证 | 捆绑技能锚点 `#bundled-skills` 已在 /skills 页面确认 | ✅ COMPLETE（章节标题存在） |
| 8 | 低 | 验证 | 所有 CONCEPTS 描述已对照官方文档检查 — 未检测到漂移 | ✅ COMPLETE（所有描述准确） |

---

## [2026-04-04 22:46 PKT] Claude Code v2.1.92

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 缺失概念 | 向 Hot 表添加 Ultraplan 行 — 基于云的计划起草，带浏览器审查、内联评论和灵活执行（`/ultraplan`） | ✅ COMPLETE（已在 Power-ups 后添加行，带 beta 徽章和 /ultraplan 位置） |
| 2 | 高 | 缺失概念 | 向 Hot 表添加 Claude Code Web 行 — 在 claude.ai/code 的云基础设施上运行任务，带 PR 自动修复和并行会话 | ✅ COMPLETE（已在 Ultraplan 后添加行，带 beta 徽章、claude.ai/code 位置和 Web 计划任务内联链接） |
| 3 | 高 | URL 过时 | 命令 URL `/slash-commands` 不在官方站点地图中 — 重定向到 `/skills` 页面；文档说"命令已合并到技能中" | ❌ INVALID（自 2026-03-10 起重复出现；URL 仍可通过重定向解析；用户选择保持原样） |
| 4 | 中 | 缺失概念 | 向 Hot 表添加桌面应用行 — 独立应用，带视觉差异、Dispatch、计算机使用和并行会话 | ❌ INVALID（自 2026-03-17 起重复出现；用户认为它是平台界面，非配置概念） |

---

## [2026-04-08 21:37 PKT] Claude Code v2.1.96

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | URL 过时 | 命令 URL `/slash-commands` 不在官方站点地图中 — 重定向到 `/skills` 页面；文档说"命令已合并到技能中" | ❌ INVALID（自 2026-03-10 起重复出现；URL 仍可通过重定向解析；用户选择保持原样） |
| 2 | 中 | 名称变更 | Hot 表中的"无闪烁模式" — 官方文档页面标题为"全屏渲染"；考虑重命名或添加副标题 | ❌ INVALID（用户选择保持"无闪烁模式"以符合 Boris 的推文命名约定；环境变量为 `CLAUDE_CODE_NO_FLICKER`） |
| 3 | 中 | 缺失概念 | 向 Hot 表添加桌面应用行 — 独立应用，带视觉差异、Dispatch、计算机使用和并行会话 | ❌ INVALID（自 2026-03-17 起重复出现；用户认为它是平台界面，非配置概念） |
| 4 | 低 | 验证 | 所有 41 个外部文档 URL 已验证 — 未发现损坏链接 | ✅ COMPLETE（所有 URL 返回有效页面，包括 /slash-commands 重定向） |
| 5 | 低 | 验证 | 所有本地徽章文件路径已验证 — 无缺失文件 | ✅ COMPLETE（所有 20+ 个徽章目标在文件系统上存在） |
| 6 | 低 | 验证 | 记忆锚点 `#organize-rules-with-clauderules` 已在 /memory 页面确认 | ✅ COMPLETE（章节标题"使用 `.claude/rules/` 组织规则"存在） |
| 7 | 低 | 验证 | Git Worktrees 锚点 `#run-parallel-claude-code-sessions-with-git-worktrees` 已在 /common-workflows 页面确认 | ✅ COMPLETE（章节标题存在） |
| 8 | 低 | 验证 | 自动模式锚点 `#eliminate-prompts-with-auto-mode` 已在 /permission-modes 页面确认 | ✅ COMPLETE（章节标题存在） |
| 9 | 低 | 验证 | 捆绑技能锚点 `#bundled-skills` 已在 /skills 页面确认 | ✅ COMPLETE（章节标题存在） |
| 10 | 低 | 验证 | 所有 CONCEPTS 描述已对照官方文档检查 — 未检测到漂移 | ✅ COMPLETE（所有描述准确） |

---

## [2026-04-09 23:37 PKT] Claude Code v2.1.97

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 缺失概念 | 向 Hot 表添加 Agent SDK 行 — 使用 Python/TypeScript SDK 构建生产级 AI 代理（29 个文档页面，`/en/agent-sdk/overview`） | ✅ COMPLETE（已在 Claude Code Web 后添加行，带 Quickstart 和示例内联链接） |
| 2 | 高 | URL 过时 | 命令 URL `/slash-commands` 不在官方站点地图中 — 重定向到 `/skills`；规范命令参考现为 `/en/commands` | ❌ INVALID（自 2026-03-10 起重复出现；URL 仍可通过重定向解析；用户选择保持原样） |
| 3 | 中 | 缺失内联链接 | 向 CLI 启动标志行添加环境变量（`/env-vars`）内联链接 — 新增专用文档页面 | ✅ COMPLETE（环境变量内联链接已在交互模式后添加） |
| 4 | 低 | 验证 | 所有 42 个外部文档 URL 已对照 llms.txt 站点地图（110 页）验证 — 未发现损坏链接 | ✅ COMPLETE（所有 URL 返回有效页面，包括 /slash-commands 重定向） |
| 5 | 低 | 验证 | 所有本地徽章文件路径已验证 — 无缺失文件（已检查 20+ 个徽章目标） | ✅ COMPLETE（所有徽章目标在文件系统上存在） |
| 6 | 低 | 验证 | 记忆锚点 `#organize-rules-with-clauderules` 已在 /memory 页面确认 | ✅ COMPLETE（章节标题"使用 `.claude/rules/` 组织规则"存在） |
| 7 | 低 | 验证 | Git Worktrees 锚点 `#run-parallel-claude-code-sessions-with-git-worktrees` 已在 /common-workflows 页面确认 | ✅ COMPLETE（章节标题存在） |
| 8 | 低 | 验证 | 自动模式锚点 `#eliminate-prompts-with-auto-mode` 已在 /permission-modes 页面确认 | ✅ COMPLETE（章节标题存在） |
| 9 | 低 | 验证 | 捆绑技能锚点 `#bundled-skills` 已在 /skills 页面确认 | ✅ COMPLETE（章节标题存在） |
| 10 | 低 | 验证 | 所有 CONCEPTS 描述已对照官方文档检查 — 未检测到漂移 | ✅ COMPLETE（所有描述准确） |

---

## [2026-04-11 18:13 PKT] Claude Code v2.1.101

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | URL 过时 | 命令 URL `/slash-commands` 不在官方站点地图（110 页）中 — 重定向到 `/skills`；规范命令参考为 `/en/commands` | ❌ INVALID（自 2026-03-10 起重复出现；URL 仍可通过重定向解析；用户选择保持原样） |
| 2 | 低 | 验证 | 所有 43 个外部文档 URL 已对照 llms.txt 站点地图（110 页）验证 — 未发现损坏链接 | ✅ COMPLETE（所有 URL 返回有效页面，包括 /slash-commands 重定向） |
| 3 | 低 | 验证 | 所有本地徽章文件路径已验证 — 无缺失文件（已检查 20+ 个徽章目标） | ✅ COMPLETE（所有徽章目标在文件系统上存在） |
| 4 | 低 | 验证 | 记忆锚点 `#organize-rules-with-clauderules` 已在 /memory 页面确认 | ✅ COMPLETE（章节标题"使用 `.claude/rules/` 组织规则"存在） |
| 5 | 低 | 验证 | Git Worktrees 锚点 `#run-parallel-claude-code-sessions-with-git-worktrees` 已在 /common-workflows 页面确认 | ✅ COMPLETE（章节标题存在） |
| 6 | 低 | 验证 | 自动模式锚点 `#eliminate-prompts-with-auto-mode` 已在 /permission-modes 页面确认 | ✅ COMPLETE（章节标题存在） |
| 7 | 低 | 验证 | 捆绑技能锚点 `#bundled-skills` 已在 /skills 页面确认 | ✅ COMPLETE（章节标题存在） |
| 8 | 低 | 验证 | 所有 CONCEPTS 描述已对照官方文档检查 — 未检测到漂移 | ✅ COMPLETE（所有描述准确） |

---

## [2026-04-13 20:07 PKT] Claude Code v2.1.101

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | URL 过时 | 命令 URL `/slash-commands` 不在官方站点地图（110 页）中 — 重定向到 `/skills`；规范命令参考为 `/en/commands` | ❌ INVALID（自 2026-03-10 起重复出现；URL 仍可通过重定向解析；用户选择保持原样） |
| 2 | 低 | 验证 | 所有 44 个外部文档 URL 已对照 llms.txt 站点地图（110 页）验证 — 未发现损坏链接 | ✅ COMPLETE（所有 URL 返回有效页面，包括 /slash-commands 重定向） |
| 3 | 低 | 验证 | 所有本地徽章文件路径已验证 — 无缺失文件（已检查 20+ 个徽章目标） | ✅ COMPLETE（所有徽章目标在文件系统上存在） |
| 4 | 低 | 验证 | 记忆锚点 `#organize-rules-with-clauderules` 已在 /memory 页面确认 | ✅ COMPLETE（章节标题"使用 `.claude/rules/` 组织规则"存在） |
| 5 | 低 | 验证 | Git Worktrees 锚点 `#run-parallel-claude-code-sessions-with-git-worktrees` 已在 /common-workflows 页面确认 | ✅ COMPLETE（章节标题存在） |
| 6 | 低 | 验证 | 自动模式锚点 `#eliminate-prompts-with-auto-mode` 已在 /permission-modes 页面确认 | ✅ COMPLETE（章节标题存在） |
| 7 | 低 | 验证 | 捆绑技能锚点 `#bundled-skills` 已在 /skills 页面确认 | ✅ COMPLETE（章节标题存在） |
| 8 | 低 | 验证 | 所有 CONCEPTS 描述已对照官方文档检查 — 未检测到漂移 | ✅ COMPLETE（所有描述准确） |

---

## [2026-04-14 23:17 PKT] Claude Code v2.1.107

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 缺失概念 | 向 Hot 表添加 Routines 行 — 在 Anthropic 基础设施上的云自动化，支持计划、API 和 GitHub 事件触发器（`/en/routines`） | ✅ COMPLETE（已在计划任务后添加行，带 beta 徽章、桌面任务内联链接） |
| 2 | 高 | URL 过时 | 更新 Claude Code Web 行（第 45 行）中的 `web-scheduled-tasks` 内联链接为 `/en/routines` — URL 不在站点地图中，重定向到 Routines 页面 | ✅ COMPLETE（内联链接文本已改为"Routines"，URL 已更新为 /routines） |
| 3 | 高 | URL 过时 | 更新计划任务行（第 55 行）中的 `web-scheduled-tasks` 内联链接为 `/en/routines` — 相同的过时 URL | ✅ COMPLETE（URL 已更新为 /routines） |
| 4 | 高 | URL 过时 | 命令 URL `/slash-commands` 不在官方站点地图（119 页）中 — 重定向到 `/skills`；规范命令参考为 `/en/commands` | ❌ INVALID（自 2026-03-10 起重复出现；URL 仍可通过重定向解析；用户选择保持原样） |
| 5 | 中 | 描述变更 | 更新计划任务描述从"最长 3 天"到"最长 7 天" — 文档现在指定重复任务七天后过期 | ✅ COMPLETE（描述已更新为"最长 7 天"） |
| 6 | 中 | 缺失概念 | 向 Hot 表添加 Devcontainers 行 — 预配置的开发容器，带安全隔离和防火墙规则（`/en/devcontainer`） | ✅ COMPLETE（已在 Routines 后添加行，位置为 .devcontainer/） |

---

## [2026-04-16 20:20 PKT] Claude Code v2.1.110

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | URL 过时 | 修复 TIPS 中的 `web-scheduled-tasks` URL（第 223 行）为 `/en/routines` — URL 不在站点地图中；相同的过时 URL 在 2026-04-14 已在 Hot 表中修复，但 TIPS 中的实例被遗漏 | ✅ COMPLETE（URL 已更新为 /routines） |
| 2 | 高 | URL 过时 | 命令 URL `/slash-commands` 不在官方站点地图（111 页）中 — 重定向到 `/skills`；规范命令参考为 `/en/commands` | ❌ INVALID（自 2026-03-10 起重复出现；URL 仍可通过重定向解析；用户选择保持原样） |
| 3 | 中 | 描述变更 | 在 TIPS 中更新"最长 3 天"为"最长 7 天"（第 223 行）— 相同的描述更新已在 2026-04-14 在 Hot 表中完成，但 TIPS 中的实例被遗漏 | ✅ COMPLETE（描述已更新为"最长 7 天"） |
| 4 | 低 | 验证 | 所有 45 个外部文档 URL 已对照 llms.txt 站点地图（111 页）验证 — 发现 1 个损坏链接（见 #1） | ✅ COMPLETE（已标记 web-scheduled-tasks） |
| 5 | 低 | 验证 | 所有本地徽章文件路径已验证 — 无缺失文件（已检查 20+ 个徽章目标） | ✅ COMPLETE（所有徽章目标在文件系统上存在） |
| 6 | 低 | 验证 | 记忆锚点 `#organize-rules-with-clauderules` 已在 /memory 页面确认 | ✅ COMPLETE（章节标题"使用 `.claude/rules/` 组织规则"存在） |
| 7 | 低 | 验证 | Git Worktrees 锚点 `#run-parallel-claude-code-sessions-with-git-worktrees` 已在 /common-workflows 页面确认 | ✅ COMPLETE（章节标题存在） |
| 8 | 低 | 验证 | 自动模式锚点 `#eliminate-prompts-with-auto-mode` 已在 /permission-modes 页面确认 | ✅ COMPLETE（章节标题存在） |
| 9 | 低 | 验证 | 捆绑技能锚点 `#bundled-skills` 已在 /skills 页面确认 | ✅ COMPLETE（章节标题存在） |
| 10 | 低 | 验证 | 所有 CONCEPTS 描述已对照官方文档检查 — 未检测到漂移 | ✅ COMPLETE（所有描述准确） |

---

## [2026-04-18 19:53 PKT] Claude Code v2.1.113

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 描述变更 | 自动模式行（第 48 行）仍引用 `claude --enable-auto-mode` — 该标志在 v2.1.111 中已移除；自动模式现在通过 `--permission-mode auto` 或 Shift+Tab 循环启动（Max 订阅者默认使用 Opus 4.7） | ✅ COMPLETE（位置已更新为 `--permission-mode auto`、`Shift+Tab`；描述注明了标志移除和 Max+Opus-4.7 默认行为） |
| 2 | 高 | 缺失概念 | 向 Hot 表添加 Ultrareview 行 — 基于云的多代理代码审查（`/ultrareview`，v2.1.86+，专用文档在 `/en/ultrareview`）；Pro/Max 免费 3 次运行 | ✅ COMPLETE（已在 Routines 后添加行，带 beta 徽章、/ultrareview 位置、Tasks 跟踪内联链接） |
| 3 | 高 | 缺失概念 | 添加 Tasks 行 — `/tasks` 命令用于跟踪后台工作（在 Ultrareview 页面上引用）；替代 TodoWrite，详见 `reports/claude-global-vs-project-settings.md` | ✅ COMPLETE（已在计划任务后添加行，位置为 /tasks，BP 徽章链接到 global-vs-project-settings 报告） |
| 4 | 中 | 描述变更 | 无闪烁模式行（第 47 行）— 官方文档现在以 `/tui fullscreen` 命令为先（v2.1.110）；环境变量是 v2.1.110 之前的传统路径，见 /fullscreen 页面 | ✅ COMPLETE（位置已更新为 `/tui fullscreen`、`CLAUDE_CODE_NO_FLICKER=1`；描述注明了 /tui 为规范路径，环境变量为传统方式） |
| 5 | 中 | 命令名称过时 | TIPS 第 249 行引用 `/fewer-permission-prompts` — 官方技能名称为 `/less-permission-prompts`（根据 v2.1.111 更新日志；本地技能文件夹为 `fewer-permission-prompts`，但用户可见命令应与官方名称匹配） | ✅ COMPLETE（TIPS 第 249 行已更新为 /less-permission-prompts） |
| 6 | 低 | 描述变更 | 计划任务行（第 60 行）— 第 15 周添加了 Monitor 工具 + 自定步调 `/loop`（LLM 自行选择间隔）；描述未提及此内容 | ✅ COMPLETE（描述已追加自定步调/Monitor 工具说明） |
| 7 | 低 | 描述变更 | Git Worktrees 行（第 63 行）— v2.1.105/106 添加了 EnterWorktree/ExitWorktree 工具和 `isolation: "worktree"` 子代理前置元数据；描述未提及这些 | ✅ COMPLETE（位置已更新以包含 EnterWorktree/ExitWorktree 和 isolation 前置元数据；描述注明了 v2.1.106+ 子代理工作树支持） |
| 8 | 高 | URL 过时 | 命令 URL `/slash-commands` 不在官方站点地图（119 页）中 — 重定向到 `/skills`；规范命令参考为 `/en/commands` | ❌ INVALID（自 2026-03-10 起重复出现；URL 仍可通过重定向解析；用户已在 17+ 次运行中选择保持原样） |
| 9 | 低 | 验证 | 所有 45+ 个外部文档 URL 已对照 llms.txt 站点地图（119 页）验证 — 除反复出现的 `/slash-commands` 重定向外，未发现新的损坏链接 | ✅ COMPLETE（所有标记的 URL 返回有效页面） |
| 10 | 低 | 验证 | 所有本地徽章文件路径已验证 — 无缺失文件（已检查 20+ 个徽章目标） | ✅ COMPLETE（所有徽章目标在文件系统上存在） |
| 11 | 低 | 验证 | 记忆锚点 `#organize-rules-with-clauderules` 已在 /memory 页面确认 | ✅ COMPLETE（章节标题"使用 `.claude/rules/` 组织规则"存在） |
| 12 | 低 | 验证 | Git Worktrees 锚点 `#run-parallel-claude-code-sessions-with-git-worktrees` 已在 /common-workflows 页面确认 | ✅ COMPLETE（章节标题存在） |
| 13 | 低 | 验证 | 自动模式锚点 `#eliminate-prompts-with-auto-mode` 已在 /permission-modes 页面确认 | ✅ COMPLETE（章节标题存在） |
| 14 | 低 | 验证 | 捆绑技能锚点 `#bundled-skills` 已在 /skills 页面确认 | ✅ COMPLETE（章节标题存在） |
| 15 | 低 | 验证 | 全屏页面确认 `/tui fullscreen` 为规范命令且 `tui` 为设置字段（v2.1.110） | ✅ COMPLETE（页面已获取并引用） |
| 16 | 低 | 验证 | 权限模式页面确认 `--enable-auto-mode` 标志不再有文档说明；自动模式现在需要 Max 计划 + Opus 4.7 | ✅ COMPLETE（页面已获取；标志不在文档中） |
| 17 | 低 | 验证 | Ultrareview 页面存在于 `/en/ultrareview`（v2.1.86+），确认了 `/ultrareview` 和 `/tasks` 命令 | ✅ COMPLETE（页面已获取，内容已捕获） |

---

## [2026-04-24 00:32 PKT] Claude Code v2.1.118

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 描述变更 | 钩子行（第 28 行）列出 4 种处理程序类型（"脚本、HTTP、提示、代理"）— 官方 `/en/hooks` 页面现在记录了 5 种类型，新增了 `mcp_tool`（v2.1.118 更新日志："钩子可以直接调用 MCP 工具"通过 `type: "mcp_tool"`） | ✅ COMPLETE（描述已更新为"脚本、HTTP、MCP 工具、提示、代理"） |
| 2 | 中 | 描述为空 | 工作流行（第 27 行）描述单元格为空（仅有编排工作流徽章）— 官方 `/en/common-workflows` 页面涵盖了探索、修复、重构、测试的分步指南 | ✅ COMPLETE（描述已填写官方文档来源文本："探索代码库、修复错误、重构和测试的分步指南——多步骤任务的编排模式"） |
| 3 | 低 | 描述变更 | 考虑在 CLI 启动标志行中内联提及 `/usage`（v2.1.118 合并了 `/cost`+`/stats`）— 新的斜杠命令替代了两个传统命令 | ✅ COMPLETE（内联说明"`/usage`（在 v2.1.118 中合并了 `/cost`+`/stats`）"已附加在环境变量之后） |
| 4 | 高 | URL 过时 | 命令 URL `/slash-commands` 不在官方站点地图（117 页）中 — 重定向到 `/skills`；规范命令参考为 `/en/commands` | ❌ INVALID（自 2026-03-10 起重复出现；URL 仍可通过重定向解析；用户已在 18+ 次运行中选择保持原样） |
| 5 | 低 | 验证 | 钩子页面 `/en/hooks` 已获取 — 确认了 5 种处理程序类型，包括 `mcp_tool`（v2.1.118） | ✅ COMPLETE（实时获取记录了 5 类型模式） |
| 6 | 低 | 验证 | Ultrareview 页面 `/en/ultrareview#track-a-running-review` 锚点已获取并确认 | ✅ COMPLETE（章节存在，描述了 `/tasks` 集成） |
| 7 | 低 | 验证 | 检查点页面 `/en/checkpointing` 已获取 — `/undo` 别名（v2.1.108）未在文档中显示，仅在更新日志中；无需 CONCEPTS 更新 | ✅ COMPLETE（文档页面内容与现有描述匹配） |
| 8 | 低 | 验证 | 所有本地徽章文件路径 — 自 2026-04-18 的 v2.1.113 运行以来无变化 | ✅ COMPLETE（自上次运行以来稳定） |
| 9 | 低 | 验证 | 记忆锚点 `#organize-rules-with-clauderules` — 本次运行未重新检查；自 v2.1.113 以来稳定 | ✅ COMPLETE（稳定） |
| 10 | 低 | 验证 | Git Worktrees 锚点 `#run-parallel-claude-code-sessions-with-git-worktrees` — 自 v2.1.113 以来稳定 | ✅ COMPLETE（稳定） |
| 11 | 低 | 验证 | 自动模式锚点 `#eliminate-prompts-with-auto-mode` — 自 v2.1.113 以来稳定 | ✅ COMPLETE（稳定） |
| 12 | 低 | 验证 | 捆绑技能锚点 `#bundled-skills` — 自 v2.1.113 以来稳定 | ✅ COMPLETE（稳定） |
| 13 | 低 | 验证 | claude-code-guide 代理交叉检查 — 与专用代理无矛盾；提供了 /recap（v2.1.108）、/usage（v2.1.118）、MCP 工具钩子（v2.1.118）作为佐证 | ✅ COMPLETE（两个代理一致） |

---

## [2026-04-26 13:10 PKT] Claude Code v2.1.119

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | URL 过时 | 命令 URL `/slash-commands` 不在官方站点地图（139 页）中 — 重定向到 `/skills`；规范命令参考为 `/en/commands` | ❌ INVALID（自 2026-03-10 起重复出现；URL 仍可通过重定向解析；用户已在 19+ 次运行中选择保持原样） |
| 2 | 高 | URL 目标错误 | Tasks 行（第 62 行）主 URL 指向 `/ultrareview#track-a-running-review` — 锚点有效但目标是 ultrareview 跟踪章节，而非更广泛的 Tasks 系统；规范主页是本地报告 `reports/claude-global-vs-project-settings.md#tasks-system` | ✅ COMPLETE（主 URL 已更新为 `reports/claude-global-vs-project-settings.md#tasks-system`；ultrareview 跟踪锚点保留为描述末尾的内联链接"Ultrareview 跟踪"） |
| 3 | 中 | Beta 徽章时效性 | Routines / 无闪烁模式 / 计算机使用 / 代码审查在 README 中有 `![beta]` 但它们的文档页面不再将其标记为 beta — 重新评估并适当地降级 | ❌ INVALID（验证获取了所有 4 个文档页面 — Routines："处于研究预览阶段"；全屏："研究预览"；计算机使用："macOS 上的研究预览"；代码审查："处于研究预览阶段" — README beta 徽章准确；代理对正文内容 0.6 置信度的读取被 `<Note>` 横幅文本推翻） |
| 4 | 中 | 描述歧义 | 计划任务行（第 61 行）描述混淆了 `/loop`（本地，会话作用域，7 天过期）和 `/schedule`（Anthropic 基础设施上的云 Routines）— 官方 `/en/scheduled-tasks` 页面现在正式区分了云/桌面/循环三种界面 | ✅ COMPLETE（描述现在明确命名"三种界面"，分别说明了 `/loop` 本地、`/schedule` 云 Routines 和桌面计划任务） |
| 5 | 低 | 缺失概念（可选） | 快速模式目前只是设置（第 31 行）内的侧链接 — 有自己专用的 `/en/fast-mode` 页面，带 `↯` 指示器和 `/fast` 切换（v2.1.36+）；可以是 Hot 行 | ✅ COMPLETE（Hot 行已插入在 Power-ups 和计算机使用之间，带 beta 徽章；从设置中移除了冗余的快速模式侧链接以防止重复） |
| 6 | 低 | 缺失内联链接 | 记忆行可以展示 `reports/claude-agent-memory.md` 作为内联链接 — 自动记忆被引用但本地深入分析未从 CONCEPTS 链接 | ✅ COMPLETE（"自动记忆深入分析"内联链接已添加在记忆行的自动记忆文档和规则之间） |
| 7 | 低 | 缺失内联链接 | 技能行可以展示 `reports/claude-skills-for-larger-mono-repos.md` 作为内联链接 — 本地存在但仅从 TIPS 引用 | ✅ COMPLETE（"单体仓库技能"内联链接已附加在技能行的官方技能之后） |
| 8 | 低 | 可选概念 | Vim 可视模式（v2.1.118）、主题定制（`~/.claude/themes/`，v2.1.118）和 PowerShell 工具（v2.1.111）可以是设置侧链接 — claude-code-guide 交叉检查发现的小概念 | ❌ INVALID（Vim 模式由现有的键绑定侧链接覆盖；主题没有独立于设置的专用文档页面；PowerShell 工具也没有专用文档页面 — 没有具体的子链接目标值得添加） |
| 9 | 低 | 验证 | 所有 35+ 个外部 CONCEPTS 文档 URL 已对照 llms.txt 站点地图（139 页）验证 — 仅标记了反复出现的 `/slash-commands` 重定向；所有其他 URL 解析到预期页面 | ✅ COMPLETE（没有新的损坏 URL） |
| 10 | 低 | 验证 | 所有本地徽章文件路径已验证 — 所有 20+ 个 `best-practice/`、`implementation/` 和 `reports/` 目标在文件系统上存在 | ✅ COMPLETE（无缺失的本地文件） |
| 11 | 低 | 验证 | 记忆锚点 `#organize-rules-with-clauderules` 在 `/en/memory` 页面上确认 | ✅ COMPLETE（自 v2.1.113 以来稳定） |
| 12 | 低 | 验证 | Git Worktrees 锚点 `#run-parallel-claude-code-sessions-with-git-worktrees` 在 `/en/common-workflows` 页面上确认 | ✅ COMPLETE（稳定） |
| 13 | 低 | 验证 | 自动模式锚点 `#eliminate-prompts-with-auto-mode` 在 `/en/permission-modes` 页面上确认 | ✅ COMPLETE（稳定） |
| 14 | 低 | 验证 | 捆绑技能锚点 `#bundled-skills` 在 `/en/skills` 页面上确认 | ✅ COMPLETE（稳定） |
| 15 | 低 | 验证 | Ultrareview 锚点 `#track-a-running-review` 在 `/en/ultrareview` 页面上确认 | ✅ COMPLETE（自 v2.1.118 以来稳定） |
| 16 | 低 | 验证 | claude-code-guide 交叉检查 — 佐证了专用代理关于 Vim 模式（v2.1.118）、主题（v2.1.118）、Effort xhigh（v2.1.111+ Opus 4.7）、Worktrees（v2.1.105+）的发现；无矛盾 | ✅ COMPLETE（两个代理一致） |
| 17 | 低 | 验证检查清单更新 | 向 verification-checklist.md 添加了新规则（#7）"Beta 徽章时效性" — 涵盖根据上游文档页面生命周期重新评估 beta 徽章 | ✅ COMPLETE（规则已添加） |

---

## [2026-04-29 00:53 PKT] Claude Code v2.1.121

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | URL 过时 | 命令 URL `/slash-commands` 不在官方站点地图（139+ 页）中 — 重定向到 `/skills`；规范命令参考为 `/en/commands` | ❌ INVALID（自 2026-03-10 起重复出现；URL 仍可通过重定向解析；用户已在 20+ 次运行中选择保持原样） |
| 2 | 中 | 描述变更 | Ultrareview 行（第 44 行）未提及 v2.1.120 引入的 `claude ultrareview [target]` 非交互式子命令 — 文档确认了用于 CI 使用的 `--json` 和 `--timeout` 标志 | ✅ COMPLETE（位置已更新以包含 `claude ultrareview [target]`；描述附加了非交互式子命令及 `--json` 和 `--timeout` 标志说明，v2.1.120+） |
| 3 | 中 | 描述变更 | MCP 服务器行（第 29 行）未提及 v2.1.121 添加的 `alwaysLoad` 设置 — 绕过工具搜索延迟，使服务器的工具始终加载到上下文中 | ✅ COMPLETE（描述已附加 `alwaysLoad` 说明，解释工具搜索延迟绕过，v2.1.121+） |
| 4 | 中 | 描述变更 | 钩子行（第 28 行）未提及 v2.1.121 添加的 `updatedToolOutput` 能力 — PostToolUse 钩子现在可以通过 `hookSpecificOutput.updatedToolOutput` 替换工具输出 | ✅ COMPLETE（描述已附加 `hookSpecificOutput.updatedToolOutput` 说明，用于 PostToolUse 输出替换，v2.1.121+） |
| 5 | 低 | 描述变更 | 子代理行（第 24 行）未提及分叉子代理现在可通过 `CLAUDE_CODE_FORK_SUBAGENT=1` 在外部构建上使用（v2.1.117）— 以前仅限内部使用 | ✅ COMPLETE（描述已附加 `CLAUDE_CODE_FORK_SUBAGENT=1` 说明，用于外部构建，v2.1.117+） |
| 6 | 低 | 缺失内联链接 | 设置行（第 31 行）内联链接涵盖了权限/模型配置/输出样式/沙箱/键绑定，但不包括自动模式配置（`/auto-mode-config`）— 作为独立页面存在 | ✅ COMPLETE（自动模式配置内联链接已在键绑定后附加） |
| 7 | 低 | 验证 | 所有 35+ 个外部 CONCEPTS 文档 URL 经过抽查验证 — 子代理、技能、MCP、Ultrareview 页面已确认；仅标记了反复出现的 `/slash-commands` 重定向 | ✅ COMPLETE（没有新的损坏 URL） |
| 8 | 低 | 验证 | 所有本地徽章文件路径已验证 — 所有 22 个 `best-practice/`、`implementation/`、`reports/`、`.claude/`、`CLAUDE.md` 目标在文件系统上存在 | ✅ COMPLETE（无缺失的本地文件） |
| 9 | 低 | 验证 | 记忆锚点 `#organize-rules-with-clauderules` — 自 v2.1.113 以来稳定（本次运行未重新获取） | ✅ COMPLETE（稳定） |
| 10 | 低 | 验证 | Git Worktrees 锚点 `#run-parallel-claude-code-sessions-with-git-worktrees` — 自 v2.1.113 以来稳定 | ✅ COMPLETE（稳定） |
| 11 | 低 | 验证 | 自动模式锚点 `#eliminate-prompts-with-auto-mode` — 自 v2.1.113 以来稳定 | ✅ COMPLETE（稳定） |
| 12 | 低 | 验证 | 捆绑技能锚点 `#bundled-skills` — 自 v2.1.113 以来稳定 | ✅ COMPLETE（稳定） |
| 13 | 低 | 验证 | Ultrareview 锚点 `#track-a-running-review` 在 `/en/ultrareview` 页面上确认 — 章节存在并描述了 `/tasks` 集成 | ✅ COMPLETE（自 v2.1.118 以来稳定） |
| 14 | 低 | 验证 | claude-code-guide 交叉检查 — 佐证了专用代理关于 v2.1.117–v2.1.121 变更的发现（外部化分叉子代理、alwaysLoad、updatedToolOutput、claude ultrareview 子命令）；还发现了 Bedrock/Vertex/Foundry、桌面、IDE 集成作为长期缺失的概念 | ✅ COMPLETE（两个代理一致；所有"缺失的平台界面"已根据用户反复决定标记为 INVALID） |

---

## [2026-05-01 15:34 PKT] Claude Code v2.1.126

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 版本过时 | README 徽章固定在 v2.1.121（4 月 29 日）— 最新为 v2.1.126（5 月 1 日）；落后 5 个版本 | ✅ COMPLETE（徽章已升级到 v2.1.126，2026 年 5 月 1 日 15:34 PKT） |
| 2 | 中 | 新概念（可选） | v2.1.126 引入了 `claude project purge [path]` 子命令，带 `--dry-run`/`--all` 标志 — 目前未出现在 CLI 启动标志行中；可以作为内联说明 | ✋ ON HOLD（已推迟 — 单一版本旧的子命令；如果用户要求刷新 CLI 启动标志则重新审视） |
| 3 | 中 | 新概念（可选） | v2.1.126 添加了网关驱动的模型选择器 — 当网关与 Anthropic 兼容时，`/model` 从 `ANTHROPIC_BASE_URL` 的 `/v1/models` 端点列出模型 | ✋ ON HOLD（已推迟 — 小众 LLM 网关功能；仅对自托管网关用户相关；按设计不在 CONCEPTS 中展示） |
| 4 | 低 | 描述变更（可选） | v2.1.122 将 `--from-pr` 扩展为接受 GitLab MR + Bitbucket PR + GitHub Enterprise PR URL（最初仅 GitHub）— CLI 启动标志行未展示此内容 | ✋ ON HOLD（已推迟 — `--from-pr` 目前未作为内联链接展示；需要添加新的子链接） |
| 5 | 高 | URL 过时 | 命令 URL `/slash-commands` 不在官方站点地图中 — 重定向到 `/skills`；规范命令参考为 `/en/commands` | ❌ INVALID（自 2026-03-10 起重复出现；URL 仍可通过重定向解析；用户已在 21+ 次运行中选择保持原样） |
| 6 | 中 | 缺失概念（重复出现） | 专用代理重新标记了输出样式、权限、沙箱、无头模式、桌面应用、IDE 集成作为缺失的独立行 | ❌ INVALID（自 2026-03-10/2026-03-17/2026-04-08/2026-04-09 起重复出现；用户认为所有六个都是平台界面或作为设置子链接涵盖 — 非独立概念） |
| 7 | 中 | 缺失概念（重复出现） | 专用代理标记了自动记忆需要独立于记忆的单独行 | ❌ INVALID（重复出现 — 当前记忆行已经通过内联链接展示了 `/en/memory#auto-memory` 和 `reports/claude-agent-memory.md`；用户选择的跨领域特征模式） |
| 8 | 低 | 发现过时 | 专用代理标记 Tasks 行主 URL 需要 `/en/agent-sdk/todo-tracking` 交叉引用 | ❌ INVALID（已在 2026-04-26 解决 — 用户明确将 Tasks 主 URL 移至 `reports/claude-global-vs-project-settings.md#tasks-system` 并保留 ultrareview 跟踪作为内联链接；代理的分析已过时） |
| 9 | 低 | 验证 | 所有 23 个本地徽章文件路径已验证 — `best-practice/`、`implementation/`、`reports/`、`.claude/`、`.mcp.json`、`CLAUDE.md` 全部存在 | ✅ COMPLETE（无缺失的本地文件） |
| 10 | 低 | 验证 | 抽查验证了外部 CONCEPTS URL（`/en/cli-reference`、`/en/agent-teams`、`/en/changelog`、`/en/mcp`）— 均返回有效页面 | ✅ COMPLETE（没有新的损坏 URL） |
| 11 | 低 | 验证 | Beta 徽章时效性（规则 #7）— 获取了 `/en/agent-teams` 并确认了 `<Warning>` 横幅："代理团队是实验性的，默认禁用" — README beta 徽章准确 | ✅ COMPLETE（无需降级） |
| 12 | 低 | 验证 | 记忆锚点 `#organize-rules-with-clauderules` — 自 v2.1.113 以来稳定 | ✅ COMPLETE（稳定） |
| 13 | 低 | 验证 | Git Worktrees 锚点 `#run-parallel-claude-code-sessions-with-git-worktrees` — 自 v2.1.113 以来稳定 | ✅ COMPLETE（稳定） |
| 14 | 低 | 验证 | 自动模式锚点 `#eliminate-prompts-with-auto-mode` — 自 v2.1.113 以来稳定 | ✅ COMPLETE（稳定） |
| 15 | 低 | 验证 | 捆绑技能锚点 `#bundled-skills` — 自 v2.1.113 以来稳定 | ✅ COMPLETE（稳定） |
| 16 | 低 | 验证 | Ultrareview 锚点 `#track-a-running-review` — 自 v2.1.118 以来稳定 | ✅ COMPLETE（稳定） |
| 17 | 低 | 验证 | claude-code-guide 交叉检查 — 独立研究发现了相同的 v2.1.122–126 变更（`claude project purge`、网关模型选择器、`--from-pr` 扩展）；还重新发现了长期存在的平台界面概念（桌面、IDE 集成、Bedrock/Vertex/Foundry），这些根据用户策略为重复出现的 INVALID；无矛盾 | ✅ COMPLETE（两个代理一致） |

---

## [2026-05-12 23:36 PKT] Claude Code v2.1.139

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 版本过时 | README 徽章固定在 v2.1.128（5 月 8 日）— 最新为 v2.1.139（5 月 11 日）；落后 11 个版本 | ✅ COMPLETE（徽章已在阶段 2.6 中升级到 v2.1.139，2026 年 5 月 12 日 23:36 PKT） |
| 2 | 高 | URL/锚点过时（新） | Git Worktrees 行主 URL 指向 `/common-workflows#run-parallel-claude-code-sessions-with-git-worktrees` — 但现在存在专用的 `/en/worktrees` 页面（涵盖 `--worktree`/`-w` 标志、`.worktreeinclude`、WorktreeCreate/Remove 钩子、非 git VCS）并且传统的 common-workflows 锚点已重命名为 `#run-parallel-sessions-with-worktrees`（省略了"git"一词）。两者均已实时验证 | ✅ COMPLETE（URL 已切换为专用的 `/en/worktrees` 页面；位置列已根据用户授权扩展为包含 `--worktree`/`-w`、`.worktreeinclude`、`WorktreeCreate`/`WorktreeRemove` 钩子） |
| 3 | 高 | 缺失概念（新） | v2.1.139 引入了**代理视图**（`claude agents`、`--bg`、`/bg`）— 研究预览"一个屏幕管理多个后台会话"，支持 peek/attach/dispatch。专用文档页面 `/en/agent-view` 已确认在线 | ✅ COMPLETE（Hot 行已添加在代理团队之后，带 `![beta]` 徽章，根据 `<Note>`"研究预览"横幅；描述注明了监督主机托管和重启持久化） |
| 4 | 高 | 缺失概念（新） | v2.1.139 引入了 **/goal** 命令 — 让 Claude 跨轮次持续工作，直到模型评估的条件成立（会话作用域的 Stop 钩子包装器）。专用文档页面 `/en/goal` 已确认在线 | ✅ COMPLETE（Hot 行已添加在 Tasks 之后；描述根据文档框架与 `/loop` 和自动模式进行了比较） |
| 5 | 中 | 缺失概念（新） | **深度链接**（`claude-cli://open?repo=...&q=...`）在 v2.1.91 引入 — 用于运行手册/告警/仪表板的自定义 URL 方案。专用文档页面 `/en/deep-links` 已确认在线；从未在任何先前运行中在 CONCEPTS 中展示 | ✅ COMPLETE（Hot 行已添加在远程控制之后 — 两者都是会话启动界面；描述提到了运行手册/告警/仪表板用例和 OS 级别处理程序注册） |
| 6 | 低 | 缺失概念（新） | v2.1.139 添加了 `/scroll-speed` 命令 — 调整鼠标滚轮滚动速度，带实时预览 | ✋ ON HOLD（已推迟 — 小 UX 命令，无专用文档页面；最多只能作为 CLI 启动标志的子链接） |
| 7 | 高 | URL 过时（重复出现） | 命令 URL `/slash-commands` 不在官方站点地图中 — 重定向到 `/skills`；规范命令参考为 `/en/commands` | ❌ INVALID（自 2026-03-10 起重复出现；URL 仍可通过重定向解析；用户已在 22+ 次运行中选择保持原样） |
| 8 | 中 | 缺失概念（重复出现） | 专用代理重新标记了输出样式、权限、沙箱、无头模式、桌面应用、IDE 集成、.claude 目录、工具参考作为缺失的独立行 | ❌ INVALID（自 2026-03-10/2026-03-17/2026-04-08/2026-04-09/2026-05-01 起重复出现；用户认为所有都是平台界面或作为设置子链接涵盖 — 非独立概念） |
| 9 | 中 | 缺失概念（重复出现） | 专用代理标记了自动记忆需要独立于记忆的单独行 | ❌ INVALID（重复出现 — 当前记忆行已经通过内联链接展示了 `/en/memory#auto-memory` 和 `reports/claude-agent-memory.md`；用户选择的模式） |
| 10 | 低 | 验证 | 所有 4 个新候选 URL 通过 WebFetch 验证：`/en/worktrees`（在线，完整专用页面）、`/en/agent-view`（在线，研究预览横幅）、`/en/goal`（在线，/goal 命令页面）、`/en/deep-links`（在线，v2.1.91+ 横幅） | ✅ COMPLETE（所有 4 个新 URL 返回预期的规范页面） |
| 11 | 低 | 验证 | 本地徽章文件路径已验证 — `best-practice/`、`implementation/`、`reports/`、`.claude/`、`.mcp.json`、`CLAUDE.md` 目标在文件系统上存在 | ✅ COMPLETE（无缺失的本地文件） |
| 12 | 低 | 验证 | Beta 徽章时效性（规则 #7）— 获取了 `/en/agent-view` 并确认了 `<Note>` 横幅："代理视图是研究预览，需要 Claude Code v2.1.139 或更高版本" — 如果添加，beta 徽章将是准确的 | ✅ COMPLETE（徽章建议已在操作项 #3 中记录） |
| 13 | 低 | 验证 | 记忆锚点 `#organize-rules-with-clauderules` — 自 v2.1.113 以来稳定 | ✅ COMPLETE（稳定） |
| 14 | 低 | 验证 | Git Worktrees 锚点 — `/en/common-workflows` 中的标题已从 `#run-parallel-claude-code-sessions-with-git-worktrees` 重命名为 `#run-parallel-sessions-with-worktrees`（省略了"git"一词）；传统锚点仍可解析但不再是规范版本 | ⚠️ 已标记（在操作项 #2 下捕获；被视为过时 URL 操作的一部分，而非独立项目） |
| 15 | 低 | 验证 | 自动模式锚点 `#eliminate-prompts-with-auto-mode` — 自 v2.1.113 以来稳定 | ✅ COMPLETE（稳定） |
| 16 | 低 | 验证 | 捆绑技能锚点 `#bundled-skills` — 自 v2.1.113 以来稳定 | ✅ COMPLETE（稳定） |
| 17 | 低 | 验证 | Ultrareview 锚点 `#track-a-running-review` — 自 v2.1.118 以来稳定 | ✅ COMPLETE（稳定） |
| 18 | 低 | 验证 | claude-code-guide 交叉检查 — 独立研究佐证了 v2.1.139 的新增内容（代理视图、/goal、/scroll-speed）并发现了相同的深度链接页面；还重新发现了长期存在的平台界面概念（桌面、IDE 集成、.claude 目录、工具参考），这些根据用户策略为重复出现的 INVALID；无矛盾 | ✅ COMPLETE（两个代理在 v2.1.139 新发现上一致） |

---

## [2026-05-21 00:07 PKT] Claude Code v2.1.145

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 位置错误（新） | 检查点行（第 36 行）位置显示为 `automatic (git-based)` — 事实错误。实时获取 `/en/checkpointing` 确认检查点跟踪"其文件编辑工具所做的所有更改"，明确"不跟踪由 bash 命令修改的文件"，并且"不能替代版本控制" — *"将检查点视为'本地撤销'，将 Git 视为'永久历史'。"* 2026-04-24 运行仅检查了（空的）描述列，从未检查位置列，因此这个问题在所有先前运行中都未被发现。建议 `automatic (file-edit tracking)` | ✅ COMPLETE（用户已授权；第 36 行位置从 `automatic (git-based)` 更新为 `automatic (file-edit tracking)`） |
| 2 | 中 | 缺失概念（新） | **会话**有专用的 `/en/sessions` 页面（恢复、`/rename`、通过 `--fork-session` 分叉/分支）从未在任何先前运行的 CONCEPTS 中展示；concepts-agent 以 0.6 置信度标记为可能是运行时界面而非创作概念 | ❌ INVALID（用户选择跳过 — 与一贯的"平台/运行时界面，非配置概念"拒绝模式一致） |
| 3 | 高 | URL 过时（重复出现） | 命令 URL `/slash-commands` 不在官方站点地图中 — 重定向到 `/skills`；规范命令参考为 `/en/commands` | ❌ INVALID（自 2026-03-10 起重复出现；URL 仍可通过重定向解析；用户已在 23+ 次运行中选择保持原样） |
| 4 | 中 | 缺失概念（重复出现） | 专用代理 + claude-code-guide 代理重新标记了 IDE 集成、桌面应用、输出样式、权限、沙箱、无头模式、.claude 目录、工具参考作为缺失的独立行 | ❌ INVALID（自 2026-03-10/2026-03-17/2026-04-08/2026-05-01/2026-05-12 起重复出现；用户认为所有都是平台界面或作为设置/记忆子链接涵盖 — 非独立概念） |
| 5 | 低 | 验证 | 快速模式 URL `/en/fast-mode` 已实时获取 — 页面有效（"使用快速模式加速响应"），研究预览，`/fast` 切换 + `"fastMode": true` 设置，自 v2.1.142 以来 Opus 4.7 默认；解决了 concepts-agent 0.5 置信度的疑问 — README 快速模式行（第 52 行）完全准确 | ✅ COMPLETE（行已确认准确，无需更改） |
| 6 | 低 | 验证 | 通过原始 CHANGELOG.md 确认最新版本为 v2.1.145（blob URL 返回空正文 — 根据记录的工作区使用 raw.githubusercontent.com）；v2.1.145 添加了 JSON 会话列表和 OTEL 代理身份 — 无值得 CONCEPTS 关注的内容 | ✅ COMPLETE（版本已验证；徽章已在阶段 2.6 中从 v2.1.144 升级到 v2.1.145） |
| 7 | 低 | 验证 | 外部 CONCEPTS 文档 URL 经过抽查验证（`/en/checkpointing`、`/en/fast-mode`、原始 CHANGELOG）+ 其余部分自 v2.1.139 运行以来稳定 — 仅标记了反复出现的 `/slash-commands` 重定向 | ✅ COMPLETE（没有新的损坏 URL） |
| 8 | 低 | 验证 | 本地徽章文件路径 — 自 v2.1.139 以来无 CONCEPTS 表结构变更；`best-practice/`、`implementation/`、`reports/`、`.claude/`、`.mcp.json`、`CLAUDE.md` 目标稳定 | ✅ COMPLETE（自上次运行以来稳定） |
| 9 | 低 | 验证 | Beta 徽章时效性（规则 #7）— `/en/fast-mode` 确认了"研究预览"`<Note>` 横幅；README 中快速模式上的 `![beta]` 准确 | ✅ COMPLETE（无需降级） |
| 10 | 低 | 验证 | 锚点（`#organize-rules-with-clauderules`、`#run-parallel-...-worktrees`、`#eliminate-prompts-with-auto-mode`、`#bundled-skills`、`#track-a-running-review`）— 自 v2.1.113/v2.1.139 以来稳定 | ✅ COMPLETE（稳定） |
| 11 | 低 | 验证 | claude-code-guide 交叉检查 — 独立的 80 概念扫描佐证了覆盖率；发现了 Auto Dream + MCP 工具搜索作为可能的记忆/MCP 子链接，并重新发现了平台界面（重复出现的 INVALID）。其版本号不可靠（例如"MCP 于 2024 年 12 月引入"，模糊的 v 编号）— 所有日期依赖专用代理 + 实时获取；无影响 CONCEPTS 的矛盾 | ✅ COMPLETE（代理一致；指南的模糊版本记录已注意，未使用） |
