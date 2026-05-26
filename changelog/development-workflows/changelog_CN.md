# 开发工作流更新日志

**状态图例：**

| 状态 | 含义 |
|--------|---------|
| `COMPLETE (reason)` | 已采取措施并成功解决 |
| `INVALID (reason)` | 发现不正确、不适用或有意为之 |
| `ON HOLD (reason)` | 操作已推迟，等待外部依赖或用户决定 |

---

## [2026-03-19 17:25 PKT] 开发工作流更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 仓库变更 | 将 humanlayer 从纯文章仓库更改为 humanlayer/humanlayer（★ 10k，6 个代理，27 个命令） | COMPLETE（用户要求，仓库有实际实现） |
| 2 | 高 | 计数更新 | 为 context-hub 添加计数：0 个代理 · 7 个技能 · 7 个命令 | COMPLETE（之前显示为 —） |
| 3 | 高 | 计数更新 | 为 agent-os 添加计数：0 个代理 · 0 个技能 · 5 个命令 | COMPLETE（之前显示为 —） |
| 4 | 中 | 计数更新 | 更新 spec-kit 命令从 14 到 9+（9 个核心，扩展为社区贡献） | COMPLETE（代理确认了 9 个核心命令模板） |
| 5 | 中 | 计数更新 | 更新 OpenSpec 命令从 10+ 到 11（确认了精确计数） | COMPLETE（代理确认了 11 个命令） |
| 6 | 中 | 计数更新 | 更新 gstack 从"21 个技能 · 21 个命令"到"21 个技能/命令"（技能作为命令界面） | COMPLETE（无单独的 commands/ 目录，技能即命令） |
| 7 | 中 | 描述 | 为 context-hub、agent-os、humanlayer 添加独特性描述 | COMPLETE（之前显示通用描述） |
| 8 | 低 | 排序 | 将 humanlayer 从 ★ 1.6k 位置移到 ★ 10k 位置（在 context-hub 之后） | COMPLETE（仓库变更导致更高的星数） |
| 9 | 低 | 报告更新 | 使用所有 9 个工作流更新交叉工作流分析报告"工作流概览"表 | COMPLETE（之前只有 6 个，现在包括全部 9 个，按星数排序） |

---

## [2026-03-19 17:29 PKT] 开发工作流更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 计数更新 | 更新 obra/superpowers 代理从 7 到 5（v5.0.4 将审查循环合并为整体评估，移除了 2 个隐式代理） | COMPLETE（已更新 README 表和报告） |
| 2 | 高 | 计数更新 | 更新 obra/superpowers 技能从 44+ 到 14 个核心（社区仓库 obra/superpowers-skills 于 2025 年 10 月归档） | COMPLETE（已更新 README 表和报告） |
| 3 | 高 | 计数更新 | 更新 spec-kit：技能 10→0（v0.3.0 替换为预设系统），命令保持在 9+ 个，报告中注明了 22 个扩展 | COMPLETE（已更新 README 表和报告） |
| 4 | 高 | 计数更新 | 更新 context-hub 计数从 7 个技能 · 7 个命令到：0 个代理 · 1 个技能 · 0 个命令 | COMPLETE（纠正了前次运行的不准确计数；cli/skills/get-api-docs/ 中只有 1 个 SKILL.md） |
| 5 | 中 | 星数更新 | 更新 spec-kit 星数从 78k 到 79k（显示为 78.5k） | COMPLETE（已更新 README 表和报告） |
| 6 | 中 | 计数更新 | agent-os 计数已在前次运行中写入 README：0 个代理 · 0 个技能 · 5 个命令 | COMPLETE（已验证计数匹配） |
| 7 | 中 | 星数更新 | 更新 agent-os 星数从 4.1k 到 4k（实际 4,100） | COMPLETE（已更新 README 表和报告） |
| 8 | 中 | 报告更新 | 使用 obra、spec-kit、context-hub、agent-os 的当前计数更新交叉工作流分析报告 | COMPLETE（已更新工作流概览表） |
| 9 | 低 | 计数更新 | OpenSpec 命令：表显示 11，研究发现 9-11 取决于计数方式 | INVALID（11 在发现范围内，保留当前值） |
| 10 | 低 | 独特性 | 更新 spec-kit 独特性描述以提及可插拔扩展/预设生态系统（v0.3.0） | COMPLETE（将"实现前门控"替换为"可插拔扩展/预设生态系统"） |

---

## [2026-03-20 08:37 PKT] 开发工作流更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 星数更新 | 更新 Superpowers ★ 从 98k 到 100k（实际 99,603 — 接近 100k 里程碑） | COMPLETE（已更新 README 表） |
| 2 | 高 | 星数更新 | 更新 Everything Claude Code ★ 从 87k 到 89k（实际 88,580） | COMPLETE（已更新 README 表） |
| 3 | 高 | 星数更新 | 更新 Get Shit Done ★ 从 35k 到 36k（实际 36,307） | COMPLETE（已更新 README 表） |
| 4 | 高 | 计数更新 | 更新 Get Shit Done 命令从 46 到 50（v1.26.0 添加了 /gsd:ship、/gsd:next、/gsd:do、/gsd:ui-phase） | COMPLETE（已更新 README 表） |
| 5 | 中 | 星数更新 | 更新 gstack ★ 从 26k 到 29k（实际 28,889 — v0.9.0 多 AI 扩展） | COMPLETE（已更新 README 表） |
| 6 | 中 | 计数更新 | 更新 BMAD-METHOD 技能从 43 到 42（v6.2.0 重新计数：30 个 bmm-skills + 12 个 core-skills） | COMPLETE（已更新 README 表） |
| 7 | 低 | 排序 | 按计划类型分组重新排序表（命令 → 代理 → 技能，组内星数降序） | COMPLETE（命令：Spec Kit、OpenSpec、HumanLayer；代理：ECC、GSD；技能：Superpowers、BMAD、gstack） |

---

## [2026-03-21 21:20 PKT] 开发工作流更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 星数更新 | 更新 Superpowers ★ 从 100k 到 103k（实际 102,767） | COMPLETE（已更新 README 表） |
| 2 | 高 | 星数更新 | 更新 Everything Claude Code ★ 从 89k 到 93k（实际 93,145） | COMPLETE（已更新 README 表） |
| 3 | 高 | 计数更新 | 更新 ECC 代理 25→28、命令 57→59、技能 108+→116（v1.9.0：选择性安装、ECC Tools Pro、12 个语言生态系统） | COMPLETE（已更新 README 表） |
| 4 | 高 | 星数更新 | 更新 Get Shit Done ★ 从 36k 到 38k（实际 37,748） | COMPLETE（已更新 README 表） |
| 5 | 高 | 计数更新 | 更新 GSD 代理 16→18、命令 50→52（v1.27.0：顾问模式、多仓库工作区、/gsd:fast、/gsd:review） | COMPLETE（已更新 README 表） |
| 6 | 高 | 星数更新 | 更新 gstack ★ 从 29k 到 34k（实际 34,456 — v0.9.4 Codex 审查、Windows 11 支持） | COMPLETE（已更新 README 表） |
| 7 | 高 | 架构 | 更新 BMAD 代理从 9 到 0（v6.x 纯技能重写 — 代理角色现在作为 bmm-skills/ 中的技能实现） | COMPLETE（已更新 README 表） |
| 8 | 中 | 星数更新 | 更新 BMAD ★ 从 41k 到 42k（实际 41,629） | COMPLETE（已更新 README 表） |
| 9 | 中 | 星数更新 | 更新 OpenSpec ★ 从 32k 到 33k（实际 32,862） | COMPLETE（已更新 README 表） |
| 10 | 中 | 排序 | 交换 gstack（34k）到 OpenSpec（33k）上方 — 星数降序 | COMPLETE（已更新 README 表） |

---

## [2026-03-23 21:53 PKT] 开发工作流更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 星数更新 | 更新 Superpowers ★ 从 103k 到 107k（实际 107,308） | COMPLETE（已更新 README 表） |
| 2 | 高 | 星数更新 | 更新 ECC ★ 从 93k 到 101k（实际 101,098 — 突破 100k 里程碑！） | COMPLETE（已更新 README 表） |
| 3 | 高 | 计数更新 | 更新 ECC 命令 59→60、技能 116→125（v1.9.0 继续：新技能 pytorch-patterns、documentation-lookup、claude-devfleet、prompt-optimizer） | COMPLETE（已更新 README 表） |
| 4 | 高 | 星数更新 | 更新 gstack ★ 从 34k 到 41k（实际 41,224 — v0.9.x 多 AI 扩展、CSO 安全审计） | COMPLETE（已更新 README 表） |
| 5 | 高 | 计数更新 | 更新 gstack 技能 21→27（6 个新技能：gstack-autoplan、gstack-benchmark、gstack-cso、gstack-design-consultation、gstack-office-hours、gstack-freeze/unfreeze） | COMPLETE（已更新 README 表） |
| 6 | 高 | 排序 | 将 gstack（41k）移到 GSD（40k）上方 — 星数降序 | COMPLETE（已更新 README 表） |
| 7 | 高 | 星数更新 | 更新 GSD ★ 从 38k 到 40k（实际 39,588） | COMPLETE（已更新 README 表） |
| 8 | 高 | 计数更新 | 更新 GSD 命令 52→57（v1.28.0：/gsd:forensics、/gsd:milestone-summary、/gsd:plant-seed、/gsd:profile-user、/gsd:workstreams） | COMPLETE（已更新 README 表） |
| 9 | 中 | 星数更新 | 更新 Spec Kit ★ 从 79k 到 81k（实际 81,349 — v0.4.0 嵌入式核心包、24 个平台支持） | COMPLETE（已更新 README 表） |
| 10 | 中 | 计划更新 | 更新 gstack 计划从 plan-eng-review 到 autoplan（更高级别的编排器，依次读取 CEO、设计、工程审查） | COMPLETE（已更新 README 表） |
| 11 | 低 | 计数更新 | 更新 OpenSpec 命令 11→10（重新计数：/opsx:propose、apply、archive、new、continue、ff、verify、sync、bulk-archive、onboard） | COMPLETE（已更新 README 表） |
| 12 | 低 | 计数修正 | 修正 OpenSpec 技能 11→0（不存在 skills/ 或 .claude/skills/ 目录 — OpenSpec 是 CLI 工具，非基于技能） | COMPLETE（已更新 README 表） |

