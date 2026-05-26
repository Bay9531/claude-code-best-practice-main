创建一个代理团队，构建一个展示迪拜当前时间并生成可视化 SVG 卡片的时间编排工作流。该工作流遵循"命令 → 代理 → 技能"架构模式：

- 命令负责编排流程并处理用户交互
- 代理使用预加载的技能获取迪拜的实时当前时间
- 技能根据获取到的数据创建可视化 SVG 时间卡片

**重要**：所有文件必须创建在 `agent-teams/.claude/` 目录下——而不是仓库根目录的 `.claude/` 目录中。这样可以保持代理团队的输出自包含，并可通过 `cd agent-teams && claude` 运行。
切勿引用或复制现有的天气工作流——所有内容均需从头构建。

分配以下团队成员：

1. **命令架构师**——在 `agent-teams/.claude/commands/time-orchestrator.md` 中设计并实现 `/time-orchestrator` 命令。该命令应：
   - 通过 Agent 工具（而非 bash）调用 time-agent 获取阿联酋迪拜的当前时间（Asia/Dubai 时区，UTC+4）
   - 通过 Skill 工具调用 time-svg-creator 技能，根据获取到的时间数据渲染 SVG 卡片
   - 在 frontmatter 中使用 model: haiku
   - 包含关键要求：顺序执行流程、正确的工具使用方式（代理使用 Agent 工具，技能使用 Skill 工具），以及输出摘要
   - 通过共享任务列表与其他团队成员协调，就组件之间传递的数据契约（{time, timezone, formatted}）达成一致

2. **代理工程师**——在 `agent-teams/.claude/agents/time-agent.md` 中设计并实现 `time-agent`，以及其预加载的 `time-fetcher` 技能（位于 `agent-teams/.claude/skills/time-fetcher/SKILL.md`）。该代理应：
   - 使用 Bash 命令 `TZ='Asia/Dubai' date '+%Y-%m-%d %H:%M:%S %Z'` 获取迪拜（Asia/Dubai，UTC+4）的当前时间
   - 向命令返回时间值、时区名称和格式化字符串
   - 使用 frontmatter：tools（Bash）、model: haiku、color: blue、maxTurns: 3
   - 通过 `skills:` 字段预加载 time-fetcher 技能
   - time-fetcher 技能（`agent-teams/.claude/skills/time-fetcher/SKILL.md`）应包含获取迪拜时间的 bash 命令、预期的输出格式，并设置 user-invocable: false，因其仅为代理专用的领域知识。
   - 将已商定的数据契约发布到共享任务列表，以便命令架构师和技能设计师能够对齐接口。

3. **技能设计师**——在 `agent-teams/.claude/skills/time-svg-creator/SKILL.md` 中设计并实现 `time-svg-creator` 技能，并附带支持文件 `reference.md`（SVG 模板 + 输出模板）和 `examples.md`（示例输入/输出对）。该技能应：
   - 从调用上下文接收时间值、时区和格式化字符串
   - 创建一个自包含的迪拜 SVG 时间卡片，显示当前时间
   - 将 SVG 写入 `agent-teams/output/dubai-time.svg`
   - 将 markdown 摘要写入 `agent-teams/output/output.md`
   - 使用提供的精确时间——切勿重新获取
   - 将模板保存在 reference.md（带占位符的 SVG 标记、markdown 输出模板）中，示例对保存在 examples.md 中
   - 同时创建 `agent-teams/output/` 目录用于存放输出文件

所有三位团队成员应在共享任务列表中创建任务以协调数据契约：代理返回 {time, timezone, formatted}，命令通过上下文传递，技能消费该数据。
由于各组件相互独立，请并行启动所有三位成员——他们只需就数据接口达成一致，无需等待彼此的实现。
