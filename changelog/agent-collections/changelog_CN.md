# 代理集合 — 更新日志

跟踪 `README.md` 中代理集合表的更新。

## 状态图例

- `COMPLETE (reason)` — 操作项已成功执行
- `INVALID (reason)` — 操作项被判定为不必要或不正确
- `ON HOLD (reason)` — 操作项暂缓处理

---

## [2026-05-24 08:46 PM PKT] 代理集合更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 星标 | 更新 msitarzewski/agency-agents ★ 从 104k 到 105k | COMPLETE (GitHub API: 104,690 精确值; 跨越千位边界至 105k; 新增 — 里程碑跨越) |
| 2 | LOW | 数量 | msitarzewski/agency-agents 代理 144 vs 169 (置信度 0.88) | INVALID (周期性方法学差异; 自 2026 年 4 月 12 日以来无提交; 多次运行中记录了 144↔169-185 的波动; 代理定义与工作流文档之间的边界每次运行不同) |
| 3 | LOW | 数量 | VoltAgent/awesome-claude-code-subagents 代理 151 vs 142 (置信度 0.91) | INVALID (周期性波动; 在 142-152 历史范围内; 5 月 20 日为仅维护提交; 未确认净增或净减代理) |
| 4 | LOW | 排序 | 验证排序顺序 (105k > 20k — 星标降序) | COMPLETE (顺序保持不变; 周期性) |

---

## [2026-05-23 08:46 PM PKT] 代理集合更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | LOW | 星标 | msitarzewski/agency-agents ★ 无变化 (104k) | INVALID (无需更改) |
| 2 | LOW | 数量 | msitarzewski/agency-agents 代理 144 → 184 (置信度 0.80) | INVALID (周期性方法学差异; 自 2026 年 4 月 12 日以来无提交; 多次运行中记录了 144↔184 的波动; 184 包含先前 144 基线未计数的策略/剧本/操作手册等元文档) |
| 3 | LOW | 数量 | VoltAgent/awesome-claude-code-subagents 代理 151 → 152 (置信度 0.92) | INVALID (周期性 ±1 波动; 过去 30 天内无新代理 — 4 月 25 日 / 5 月 20 日为仅维护提交; 在波动阈值内) |
| 4 | LOW | 排序 | 验证排序顺序 (104k > 20k — 星标降序) | COMPLETE (顺序保持不变; 周期性) |

---

## [2026-05-22 08:44 PM PKT] 代理集合更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 星标 | 更新 msitarzewski/agency-agents ★ 从 103k 到 104k | COMPLETE (GitHub API: 104,132 精确值; 跨越千位边界; 新增 — 里程碑跨越) |
| 2 | LOW | 数量 | msitarzewski/agency-agents 代理 144 → 185 (置信度 0.93) | INVALID (周期性方法学差异; 自 4 月 12 日 (~40 天) 以来无提交; 多次运行中记录了 144↔185 的波动; 未确认净新增代理) |
| 3 | LOW | 数量 | VoltAgent/awesome-claude-code-subagents 代理 151 → 144 (置信度 0.94) | INVALID (周期性 144↔151 波动; 最后一次提交 2026-05-20 仅为维护 (修复 plugin.json 孤立条目); ui-ux-tester/codebase-orchestrator 已在 5 月 16 日更新中计数) |
| 4 | LOW | 排序 | 验证排序顺序 (104k > 20k — 星标降序) | COMPLETE (顺序保持不变; 周期性) |

---

## [2026-05-21 08:47 PM PKT] 代理集合更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | LOW | 星标 | msitarzewski/agency-agents ★ 无变化 (103k = ~103,000) | INVALID (无需更改) |
| 2 | LOW | 数量 | msitarzewski/agency-agents 代理 144 → 179 (置信度 0.88) | INVALID (周期性方法学差异; 自 4 月 12 日以来无提交; 先前 git 树在置信度 0.96 确认 144; 当前置信度 0.88 运行使用了 15 个目录 vs 先前 10 个目录 — 目录范围边界解释了 +35 的波动) |
| 3 | LOW | 星标 | VoltAgent/awesome-claude-code-subagents ★ 无变化 (20k = ~20,300) | INVALID (无需更改) |
| 4 | LOW | 数量 | VoltAgent/awesome-claude-code-subagents 代理 151 → 144 (置信度 0.94) | INVALID (周期性 144↔151 波动; 自 4 月 20 日以来无新 .md 代理提交; 5 月 16 日新增两个文件后确认为 151; 当前 144 为周期性方法学边界问题 — 第 9 次出现) |
| 5 | LOW | 排序 | 验证排序顺序 (103k > 20k — 星标降序) | COMPLETE (顺序保持不变; 周期性) |

