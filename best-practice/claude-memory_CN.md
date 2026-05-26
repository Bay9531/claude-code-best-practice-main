# Claude 记忆

通过 CLAUDE.md 文件实现持久化上下文 — 如何编写以及在单体仓库中如何加载。

<table width="100%">
<tr>
<td><a href="../">← 返回 Claude Code 最佳实践</a></td>
<td align="right"><img src="../!/claude-jumping.svg" alt="Claude" width="60" /></td>
</tr>
</table>

---

## 1. 编写优秀的 CLAUDE.md

结构良好的 CLAUDE.md 是改善 Claude Code 为你的项目输出结果的最有效方式。Humanlayer 有一份优秀的指南，涵盖了包含什么内容、如何组织以及常见陷阱。

- [Humanlayer - 编写优秀的 Claude.md](https://www.humanlayer.dev/blog/writing-a-good-claude-md)

---

## 2. 大型单体仓库中的 CLAUDE.md

在单体仓库中使用 Claude Code 时，理解 CLAUDE.md 文件如何加载到上下文中对于有效组织项目指令至关重要。

<p align="center">
  <a href="https://x.com/bcherny/status/2016339448863355206"><img src="assets/claude-memory/claude-memory-monorepo.jpg" alt="CLAUDE.md 在单体仓库中的加载方式" width="600"></a>
</p>

### 两种加载机制

Claude Code 使用两种不同的机制来加载 CLAUDE.md 文件：

#### 祖先加载（向上遍历目录树）

当你启动 Claude Code 时，它会从当前工作目录**向上**向文件系统根目录遍历，并加载沿途找到的每个 CLAUDE.md。这些文件在**启动时立即加载**。

#### 后代加载（向下遍历目录树）

当前工作目录以下子目录中的 CLAUDE.md 文件**在启动时不会加载**。只有当 Claude 在你的会话期间读取这些子目录中的文件时，它们才会被包含进来。这被称为**懒加载**。

### 单体仓库结构示例

考虑一个典型的单体仓库，其中不同组件有独立的目录：

```
/mymonorepo/
├── CLAUDE.md          # 根级别指令（所有组件共享）
├── frontend/
│   └── CLAUDE.md      # 前端特定指令
├── backend/
│   └── CLAUDE.md      # 后端特定指令
└── api/
    └── CLAUDE.md      # API 特定指令
```

### 场景 1：从根目录运行 Claude Code

当你从 `/mymonorepo/` 运行 Claude Code 时：

```bash
cd /mymonorepo
claude
```

| 文件 | 启动时加载？ | 原因 |
|------|-------------|------|
| `/mymonorepo/CLAUDE.md` | 是 | 这是你的当前工作目录 |
| `/mymonorepo/frontend/CLAUDE.md` | 否 | 仅在读取/编辑 `frontend/` 中的文件时加载 |
| `/mymonorepo/backend/CLAUDE.md` | 否 | 仅在读取/编辑 `backend/` 中的文件时加载 |
| `/mymonorepo/api/CLAUDE.md` | 否 | 仅在读取/编辑 `api/` 中的文件时加载 |

### 场景 2：从组件目录运行 Claude Code

当你从 `/mymonorepo/frontend/` 运行 Claude Code 时：

```bash
cd /mymonorepo/frontend
claude
```

| 文件 | 启动时加载？ | 原因 |
|------|-------------|------|
| `/mymonorepo/CLAUDE.md` | 是 | 它是祖先目录 |
| `/mymonorepo/frontend/CLAUDE.md` | 是 | 它是你的当前工作目录 |
| `/mymonorepo/backend/CLAUDE.md` | 否 | 目录树的不同分支 |
| `/mymonorepo/api/CLAUDE.md` | 否 | 目录树的不同分支 |

### 关键要点

1. **祖先目录始终在启动时加载** — Claude 向上遍历目录树并加载找到的所有 CLAUDE.md 文件。这确保你始终可以访问根级别、仓库范围的指令。

2. **后代目录懒加载** — 子目录中的 CLAUDE.md 文件仅在你与这些子目录中的文件交互时加载。这可以防止不相关的上下文使你的会话变得臃肿。

3. **同级目录从不加载** — 如果你在 `frontend/` 中工作，`backend/CLAUDE.md` 或 `api/CLAUDE.md` 不会被加载到上下文中。

4. **全局 CLAUDE.md** — 你也可以在主目录的 `~/.claude/CLAUDE.md` 放置一个 CLAUDE.md，它将适用于所有 Claude Code 会话，无论项目是什么。

### 为何此设计适用于单体仓库

- **共享指令向下传播** — 根级别的 CLAUDE.md 包含仓库范围的约定、编码标准和通用模式，适用于所有地方。

- **组件特定指令保持隔离** — 前端开发者不需要后端特定的指令来占用他们的上下文，反之亦然。

- **上下文得到优化** — 通过懒加载后代 CLAUDE.md 文件，Claude Code 避免了在启动时加载可能数百千字节的不相关指令。

### 最佳实践

1. **将共享约定放在根 CLAUDE.md 中** — 编码标准、提交消息格式、PR 模板和其他仓库范围的指南。

2. **将组件特定指令放在组件 CLAUDE.md 中** — 特定于该组件的框架特定模式、组件架构、测试约定。

3. **使用 CLAUDE.local.md 存储个人偏好** — 将其添加到 `.gitignore` 中，用于不应与团队共享的指令。

---

## 来源

- [Claude Code 文档 - Claude 如何查找记忆](https://code.claude.com/docs/en/memory#how-claude-looks-up-memories)
- [Boris Cherny 在 X 上 - 关于 CLAUDE.md 加载的说明](https://x.com/bcherny/status/2016339448863355206)
- [Humanlayer - 编写优秀的 Claude.md](https://www.humanlayer.dev/blog/writing-a-good-claude-md)
