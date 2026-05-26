---
description: Translate a markdown file to Chinese, writing to {basename}_CN.md
argument-hint: [file-path]
model: haiku
---

# Translate Command

Translate a markdown file from English to Chinese. Follow the existing naming convention: `BASENAME.md` → `BASENAME_CN.md`.

## Execution Contract

You MUST:

- Read the source file in full before translating
- Preserve ALL markdown formatting exactly: headers, tables, code blocks, links, inline code, frontmatter, lists
- Preserve ALL image references (`![alt](path)`) unchanged — do not translate paths or alt text
- Preserve ALL badge/link URLs unchanged — only translate link text
- Preserve ALL code blocks verbatim (including comments in code)
- Preserve inline code (`backticks`) — do not translate identifiers or commands
- Preserve YAML frontmatter keys and boolean/string values — translate description strings and comment text only
- Produce idiomatic Simplified Chinese for technical concepts
- Use consistent translations for domain terms:
  - subagent → 子代理
  - hook → 钩子
  - harness → 框架系统
  - tool → 工具
  - skill → 技能
  - command → 命令
  - agent → 代理
  - context → 上下文
  - prompt → 提示词
  - workflow → 工作流
  - orchestration → 编排
  - repository → 仓库

## Workflow

### Step 1: Read Source File

Read the file specified by `[file-path]`. If the file does not exist, report the error and stop.

If the file is already a `_CN.md` file, warn the user and stop.

### Step 2: Translate

Translate the file to Simplified Chinese, following the execution contract rules above.

### Step 3: Write Output

Determine the output path:
- If source is `path/to/NAME.md` → output to `path/to/NAME_CN.md`

Write the translated content to the output file.

## Output Summary

Report:
- Source file path
- Output file path
- Line count of source and output
