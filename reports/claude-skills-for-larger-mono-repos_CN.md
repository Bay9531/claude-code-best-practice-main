# 理解大型单体仓库中的 Claude 技能发现机制

在单体仓库中使用 Claude Code 时，理解技能如何被发现并加载到上下文中，对于有效组织项目特定能力至关重要。

<table width="100%">
<tr>
<td><a href="../">← 返回 Claude Code 最佳实践</a></td>
<td align="right"><img src="../!/claude-jumping.svg" alt="Claude" width="60" /></td>
</tr>
</table>

## 与 CLAUDE.md 的重要区别

**技能的加载行为与 CLAUDE.md 文件不同。** CLAUDE.md 文件会沿目录树向上遍历（祖先加载），而技能则采用不同的发现机制，专注于项目内的嵌套目录。

## 技能如何被发现

### 1. 标准技能位置

技能根据作用域从以下固定位置加载：

| 位置 | 路径 | 适用范围 |
|----------|------|------------|
| 企业级 | 托管设置 | 组织内所有用户 |
| 个人 | `~/.claude/skills/<技能名称>/SKILL.md` | 你的所有项目 |
| 项目级 | `.claude/skills/<技能名称>/SKILL.md` | 仅限本项目 |
| 插件 | `<插件>/skills/<技能名称>/SKILL.md` | 插件启用处 |

### 2. 从嵌套目录自动发现

当你在子目录中处理文件时，Claude Code 会自动从嵌套的 `.claude/skills/` 目录中发现技能。例如，如果你正在编辑 `packages/frontend/` 中的文件，Claude Code 也会在 `packages/frontend/.claude/skills/` 中查找技能。

这支持了各包拥有自己技能的单体仓库设置。

## 示例单体仓库结构

考虑一个包含多个独立包的典型单体仓库：

```
/mymonorepo/
├── .claude/
│   └── skills/
│       └── shared-conventions/SKILL.md    # 项目级技能
├── packages/
│   ├── frontend/
│   │   ├── .claude/
│   │   │   └── skills/
│   │   │       └── react-patterns/SKILL.md  # 前端特定技能
│   │   └── src/
│   │       └── App.tsx
│   ├── backend/
│   │   ├── .claude/
│   │   │   └── skills/
│   │   │       └── api-design/SKILL.md      # 后端特定技能
│   │   └── src/
│   └── shared/
│       ├── .claude/
│       │   └── skills/
│       │       └── utils-patterns/SKILL.md  # 共享工具技能
│       └── src/
```

## 场景 1：刚在根目录启动 Claude（尚未编辑任何文件）

当你从 `/mymonorepo/` 运行 Claude Code 且尚未编辑任何文件时：

```bash
cd /mymonorepo
claude
# 刚启动 - 尚未编辑任何文件
```

| 技能 | 是否在上下文中？ | 原因 |
|-------|-------------|--------|
| `shared-conventions` | **是** | 根目录 `.claude/skills/` 中的项目级技能 |
| `react-patterns` | **否** | 未发现 - 尚未处理 `packages/frontend/` 中的文件 |
| `api-design` | **否** | 未发现 - 尚未处理 `packages/backend/` 中的文件 |
| `utils-patterns` | **否** | 未发现 - 尚未处理 `packages/shared/` 中的文件 |

## 场景 2：编辑包中文件后

在你要求 Claude 编辑 `packages/frontend/src/App.tsx` 之后：

| 技能 | 是否在上下文中？ | 原因 |
|-------|-------------|--------|
| `shared-conventions` | **是** | 根目录 `.claude/skills/` 中的项目级技能 |
| `react-patterns` | **是** | 编辑 `packages/frontend/` 中文件时被发现 |
| `api-design` | **否** | 仍未发现 - 尚未处理 `packages/backend/` 中的文件 |
| `utils-patterns` | **否** | 仍未发现 - 尚未处理 `packages/shared/` 中的文件 |

**关键洞察**：嵌套技能是在你处理这些目录中的文件时**按需发现**的，而非在会话启动时预加载。

## 关键行为：描述 vs 完整内容

技能描述会被加载到上下文中，以便 Claude 了解可用内容，但**完整技能内容仅在调用时加载**。这是一项重要的优化：

- **描述**：始终在上下文中（在字符预算范围内）
- **完整内容**：在技能被调用时按需加载

> 注意：预加载了技能的子代理行为不同——完整技能内容会在启动时注入。

## 优先级顺序（技能名称相同时）

当不同层级的技能名称相同时，优先级较高的位置胜出：

| 优先级 | 位置 | 作用域 |
|----------|----------|-------|
| 1（最高） | 企业级 | 组织范围 |
| 2 | 个人（`~/.claude/skills/`） | 你的所有项目 |
| 3（最低） | 项目级（`.claude/skills/`） | 仅限本项目 |

插件技能使用 `插件名称:技能名称` 的命名空间，因此不会与其他层级冲突。

## 此设计为何适用于单体仓库

- **包特定技能保持隔离** - 在 `packages/frontend/` 中工作的前端开发者获得前端特定技能，而不会让后端技能杂乱地占用上下文。

- **自动发现减少配置** - 无需显式注册包级技能；当你在这些目录中工作时技能会被自动发现。

- **上下文得到优化** - 初始仅加载技能描述，嵌套技能按需发现。

- **团队可维护自己的技能** - 每个包团队可以定义特定于其领域的技能，而无需与其他团队协调。

## 字符预算考量

技能描述会加载到上下文中，受字符预算限制（默认为 15,000 字符）。在包含大量包和技能的大型单体仓库中，你可能会达到此限制。

- 运行 `/context` 检查有关被排除技能的警告
- 设置 `SLASH_COMMAND_TOOL_CHAR_BUDGET` 环境变量以提高限制

## 最佳实践

1. **将共享工作流放在根目录 `.claude/skills/` 中** - 仓库范围的约定、提交工作流和共享模式。

2. **将包特定技能放在包的 `.claude/skills/` 中** - 该包特有的框架特定模式、组件约定和测试工具。

3. **对危险技能使用 `disable-model-invocation: true`** - 部署或破坏性技能应要求用户显式调用。

4. **保持技能描述简洁** - 描述始终在上下文中（在字符预算范围内），因此冗长的描述会浪费上下文空间。

5. **在技能名称中使用命名空间** - 考虑添加包名称前缀（如 `frontend-review`、`backend-deploy`）以避免混淆。

## 比较：技能与 CLAUDE.md 加载

| 行为 | CLAUDE.md | 技能 |
|----------|-----------|--------|
| 祖先加载（沿目录树向上） | 是 | 否 |
| 嵌套/后代发现（沿目录树向下） | 是（延迟） | 是（自动发现） |
| 全局位置 | `~/.claude/CLAUDE.md` | `~/.claude/skills/` |
| 项目位置 | `.claude/` 或仓库根目录 | `.claude/skills/` |
| 内容加载 | 完整内容 | 仅描述（调用时加载完整内容） |

---

## 来源

- [Claude Code 文档 - 使用技能扩展 Claude](https://code.claude.com/docs/en/skills)
- [Claude Code 文档 - 从嵌套目录自动发现](https://code.claude.com/docs/en/skills#automatic-discovery-from-nested-directories)
