# Linux 安装配置

[返回第 0 天](README.md)

## 前提条件

您需要 **Node.js v18 或更高版本**以及 **npm**。

## 步骤 1：安装 Node.js

### 选项 A：通过 nodejs.org 下载页面使用 fnm（推荐）

**fnm**（Fast Node Manager）是 Node.js 官方推荐的版本管理器。它快速、轻量，并且如果需要，您可以轻松切换 Node 版本。

1. 打开浏览器，访问 [nodejs.org/en/download](https://nodejs.org/en/download)。

2. 您会看到一排下拉菜单，显示：**"Get Node.js® vXX.XX.X (LTS) for __ using __ with __"**。按如下方式设置下拉菜单：

   | 下拉菜单 | 选择 |
   |----------|------|
   | Version | **vXX.XX.X (LTS)** — 保持默认的 LTS 版本，不要更改 |
   | OS | **Linux** |
   | Package Manager | **fnm**（位于 "Recommended (Official)" 下） |
   | Package Format | **npm** — 保持默认 |

3. 页面会显示您需要运行的准确命令。打开终端并复制粘贴。命令大致如下：

   ```bash
   # 步骤 1 — 安装 fnm
   curl -fsSL https://fnm.vercel.app/install | bash

   # 步骤 2 — 重启终端或重新加载 shell 配置文件
   source ~/.bashrc   # 或：source ~/.zshrc（如果您使用 zsh）

   # 步骤 3 — 安装 Node.js
   fnm install 24   # 页面会显示准确的版本号
   ```

   > 版本号可能与上述不同 — 请始终使用网站上显示的内容。

4. **关闭并重新打开终端**（或运行上面的 `source` 命令），以便 `fnm`、`node` 和 `npm` 可用。

> **为什么选择 fnm？** 它位于 Node.js 下载页面的 "Recommended (Official)" 分类中。与 nvm 一样，它将 Node 安装到您的主目录下，因此您永远不需要为 npm 全局安装使用 `sudo` — 但 fnm 速度明显更快（使用 Rust 编写），并且在 Windows、macOS 和 Linux 上的工作方式相同。

### 选项 B：使用发行版的包管理器

这种方法更快，但可能安装较旧版本的 Node.js。**安装后请检查版本** — 如果低于 v18，请改用选项 A。

**Ubuntu / Debian：**

```bash
sudo apt update
sudo apt install -y nodejs npm

# 检查版本
node --version   # 必须是 v18 或更高版本
```

**Fedora：**

```bash
sudo dnf install -y nodejs npm
```

**Arch Linux：**

```bash
sudo pacman -S nodejs npm
```

### 选项 C：NodeSource（通过 apt 获取最新 LTS，无需 nvm）

适用于希望获取最新 LTS 而不使用 nvm 的 Ubuntu/Debian 用户：

```bash
curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash -
sudo apt install -y nodejs
```

## 步骤 2：验证 Node.js

```bash
node --version
npm --version
```

两者都应打印版本号。`node --version` 必须显示 v18.x 或更高版本。

## 步骤 3：安装 Claude Code

```bash
npm install -g @anthropic-ai/claude-code
```

> **权限错误？**
> - 如果您使用了 **fnm** 或 **nvm**：不应出现此问题。请检查它是否已激活（`which node` 应指向您主目录中的路径，而不是 `/usr/...`）。
> - 如果您使用了系统安装：可以使用 `sudo npm install -g @anthropic-ai/claude-code`，或者修复 npm 的全局目录权限：
>   ```bash
>   mkdir -p ~/.npm-global
>   npm config set prefix '~/.npm-global'
>   echo 'export PATH=~/.npm-global/bin:$PATH' >> ~/.bashrc
>   source ~/.bashrc
>   ```

## 步骤 4：验证 Claude Code

```bash
claude --version
```

您应该看到打印出的 Claude Code 版本。现在返回 [README.md](README.md) 进行身份验证配置。

---

## 注意事项

- **WSL（Windows Subsystem for Linux）：** 本指南同样适用于 WSL 内部。只需在 WSL 终端中按照这些步骤操作即可。
- **PATH 问题：** 如果安装后找不到 `claude`，请确保 npm 的全局 bin 目录在您的 PATH 中。运行 `npm config get prefix` — 该路径下的 `bin/` 子目录需要位于您的 PATH 中。
