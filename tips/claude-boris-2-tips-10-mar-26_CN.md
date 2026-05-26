# 代码审查与测试时计算 — Boris Cherny 的技巧

Claude Code 创建者 Boris Cherny（[@bcherny](https://x.com/bcherny)）于 2026 年 3 月 10 日分享的见解总结。

<table width="100%">
<tr>
<td><a href="../">← 返回 Claude Code 最佳实践</a></td>
<td align="right"><img src="../!/claude-jumping.svg" alt="Claude" width="60" /></td>
</tr>
</table>

---

## 1/ 引入代码审查

Claude Code 新增功能：**代码审查**。一组代理对每个 PR 进行深度审查。

- 首先为 Anthropic 自己的团队构建——今年每位工程师的代码产出增加了 **200%**，而审查成了瓶颈
- Boris 已经使用了几周，发现它捕获了许多他否则不会注意到的真实错误
- 当 PR 打开时，Claude 会派遣一组代理去搜寻错误

<a href="https://x.com/bcherny/status/2031089411820228645"><img src="assets/boris-26-3-10/0.png" alt="Boris Cherny 宣布代码审查" width="50%" /></a>

---

## 2/ 测试时计算与多上下文窗口

粗略来说，你向编码问题投入的令牌越多，结果就越好。Boris 称之为**测试时计算**。

- 使用**独立的上下文窗口**会让结果更好——这就是子代理工作的原理，也是为什么一个代理可能引入错误而另一个（使用完全相同模型）可以发现它们
- 类似于工程团队：如果 Boris 引发了一个错误，他同事审查代码时可能比他更可靠地发现它
- 最终，代理可能会写出完美无错的代码——在那之前，**多个不相关的上下文窗口**通常是一个好方法

<a href="https://x.com/bcherny/status/2031151689219321886"><img src="assets/boris-26-3-10/1.png" alt="Boris Cherny 关于测试时计算" width="50%" /></a>

---

## 来源

- [Boris Cherny (@bcherny) 在 X — 2026 年 3 月 10 日](https://x.com/bcherny)
