# 跨模型工作流更新日志

**状态图例：**

| 状态 | 含义 |
|--------|---------|
| `COMPLETE (reason)` | 已采取措施并成功解决 |
| `INVALID (reason)` | 发现不正确、不适用或有意为之 |
| `ON HOLD (reason)` | 操作已推迟，等待外部依赖或用户决定 |

---

## [2026-05-13 PKT] 跨模型工作流章节创建

| # | 优先级 | 类型 | 操作 | 状态 |
|---|----------|------|--------|--------|
| 1 | 高 | 章节 | 在 README.md 中创建新的 `CROSS-MODEL WORKFLOWS` 章节，插入在 DEVELOPMENT WORKFLOWS 和 SKILL COLLECTIONS 之间；章节解释三种桥接机制（插件 / MCP / 路由器）并将现有的跨模型方法论文档链接为章节介绍 | COMPLETE（新章节已上线） |
| 2 | 高 | 添加 | 以 10k+ 星数门槛为基准，在表中植入 4 个仓库：musistudio/claude-code-router（34k，路由器）、router-for-me/CLIProxyAPI（32k，路由器）、openai/codex-plugin-cc（18k，插件）、BeehiveInnovations/pal-mcp-server（12k，MCP — 原 zen-mcp-server） | COMPLETE（表已植入） |
| 3 | 中 | 移动 | 从 `DEVELOPMENT WORKFLOWS → Others` 列表中移除 `Cross-Model (Claude Code + Codex) Workflow` 条目；将其重新安置为新章节内的方法论介绍行，以便用户撰写的双终端工作流保持可发现性而不重复 | COMPLETE（已去重） |
| 4 | 低 | 门槛 | 确立 10k+ 星数下限作为收录标准（与 AGENT COLLECTIONS 门槛一致）；在后续运行中自动拒绝星数较低的仓库 | COMPLETE（策略已记录在记忆中） |
| 5 | 低 | 待定 | decolua/9_router（9.3k 星 — "通过 40+ 提供商免费使用 Claude/GPT/Gemini"）略低于门槛；在下次运行时重新评估 | ON HOLD（低于门槛） |
| 6 | 低 | 排除 | EveryInc/compound-engineering-plugin（17k）最初被标记为跨模型 — 验证为纯 Claude 工作流插件（37 个技能 + 51 个代理均在 Claude 内运行）；保留在 DEVELOPMENT WORKFLOWS 表中 | INVALID（非跨模型） |
| 7 | 低 | 排除 | 低于 10k 但具有独特角度的仓库已记录供参考（若超过门槛则重新评估）：1rgs/claude-code-proxy（4k，路由器→OpenAI/Gemini 通过 LiteLLM）、jamubc/gemini-mcp-tool（2k，MCP→Gemini 上下文窗口）、LLM-Red-Team/kimi-cc（2k，路由器→Kimi K2）、jarrodwatts/claude-delegator（1k，插件→Codex/Gemini 委托） | ON HOLD（低于门槛，候选观察列表） |
