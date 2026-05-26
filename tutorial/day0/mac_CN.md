# macOS 安装配置

[返回第 0 天](README.md)

---

**终端**
- 打开终端（按下 `Cmd + Space`，输入 "Terminal"，按 Enter）

**Homebrew**
- 检查 Homebrew 是否已安装：
  ```bash
  brew --version
  ```
- 如果显示 "command not found"，请先安装 Homebrew：
  ```bash
  /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
  ```

**Claude Code**
- ```bash
  brew install --cask claude-code
  ```

**验证**
- ```bash
  claude --version
  ```

---

现在返回 [README.md](README.md) 进行身份验证配置。