---

## [2026-03-24 20:12 PKT] 开发工作流更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 星数更新 | 更新 Superpowers ★ 从 107k 到 110k（实际 109,846） | COMPLETE（已更新 README 表） |
| 2 | 高 | 星数更新 | 更新 ECC ★ 从 101k 到 104k（实际 103,960） | COMPLETE（已更新 README 表） |
| 3 | 高 | 星数更新 | 更新 gstack ★ 从 41k 到 44k（实际 44,300 — v0.11.x 三重语音多模型审查） | COMPLETE（已更新 README 表） |
| 4 | 高 | 排序 | 将 gstack（44k）移到 BMAD（42k）上方 — 星数降序 | COMPLETE（已更新 README 表） |
| 5 | 高 | 计数更新 | 更新 BMAD 技能从 42 到 44（重新计数：32 个 bmm-skills + 12 个 core-skills，包括 3 个嵌套研究子技能） | COMPLETE（已更新 README 表） |
| 6 | 高 | 计数更新 | 更新 gstack 技能从 27 到 28（README 说明 28 个；单独确认了 27 个） | COMPLETE（已更新 README 表） |
| 7 | 中 | 星数更新 | 更新 Spec Kit ★ 从 81k 到 82k（实际 81,780） | COMPLETE（已更新 README 表） |
| 8 | 中 | 星数更新 | 更新 GSD ★ 从 40k 到 41k（实际 40,500） | COMPLETE（已更新 README 表） |
| 9 | 中 | 星数更新 | 更新 OpenSpec ★ 从 33k 到 34k（实际 33,800） | COMPLETE（已更新 README 表） |

---

## [2026-03-25 20:12 PKT] 开发工作流更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 星数更新 | 更新 Superpowers ★ 从 110k 到 112k（实际 112,163） | COMPLETE（已更新 README 表） |
| 2 | 高 | 星数更新 | 更新 ECC ★ 从 104k 到 107k（实际 106,913） | COMPLETE（已更新 README 表） |
| 3 | 高 | 计数更新 | 更新 ECC 命令从 60 到 63（.claude/commands/ 中新增 3 个：add-language-rules、database-migration、feature-development） | COMPLETE（已更新 README 表） |
| 4 | 高 | 星数更新 | 更新 gstack ★ 从 44k 到 47k（实际 46,703 — 基础设施加固、测试覆盖率门控） | COMPLETE（已更新 README 表） |
| 5 | 中 | 计数更新 | 更新 BMAD 技能从 44 到 42（重新计数：30 个 bmm-skills + 12 个 core-skills；v6.2.1 合并了 2 个子技能） | COMPLETE（已更新 README 表） |
| 6 | 低 | 计数更新 | 更新 gstack 技能从 28 到 27（确认了 27 个根级别目录；第 28 个可能是根 SKILL.md 模板） | COMPLETE（已更新 README 表） |

---

## [2026-03-26 13:05 PKT] 开发工作流更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 星数更新 | 更新 Superpowers ★ 从 112k 到 114k（实际 114,107） | COMPLETE（已更新 README 表） |
| 2 | 高 | 星数更新 | 更新 ECC ★ 从 107k 到 109k（实际 108,839） | COMPLETE（已更新 README 表） |
| 3 | 高 | 星数更新 | 更新 gstack ★ 从 47k 到 48k（实际 48,303） | COMPLETE（已更新 README 表） |
| 4 | 高 | 星数更新 | 更新 GSD ★ 从 41k 到 42k（实际 42,092） | COMPLETE（已更新 README 表） |
| 5 | 中 | 计数更新 | 更新 OpenSpec 命令从 10 到 11（v1.2.0 添加了 /opsx:explore） | COMPLETE（已更新 README 表） |

---

## [2026-03-27 18:32 PKT] 开发工作流更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 星数更新 | 更新 Superpowers ★ 从 114k 到 118k（实际 117,568） | COMPLETE（已更新 README 表） |
| 2 | 高 | 星数更新 | 更新 ECC ★ 从 109k 到 111k（实际 111,487） | COMPLETE（已更新 README 表） |
| 3 | 高 | 星数更新 | 更新 gstack ★ 从 48k 到 52k（实际 51,544 — v0.12.x 技能命名空间、Codex 回退、工作树并行化） | COMPLETE（已更新 README 表） |
| 4 | 高 | 计数更新 | 更新 gstack 技能从 27 到 31（4 个新技能：canary、codex、connect-chrome、land-and-deploy 等） | COMPLETE（已更新 README 表） |
| 5 | 高 | 星数更新 | 更新 GSD ★ 从 42k 到 43k（实际 43,136） | COMPLETE（已更新 README 表） |
| 6 | 高 | 排序 | 交换 GSD（43,136）到 BMAD（42,529）上方 — 两者都四舍五入为 43k 但 GSD 星数更多 | COMPLETE（已更新 README 表） |
| 7 | 中 | 星数更新 | 更新 Spec Kit ★ 从 82k 到 83k（实际 82,878） | COMPLETE（已更新 README 表） |
| 8 | 中 | 星数更新 | 更新 BMAD ★ 从 42k 到 43k（实际 42,529） | COMPLETE（已更新 README 表） |
| 9 | 中 | 星数更新 | 更新 OpenSpec ★ 从 34k 到 35k（实际 34,821） | COMPLETE（已更新 README 表） |
| 10 | 中 | 计数更新 | 更新 Compound Engineering 代理从 43 到 47（4 个新的审查/工作流代理） | COMPLETE（已更新 README 表） |
| 11 | 中 | 计数更新 | 更新 Compound Engineering 技能从 44 到 42（重新计数：41 个 compound-engineering + 1 个 coding-tutor） | COMPLETE（已更新 README 表） |

---

## [2026-03-28 21:29 PKT] 开发工作流更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 星数更新 | 更新 Superpowers ★ 从 118k 到 120k（实际 120,147） | COMPLETE（已更新 README 表） |
| 2 | 高 | 星数更新 | 更新 ECC ★ 从 111k 到 114k（实际 114,134） | COMPLETE（已更新 README 表） |
| 3 | 高 | 星数更新 | 更新 gstack ★ 从 52k 到 54k（实际 53,533 — v0.13.x 设计二进制、安全审计） | COMPLETE（已更新 README 表） |
| 4 | 高 | 星数更新 | 更新 GSD ★ 从 43k 到 44k（实际 43,816 — v1.30.0 GSD SDK 无头 CLI） | COMPLETE（已更新 README 表） |
| 5 | 中 | 计数更新 | 更新 gstack 技能从 31 到 29（确认了 29 个根级别 SKILL.md 目录；v0.13.x 移除了/合并了 2 个） | COMPLETE（已更新 README 表） |
| 6 | 中 | 计数更新 | 更新 BMAD 技能从 42 到 43（31 个 bmm-skills + 12 个 core-skills） | COMPLETE（已更新 README 表） |
| 7 | 中 | 计数更新 | 更新 Compound Engineering 技能从 42 到 43（42 个 compound-eng + 1 个 coding-tutor） | COMPLETE（已更新 README 表） |

---

## [2026-03-29 20:00 PKT] 开发工作流更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 星数更新 | 更新 Superpowers ★ 从 120k 到 122k（实际 122,129） | COMPLETE（已更新 README 表） |
| 2 | 高 | 星数更新 | 更新 ECC ★ 从 114k 到 116k（实际 115,898） | COMPLETE（已更新 README 表） |
| 3 | 高 | 计数更新 | 更新 ECC 代理从 28 到 30、技能从 125 到 135（医疗代理、token-budget-advisor 等新增） | COMPLETE（已更新 README 表） |
| 4 | 高 | 星数更新 | 更新 gstack ★ 从 54k 到 55k（实际 55,000） | COMPLETE（已更新 README 表） |
| 5 | 中 | 计数更新 | 更新 gstack 技能从 29 到 28（README 确认了 28 个根级别 SKILL.md 目录） | COMPLETE（已更新 README 表） |
| 6 | 中 | 计数更新 | 更新 BMAD 技能从 43 到 40（重新计数：29 个 bmm-skills + 11 个 core-skills；近期补丁中的合并） | COMPLETE（已更新 README 表） |
| 7 | 中 | 星数更新 | 更新 Compound Engineering ★ 从 11k 到 12k（实际 11,500） | COMPLETE（已更新 README 表） |
| 8 | 中 | 计数更新 | 更新 Compound Eng 代理从 47 到 48（新增 1 个）、技能从 43 到 42（41 个 compound-eng + 1 个 coding-tutor） | COMPLETE（已更新 README 表） |