---

## [2026-05-20 08:47 PM PKT] 代理集合更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 星标 | 更新 msitarzewski/agency-agents ★ 从 101k 到 103k | COMPLETE (GitHub 页面: ~103,000 精确值; 跨越两个千位边界; 新增 — 两日跃升自 101k) |
| 2 | LOW | 数量 | msitarzewski/agency-agents 代理 144 → 181 (HTML 抓取, 置信度 0.65) | INVALID (周期性方法学差异; git 树 API 被屏蔽 (403); 自 4 月 12 日以来无提交; 5 月 19 日 git 树运行在置信度 0.96 确认 144 — 更高置信度的运行优先) |
| 3 | LOW | 数量 | VoltAgent/awesome-claude-code-subagents 代理 151 → 144 (HTML 抓取, 置信度 0.82) | INVALID (周期性 144↔151 波动; 自 4 月 20 日以来无提交; 历史模式显示反复的 144↔151 翻转; 未确认真实变化) |
| 4 | LOW | 排序 | 验证排序顺序 (103k > 20k — 星标降序) | COMPLETE (顺序保持不变; 周期性) |

---

## [2026-05-19 08:50 PM PKT] 代理集合更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 星标 | 更新 msitarzewski/agency-agents ★ 从 100k 到 101k | COMPLETE (GitHub API: 101,089 精确值; 跨越千位边界至 101k; 新增 — 里程碑跨越) |
| 2 | MED | 数量 | 更新 msitarzewski/agency-agents 代理从 188 到 144 | COMPLETE (README 自我声明 144; git 树确认 10 个类别目录中为 144; 置信度 0.96; 自 4 月 12 日以来无提交; 先前的 188 使用了更广泛的方法学 — 周期性修正) |
| 3 | LOW | 数量 | VoltAgent/awesome-claude-code-subagents 代理 151 vs 185 (+34) | INVALID (周期性方法学差异; 过去 30 天内无提交 — 最后一次提交 4 月 20 日; 185 vs 151 在波动范围 145-189 内; 未确认真实变化) |
| 4 | LOW | 排序 | 验证排序顺序 (101k > 20k — 星标降序) | COMPLETE (顺序保持不变; 周期性) |

---

## [2026-05-18 08:46 PM PKT] 代理集合更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 星标 | 更新 msitarzewski/agency-agents ★ 从 99k 到 100k | COMPLETE (GitHub HTML: ~99,800 精确值; 跨越千位边界至 100k; 新增 — 首次 100k 里程碑跨越) |
| 2 | LOW | 数量 | msitarzewski/agency-agents 代理 188 vs 184 (−4) | INVALID (周期性方法学差异; 过去 30 天内无提交 — 最后一次提交 4 月 11-12 日; −4 在 ±10 波动范围内; 未应用更改) |
| 3 | LOW | 数量 | VoltAgent/awesome-claude-code-subagents 代理 151 vs 149 (−2) | INVALID (周期性在 ±3 误差范围内; 过去 30 天内无提交 — 最后活动 4 月 19-20 日; −2 在波动阈值内; 未应用更改) |
| 4 | LOW | 排序 | 验证排序顺序 (100k > 20k — 星标降序) | COMPLETE (顺序保持不变; 周期性) |

---

## [2026-05-17 08:47 PM PKT] 代理集合更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 星标 | 更新 msitarzewski/agency-agents ★ 从 98k 到 99k | COMPLETE (GitHub API: 98,908 精确值; 跨越千位边界; 新增 — 首次 99k 跨越) |
| 2 | LOW | 数量 | VoltAgent/awesome-claude-code-subagents 代理 151 → 144 | INVALID (周期性波动; 过去 30 天内无提交 — 最后一次提交 4 月 19-20 日; 先前存在 144↔151 模式; 未确认真实变化) |
| 3 | LOW | 数量 | msitarzewski/agency-agents 代理 188 vs 研究范围 144-184 | INVALID (周期性方法学差异; 置信度 0.60; README 自我声明 144-147; 按目录枚举 ~184; 过去 30 天无提交; 未应用更改) |
| 4 | LOW | 排序 | 验证排序顺序 (99k > 20k — 星标降序) | COMPLETE (顺序保持不变; 周期性) |

---

