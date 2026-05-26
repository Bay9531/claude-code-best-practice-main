# 第 0 天 — Claude Code 安装配置

本指南将引导您在机器上安装 Claude Code 并进行身份验证，以便您开始使用它。

## 步骤 1：安装 Claude Code

选择您的操作系统：

| 操作系统 | 指南 |
|----------|------|
| Windows | [windows.md](windows.md) |
| Linux | [linux.md](linux.md) |
| macOS | [mac.md](mac.md) |

按照您操作系统的指南操作，然后返回此处进行身份验证。

---

## 步骤 2：验证安装

按照您操作系统的指南操作后，确认一切正常：

```bash
node --version    # 应显示 v18.x 或更高版本
claude --version  # 应显示已安装的 Claude Code 版本
```

---

## 步骤 3：登录

<img src="assets/login.png" alt="Claude Code 登录界面" width="50%">

在终端中运行 `claude`。首次启动时，它会要求您选择登录方式。

### 方式 1：订阅（Claude Pro / Max）

- 选择 **Claude.ai 账户**
- 浏览器会打开 — 登录并授权
- 返回终端，您已登录成功

### 方式 2a：API 密钥（团队邀请）

您的团队管理员会从 Anthropic 控制台邀请您。

- 您会收到一封**邀请邮件** — 接受邀请并创建您的 Anthropic 账户
- 在终端中运行 `claude`
- 选择 **Anthropic API 密钥**
- 您的密钥将在控制台上**自动生成** — 无需手动配置

### 方式 2b：API 密钥（您已有密钥）

如果有人通过 Slack、邮件等方式与您共享了密钥，或者您自己创建了密钥：

- 在终端中运行 `claude`
- 选择 **Anthropic API 密钥**
- 粘贴您的密钥（以 `sk-ant-` 开头）
- 密钥会**永久保存** — 下次不会再询问

---