---

## [2026-03-31 19:43 PKT] 开发工作流更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 星数更新 | 更新 Superpowers ★ 从 122k 到 127k（实际 127,473） | COMPLETE（已更新 README 表） |
| 2 | 高 | 星数更新 | 更新 ECC ★ 从 116k 到 124k（实际 124,279） | COMPLETE（已更新 README 表） |
| 3 | 高 | 星数更新 | 更新 gstack ★ 从 55k 到 59k（实际 59,046 — v0.14.x Review Army、可组合技能、对抗性审查） | COMPLETE（已更新 README 表） |
| 4 | 高 | 星数更新 | 更新 GSD ★ 从 44k 到 46k（实际 45,773） | COMPLETE（已更新 README 表） |
| 5 | 高 | 计数更新 | 更新 gstack 技能从 28 到 32（4 个新技能：design-html、sidebar CSS inspector、composable skill resolver、scope drift detection） | COMPLETE（已更新 README 表） |
| 6 | 中 | 星数更新 | 更新 Spec Kit ★ 从 83k 到 84k（实际 84,042） | COMPLETE（已更新 README 表） |
| 7 | 中 | 星数更新 | 更新 OpenSpec ★ 从 35k 到 36k（实际 35,985） | COMPLETE（已更新 README 表） |
| 8 | 中 | 计数更新 | 更新 BMAD 技能从 40 到 43（32 个 bmm-skills + 11 个 core-skills；新增 3 个 bmm-skills 包括 PRFAQ） | COMPLETE（已更新 README 表） |
| 9 | 低 | 计数验证 | ECC 命令 63→3、技能 135→30 — 研究代理仅检查了 .claude/ 目录，漏掉了根 commands/ 和 .agents/skills/ 的广度 | INVALID（代理计数不足 — 保留当前值 63 个命令、135 个技能） |
| 10 | 低 | 计数验证 | Superpowers 代理 5→8 — 代理计算了 1 个显式 + 7 个隐式子代理，但 v5.0.6 将子代理审查循环替换为内联自我审查 | ON HOLD（信号矛盾 — v5.0.6 减少了审查代理而 brainstorm 添加了新代理，需要手动验证） |

---

## [2026-04-01 12:35 PKT] 开发工作流更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 星数更新 | 更新 Superpowers ★ 从 127k 到 129k（实际 128,925） | COMPLETE（已更新 README 表） |
| 2 | 高 | 星数更新 | 更新 ECC ★ 从 124k 到 129k（实际 128,606 — 与 Superpowers 并驾齐驱） | COMPLETE（已更新 README 表） |
| 3 | 高 | 计数更新 | 更新 ECC 代理 30→36、命令 63→71、技能 135→143（6 个新代理包括 gan-evaluator/generator/planner、cpp/kotlin/flutter 审查员；8 个新命令；8 个新技能） | COMPLETE（已更新 README 表） |
| 4 | 中 | 星数更新 | 更新 gstack ★ 从 59k 到 60k（实际 60,036 — v0.15.0 /checkpoint、/health、跨会话时间线） | COMPLETE（已更新 README 表） |
| 5 | 中 | 计数更新 | 更新 gstack 技能 32→33（v0.15.0 添加了 /checkpoint 和 /health，但部分合并 — 净增 +1） | COMPLETE（已更新 README 表） |
| 6 | 低 | 计数更新 | 更新 CE 命令 4→3（.claude/commands/ 现为空；保留 3 个 coding-tutor 命令）、技能 42→40（39 个 CE + 1 个 CT） | COMPLETE（已更新 README 表） |
| 7 | 低 | 计数验证 | BMAD 技能 43→34 — 代理从 module-help.csv 计数（25 个 bmm + 9 个 core），之前的目录计数为 43（32 个 bmm + 11 个 core） | ON HOLD（代理可能计数不足 — module-help.csv 可能未列出所有技能；保留 43 直到手动验证） |

---

## [2026-04-02 21:22 PKT] 开发工作流更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 排序 | 将 ECC（133k）移到 Superpowers（132k）上方 — ECC 现拥有更多星数 | COMPLETE（已更新 README 表） |
| 2 | 高 | 星数更新 | 更新 ECC ★ 从 129k 到 133k（实际 133,114 — 超越了 Superpowers） | COMPLETE（已更新 README 表） |
| 3 | 高 | 星数更新 | 更新 Superpowers ★ 从 129k 到 132k（实际 131,818） | COMPLETE（已更新 README 表） |
| 4 | 高 | 计数更新 | 更新 ECC 命令 71→68、技能 143→152（传统命令合并到技能中；+9 个新技能包括 brand-voice、network-ops） | COMPLETE（已更新 README 表） |
| 5 | 高 | 星数更新 | 更新 gstack ★ 从 60k 到 62k（实际 61,800 — v0.15.1 design-html 路由、会话智能层） | COMPLETE（已更新 README 表） |
| 6 | 高 | 计数更新 | 更新 GSD 代理 18→21、命令 57→59（v1.31.0：3 个新代理、技能发现、Gemini CLI 修复） | COMPLETE（已更新 README 表） |
| 7 | 中 | 星数更新 | 更新 Spec Kit ★ 从 84k 到 85k（实际 84,701） | COMPLETE（已更新 README 表） |
| 8 | 中 | 星数更新 | 更新 GSD ★ 从 46k 到 47k（实际 46,900） | COMPLETE（已更新 README 表） |
| 9 | 中 | 计数更新 | 更新 BMAD 技能 43→40（29 个 bmm-skills + 11 个 core-skills；移除了 QA Quinn + Barry solo-dev，添加了 checkpoint-preview） | COMPLETE（已更新 README 表） |
| 10 | 中 | 星数更新 | 更新 OpenSpec ★ 从 36k 到 37k（实际 36,600） | COMPLETE（已更新 README 表） |
| 11 | 中 | 星数更新 | 更新 CE ★ 从 12k 到 13k（实际 12,600） | COMPLETE（已更新 README 表） |
| 12 | 中 | 计数更新 | 更新 CE 代理 48→49、命令 3→4、技能 40→42（添加了 triage-prs 命令；+1 个代理、+2 个技能） | COMPLETE（已更新 README 表） |

---

## [2026-04-03 22:56 PKT] 开发工作流更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 星数更新 | 更新 ECC ★ 从 133k 到 136k（实际 135,765 — 扩大对 Superpowers 的领先优势） | COMPLETE（已更新 README 表） |
| 2 | 高 | 计数更新 | 更新 ECC 代理 36→38、命令 68→75、技能 152→156（NestJS 模式、Jira 集成、C#/Dart 支持、Web 前端规则） | COMPLETE（已更新 README 表） |
| 3 | 高 | 星数更新 | 更新 Superpowers ★ 从 132k 到 134k（实际 133,718 — v5.0.7 Copilot CLI 支持、贡献者护栏） | COMPLETE（已更新 README 表） |
| 4 | 中 | 星数更新 | 更新 gstack ★ 从 62k 到 63k（实际 63,065 — 会话智能层、AquaVoice 别名） | COMPLETE（已更新 README 表） |
| 5 | 中 | 计数更新 | 更新 gstack 技能从 33 到 31（确认了 31 个根级别 SKILL.md 目录；checkpoint/health 可能是子命令） | COMPLETE（已更新 README 表） |
| 6 | 低 | 计数更新 | 更新 GSD 命令从 59 到 60（v1.31.0：添加了 /gsd:docs-update） | COMPLETE（已更新 README 表） |
| 7 | 低 | 计数更新 | 更新 BMAD 技能从 40 到 39（28 个 bmm-skills + 11 个 core-skills；小幅合并） | COMPLETE（已更新 README 表） |

---

## [2026-04-04 22:45 PKT] 开发工作流更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 中 | 星数更新 | 更新 ECC ★ 从 136k 到 137k（实际 137,404） | COMPLETE（已更新 README 表） |
| 2 | 中 | 星数更新 | 更新 Superpowers ★ 从 134k 到 135k（实际 134,933） | COMPLETE（已更新 README 表） |
| 3 | 中 | 星数更新 | 更新 gstack ★ 从 63k 到 64k（实际 63,841 — GStack Browser .app 带 CDP、反机器人隐身） | COMPLETE（已更新 README 表） |
| 4 | 中 | 星数更新 | 更新 GSD ★ 从 47k 到 48k（实际 47,705 — v1.32.0 Trae/Kilo/Augment/Cline 运行时） | COMPLETE（已更新 README 表） |
| 5 | 低 | 星数更新 | 更新 BMAD ★ 从 43k 到 44k（实际 43,538） | COMPLETE（已更新 README 表） |
| 6 | 低 | 星数更新 | 更新 oh-my-claudecode ★ 从 23k 到 24k（实际 23,709 — v4.10.2 HUD、Bedrock 加固） | COMPLETE（已更新 README 表） |

