# 技能集合更新日志

**状态图例：**

| 状态 | 含义 |
|--------|---------|
| `COMPLETE (reason)` | 已采取措施并成功解决 |
| `INVALID (reason)` | 发现不正确、不适用或有意为之 |
| `ON HOLD (reason)` | 操作已推迟，等待外部依赖或用户决定 |

---

## [2026-04-28 16:39 PKT] 技能集合更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 低 | 初始运行 | 在 README 中创建 SKILL COLLECTIONS 章节，包含 5 个仓库：anthropics/skills（125k/17）、wshobson/agents（35k/152）、mattpocock/skills（33k/17）、K-Dense-AI/scientific-agent-skills（20k/134）、VoltAgent/awesome-agent-skills（19k/1,100+ 精选） | COMPLETE（来自 research-agent 发现的初始植入，2026-04-28 会话） |

---

## [2026-04-29 00:52 PKT] 技能集合更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 中 | 星数 | 更新 mattpocock/skills ★ 从 33k 到 36k（精确值 36,476） | NEW |
| 2 | 中 | 计数 | 更新 mattpocock/skills 技能计数从 17 到 18（添加了 setup-matt-pocock-skills，deprecated/ 文件夹于 2026-04-28 重组） | NEW |
| 3 | 低 | 星数 | 更新 wshobson/agents ★ 从 35k 到 34k（精确值 34,477 — 略有下降） | NEW |
| 4 | 中 | 排序 | 将 mattpocock/skills 行移到 wshobson/agents 行上方（因星数变化导致的排名交换） | NEW |
| 5 | 低 | 计数 | 更新 VoltAgent/awesome-agent-skills 精选计数从 1,100+ 到 930+（实际 README 列表解析；徽章多报了约 170 个） | NEW |
| 6 | 低 | 无变化 | anthropics/skills（125k/17）和 K-Dense-AI/scientific-agent-skills（20k/134）— 数值匹配，无需编辑 | COMPLETE（已验证，无差异） |

---

## [2026-05-01 15:31 PKT] 技能集合更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 中 | 星数 | 更新 anthropics/skills ★ 从 125k 到 127k（精确值 126,746） | NEW |
| 2 | 高 | 星数 | 更新 mattpocock/skills ★ 从 36k 到 51k（精确值 50,819 — 约 3 天内激增 +15k，可能是外部放大效应） | NEW |
| 3 | 低 | 星数 | 更新 wshobson/agents ★ 从 34k 到 35k（精确值 34,595） | NEW |
| 4 | 低 | 星数 | 更新 VoltAgent/awesome-agent-skills ★ 从 19k 到 20k（精确值 19,729） | NEW |
| 5 | 低 | 无变化 | 所有 5 个技能计数稳定（anthropics 17、mattpocock 18、wshobson 152、scientific 134、voltagent 930 精选） | COMPLETE（已验证，无差异） |
| 6 | 低 | 排序 | 顺序保持不变 — scientific（19,829）仍以约 100 星的差距领先 voltagent（19,729）；无需行重新排序 | COMPLETE（已验证） |

---

## [2026-05-01 16:05 PKT] 技能集合更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 添加 | 添加 addyosmani/agent-skills（27k 星 / 21 个 SKILL.md 文件）到第 4 行，位于 wshobson/agents（35k）和 scientific-agent-skills（20k）之间；用户请求的手动添加 | COMPLETE（已插入 SKILL COLLECTIONS 表） |
| 2 | 低 | 备注 | 仓库是双重分类的——也添加到 DEVELOPMENT WORKFLOWS 表中，因为它提供了完整的 /spec → /plan → /build → /test → /review → /ship 生命周期，而不仅仅是 SKILL.md 库 | COMPLETE（已交叉引用） |

---

## [2026-05-12 23:40 PKT] 技能集合更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 星数 | 更新 anthropics/skills ★ 从 127k 到 133k（精确值 132,946） | NEW |
| 2 | 高 | 星数 | 更新 mattpocock/skills ★ 从 51k 到 76k（精确值 75,562 — 约 11 天内激增 +25k，连续第二次放大事件） | RECURRING（2026-05-01 记录了类似的 +15k 激增） |
| 3 | 中 | 计数 | 更新 mattpocock/skills 活跃技能数从 18 到 24（添加了 handoff 2026-05-11、review 2026-05-10，以及 engineering/in-progress 新增；4 个弃用保持不变） | NEW |
| 4 | 低 | 计数 | 更新 wshobson/agents 技能计数从 152 到 153（2026-05-09 提交中 README 计数已同步） | NEW |
| 5 | 低 | 星数 | 更新 K-Dense-AI/scientific-agent-skills ★ 从 20k 到 21k（精确值 20,758） | NEW |
| 6 | 低 | 计数 | 更新 K-Dense-AI/scientific-agent-skills 计数从 134 到 135（添加了 exa-search 2026-05-06 PR #143、autoskill 2026-05-03 PR #141） | NEW |
| 7 | 中 | 星数 | 更新 VoltAgent/awesome-agent-skills ★ 从 20k 到 21k（精确值 21,417 — 在星数上超过了 K-Dense-AI） | NEW |
| 8 | 中 | 计数 | 更新 VoltAgent/awesome-agent-skills 精选计数从 930+ 到 1,100+（恢复使用 README 徽章作为来源；之前的 930+ 是保守的列表解析） | RECURRING（2026-04-29 讨论了计数来源方法） |
| 9 | 高 | 排序 | 交换第 5 行（K-Dense-AI 20,758）和第 6 行（VoltAgent 21,417）——VoltAgent 因约 660 星的领先优势上移 | NEW |
| 10 | 低 | 无变化 | addyosmani/agent-skills（27k/21）未触及——超出标准 5 仓库研究范围，等待单独审查 | COMPLETE（已验证，手动条目已保留） |

