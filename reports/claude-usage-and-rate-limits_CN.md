# Claude Code：用量、速率限制与额外用量

了解 Claude Code 中的用量限制工作原理，以及在达到限制后如何继续工作。

<table width="100%">
<tr>
<td><a href="../">← 返回 Claude Code 最佳实践</a></td>
<td align="right"><img src="../!/claude-jumping.svg" alt="Claude" width="60" /></td>
</tr>
</table>

---

## 概述

订阅计划（Pro、Max 5x、Max 20x）上的 Claude Code 具有用量限制，这些限制会在滚动时间窗口内重置。三个内置斜杠命令可帮助您监控和管理用量：

| 命令 | 描述 | 适用对象 |
|---------|-------------|--------------|
| `/usage` | 查看计划限制与速率限制状态 | Pro、Max 5x、Max 20x |
| `/extra-usage` | 配置达到限制时的按量付费超额用量 | Pro、Max 5x、Max 20x |
| `/cost` | 显示当前会话的令牌用量与花费 | API 密钥用户 |

---

## `/usage` — 查看您的限制

显示当前计划的用量限制和速率限制状态。在达到限制前查看剩余容量时非常有用。

---

## `/extra-usage` — 超过限制后继续工作

`/extra-usage` 命令用于配置**按量付费超额计费**，以便 Claude Code 在达到计划速率限制时无缝继续工作，而不是阻止您。

### 工作原理

1. 您达到计划的速率限制（限制每 5 小时重置一次）
2. 如果已启用超额用量且账户有可用余额，Claude Code 将无中断地继续工作
3. 超额令牌将按**标准 API 费率**计费，与您的订阅费用分开

### 设置方法

CLI 中的 `/extra-usage` 命令将引导您完成配置。您也可以在 claude.ai 上的**设置 > 用量**页面进行配置：

1. 启用超额用量
2. 添加支付方式
3. 设置**月度支出上限**（或选择不限额度）
4. 可选地添加**预付款项**，并在余额低于阈值时自动充值

### 关键信息

| 详情 | 值 |
|--------|-------|
| 每日兑换限额 | 2,000 美元/天 |
| 计费方式 | 与订阅分开，按标准 API 费率计费 |
| 限制重置窗口 | 每 5 小时 |

### 已知问题

截至 2026 年 2 月，`/extra-usage` CLI 命令尚未[提供文档](https://github.com/anthropics/claude-code/issues/12396)，可能会打开一个登录窗口而没有清晰的配置选项。目前通过 **claude.ai 网页界面**进行配置是更可靠的方式。

---

## `/cost` — 会话花费（API 用户）

对于使用 API 密钥（而非订阅计划）进行身份验证的用户，`/cost` 显示：

- 当前会话的总花费
- API 持续时间和实际运行时间
- 令牌用量明细
- 所做的代码更改

此命令不适用于 Pro/Max 订阅用户。

---

## 快速模式与额外用量

快速模式（`/fast`）使用 Claude Opus 4.6 并提供更快的输出。它与超额用量有特殊的计费关系：

- 快速模式的用量**始终从第一个令牌起按超额用量计费**
- 即使您的订阅计划仍有剩余用量，此规则同样适用
- 快速模式不会消耗您计划中包含的速率限制

这意味着您需要启用并充值超额用量才能使用 `/fast`。

---

## CLI 启动参数

两个与用量预算相关的启动参数（仅限 API 密钥用户，打印模式）：

| 参数 | 描述 |
|------|-------------|
| `--max-budget-usd <AMOUNT>` | API 调用的最大美元金额，达到后停止 |
| `--max-turns <NUMBER>` | 限制代理轮次数量 |

完整列表请参阅 [CLI 启动参数参考](claude-cli-startup-flags.md)。

---

## 来源

- [付费 Claude 计划的超额用量 — Claude 帮助中心](https://support.claude.com/en/articles/12429409-extra-usage-for-paid-claude-plans)
- [在 Pro 或 Max 计划中使用 Claude Code — Claude 帮助中心](https://support.claude.com/en/articles/11145838-using-claude-code-with-your-pro-or-max-plan)
- [/extra-usage 斜杠命令尚未提供文档 — GitHub Issue #12396](https://github.com/anthropics/claude-code/issues/12396)
- [Claude Code CLI 参考](https://code.claude.com/docs/en/cli-reference)