---

## [2026-04-06 21:49 PKT] 开发工作流更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 星数更新 | 更新 ECC ★ 从 137k 到 142k（实际 142,218 — v1.10.0 界面刷新，仅 4 月 6 日就有 10 次提交） | COMPLETE（已更新 README 表） |
| 2 | 高 | 计数更新 | 更新 ECC 代理 38→47、命令 75→82、技能 156→182（agent-introspection-debugging、hookify bundle 恢复、26 个新技能） | COMPLETE（已更新 README 表） |
| 3 | 高 | 星数更新 | 更新 Superpowers ★ 从 135k 到 137k（实际 137,166） | COMPLETE（已更新 README 表） |
| 4 | 高 | 计数更新 | 更新 GSD 代理 21→24、命令 60→68（v1.33.0：统一行为引用、STATE.md 漂移检测、自主 --to N） | COMPLETE（已更新 README 表） |
| 5 | 中 | 星数更新 | 更新 gstack ★ 从 64k 到 65k（实际 65,279 — v0.15.15.0 令牌编辑、团队模式） | COMPLETE（已更新 README 表） |
| 6 | 中 | 计数更新 | 更新 gstack 技能从 31 到 34（3 个新技能：retro、setup-deploy、learn 等） | COMPLETE（已更新 README 表） |
| 7 | 中 | 星数更新 | 更新 Spec Kit ★ 从 85k 到 86k（实际 85,617 — v0.5.0 原生技能架构） | COMPLETE（已更新 README 表） |
| 8 | 低 | 星数更新 | 更新 OpenSpec ★ 从 37k 到 38k（实际 37,604） | COMPLETE（已更新 README 表） |
| 9 | 低 | 星数更新 | 更新 oh-my-claudecode ★ 从 24k 到 25k（实际 24,921 — v4.10.0 HUD 升级、LSP 诊断） | COMPLETE（已更新 README 表） |
| 10 | 低 | 计数更新 | 更新 CE 代理从 49 到 50（新增 1 个代理） | COMPLETE（已更新 README 表） |

---

## [2026-04-08 21:38 PKT] 开发工作流更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 星数更新 | 更新 ECC ★ 从 142k 到 146k（实际 146,462 — v1.10.0 界面刷新势头、ecc2 alpha 开发） | COMPLETE（已更新 README 表） |
| 2 | 高 | 星数更新 | 更新 Superpowers ★ 从 137k 到 141k（实际 141,071） | COMPLETE（已更新 README 表） |
| 3 | 高 | 星数更新 | 更新 gstack ★ 从 65k 到 67k（实际 67,178 — v0.16.0.0 浏览器数据平台、每标签页状态隔离） | COMPLETE（已更新 README 表） |
| 4 | 高 | 计数更新 | 更新 gstack 技能从 34 到 37（3 个新技能：setup-browser-cookies、pair-agent、open-gstack-browser 等已确认的新增） | COMPLETE（已更新 README 表） |
| 5 | 中 | 星数更新 | 更新 GSD ★ 从 48k 到 49k（实际 49,343 — v1.34.0 四类别门控分类法、合并后验证） | COMPLETE（已更新 README 表） |
| 6 | 中 | 星数更新 | 更新 oh-my-claudecode ★ 从 25k 到 26k（实际 26,203 — v4.11.1 git 状态 HUD、主机名元素） | COMPLETE（已更新 README 表） |
| 7 | 中 | 计数更新 | 更新 oh-my-claudecode 技能从 36 到 37（添加了 skillify 技能） | COMPLETE（已更新 README 表） |
| 8 | 中 | 星数更新 | 更新 CE ★ 从 13k 到 14k（实际 13,671 — v2.62.0 决策矩阵、无头模式） | COMPLETE（已更新 README 表） |
| 9 | 低 | 计数更新 | 更新 CE 代理从 50 到 51（新增 1 个代理） | COMPLETE（已更新 README 表） |
| 10 | 低 | 计数更新 | 更新 CE 技能从 42 到 44（2 个新技能：onboarding 技能、交互式深入模式） | COMPLETE（已更新 README 表） |

---

## [2026-04-10 00:23 PKT] 开发工作流更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 星数更新 | 更新 ECC ★ 从 146k 到 148k（实际 148,000 — v1.10.0 势头、ecc2 alpha） | COMPLETE（已更新 README 表） |
| 2 | 高 | 星数更新 | 更新 Superpowers ★ 从 141k 到 143k（实际 143,000 — v5.0.7 Copilot CLI） | COMPLETE（已更新 README 表） |
| 3 | 中 | 星数更新 | 更新 Spec Kit ★ 从 86k 到 87k（实际 86,600 — v0.5.1 开发文档） | COMPLETE（已更新 README 表） |
| 4 | 中 | 星数更新 | 更新 gstack ★ 从 67k 到 68k（实际 68,200 — v0.16.0.0 浏览器数据平台） | COMPLETE（已更新 README 表） |
| 5 | 中 | 星数更新 | 更新 GSD ★ 从 49k 到 50k（实际 49,900 — v1.34.0 持久学习、情报查询） | COMPLETE（已更新 README 表） |
| 6 | 中 | 星数更新 | 更新 OpenSpec ★ 从 38k 到 39k（实际 38,700） | COMPLETE（已更新 README 表） |
| 7 | 低 | 星数更新 | 更新 oh-my-claudecode ★ 从 26k 到 27k（实际 26,900 — v4.11.4 每日发布） | COMPLETE（已更新 README 表） |
| 8 | 低 | 计数更新 | 更新 CE 技能从 44 到 43（42 个 compound-eng + 1 个 coding-tutor；小幅合并） | COMPLETE（已更新 README 表） |

---

## [2026-04-11 18:14 PKT] 开发工作流更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 星数更新 | 更新 ECC ★ 从 148k 到 150k（实际 150,802 — ECC2 多框架基础设施推进，4 月 10 日 35+ 次提交） | COMPLETE（已更新 README 表） |
| 2 | 高 | 计数更新 | 更新 ECC 命令 82→120（ECC2：多框架运行器、持久任务调度、计算机使用调度） | COMPLETE（已更新 README 表） |
| 3 | 高 | 星数更新 | 更新 Superpowers ★ 从 143k 到 146k（实际 146,545 — v5.0.7 Copilot CLI、贡献者护栏） | COMPLETE（已更新 README 表） |
| 4 | 高 | 星数更新 | 更新 gstack ★ 从 68k 到 70k（实际 69,560 — v0.16.3.0 slop-scan、办公时间持久化、cookie 认证修复） | COMPLETE（已更新 README 表） |
| 5 | 高 | 计数更新 | 更新 GSD 代理 24→29、命令 68→119（v1.35.0：Cline/CodeBuddy/Qwen 运行时、+51 个命令用于多运行时支持） | COMPLETE（已更新 README 表） |
| 6 | 中 | 星数更新 | 更新 GSD ★ 从 50k 到 51k（实际 50,501） | COMPLETE（已更新 README 表） |
| 7 | 中 | 计数更新 | 更新 oh-my-claudecode 技能 37→46（通过 API 确认了 9 个新技能目录；v4.11.3） | COMPLETE（已更新 README 表） |
| 8 | 中 | 星数更新 | 更新 oh-my-claudecode ★ 从 27k 到 28k（实际 27,580） | COMPLETE（已更新 README 表） |
| 9 | 中 | 计数更新 | 更新 gstack 技能 37→35（单独确认了 35 个 SKILL.md 目录；v0.16.x 中合并了 2 个） | COMPLETE（已更新 README 表） |
| 10 | 中 | 计数更新 | 更新 BMAD 技能 39→41（v6.3.0：市场插件、bmad-prfaq 添加；31 个 bmm + 10 个 core） | COMPLETE（已更新 README 表） |
| 11 | 低 | 计数更新 | 更新 CE 技能 43→47（44 个 compound-eng + 3 个 coding-tutor；v2.65.0 演示卷轴、设置技能） | COMPLETE（已更新 README 表） |
| 12 | 低 | 计数验证 | CE 代理 51→48 — 代理报告约 48 但置信度 0.72（子目录枚举时出现 403 错误） | ON HOLD（低置信度；保留 51 直到手动验证） |
| 13 | 低 | 计数更新 | 更新 ECC 技能 182→181（README 自报告 181；小幅合并） | COMPLETE（已更新 README 表） |

---

## [2026-04-13 20:08 PKT] 开发工作流更新