---

## [2026-05-13 PKT] 技能集合更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 添加 | 添加 pbakaus/impeccable（27k 星 / 1 个 SKILL.md，包含 7 个设计领域引用）到第 4 行，位于 wshobson/agents（35k）和 addyosmani/agent-skills（27k）之间；用户请求的手动添加 | COMPLETE（已插入 SKILL COLLECTIONS 表） |
| 2 | 低 | 备注 | 单技能仓库，包含 7 个参考文件（排版、色彩与对比度、空间设计、动效设计、交互设计、响应式设计、UX 写作）、23 个命令、27 条反模式规则——面向前端 AI 工作的设计语言技能 | COMPLETE（计数表示法匹配 VoltAgent 的括号说明模式） |

---

## [2026-05-13 01:28 PKT] 技能集合更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 添加 | 添加 alirezarezvani/claude-skills（精确值 14,550 → 15k / 246 个技能，涵盖 9 个领域）到 SKILL COLLECTIONS 表的第 8 行（位于 K-Dense-AI/scientific-agent-skills 21k 之后）；用户请求的手动添加 | COMPLETE（已插入 SKILL COLLECTIONS 表） |
| 2 | 中 | 备注 | 将经验性的 SKILL COLLECTIONS 星数下限从 21k 降低到约 15k。此表之前没有明确的星数门槛记忆（只有 AGENT COLLECTIONS 和 CROSS-MODEL WORKFLOWS 有 10k+ 规则），因此这是先例设置性添加而非规则违反 | COMPLETE（决策已记录） |
| 3 | 低 | 备注 | 仓库设计为跨工具使用（支持 Claude Code、Codex、Gemini CLI、Cursor + 8 个以上，根据其 README 描述）。未来审查中可列入 CROSS-MODEL WORKFLOWS 表的候选，但根据用户指示分类在此处 | COMPLETE（交叉分类已记录） |

---

## [2026-05-20 23:55 PKT] 技能集合更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 星数 | 更新 mattpocock/skills ★ 从 76k 到 97k（精确值 96,663 — 约 8 天内激增 +21k，连续第三次放大事件） | RECURRING（2026-05-12 记录了类似的 +25k 激增，2026-05-01 记录了 +15k） |
| 2 | 中 | 星数 | 更新 anthropics/skills ★ 从 133k 到 138k（精确值 138,169） | RECURRING（常规星数增长，2026-05-12 有记录） |
| 3 | 低 | 星数 | 更新 wshobson/agents ★ 从 35k 到 36k（精确值 35,706） | RECURRING（星数增长记录于 2026-05-01、2026-05-12） |
| 4 | 低 | 计数 | 更新 wshobson/agents 技能计数从 153 到 155（添加了 recsys-pipeline-architect 2026-05-17、ship-mate 插件 2026-05-11） | RECURRING（计数差异记录于 2026-05-12） |
| 5 | 中 | 星数 | 更新 K-Dense-AI/scientific-agent-skills ★ 从 21k 到 25k（精确值 24,924 — +4k，超过了 VoltAgent） | RECURRING（星数增长记录于 2026-05-12） |
| 6 | 低 | 计数 | 更新 K-Dense-AI/scientific-agent-skills 计数从 135 到 138（v2.39.0 社区贡献 2026-05-19、Hugging Science 2026-05-01） | RECURRING（计数差异记录于 2026-05-12） |
| 7 | 低 | 星数 | 更新 VoltAgent/awesome-agent-skills ★ 从 21k 到 22k（精确值 22,473） | RECURRING（星数增长记录于 2026-05-12） |
| 8 | 中 | 排序 | 交换 K-Dense-AI（24,924）和 VoltAgent（22,473）——K-Dense-AI 以约 2,450 星的领先优势重新获得更高排名 | RECURRING（逆转了 2026-05-12 记录的 VoltAgent 上移） |
| 9 | 低 | 无变化 | anthropics 和 mattpocock 的活跃技能计数稳定（17、24）；VoltAgent 精选计数稳定（1,100+） | COMPLETE（已验证，无差异） |
| 10 | 低 | 无变化 | 手动条目未触及——impeccable（27k/1）、addyosmani/agent-skills（27k/21）、alirezarezvani/claude-skills（15k/246）——超出 5 仓库研究范围 | COMPLETE（已验证，手动条目已保留） |
