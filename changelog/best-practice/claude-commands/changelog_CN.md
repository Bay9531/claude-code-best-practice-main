# 命令报告 — 更新日志历史

## 状态图例

| 状态 | 含义 |
|------|------|
| ✅ `COMPLETE (reason)` | 已采取措施并成功解决 |
| ❌ `INVALID (reason)` | 发现结果不正确、不适用或有意为之 |
| ✋ `ON HOLD (reason)` | 操作延期 — 等待外部依赖或用户决定 |

---

## [2026-03-13 04:23 PM PKT] Claude Code v2.1.74

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 新字段 | 在元信息表中添加 `name` — 技能显示名称 | ❌ INVALID (仅技能字段, 不适用于命令元信息) |
| 2 | HIGH | 新字段 | 在元信息表中添加 `disable-model-invocation` — 防止自动加载 | ❌ INVALID (仅技能字段, 不适用于命令元信息) |
| 3 | HIGH | 新字段 | 在元信息表中添加 `user-invocable` — 从 `/` 菜单隐藏 | ❌ INVALID (仅技能字段, 不适用于命令元信息) |
| 4 | HIGH | 新字段 | 在元信息表中添加 `context` — fork 以在子代理上下文中运行 | ❌ INVALID (仅技能字段, 不适用于命令元信息) |
| 5 | HIGH | 新字段 | 在元信息表中添加 `agent` — context: fork 的子代理类型 | ❌ INVALID (仅技能字段, 不适用于命令元信息) |
| 6 | HIGH | 新字段 | 在元信息表中添加 `hooks` — 作用于技能的生命周期钩子 | ❌ INVALID (仅技能字段, 不适用于命令元信息) |
| 7 | HIGH | 新命令 | 添加 `/btw <question>` — 快速提出侧面问题而不加入对话 | ✅ COMPLETE (在 Session 标签中作为 #53 添加) |
| 8 | HIGH | 新命令 | 添加 `/hooks` — 管理工具事件的钩子配置 | ✅ COMPLETE (在 Extensions 标签中作为 #30 添加) |
| 9 | HIGH | 新命令 | 添加 `/insights` — 生成会话分析报告 | ✅ COMPLETE (在 Context 标签中作为 #17 添加) |
| 10 | HIGH | 新命令 | 添加 `/plugin` — 管理 Claude Code 插件 | ✅ COMPLETE (在 Extensions 标签中作为 #33 添加) |
| 11 | HIGH | 新命令 | 添加 `/skills` — 列出可用技能 | ✅ COMPLETE (在 Extensions 标签中作为 #35 添加) |
| 12 | HIGH | 新命令 | 添加 `/upgrade` — 打开升级页面以切换计划层级 | ✅ COMPLETE (在 Auth 标签中作为 #3 添加) |
| 13 | HIGH | 移除命令 | 移除 `/output-style` — 在 v2.1.73 中弃用, 请使用 `/config` 代替 | ✅ COMPLETE (从 Config 标签中移除) |
| 14 | HIGH | 移除命令 | 移除 `/bug` 行 — 现在列为 `/feedback` 的别名 | ✅ COMPLETE (已移除行, 在 /feedback 描述中添加 "别名: /bug") |
| 15 | HIGH | 更改描述 | 更新 `/passes` — 从审查通过重定为分享推荐 | ✅ COMPLETE (已更新描述, 保留在 Model 标签中) |
| 16 | HIGH | 更改描述 | 更新 `/review` — 已弃用, 由 `code-review` 市场插件取代 | ✅ COMPLETE (已在 Project 标签中更新描述) |
| 17 | MED | 更改描述 | 更新 `/stickers` — 从 UI 贴纸包改为订购实体贴纸 | ✅ COMPLETE (已在 Config 标签中更新描述) |

---

## [2026-03-15 12:50 PM PKT] Claude Code v2.1.76

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 新命令 | 在 Config 标签中添加 `/color [color|default]` — 设置当前会话的提示栏颜色 | ✅ COMPLETE (在 Config 标签中作为 #4 添加) |
| 2 | HIGH | 新命令 | 在 Model 标签中添加 `/effort [low|medium|high|max|auto]` — 设置模型努力级别 | ✅ COMPLETE (在 Model 标签中作为 #38 添加) |
| 3 | MED | 更改描述 | 更新 `/status` — 现在显示"打开设置界面 (状态标签)"而非"显示简洁的会话状态摘要" | ✅ COMPLETE (已在 Context 标签 #20 更新描述) |
| 4 | MED | 更改描述 | 更新 `/desktop` — 现在为"在 Claude Code 桌面应用中继续当前会话。仅限 macOS 和 Windows。" | ✅ COMPLETE (已在 Remote 标签 #49 更新描述) |
| 5 | LOW | 更改参数 | 更新 `/init` — 官方文档已删除 `[prompt]` 参数提示 | ✅ COMPLETE (已在 Project 标签 #45 移除 [prompt] 提示) |

---

## [2026-03-17 12:45 PM PKT] Claude Code v2.1.77

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 新别名 | 在 `/fork` 条目中添加 `别名: /branch` (v2.1.77 重命名 fork→branch) | ✅ COMPLETE (在 Session 标签 #59 的 /fork 中添加 "别名: /branch") |
| 2 | HIGH | 新别名 | 为 8 个命令添加别名: `/clear` (+/reset, /new), `/config` (+/settings), `/desktop` (+/app), `/exit` (+/quit), `/rewind` (+/checkpoint), `/resume` (+/continue), `/remote-control` (+/rc), `/mobile` (+/ios, /android) | ✅ COMPLETE (已为所有 8 个命令描述添加别名标注) |
| 3 | MED | 更改描述 | 更新 `/diff` — "打开交互式差异查看器, 显示未提交的更改和每轮差异" | ✅ COMPLETE (已在 Project 标签 #44 更新描述) |
| 4 | MED | 更改描述 | 更新 `/memory` — "编辑 CLAUDE.md 记忆文件, 启用或禁用自动记忆, 查看自动记忆条目" | ✅ COMPLETE (已在 Memory 标签 #37 更新描述) |
| 5 | MED | 更改描述 | 更新 `/copy` — "将最后一条助手回复复制到剪贴板。显示代码块的交互式选择器。" | ✅ COMPLETE (已在 Export 标签 #27 更新描述) |
| 6 | MED | 更改描述 | 更新 `/mobile` — "显示下载 Claude 移动应用的二维码" | ✅ COMPLETE (已在 Remote 标签 #52 更新描述 + 别名) |
| 7 | MED | 更改描述 | 更新 `/remote-control` — "使此会话可从 claude.ai 进行远程控制" | ✅ COMPLETE (已在 Remote 标签 #53 更新描述 + 别名) |
| 8 | LOW | 元信息范围 | 6 个仅技能字段仍不在报告中 (有意限定范围) | ❌ INVALID (仅技能字段 — 与 v2.1.74 运行相同的判定) |

---

## [2026-03-18 11:38 PM PKT] Claude Code v2.1.78

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 新命令 | 在 Config 标签中添加 `/voice` — 切换即按即说语音听写 | ✅ COMPLETE (在 Config 标签中作为 #15 添加) |
| 2 | HIGH | 倒置别名 | 交换 `/fork` → `/branch` 为主名称, `/fork` 为别名 | ✅ COMPLETE (已交换为 Session 标签 #56 的 `/branch`, 重新按字母排序) |
| 3 | MED | 新别名 | 添加 `/allowed-tools` 作为 `/permissions` 的别名 | ✅ COMPLETE (已在 Config 标签 #7 添加别名) |
| 4 | MED | 新参数 | 为 `/copy` 添加 `[N]` 参数语法 | ✅ COMPLETE (已在 Export 标签 #28 更新为 `/copy [N]`) |
| 5 | LOW | 元信息范围 | 6 个仅技能字段仍不在报告中 (有意限定范围) | ❌ INVALID (仅技能字段 — 与 v2.1.74 和 v2.1.77 运行相同的判定) |

---

## [2026-03-19 11:54 AM PKT] Claude Code v2.1.79

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | LOW | 元信息范围 | 6 个仅技能字段仍不在报告中 (有意限定范围) | ❌ INVALID (仅技能字段 — 与 v2.1.74、v2.1.77 和 v2.1.78 运行相同的判定) |

---

## [2026-03-20 08:33 AM PKT] Claude Code v2.1.80

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | MED | 新字段 | 在元信息表中添加 `effort` — 命令调用时覆盖模型努力级别 (v2.1.80) | ✅ COMPLETE (作为第 5 个字段添加, 后在添加完整字段集时重新定位到第 8 位) |
| 2 | HIGH | QA 修正 | 添加 6 个缺失字段 (`name`, `disable-model-invocation`, `user-invocable`, `context`, `agent`, `hooks`) — 官方文档说明命令支持"与技能相同的元信息"; 先前的 INVALID 判定 (v2.1.74–v2.1.79) 不正确 | ✅ COMPLETE (已添加所有 6 个字段, 计数从 5 更新到 11, 字段顺序与官方文档一致) |
| 3 | HIGH | 跨报告修复 | 在技能报告 (`claude-skills.md`) 中添加 `effort` — 该字段此前也缺失 | ✅ COMPLETE (已在技能报告中添加为第 8 个字段, 计数从 10 更新到 11) |

---

## [2026-03-21 09:08 PM PKT] Claude Code v2.1.81

无优先级操作项 — 报告与官方文档完全同步 (11 个元信息字段, 63 个内置命令)。

---

## [2026-03-23 09:48 PM PKT] Claude Code v2.1.81

无优先级操作项 — 报告与官方文档完全同步 (11 个元信息字段, 63 个内置命令)。

---

## [2026-03-25 08:07 PM PKT] Claude Code v2.1.83

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 新命令 | 在 Remote 标签中添加 `/schedule [description]` — 创建、更新、列出或运行云端定时任务 | ✅ COMPLETE (在 Remote 标签中作为 #56 添加, 计数从 63 更新到 64) |

---

## [2026-03-26 01:01 PM PKT] Claude Code v2.1.84

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 新字段 | 在元信息表中添加 `shell` — `!command` 块的 shell (`bash` 或 `powershell`) | ✅ COMPLETE (在 `hooks` 前添加为第 12 个字段, 计数从 11 更新到 12) |
| 2 | LOW | 更改参数 | 为 `/fast` 命令添加 `[on|off]` 参数提示 | ✅ COMPLETE (已在 Model 标签 #40 更新 `/fast` 为 `/fast [on|off]`) |

---

## [2026-03-27 06:25 PM PKT] Claude Code v2.1.85

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 新字段 | 在元信息表中添加 `paths` — 限制技能激活时机的 glob 模式 | ✅ COMPLETE (在 `user-invocable` 后添加为第 6 个字段, 计数从 12 更新到 13) |

---

## [2026-03-28 06:05 PM PKT] Claude Code v2.1.86

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | MED | 更改参数 | 更新 `/add-dir` — 根据官方文档添加 `<path>` 必需参数提示 | ✅ COMPLETE (已在 Project 标签 #44 更新) |
| 2 | MED | 更改参数 | 更新 `/branch` — 根据官方文档添加 `[name]` 可选参数提示 | ✅ COMPLETE (已在 Session 标签 #57 更新) |
| 3 | MED | 更改参数 | 更新 `/model` — 根据官方文档添加 `[model]` 可选参数提示 | ✅ COMPLETE (已在 Model 标签 #41 更新) |
| 4 | MED | 更改参数 | 更新 `/plan` — 根据官方文档添加 `[description]` 可选参数提示 | ✅ COMPLETE (已在 Model 标签 #43 更新) |
| 5 | MED | 更改参数 | 更新 `/pr-comments` — 根据官方文档添加 `[PR]` 可选参数提示 | ✅ COMPLETE (已在 Project 标签 #47 更新) |
| 6 | MED | 更改参数 | 更新 `/passes` — 移除 `[number]` 参数提示 (不在官方文档中) | ✅ COMPLETE (已在 Model 标签 #42 更新) |
| 7 | MED | 更改参数 | 更新 `/rename` — 根据官方文档从 `<name>` (必需) 改为 `[name]` (可选) | ✅ COMPLETE (已在 Session 标签 #62 更新) |
| 8 | LOW | 更改参数 | 更新 `/compact` — 根据官方文档将参数标签从 `[prompt]` 改为 `[instructions]` | ✅ COMPLETE (已在 Session 标签 #60 更新) |
| 9 | LOW | 更改参数 | 更新 `/feedback` — 根据官方文档将参数标签从 `[description]` 改为 `[report]` | ✅ COMPLETE (已在 Debug 标签 #24 更新) |

---

## [2026-03-31 06:55 PM PKT] Claude Code v2.1.88

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | MED | 描述同步 | 同步所有 43 个命令描述以匹配官方文档 — 行为澄清 (`/vim` 切换, `/sandbox` 切换, `/hooks` 查看), 扩展细节 (`/effort` 持久化, `/copy` SSH 写入, `/model` 努力箭头), 以及跨 Auth、Config、Context、Debug、Export、Extensions、Model、Project、Remote 和 Session 标签的措辞对齐 | ✅ COMPLETE (所有 64 个描述现在与 code.claude.com/docs/en/commands 的官方文档匹配) |

---

## [2026-04-01 12:26 PM PKT] Claude Code v2.1.89

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | LOW | 更改描述 | 更新 `/init` — 官方文档现在使用 `CLAUDE_CODE_NEW_INIT=1` 而非 `=true` | ✅ COMPLETE (环境变量值已从 `=true` 更新为 `=1` 以匹配官方文档) |

---

## [2026-04-02 09:14 PM PKT] Claude Code v2.1.90

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | MED | 更改描述 | 更新 `/permissions` — 官方文档扩展描述, 包括作用域规则、目录管理和自动模式拒绝审查的交互式对话框 | ✅ COMPLETE (描述已更新以匹配官方文档) |
| 2 | MED | 新别名 | 根据官方文档为 `/tasks` 命令添加 `/bashes` 别名 | ✅ COMPLETE (在 Debug 标签 #27 的 /tasks 中添加 "别名: /bashes") |

---

## [2026-04-03 08:34 PM PKT] Claude Code v2.1.91

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 新命令 | 在 Config 标签中添加 `/powerup` — 通过带有动画演示的快速交互式课程发现 Claude Code 功能 | ✅ COMPLETE (在 Debug 标签中作为 #26 添加 — 在 v2.1.92 运行中解决) |

---

## [2026-04-04 10:40 PM PKT] Claude Code v2.1.92

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 新命令 | 在 Debug 标签中添加 `/powerup` — 通过带有动画演示的快速交互式课程发现 Claude Code 功能 | ✅ COMPLETE (在 Debug 标签中作为 #26 添加, 从 v2.1.91 重复) |
| 2 | HIGH | 新命令 | 在 Auth 标签中添加 `/setup-bedrock` — 通过交互式向导配置 Amazon Bedrock 认证、区域和模型固定 | ✅ COMPLETE (在 Auth 标签中作为 #3 添加) |
| 3 | HIGH | 新命令 | 在 Model 标签中添加 `/ultraplan <prompt>` — 在超级计划会话中起草计划, 在浏览器中审阅, 然后远程执行或发回 | ✅ COMPLETE (在 Model 标签中作为 #45 添加) |
| 4 | HIGH | 移除命令 | 从 Config 标签中移除 `/vim` — 在 v2.1.92 中移除 (最大版本: 2.1.91), 请使用 `/config` 编辑器模式代替 | ✅ COMPLETE (已从 Config 标签移除) |
| 5 | HIGH | 移除命令 | 从 Project 标签中移除 `/pr-comments [PR]` — 在 v2.1.91 中移除 (最大版本: 2.1.90), 直接询问 Claude | ✅ COMPLETE (已从 Project 标签移除) |
| 6 | MED | 更改描述 | 更新 `/release-notes` — 现在显示"在交互式版本选择器中查看更新日志。选择特定版本查看其发布说明, 或选择显示所有版本。" | ✅ COMPLETE (已在 Debug 标签 #27 更新描述) |

---

## [2026-04-08 09:35 PM PKT] Claude Code v2.1.96

无优先级操作项 — 报告与官方文档完全同步 (13 个元信息字段, 65 个内置命令)。

---

## [2026-04-09 11:31 PM PKT] Claude Code v2.1.97

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 新命令 | 在 Remote 标签中添加 `/autofix-pr [prompt]` — 生成监视当前分支 PR 的网络会话, 在 CI 失败或审阅者留下评论时推送修复 | ✅ COMPLETE (在 Remote 标签中作为 #51 添加, 计数从 65 更新到 68) |
| 2 | HIGH | 新命令 | 在 Remote 标签中添加 `/teleport` — 将网络上的 Claude Code 会话拉入此终端。别名: `/tp` | ✅ COMPLETE (在 Remote 标签中作为 #59 添加) |
| 3 | HIGH | 新命令 | 在 Remote 标签中添加 `/web-setup` — 使用本地 `gh` CLI 凭据将 GitHub 账户连接到网络上的 Claude Code | ✅ COMPLETE (在 Remote 标签中作为 #60 添加) |
| 4 | MED | 更改描述 | 更新 `/add-dir` — 官方文档现在包含关于 `.claude/` 配置无法从添加的目录中被发现的说明 | ✅ COMPLETE (已在 Project 标签 #46 更新描述) |

---

## [2026-04-13 08:00 PM PKT] Claude Code v2.1.101

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 新命令 | 在 Auth 标签中添加 `/setup-vertex` — 通过交互式向导配置 Google Vertex AI 认证、项目、区域和模型固定。仅在设置了 `CLAUDE_CODE_USE_VERTEX=1` 时可见 | ✅ COMPLETE (在 Auth 标签中作为 #4 添加, 计数从 68 更新到 69) |

---

## [2026-04-14 11:13 PM PKT] Claude Code v2.1.107

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 新字段 | 在元信息表中添加 `when_to_use` — Claude 何时应调用技能的额外上下文, 附加到 `description` 后 (计数 13 → 14) | ✅ COMPLETE (在 `description` 字段后添加, 计数从 13 更新到 14) |
| 2 | HIGH | 新命令 | 在 Project 标签中添加 `/team-onboarding` — 从 Claude Code 使用历史生成团队入职指南 (计数 69 → 70) | ✅ COMPLETE (在 Project 标签中作为 #52 添加, 计数从 69 更新到 70) |
| 3 | MED | 范围决定 | 官方文档统一表中列出的 5 个捆绑技能 (`/batch`, `/claude-api`, `/debug`, `/loop`, `/simplify`) 但根据报告当前范围声明排除 | ❌ INVALID (用户选择保持报告仅限内置命令 — 免责声明保留) |
| 4 | MED | 更改描述 | 更新 `/doctor` — 添加"按 `f` 让 Claude 修复任何报告的问题" | ✅ COMPLETE (已向描述添加状态图标和 `f` 键修复细节) |
| 5 | MED | 更改描述 | 更新 `/schedule` — 术语从"云端定时任务"改为"例行程序" | ✅ COMPLETE (描述中的术语已更新) |

---

## [2026-04-16 08:20 PM PKT] Claude Code v2.1.110

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | MED | 新别名 | 在 `/rewind` 条目中添加 `/undo` 别名 — 在 v2.1.108 中添加 | ✅ COMPLETE (已在 Session 标签 #70 的现有 `/checkpoint` 别名旁添加 `/undo`) |

---

## [2026-04-18 07:54 PM PKT] Claude Code v2.1.114

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 新命令 | 在 Session 标签中添加 `/recap` — 按需生成当前会话的一行摘要 (v2.1.108) | ✅ COMPLETE (在 Session 标签中作为 #72 添加, 计数从 70 更新到 75) |
| 2 | HIGH | 新命令 | 在 Config 标签中添加 `/focus` — 切换专注视图, 仅显示上一个提示、工具调用摘要和最终回复 (v2.1.110) | ✅ COMPLETE (在 Config 标签中作为 #8 添加) |
| 3 | HIGH | 新命令 | 在 Config 标签中添加 `/tui [default|fullscreen]` — 设置终端 UI 渲染器并在保持对话完整的情况下重新启动 (v2.1.110) | ✅ COMPLETE (在 Config 标签中作为 #17 添加) |
| 4 | HIGH | 新命令 | 在 Project 标签中添加 `/ultrareview [PR]` — 在云端沙箱中运行深度多代理代码审查 (v2.1.111) | ✅ COMPLETE (在 Project 标签中作为 #56 添加) |
| 5 | HIGH | 新命令 | 在 Debug 标签中添加 `/heapdump` — 将 JavaScript 堆快照和内存分解写入 `~/Desktop` 用于诊断高内存使用 | ✅ COMPLETE (在 Debug 标签中作为 #28 添加) |
| 6 | HIGH | 更改描述 | 将 `/review` 从已弃用恢复为实时内置命令 — 根据官方文档 ("在当前会话中本地审查拉取请求。如需更深入的云端审查, 请参见 `/ultrareview`") — 撤销 v2.1.74 更新 | ✅ COMPLETE (已在 Project 标签 #53 更新描述, 现在引用 `/ultrareview`) |
| 7 | MED | 更改描述 | 更新 `/effort` 描述 — 官方现在列出 `xhigh` 级别, 无参数时打开交互式滑块 (v2.1.111) | ✅ COMPLETE (参数提示已更新以包含 `xhigh`, 描述中提到交互式滑块) |
| 8 | MED | 更改描述 | 更新 `/theme` 描述 — 官方添加"自动 (匹配终端)"选项 (v2.1.111) | ✅ COMPLETE (已在 Config 标签 #16 的描述中添加"自动 (匹配终端)") |
| 9 | MED | 更改描述 | 更新 `/model` 描述 — 官方注明在对话中途切换前会发出警告 (v2.1.108) | ✅ COMPLETE (已在 Model 标签 #46 添加对话中途警告细节) |
| 10 | MED | 新别名 | 根据官方文档为 `/schedule` 命令添加 `/routines` 别名 | ✅ COMPLETE (已在 Remote 标签 #64 添加 `别名: /routines`) |

---

## [2026-04-24 12:29 AM PKT] Claude Code v2.1.118

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 新字段 | 在元信息表中添加 `arguments` — 用于 `$name` 替换的命名位置参数 (计数 14 → 15) | ✅ COMPLETE (在 `argument-hint` 后添加, 计数从 14 更新到 15) |
| 2 | HIGH | 更改描述 | 更新 `/cost` — 现在只是 `/usage` 的别名 | ✅ COMPLETE (描述简化为" `/usage` 的别名") |
| 3 | HIGH | 更改描述 | 更新 `/stats` — 现在为 `/usage` 的别名, 打开统计标签 | ✅ COMPLETE (描述更新为" `/usage` 的别名。在统计标签上打开") |
| 4 | HIGH | 更改描述 | 更新 `/usage` — 规范命令, 整合 `/cost` 和 `/stats`; 注明别名 | ✅ COMPLETE (扩展为"显示会话成本、计划使用限制和活动统计。`/cost` 和 `/stats` 是别名") |
| 5 | MED | 更改参数 | 更新 `/voice` 签名至 `/voice [hold|tap|off]` | ✅ COMPLETE (签名和描述已更新) |
| 6 | MED | 更改描述 | 更新 `/theme` — 添加自定义主题支持 (`~/.claude/themes/`, 插件, "新建自定义主题…") | ✅ COMPLETE (自定义主题细节已添加到描述) |
| 7 | MED | 更改描述 | 更新 `/terminal-setup` — 替换终端列表 (移除 Warp; 添加 Cursor, Windsurf, Zed) | ✅ COMPLETE (终端列表已替换: VS Code, Cursor, Windsurf, Alacritty, Zed) |
| 8 | LOW | 更改描述 | 更新 `/effort` — 注明 `max` 级别仅限会话 | ✅ COMPLETE (已在描述中为 `max` 添加 "(仅限会话)" 限定语) |

---

## [2026-04-26 01:10 PM PKT] Claude Code v2.1.119

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 更改描述 | 更新 `/branch` — 添加 `CLAUDE_CODE_FORK_SUBAGENT` 环境变量说明, 解释 `/fork` 分歧 (v2.1.117) | ✅ COMPLETE (已在 Session 标签 #67 的描述后附加 fork-子代理说明) |
| 2 | MED | 更改描述 | 更新 `/focus` — 添加"仅在全屏渲染中可用"限定语 (v2.1.110) | ✅ COMPLETE (已在 Config 标签 #8 附加仅全屏限定语) |
| 3 | MED | 更改描述 | 更新 `/skills` — 添加"按 `t` 按令牌数排序" (v2.1.110/111) | ✅ COMPLETE (已在 Extensions 标签 #42 附加按令牌数排序细节) |
| 4 | MED | 更改描述 | 更新 `/clear` — 根据官方文档重新措辞以与 `/compact` 形成对比 | ✅ COMPLETE (已在 Session 标签 #69 将描述替换为"开始一个具有空上下文的新对话…请改用 `/compact`") |
| 5 | LOW | 范围决定 | 上游统一表中列出的 6 个捆绑技能 (`/batch`, `/claude-api`, `/debug`, `/fewer-permission-prompts`, `/loop`, `/simplify`) 但根据报告范围排除 | ❌ INVALID (从 v2.1.107 重复 — 用户此前选择保持报告仅限内置命令) |

---

## [2026-04-29 12:50 AM PKT] Claude Code v2.1.121

无优先级操作项 — 报告与官方文档完全同步 (15 个元信息字段, 75 个内置命令)。

---

## [2026-05-01 03:31 PM PKT] Claude Code v2.1.126

无优先级操作项 — 报告与官方文档完全同步 (15 个元信息字段, 75 个内置命令)。

---

## [2026-05-12 11:39 PM PKT] Claude Code v2.1.139

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 新命令 | 在 Session 标签中添加 `/background [prompt]` — 分离当前会话以作为后台代理运行。别名: `/bg` | ✅ COMPLETE (在 Session 标签中作为 #69 添加, 计数从 75 更新到 80) |
| 2 | HIGH | 新命令 | 在 Session 标签中添加 `/goal [condition|clear]` — Claude 跨轮次持续工作直到条件满足 (v2.1.139) | ✅ COMPLETE (在 Session 标签中作为 #75 添加) |
| 3 | HIGH | 新命令 | 在 Config 标签中添加 `/radio` — 在浏览器中打开 Claude FM 低保真电台 | ✅ COMPLETE (在 Config 标签中作为 #12 添加) |
| 4 | HIGH | 新命令 | 在 Config 标签中添加 `/scroll-speed` — 交互式调整鼠标滚轮滚动速度 (v2.1.139) | ✅ COMPLETE (在 Config 标签中作为 #14 添加) |
| 5 | HIGH | 新命令 | 在 Session 标签中添加 `/stop` — 停止当前后台会话; 转录和工作树被保留 | ✅ COMPLETE (在 Session 标签中作为 #80 添加) |
| 6 | LOW | 范围决定 | 上游统一表中列出的 6 个捆绑技能 (`/batch`, `/claude-api`, `/debug`, `/fewer-permission-prompts`, `/loop`, `/simplify`) 但根据报告范围排除 | ❌ INVALID (从 v2.1.107 和 v2.1.119 重复 — 用户此前选择保持报告仅限内置命令) |

---

## [2026-05-21 12:06 AM PKT] Claude Code v2.1.145

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 重命名命令 | 将 Context 标签中的 `/extra-usage` 重命名为 `/usage-credits` (v2.1.144); 保留 `/extra-usage` 记为曾用名; 在 Context 组内重新排序 (`e`→`u`) | ✅ COMPLETE (已在 Context 标签 #27 重命名, 移至 `/usage` 之后, 行 23-27 重新编号; 计数不变仍为 80) |
| 2 | MED | 新别名 | 为 `/feedback` 添加 `/share` 别名并扩展描述为"提交反馈、报告错误或分享您的对话。别名: `/bug`, `/share`" | ✅ COMPLETE (已在 Debug 标签 #29 更新描述) |
| 3 | LOW | 更改值 | 在 `effort` 元信息字段的选项列表中添加 `xhigh` (`low`, `medium`, `high`, `xhigh`, `max`) | ✅ COMPLETE (已在 effort 字段行中添加 `xhigh`; 值列表同步, 非字段增删) |
| 4 | LOW | 范围决定 | 上游统一表中的 9 个捆绑技能 (`/batch`, `/claude-api`, `/debug`, `/fewer-permission-prompts`, `/loop`, `/run`, `/run-skill-generator`, `/simplify`, `/verify`) 根据报告范围排除 | ❌ INVALID (从 v2.1.107/119/139 重复 — 报告有意限定于内置命令) |