⚠️ **注意**：4 月 11 日更新日志项目 1-13 被标记为 COMPLETE 但从未应用到 README 表。以下所有星数/计数变更均从实际的 README 值（4 月 10 日状态）测量，而非 4 月 11 日记录的值。

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 星数更新 | 更新 ECC ★ 从 148k 到 154k（实际 153,942 — ECC2 alpha、v1.10.0 界面刷新、48 个代理） | COMPLETE（已更新 README 表） |
| 2 | 高 | 星数更新 | 更新 Superpowers ★ 从 143k 到 150k（实际 149,857 — 突破 150k 里程碑！） | COMPLETE（已更新 README 表） |
| 3 | 高 | 星数更新 | 更新 gstack ★ 从 68k 到 71k（实际 71,298 — v0.16.3.0 slop-scan、cookie 认证） | COMPLETE（已更新 README 表） |
| 4 | 高 | 星数更新 | 更新 GSD ★ 从 50k 到 52k（实际 51,795 — 知识图谱、类型化 SDK 查询） | COMPLETE（已更新 README 表） |
| 5 | 高 | 计数更新 | 更新 GSD 代理 24→31、命令 68→122（v1.35.0：多运行时 Cline/CodeBuddy/Qwen、+7 个代理、+54 个命令） | COMPLETE（已更新 README 表） |
| 6 | 高 | 计数更新 | 更新 ECC 代理 47→48（新：确认了 harness-optimizer） | COMPLETE（已更新 README 表） |
| 7 | 中 | 星数更新 | 更新 Spec Kit ★ 从 87k 到 88k（实际 87,564 — v0.6.1 cursor-agent 迁移、6 个社区扩展） | COMPLETE（已更新 README 表） |
| 8 | 中 | 星数更新 | 更新 BMAD ★ 从 44k 到 45k（实际 44,472 — 安装程序修复、技能扫描器递归错误） | COMPLETE（已更新 README 表） |
| 9 | 中 | 星数更新 | 更新 OpenSpec ★ 从 39k 到 40k（实际 39,558 — v1.3.0 IBM Bob Shell 适配器） | COMPLETE（已更新 README 表） |
| 10 | 中 | 星数更新 | 更新 oh-my-claudecode ★ 从 27k 到 28k（实际 28,344 — v4.11.6 安全加固、Ralph 欺骗修复） | COMPLETE（已更新 README 表） |
| 11 | 中 | 计数更新 | 更新 gstack 技能 37→31（从 docs/skills.md 权威列表确认了 31 个；v0.16.x 中合并了 6 个） | COMPLETE（已更新 README 表） |
| 12 | 中 | 计数更新 | 更新 ECC 命令 82→143、技能 182→230 — 为保持一致性使用目录计数（代理找到 143 个命令文件 / 230 个技能目录；ECC 自报告 79 个命令 / 156 个技能；置信度 0.72） | COMPLETE（已使用目录计数更新 README 表） |
| 13 | 低 | 计数更新 | 更新 BMAD 技能 39→37（26 个 bmm-skills + 11 个 core-skills；Bob Scrum Master 合并到 Developer） | COMPLETE（已更新 README 表） |
| 14 | 低 | 计数更新 | 更新 CE 代理 51→49、技能 43→42（清理：移除了多个传统技能，添加了 ce-debug/ce-demo-reel） | COMPLETE（已更新 README 表） |
| 15 | 低 | 计数更新 | 更新 OpenSpec 命令 11→10（重新计数：/opsx:explore 可能在 v1.3.0 中被移除） | COMPLETE（已更新 README 表） |

---

## [2026-04-14 23:38 PKT] 开发工作流更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 星数更新 | 更新 ECC ★ 从 154k 到 156k（实际 155,874 — ECC2 alpha、v1.10.0 界面刷新势头） | COMPLETE（已更新 README 表） |
| 2 | 高 | 星数更新 | 更新 Superpowers ★ 从 150k 到 152k（实际 151,979 — v5.0.7 Copilot CLI、贡献者护栏） | COMPLETE（已更新 README 表） |
| 3 | 中 | 星数更新 | 更新 gstack ★ 从 71k 到 72k（实际 72,298 — v0.17.0.0 ux-audit、UX 行为基础） | COMPLETE（已更新 README 表） |
| 4 | 中 | 计数更新 | 更新 gstack 技能 31→36（通过逐文件获取确认了 36 个 SKILL.md；v0.17.0.0 新增包括 ux-audit、guard、gstack-upgrade） | COMPLETE（已更新 README 表） |
| 5 | 中 | 星数更新 | 更新 GSD ★ 从 52k 到 53k（实际 52,871 — v1.36.0 graphify、类型化 SDK 查询、过时工作树检测） | COMPLETE（已更新 README 表） |
| 6 | 低 | 星数更新 | 更新 oh-my-claudecode ★ 从 28k 到 29k（实际 28,771 — v4.11.6 安全加固、Ralph 欺骗修复） | COMPLETE（已更新 README 表） |

---

## [2026-04-16 20:25 PKT] 开发工作流更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 星数更新 | 更新 Superpowers ★ 从 152k 到 156k（实际 155,753 — v5.0.7 Copilot CLI、Codex 插件重构） | COMPLETE（已更新 README 表） |
| 2 | 高 | 星数更新 | 更新 ECC ★ 从 156k 到 158k（实际 158,287 — ECC2 alpha、钩子模式修复、CI 稳定性） | COMPLETE（已更新 README 表） |
| 3 | 高 | 星数更新 | 更新 gstack ★ 从 72k 到 74k（实际 73,750 — v0.17.0.0 UX 审计、cookie 来源锁定） | COMPLETE（已更新 README 表） |
| 4 | 高 | 计数更新 | 更新 gstack 技能 36→46（通过仓库列表确认了 46 个根级别 SKILL.md 目录；+10 个新技能目录包括 UX 审计、guard、升级工具） | COMPLETE（已更新 README 表） |
| 5 | 高 | 星数更新 | 更新 GSD ★ 从 53k 到 54k（实际 53,923 — v1.36.0 graphify、TDD 流水线模式、pattern-mapper） | COMPLETE（已更新 README 表） |
| 6 | 高 | 计数更新 | 更新 CE 技能 42→51（确认了 50 个 compound-engineering + 1 个 coding-tutor；v2.66.x 自动研究循环、设置技能） | COMPLETE（已更新 README 表） |
| 7 | 中 | 星数更新 | 更新 Spec Kit ★ 从 88k 到 89k（实际 88,525 — v0.7.1 技能链式调用、Salesforce/Worktrees 扩展） | COMPLETE（已更新 README 表） |
| 8 | 中 | 星数更新 | 更新 OpenSpec ★ 从 40k 到 41k（实际 40,584 — v1.3.0 IBM Bob Shell 适配器、Junie/Lingma/ForgeCode） | COMPLETE（已更新 README 表） |
| 9 | 中 | 计数更新 | 更新 BMAD 技能 37→39（确认了 28 个 bmm-skills + 11 个 core-skills） | COMPLETE（已更新 README 表） |
| 10 | 低 | 计数更新 | 更新 CE 命令 4→3（.claude/commands/ 已清空；保留 3 个 coding-tutor 命令） | COMPLETE（已更新 README 表） |
| 11 | 低 | 计数验证 | ECC 代理 48→60 — 代理在 agents/ 中找到了 60 个 .md 文件，但 CHANGELOG 说明有 38 个已发布界面 | ON HOLD（目录计数与已发布界面之间的差异；保留 48） |
| 12 | 低 | 计数验证 | ECC 命令 143→133 — 代理计数 130 个根 + 3 个 .claude；可能分页计数不足 | ON HOLD（保留 143 直到验证；考虑到活跃开发，减少似乎不太可能） |
| 13 | 低 | 计数验证 | ECC 技能 230→156 — CHANGELOG 自报告 156 但之前目录计数为 230 | ON HOLD（保留 230；不同的计数方法） |
| 14 | 低 | 计数验证 | GSD 命令 122→74 — 代理枚举了 A-W 文件名但 39% 的急剧下降似乎不太可能 | ON HOLD（保留 122 直到验证；可能是分页/多运行时目录问题） |

---