## [2026-05-16 08:47 PM PKT] 代理集合更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | MED | 数量 | 更新 VoltAgent/awesome-claude-code-subagents 代理从 146 到 151 | COMPLETE (按目录枚举: 跨 10 个类别目录 151 个 .md 文件; 置信度 0.88; 2 个确认的新文件: ui-ux-tester.md, codebase-orchestrator.md 于 4 月 19-20 日; 新增 — 净增 +5 超过 ±3 波动阈值) |
| 2 | LOW | 数量 | msitarzewski/agency-agents 代理 188 → 185 | INVALID (周期性方法学差异; 置信度 0.82; ±10 可能范围; 先前的运行显示 144–188 波动; 未确认净变化) |
| 3 | LOW | 排序 | 验证排序顺序 (98k > 20k — 星标降序) | COMPLETE (顺序保持不变; 周期性) |

---

## [2026-05-15 08:47 PM PKT] 代理集合更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 星标 | 更新 msitarzewski/agency-agents ★ 从 97k 到 98k | COMPLETE (GitHub: 97,800 精确值; 跨越千位边界; 新增 — 首次 98k 跨越) |
| 2 | LOW | 数量 | msitarzewski/agency-agents 代理 188 → ~144–168+ (README 名册 144, 文件计数 ~168+) | INVALID (周期性方法学差异; 置信度 0.72; README 名册 144 vs 文件计数 168+; 先前运行以不同范围设置为 188; 未应用更改) |
| 3 | LOW | 数量 | VoltAgent/awesome-claude-code-subagents 代理 146 → ~143 (±3) | INVALID (周期性方法学差异 ±3; 置信度 0.70; 在误差范围内; 未应用更改) |
| 4 | LOW | 排序 | 验证排序顺序 (98k > 20k — 星标降序) | COMPLETE (顺序保持不变; 周期性) |

---

## [2026-05-14 08:48 PM PKT] 代理集合更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | MED | 数量 | 更新 msitarzewski/agency-agents 代理从 198 到 188 | COMPLETE (递归树: 跨领域目录 188 个 .md 文件; 置信度 0.88; 周期性方法学差异 — 代理定义与工作流/示例文档之间的边界每次运行不同) |
| 2 | HIGH | 数量 | 更新 VoltAgent/awesome-claude-code-subagents 代理从 189 到 146 | COMPLETE (递归树: categories/ 下 146 个 .md 文件; 置信度 0.92; 周期性大幅波动 — 先前的 189 运行可能计数方式不同; 最近新增记录于 2026 年 4 月) |
| 3 | LOW | 排序 | 验证排序顺序 (97k > 20k — 星标降序) | COMPLETE (msitarzewski 97k > VoltAgent 20k — 顺序保持不变; 周期性) |

---

## [2026-05-13 08:46 PM PKT] 代理集合更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 星标 | 更新 msitarzewski/agency-agents ★ 从 96k 到 97k | COMPLETE (GitHub API: 96,722 精确值; 跨越千位边界; 周期性日增长模式) |
| 2 | MED | 数量 | msitarzewski/agency-agents 代理 198 → ~164 | INVALID (置信度 0.80; 研究代理使用了 14 个类别目录 vs 先前运行的 19 个; 周期性方法学差异 — 排除了 strategy/, examples/, integrations/ 目录) |
| 3 | MED | 数量 | VoltAgent/awesome-claude-code-subagents 代理 189 → ~131–151 | INVALID (置信度 0.78; README 徽章 131+ 已过时 vs 树计数 151; 周期性方法学波动 — 未确认代理文件的净减少) |
| 4 | LOW | 排序 | 验证排序顺序 (97k > 20k — 星标降序) | COMPLETE (msitarzewski 97k > VoltAgent 20k — 顺序保持不变; 周期性) |

---

## [2026-05-12 08:47 PM PKT] 代理集合更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | HIGH | 数量 | 更新 msitarzewski/agency-agents 代理从 185 到 198 | COMPLETE (递归树扫描: 跨 19 个类别目录 198 个代理 .md 文件; 从 185 增加 +13; specialized/ 目录中最近新增; 新增) |
| 2 | HIGH | 数量 | 更新 VoltAgent/awesome-claude-code-subagents 代理从 145 到 189 | COMPLETE (递归树扫描: categories/ 下 189 个 .md 文件, 从 199 个原始中排除 10 个 README; 从 145 增加 +44; 持续的 PR 活动 ~每周 5-8 个代理; 新增) |
| 3 | LOW | 排序 | 验证排序顺序 (星标降序) | COMPLETE (msitarzewski 96k > VoltAgent 20k — 顺序保持不变; 周期性) |