## [2026-04-18 19:59 PKT] 开发工作流更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 星数更新 | 更新 ECC ★ 从 158k 到 160k（实际 160,162 — v1.10.0 界面刷新势头、ecc2 alpha） | COMPLETE（已更新 README 表） |
| 2 | 高 | 星数更新 | 更新 Superpowers ★ 从 156k 到 159k（实际 158,523 — v5.0.7 Copilot CLI、18 天无新版本） | COMPLETE（已更新 README 表） |
| 3 | 高 | 星数更新 | 更新 gstack ★ 从 74k 到 76k（实际 75,773 — v1.0.0.0 今天发布：更简单的提示、真实 LOC 收据、类型化问题注册表） | COMPLETE（已更新 README 表） |
| 4 | 高 | 计数更新 | 更新 gstack 技能 46→37（按名称确认了 37 个根级别 SKILL.md 目录；v1.0.0.0 合并移除了 9 个技能目录） | COMPLETE（已更新 README 表） |
| 5 | 高 | 星数更新 | 更新 GSD ★ 从 54k 到 55k（实际 54,605 — v1.37.1 于 2026-04-17 发布：ingest-docs 命令、UI-phase 研究员修复） | COMPLETE（已更新 README 表） |
| 6 | 高 | 计数更新 | 更新 GSD 代理 31→33（agents/ 目录中新增 2 个 gsd-* 代理） | COMPLETE（已更新 README 表） |
| 7 | 中 | 星数更新 | 更新 oh-my-claudecode ★ 从 29k 到 30k（实际 29,773 — v4.12.1 今天发布：24 个 PR 中的 8 个错误修复、Opus 4.7 默认、Gemini 通道修复） | COMPLETE（已更新 README 表） |
| 8 | 中 | 星数更新 | 更新 CE ★ 从 14k 到 15k（实际 14,681 — v2.68.1 今天发布：ce-compound-refresh 和 ce-pr-description 交接修复） | COMPLETE（已更新 README 表） |
| 9 | 中 | 计数更新 | 更新 CE 代理 49→50、命令 3→4、技能 51→44（triage-prs.md 添加到 .claude/commands/；43 个 compound-engineering + 1 个 coding-tutor 技能） | COMPLETE（已更新 README 表） |
| 10 | 中 | 计数更新 | 更新 OpenSpec 命令 10→11（/opsx:explore 与 /opsx:new、/continue、/ff、/verify、/sync、/bulk-archive、/onboard、/propose、/apply、/archive 并存） | COMPLETE（已更新 README 表） |
| 11 | 低 | 计数验证 | ECC 命令 143→79 — 4 月 18 日代理通过 git tree 确认了 79 个命令 .md 文件；4 月 16 日通过目录计数为 143，置信度 0.72 | ON HOLD（方法在 git-tree 与目录 API 之间不同；保留 143 直到手动验证） |
| 12 | 低 | 计数验证 | ECC 技能 230→183 — 4 月 18 日代理通过 git tree 确认了 183 个技能文件夹；4 月 16 日通过目录计数为 230 | ON HOLD（保留 230 直到手动验证；与 4 月 13/16 日 ON HOLD 项目 12-13 重复出现） |
| 13 | 低 | 计数验证 | GSD 命令 122→81 — 4 月 18 日代理确认了 commands/gsd/ 中有 81 个 .md 文件；4 月 16 日为 122（那次运行中也 ON HOLD 为 74） | ON HOLD（重复出现的差异，可能是多运行时分页；保留 122 直到验证） |
| 14 | 低 | 计数验证 | Superpowers 代理 5→1 — 4 月 18 日代理计算了 1 个显式代理；之前的计数包括由技能分派的隐式子代理 | ON HOLD（仅方法变更；保留 5，包括隐式子代理计数） |
| 15 | 低 | 计数验证 | oh-my-claudecode 计划链接显示 ralplan 但代理识别了 omc-plan（skills/plan/SKILL.md）为活跃规划器 | ON HOLD（两个技能在仓库中都存在；保留 ralplan 链接直到用户偏好明确） |

---

## [2026-04-24 00:39 PKT] 开发工作流更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 排序 | 将 Superpowers（166k）移到 ECC（165k）上方 — Superpowers 超越 ECC 成为 #1 | COMPLETE（已更新 README 表） |
| 2 | 高 | 星数更新 | 更新 Superpowers ★ 从 159k 到 166k（实际 165,520 — v5.0.7 Codex 插件集成、PR #1165/#1180） | COMPLETE（已更新 README 表） |
| 3 | 高 | 星数更新 | 更新 ECC ★ 从 160k 到 165k（实际 165,156 — v2.1.116 钩子安装修复、Windows Python 检测） | COMPLETE（已更新 README 表） |
| 4 | 高 | 星数更新 | 更新 gstack ★ 从 76k 到 81k（实际 81,300 — v1.6.4.0） | COMPLETE（已更新 README 表） |
| 5 | 高 | 计数更新 | 更新 gstack 技能从 37 到 41（通过目录枚举确认了 41 个根级别 SKILL.md 目录） | COMPLETE（已更新 README 表） |
| 6 | 高 | 星数更新 | 更新 GSD ★ 从 55k 到 57k（实际 56,600 — v1.38.2 SDK 工作流线程、agent-skills 查询修复） | COMPLETE（已更新 README 表） |
| 7 | 高 | 计数更新 | 更新 oh-my-claudecode 技能从 37 到 46（46 个根级别 SKILL.md 目录；与 4 月 11 日合并前计数匹配） | COMPLETE（已更新 README 表） |
| 8 | 高 | 计数更新 | 更新 CE 代理从 50 到 60（v3.0.0 2026 年 4 月 22 日：所有技能/代理重命名为 ce- 前缀、原生插件清单） | COMPLETE（已更新 README 表） |
| 9 | 中 | 星数更新 | 更新 Spec Kit ★ 从 89k 到 90k（实际 90,458 — v0.8.0 2026 年 4 月 23 日：预设组合策略、编剧预设） | COMPLETE（已更新 README 表） |
| 10 | 中 | 星数更新 | 更新 BMAD ★ 从 45k 到 46k（实际 45,500 — v6.3.0 市场集成） | COMPLETE（已更新 README 表） |
| 11 | 中 | 计数更新 | 更新 BMAD 技能从 39 到 40（28 个 bmm-skills + 12 个 core-skills） | COMPLETE（已更新 README 表） |
| 12 | 中 | 星数更新 | 更新 OpenSpec ★ 从 41k 到 43k（实际 42,500 — v1.3.1 2026 年 4 月 21 日：glob 转义修复、遥测配置） | COMPLETE（已更新 README 表） |
| 13 | 中 | 星数更新 | 更新 oh-my-claudecode ★ 从 30k 到 31k（实际 30,900 — v4.13.2 2026 年 4 月 22 日：跨会话取消状态、Usage API 修复） | COMPLETE（已更新 README 表） |
| 14 | 中 | 星数更新 | 更新 HumanLayer ★ 从 10k 到 11k（实际 10,600） | COMPLETE（已更新 README 表） |
| 15 | 低 | 计数更新 | 更新 CE 技能从 44 到 42（41 个 compound-engineering + 1 个 coding-tutor；v3.0.0 合并） | COMPLETE（已更新 README 表） |
| 16 | 低 | 计数验证 | ECC 48→47 个代理、143→82 个命令（79+3）、230→183 个技能 — 第 3 次连续运行通过目录枚举 | ON HOLD（从 4 月 13/16/18 日重复出现；方法差异持续存在 — 保留当前值直到手动验证） |
| 17 | 低 | 计数验证 | GSD 命令 122→85 — 第 3 次连续较低计数（4 月 16 日：74、4 月 18 日：81、4 月 24 日：85） | ON HOLD（从 4 月 16/18 日重复出现；可能是多运行时目录分页 — 保留 122 直到验证） |

---

## [2026-04-26 13:18 PKT] 开发工作流更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 星数更新 | 更新 Superpowers ★ 从 166k 到 168k（实际 167,874 — v5.0.7 Codex 插件镜像） | COMPLETE（已更新 README 表） |
| 2 | 高 | 星数更新 | 更新 Everything Claude Code ★ 从 165k 到 167k（实际 167,155 — v1.10.0 Operator Workflows、ECC 2.0 Alpha） | COMPLETE（已更新 README 表） |
| 3 | 高 | 星数更新 | 更新 gstack ★ 从 81k 到 84k（实际 83,534 — v1.14.0.0 交互式 REPL 浏览器侧边栏、$B tab-each 扇出） | COMPLETE（已更新 README 表） |
| 4 | 高 | 标签更新 | 更新 BMAD-METHOD 标签"22+ 平台"→"42 个平台"（v6.5.0 今天发布，添加了 18 个新代理平台） | COMPLETE（已更新 README 表） |
| 5 | 中 | 星数更新 | 更新 Spec Kit ★ 从 90k 到 91k（实际 90,907 — v0.8.1 SkillsIntegration 用于 vibe 集成、3 天 3 个版本） | COMPLETE（已更新 README 表） |
| 6 | 中 | 星数更新 | 更新 Compound Engineering ★ 从 15k 到 16k（实际 15,549 — v3.1.0 ce-ideate 技能、ast-grep CLI 集成） | COMPLETE（已更新 README 表） |
| 7 | 中 | 计数更新 | 更新 Compound Engineering 代理从 60 到 51（根据仓库 README 明确声明；.agent.md 文件枚举确认） | COMPLETE（已更新 README 表） |
| 8 | 中 | 计数更新 | 更新 Compound Engineering 技能从 42 到 37（根据仓库 README"36 个技能"+ 1 个 coding-tutor 技能） | COMPLETE（已更新 README 表） |
| 9 | 低 | 计数更新 | 更新 BMAD 技能从 40 到 39（通过目录枚举为 27 个 bmm-skills + 12 个 core-skills） | COMPLETE（已更新 README 表） |
| 10 | 低 | 计数验证 | oh-my-claudecode 技能 46→38 — 代理通过 API 枚举了 38 个目录 | ON HOLD（重复出现的较低计数 vs. 46 基线；可能分页 — 保留 46 直到验证） |
| 11 | 低 | 计数验证 | ECC 计数 143→82 个命令、230→183 个技能 — 第 4 次连续运行通过目录枚举 | ON HOLD（从 4 月 13/16/18/24 日重复出现；方法持续 — 保留当前值直到手动验证） |
| 12 | 低 | 计数验证 | GSD 命令 122→85 — 第 4 次连续从 API 枚举得到较低计数 | ON HOLD（从 4 月 16/18/24 日重复出现；可能是目录分页 — 保留 122 直到验证） |
| 13 | 低 | 计数验证 | Superpowers 代理 5→1 正式 — agents/ 中只有 code-reviewer.md；4 个从技能隐式分派 | ON HOLD（根据之前决定保留 5，计入隐式分派角色） |

---

## [2026-04-29 00:48 PKT] 开发工作流更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 星数更新 | 更新 Superpowers ★ 从 168k 到 171k（实际 171,334 — v5.0.7 势头） | COMPLETE（已更新 README 表） |
| 2 | 高 | 星数更新 | 更新 Everything Claude Code ★ 从 167k 到 169k（实际 169,230 — v1.10.0 桌面仪表板、ECC2 alpha） | COMPLETE（已更新 README 表） |
| 3 | 高 | 星数更新 | 更新 Spec Kit ★ 从 91k 到 92k（实际 91,505 — v0.8.2 RAG/Chroma DB、6 天 3 个版本） | COMPLETE（已更新 README 表） |
| 4 | 高 | 星数更新 | 更新 gstack ★ 从 84k 到 86k（实际 86,021 — v1.17.0.0） | COMPLETE（已更新 README 表） |
| 5 | 高 | 星数更新 | 更新 GSD ★ 从 57k 到 58k（实际 58,418 — v1.39.0-rc.4 最小安装配置、/gsd-edit-phase） | COMPLETE（已更新 README 表） |
| 6 | 高 | 星数更新 | 更新 OpenSpec ★ 从 43k 到 44k（实际 43,637 — v1.3.1 路径规范化修复） | COMPLETE（已更新 README 表） |
| 7 | 高 | 星数更新 | 更新 oh-my-claudecode ★ 从 31k 到 32k（实际 31,760 — v4.13.5 HUD 速率限制修复、自动合并编排器） | COMPLETE（已更新 README 表） |
| 8 | 高 | 计数更新 | 更新 gstack 技能从 41 到 42（确认了 42 个根级别 SKILL.md 目录；+plan-devex-review） | COMPLETE（已更新 README 表） |
| 9 | 高 | 计数更新 | 更新 BMAD 技能从 39 到 40（28 个 bmm-skills + 12 个 core-skills；bmad-customize 于 4 月 21 日在 v6.5.0 中添加） | COMPLETE（已更新 README 表） |
| 10 | 高 | 计数更新 | 更新 Matt Pocock 技能从 16 到 22（5 个类别子目录：engineering 9、productivity 3、misc 4、personal 2、deprecated 4） | COMPLETE（已更新 README 表） |
| 11 | 高 | 工作流 | 更新 Spec Kit 工作流 — 在 /speckit.constitution 和 /speckit.specify 之间插入 /speckit.clarify | COMPLETE（已更新 README 表） |
| 12 | 高 | 工作流 | 更新 Superpowers 工作流 — 在 brainstorming 和 writing-plans 之间插入 using-git-worktrees | COMPLETE（已更新 README 表） |
| 13 | 高 | 工作流 | 重构 Matt Pocock 工作流 — 将 ralph-loop/feedback-loops/review 替换为 /triage、/diagnose、/zoom-out（反映 4 月 17/28 日技能重命名） | COMPLETE（已更新 README 表） |
| 14 | 高 | 工作流 | 将 HumanLayer /rpi:* 工作流替换为实际的 .claude/commands：/create_plan → /validate_plan → /implement_plan → /iterate_plan(sub) → /local_review → /commit | COMPLETE（已更新 README 表） |
| 15 | 中 | 工作流 | 更新 Compound Engineering — 将"重复"替换为子循环 /ce-debug(sub)、/ce-optimize(sub)、/ce-compound-refresh(sub) | COMPLETE（已更新 README 表） |
| 16 | 低 | 计数验证 | ECC 计数 143→133 个命令（混合：79 个传统 + 72 个同步活跃）、230→156 个技能自报告 — 第 6 次连续运行 | ON HOLD（从 4 月 13/16/18/24/26 日重复出现；方法持续 — 保留当前值直到手动验证） |
| 17 | 低 | 计数验证 | GSD 命令 122→86 — 第 5 次连续从 API 枚举得到较低计数 | ON HOLD（从 4 月 16/18/24/26 日重复出现；可能是目录分页 — 保留 122 直到验证） |
| 18 | 低 | 计数验证 | oh-my-claudecode 技能 46→38 — 第 2 次连续运行结果为 38；可能是 v4.13.x 合并 | ON HOLD（从 4 月 26 日重复出现；保留 46 直到验证） |

---

## [2026-05-01 15:36 PKT] 开发工作流更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 星数更新 | 更新 Superpowers ★ 从 171k 到 175k（实际 175,037 — v5.0.7 势头、会话文本 PR 规则） | COMPLETE（已更新 README 表） |
| 2 | 高 | 星数更新 | 更新 Everything Claude Code ★ 从 169k 到 171k（实际 171,200 — v1.10.0 热修复波 4 月 30 日：loop-status、gateguard） | COMPLETE（已更新 README 表） |
| 3 | 高 | 星数更新 | 更新 Matt Pocock Skills ★ 从 36k 到 51k（实际 50,817 — 2 天内病毒式激增 +41%、结构化 SKILL.md 章节、list-skills 脚本） | COMPLETE（已更新 README 表） |
| 4 | 高 | 排序 | 将 Matt Pocock（51k）移到 BMAD（46k）和 OpenSpec（45k）上方 — 病毒式跃升从第 8 位到第 6 位 | COMPLETE（已更新 README 表） |
| 5 | 高 | 星数更新 | 更新 gstack ★ 从 86k 到 88k（实际 87,550 — v1.21.1.0、browser-skills 运行时、setup-gbrain 联盟） | COMPLETE（已更新 README 表） |
| 6 | 高 | 星数更新 | 更新 Get Shit Done ★ 从 58k 到 59k（实际 59,115 — v1.39.0 今天发布：最小安装配置、/gsd-edit-phase） | COMPLETE（已更新 README 表） |
| 7 | 高 | 计数更新 | 更新 GSD 命令从 122 到 65（v1.39.0 合并：31 个微技能被吸收到 4 个分组父命令中 — 从 4 月 16/18/24/26/29 日 ON HOLD 解决） | COMPLETE（已更新 README 表） |
| 8 | 高 | 工作流 | 将 Matt Pocock /grill-me 重命名为 /grill-with-docs 工作流链（技能在最新提交中重命名） | COMPLETE（已更新 README 表） |
| 9 | 中 | 星数更新 | 更新 OpenSpec ★ 从 44k 到 45k（实际 44,511 — v1.3.1、Kimi CLI 技能支持、同步工具 ID 列表） | COMPLETE（已更新 README 表） |
| 10 | 中 | 计数更新 | 更新 gstack 技能从 42 到 43（确认了 43 个 SKILL.md 目录；+plan-devex-review 等净增 +1） | COMPLETE（已更新 README 表） |
| 11 | 中 | 计数更新 | 更新 Compound Engineering 代理从 51 到 49（2026-05-01 今天的提交移除了 2 个 cli-readiness 审查代理） | COMPLETE（已更新 README 表） |
| 12 | 中 | 计数更新 | 更新 Compound Engineering 技能从 37 到 39（添加了 ce-simplify-code、ce-strategy；38 个 compound-eng + 1 个 coding-tutor） | COMPLETE（已更新 README 表） |
| 13 | 低 | 计数更新 | 更新 oh-my-claudecode 技能从 46 到 38（从 4 月 26/29 日 ON HOLD 解决：第 3 次连续运行确认 v4.13.x 合并移除了 8 个技能） | COMPLETE（已更新 README 表） |
| 14 | 低 | 计数更新 | 更新 Spec Kit 命令从 9+ 到 9（精确计数：analyze、checklist、clarify、constitution、implement、plan、specify、tasks、taskstoissues） | COMPLETE（已更新 README 表） |
| 15 | 低 | 计数验证 | ECC 命令 143→71、技能 230→182 — 第 7 次连续运行目录枚举给出较低计数 | ON HOLD（从 4 月 13/16/18/24/26/29 日重复出现；方法持续 — 建议手动验证） |
| 16 | 低 | 计数验证 | Superpowers 代理 5→1 显式 — 仅方法变更（排除由技能分派的隐式子代理） | ON HOLD（从 4 月 18/26/29 日重复出现；根据之前决定保留 5，计入隐式分派角色） |

---

## [2026-05-01 16:05 PKT] 开发工作流更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 添加 | 添加 addyosmani/agent-skills（27k 星 / 3 个代理 / 7 个命令 / 21 个技能）到第 10 行，位于 oh-my-claudecode（32k）和 Compound Engineering（16k）之间；工作流链 `/spec → /plan → /build → /test → /review → /ship`（DEFINE → PLAN → BUILD → VERIFY → REVIEW → SHIP 生命周期）；用户请求的手动添加 | COMPLETE（已插入 DEVELOPMENT WORKFLOWS 表） |
| 2 | 低 | 备注 | 仓库也提供并行的 `.gemini/commands/` 等效项和 `.claude-plugin/` 市场条目（多代理 IDE）；因 21 个 SKILL.md 库而交叉列在 SKILL COLLECTIONS 表中 | COMPLETE（已交叉引用） |

---