---

## [2026-05-10 08:47 PM PKT] 代理集合更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | MED | 星标 | 更新 msitarzewski/agency-agents ★ 从 95k 到 96k | COMPLETE (HTML 抓取 ~95,700; 跨越千位边界; 先前 95,300 → ~95,700; ~400 星标增长) |
| 2 | MED | 星标 | 更新 VoltAgent/awesome-claude-code-subagents ★ 从 19k 到 20k | COMPLETE (HTML 抓取 ~19,500; 跨越千位边界; 先前 19,433 → ~19,500; 边界半千舍入已应用) |
| 3 | LOW | 数量 | msitarzewski/agency-agents 代理 185 → 175 (方法学差异) | INVALID (代理排除了 strategy/playbooks(7)/runbooks(4)/coordination(2)/examples(5); 与先前运行方法学不同; 周期性方法学差异; 未应用更改) |
| 4 | LOW | 数量 | VoltAgent/awesome-claude-code-subagents 代理 145 → 144 | INVALID (周期性 ±1 波动 — 第 7 次连续翻转; 按类别求和 144 唯一 (wordpress-master 重复已排除); 策略: ±1 时不更改) |
| 5 | LOW | 排序 | 验证排序顺序 (星标降序) | COMPLETE (msitarzewski 96k > VoltAgent 20k — 顺序保持不变) |

---

## [2026-05-09 08:46 PM PKT] 代理集合更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | LOW | 数量 | 更新 VoltAgent/awesome-claude-code-subagents 代理从 144 到 145 | COMPLETE (跨所有 10 个目录按类别枚举: 145 个 .md 文件, 置信度 0.87; 周期性 144↔145 波动 — 这是第 6 次连续翻转) |
| 2 | LOW | 星标 | msitarzewski/agency-agents ★ 无变化 (95k = ~95,300) | INVALID (无需更改) |
| 3 | LOW | 星标 | VoltAgent/awesome-claude-code-subagents ★ 无变化 (19k = ~19,400) | INVALID (无需更改) |
| 4 | LOW | 数量 | msitarzewski/agency-agents 代理 185 vs 报告值 184 (−1) | INVALID (在 ±1 误差范围内; 周期性波动; 注意到 project-management/ 截断提示 — 184 计数中可能缺少 1-2 个文件; 不更改) |
| 5 | LOW | 排序 | 验证排序顺序 (星标降序) | COMPLETE (msitarzewski 95k > VoltAgent 19k — 顺序保持不变) |

---

## [2026-05-09 06:57 PM PKT] 代理集合更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | LOW | 数量 | 更新 msitarzewski/agency-agents 代理从 185 到 186 | INVALID (在 ±1 误差范围内 — Python 爬取报告 186 但按目录枚举求和为 172; 代理置信度 0.93; 与先前 184–186 波动策略一致) |
| 2 | LOW | 星标 | msitarzewski/agency-agents ★ 无变化 (95k = 95,253) | INVALID (无需更改) |
| 3 | LOW | 星标 | VoltAgent/awesome-claude-code-subagents ★ 无变化 (19k = 19,433) | INVALID (无需更改) |
| 4 | LOW | 数量 | VoltAgent/awesome-claude-code-subagents 代理无变化 (144) | COMPLETE (树未被截断; 跨 10 个目录按类别求和恰好 144; 先前 144↔145 波动已明确解决为真实内容变化, 非分页伪影) |
| 5 | LOW | 排序 | 验证排序顺序 (星标降序) | COMPLETE (msitarzewski 95k > VoltAgent 19k — 顺序保持不变) |

---

## [2026-05-08 08:46 PM PKT] 代理集合更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | LOW | 数量 | 更新 VoltAgent/awesome-claude-code-subagents 代理从 145 到 144 | COMPLETE (爬取得到 categories/ 下 144 个 .md 文件; 周期性 144↔145 波动因 GitHub 分页误差 — ±1 伪影) |
| 2 | LOW | 星标 | msitarzewski/agency-agents ★ 无变化 (GitHub 显示 95k) | INVALID (无需更改) |
| 3 | LOW | 星标 | VoltAgent/awesome-claude-code-subagents ★ 无变化 (19.4k 舍入为 19k) | INVALID (无需更改) |
| 4 | LOW | 数量 | msitarzewski/agency-agents 代理无变化 (185) | INVALID (无需更改) |
| 5 | LOW | 排序 | 验证排序顺序 (星标降序) | COMPLETE (msitarzewski 95k > VoltAgent 19k — 顺序保持不变) |

---

## [2026-05-07 08:47 PM PKT] 代理集合更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | MED | 星标 | 更新 msitarzewski/agency-agents ★ 从 94k 到 95k | COMPLETE (网络抓取 ~94,700 → 舍入为 95k; 基数为先前运行 2026-05-06 的 94k) |
| 2 | LOW | 星标 | VoltAgent/awesome-claude-code-subagents ★ 无变化 (~19.3k 舍入为 19k) | INVALID (无需更改) |
| 3 | LOW | 数量 | 更新 VoltAgent/awesome-claude-code-subagents 代理从 144 到 145 | COMPLETE (直接遍历 10 个类别目录: 145 个 .md 文件, 置信度 0.78) |
| 4 | LOW | 数量 | 验证 msitarzewski/agency-agents 代理计数 (网络抓取 184 vs 树 API 185) | INVALID (在 ±1 误差范围内 — 网络抓取 vs git 树 API 方法学; 先前的树 API 运行得到的 185 更可靠; 不更改) |
| 5 | LOW | 排序 | 验证排序顺序 (星标降序) | COMPLETE (msitarzewski 95k > VoltAgent 19k — 顺序保持不变) |

---

## [2026-05-06 10:03 PM PKT] 代理集合更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | LOW | 星标 | msitarzewski/agency-agents ★ 无变化 (94k = ~94,300) | INVALID (无需更改) |
| 2 | LOW | 数量 | msitarzewski/agency-agents 代理 ~184-186 vs 当前 185 | INVALID (在误差范围内 — ±2 分页伪影; 不更改) |
| 3 | LOW | 星标 | VoltAgent/awesome-claude-code-subagents ★ 无变化 (19k = ~19,200) | INVALID (无需更改) |
| 4 | LOW | 数量 | 更新 VoltAgent/awesome-claude-code-subagents 代理从 145 到 144 | COMPLETE (仓库内 .md 文件计数跨 categories/ 减少 1) |
| 5 | LOW | 排序 | 验证排序顺序 (星标降序) | COMPLETE (msitarzewski 94k > VoltAgent 19k — 顺序保持不变) |

---

## [2026-05-06 08:48 PM PKT] 代理集合更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | MED | 星标 | 更新 msitarzewski/agency-agents ★ 从 93k 到 94k | COMPLETE (通过 GitHub API 验证: 94,254) |
| 2 | HIGH | 数量 | 更新 msitarzewski/agency-agents 代理从 197 到 185 | COMPLETE (git 树递归计数: 跨 20 个类别目录 185 个代理 .md 文件; 排除 strategy/, examples/, integrations README) |
| 3 | LOW | 星标 | VoltAgent/awesome-claude-code-subagents ★ 无变化 (19k = 19,214) | INVALID (无需更改) |
| 4 | LOW | 数量 | 更新 VoltAgent/awesome-claude-code-subagents 代理从 144 到 145 | COMPLETE (git 树计数: 仓库内 145 个 .md 文件; 3 个 README 条目为外部链接) |
| 5 | LOW | 排序 | 验证排序顺序 (星标降序) | COMPLETE (msitarzewski 94k > VoltAgent 19k — 顺序保持不变) |

---

## [2026-05-05 09:26 PM PKT] 代理集合更新

| # | 优先级 | 类型 | 操作 | 状态 |
|---|--------|------|------|------|
| 1 | MED | 星标 | 更新 msitarzewski/agency-agents ★ 从 92k 到 93k | COMPLETE (通过 GitHub API 验证: 93,374) |
| 2 | MED | 数量 | 更新 msitarzewski/agency-agents 代理从 206 到 197 | COMPLETE (递归树计数, 跨 15 个类别代理 .md 文件) |
| 3 | LOW | 星标 | VoltAgent/awesome-claude-code-subagents ★ 无变化 (19k = 19,137) | INVALID (无需更改) |
| 4 | MED | 数量 | 更新 VoltAgent/awesome-claude-code-subagents 代理从 148 到 144 | COMPLETE (categories/ 下递归树计数, 排除 tools/) |
| 5 | LOW | 排序 | 验证排序顺序 (星标降序) | COMPLETE (msitarzewski 93k > VoltAgent 19k — 顺序保持不变) |
| 6 | MED | 规则 | 确认表格包含门槛为 10k+ 星标 | COMPLETE (用户确认; 两个列出的仓库均通过 — msitarzewski 93k, VoltAgent 19k; 已保存为反馈记忆供未来运行使用) |