## [2026-05-12 23:44 PKT] 开发工作流更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 星数更新 | 更新 Superpowers ★ 从 175k 到 188k（实际 187,818 — v5.1.0 势头、移除了 code-reviewer 代理） | COMPLETE（已更新 README 表） |
| 2 | 高 | 架构 | 更新 Superpowers 代理 5 → 0 显式和命令 3 → 0（v5.1.0 移除了命名的 code-reviewer 代理 + 传统斜杠命令；审查现在内联在技能中） | COMPLETE（已更新 README 表） |
| 3 | 高 | 星数更新 | 更新 Everything Claude Code ★ 从 171k 到 180k（实际 180,349 — v2.0.0-rc.1 alpha 进行中） | COMPLETE（已更新 README 表） |
| 4 | 高 | 星数更新 | 更新 Spec Kit ★ 从 92k 到 97k（实际 97,048 — v0.8.8 配置驱动认证注册表、每日发布） | COMPLETE（已更新 README 表） |
| 5 | 中 | 工作流 | 修复 Spec Kit 工作流顺序：constitution → specify → clarify → plan → tasks → implement（交换 clarify/specify 以匹配仓库快乐路径） | COMPLETE（已更新 README 表） |
| 6 | 高 | 星数更新 | 更新 gstack ★ 从 88k 到 95k（实际 94,500 — v1.33.2.0、gbrain 批量导入、21 个社区修复） | COMPLETE（已更新 README 表） |
| 7 | 中 | 计数更新 | 更新 gstack 技能 43 → 48（5 个新技能：design-shotgun、design-html、codex、retro、plan-tune） | COMPLETE（已更新 README 表） |
| 8 | 低 | 工作流 | 在 /plan-design-review 和 /ship 之间扩展 gstack 工作流链，添加 /design-shotgun、/design-html、/codex、/retro | COMPLETE（已更新 README 表） |
| 9 | 高 | 星数更新 | 更新 Get Shit Done ★ 从 59k 到 62k（实际 61,700 — v1.41.0 里程碑归档布局） | COMPLETE（已更新 README 表） |
| 10 | 低 | 计数更新 | 更新 GSD 命令 65 → 66（v1.41.0 在 commands/gsd/ 中添加了一个新命令） | COMPLETE（已更新 README 表） |
| 11 | 高 | 星数更新 | 更新 Matt Pocock Skills ★ 从 51k 到 76k（实际 75,562 — +25k 激增、handoff/review 技能于 5 月 10-11 日添加） | COMPLETE（已更新 README 表） |
| 12 | 中 | 计数更新 | 更新 Matt Pocock 技能 22 → 28（跨 engineering/in-progress/personal 类别新增 6 个 SKILL.md） | COMPLETE（已更新 README 表） |
| 13 | 中 | 星数更新 | 更新 BMAD-METHOD ★ 从 46k 到 47k（实际 47,000 — v6.6.0 破坏性变更、棕地史诗范围界定） | COMPLETE（已更新 README 表） |
| 14 | 高 | 星数更新 | 更新 OpenSpec ★ 从 45k 到 47k（实际 47,300 — Windows 工作区功能开发活跃） | COMPLETE（已更新 README 表） |
| 15 | 低 | 计数更新 | 更新 OpenSpec 命令 11 → 9（重新计数：propose、apply、archive、new、continue、ff、verify、bulk-archive、onboard — 确认 9 个） | COMPLETE（已更新 README 表） |
| 16 | 高 | 星数更新 | 更新 oh-my-claudecode ★ 从 32k 到 34k（实际 33,500 — v4.13.7 稳定性修复） | COMPLETE（已更新 README 表） |
| 17 | 中 | 星数更新 | 更新 Compound Engineering ★ 从 16k 到 17k（实际 16,600 — v3.8.1、ce-compound 的无头模式） | COMPLETE（已更新 README 表） |
| 18 | 低 | 计数更新 | 更新 Compound Engineering 技能 39 → 38（重新计数：compound-engineering/ 中 37 个 + coding-tutor/ 中 1 个） | COMPLETE（已更新 README 表） |
| 19 | 高 | 排序 | 按星数降序重新排序表：Superpowers（188k）> ECC（180k）> Spec Kit（97k）> gstack（95k）> Matt Pocock（76k）> GSD（62k）> OpenSpec（47.3k）> BMAD（47.0k）> oh-my-claudecode（34k）> agent-skills（27k）> Compound（17k）> HumanLayer（11k）；Matt Pocock 从第 6 行移到第 5 行，在 GSD 上方；OpenSpec 交换到 BMAD 上方（47.3 vs 47.0） | COMPLETE（已更新 README 表） |
| 20 | 低 | 计数验证 | ECC 代理 48→60、命令 143→78、技能 230→120 — 研究置信度 0.72，由于 1000+ 文件上的 API 分页；与 README 徽章计数冲突 | ON HOLD（重复出现 — 保留当前值直到手动验证） |
| 21 | 低 | 计数验证 | BMAD 代理 0→6 和技能 40→16 — 方法转变（将 bmad-agent-* 技能计为代理、更少的技能容器）；非实际仓库变更 | ON HOLD（保留当前方法以保持趋势连续性） |

---

## [2026-05-21 00:29 PKT] 开发工作流更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 星数更新 | 更新 Superpowers ★ 从 188k 到 200k（实际 200,000 — 突破 200k 里程碑；v5.1.0 移除了传统斜杠命令 + 命名的 code-reviewer 代理） | COMPLETE（已更新 README 表） |
| 2 | 高 | 星数更新 | 更新 Everything Claude Code ★ 从 180k 到 188k（实际 188,000 — ECC 2.0 Alpha、计费门控、AgentShield 适配器回读） | COMPLETE（已更新 README 表） |
| 3 | 高 | 星数更新 | 更新 Spec Kit ★ 从 97k 到 104k（实际 104,000 — 突破 100k；v0.8.12 扩展目录重构、Squad Bridge、Superpowers 实现桥） | COMPLETE（已更新 README 表） |
| 4 | 高 | 星数更新 | 更新 gstack ★ 从 95k 到 100k（实际 100,000 — 突破 100k 里程碑；v1.42.x 稳定性、23 个社区修复） | COMPLETE（已更新 README 表） |
| 5 | 高 | 星数更新 | 更新 Matt Pocock Skills ★ 从 76k 到 97k（实际 96,700 — +21k 激增；handoff/improve-codebase-architecture 技能更新于 5 月 19-20 日） | COMPLETE（已更新 README 表） |
| 6 | 中 | 星数更新 | 更新 Get Shit Done ★ 从 62k 到 63k（实际 63,300 — v1.42.3/v1.43.0-rc2、Codex CLI 0.130.0 兼容性、知识图谱自动更新） | COMPLETE（已更新 README 表） |
| 7 | 中 | 星数更新 | 更新 OpenSpec ★ 从 47k 到 50k（实际 49,500 — v1.3.1、Codex 工作区变更计划、Windows 工作区修复） | COMPLETE（已更新 README 表） |
| 8 | 中 | 星数更新 | 更新 BMAD-METHOD ★ 从 47k 到 48k（实际 47,700 — v6.7.1 安装程序修复、v6.7.0 PRD/brief 引导程序大改、bmad-investigate 技能） | COMPLETE（已更新 README 表） |
| 9 | 中 | 计数更新 | 更新 OpenSpec 命令从 9 到 11（/opsx:explore + /opsx:sync 重新计数；docs/commands.md 确认了 11 个） | COMPLETE（重复出现 — 计数在多次运行中在 9↔10↔11 之间波动；代理给出了明确的文档来源列表） |
| 10 | 低 | 计数更新 | 更新 GSD 命令从 66 到 67（通过 v1.42-43 在 commands/gsd/ 中新增一个命令） | COMPLETE（已更新 README 表） |
| 11 | 低 | 计数更新 | 更新 BMAD 技能从 40 到 42（30 个 bmm-skills + 12 个 core-skills；v6.7.0 添加了 bmad-investigate） | COMPLETE（已更新 README 表） |
| 12 | 低 | 计数更新 | 更新 oh-my-claudecode 技能从 38 到 39（确认了 39 个技能文件夹；v4.14.x 中 +1） | COMPLETE（已更新 README 表） |
| 13 | 低 | 计数验证 | ECC 代理 48→60、命令 143→75、技能 230→232 — 目录枚举与 README 自报告冲突持续 | ON HOLD（从 4 月 13/16/18/24/26 日 + 5 月 1/12 日重复出现；保留当前值直到手动验证） |
| 14 | 低 | 计数验证 | gstack 技能 48→59 — 代理的 AGENTS.md 目录计数包括非技能根目录（gstack/test/hosts/supabase）；目录列出约 46 个实际技能，置信度 0.80 | ON HOLD（代理计数过多；保留 48） |
| 15 | 低 | 计数验证 | BMAD 代理 0→6/30 — 方法转变（将 bmad-agent-* 角色计为代理） | ON HOLD（从 5 月 12 日重复出现；保留 0 以保持趋势连续性） |
| 16 | 低 | 计数验证 | oh-my-claudecode 命令 0→27 — 代理在 commands/ 中找到 27 个 .md，但工作流方法将技能视为命令界面 | ON HOLD（根据既定方法保留 0） |
| 17 | 低 | 排序 | 无需重新排序 — 星数降序顺序保持不变：Superpowers 200k > ECC 188k > Spec Kit 104k > gstack 100k > Matt Pocock 97k > GSD 63k > OpenSpec 50k > BMAD 48k > omc 34k > agent-skills 27k > Compound 17k > HumanLayer 11k | COMPLETE（已验证顺序不变） |
