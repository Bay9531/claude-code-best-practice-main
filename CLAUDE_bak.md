# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a best practices reference repository for Claude Code configuration, demonstrating patterns for skills, subagents, hooks, and commands. It is a documentation and examples repository — not a runnable application.

## Key Components

### Weather System (Example Workflow)
Demonstrates Command → Agent → Skill architecture:
- `/weather-orchestrator` command (`.claude/commands/weather-orchestrator.md`) — entry point, invokes agent then skill
- `weather-agent` agent (`.claude/agents/weather-agent.md`) — preloaded `weather-fetcher` skill, Sonnet, 5 turns
- `weather-fetcher` skill (`.claude/skills/weather-fetcher/SKILL.md`) — agent-only, fetches Dubai temp from Open-Meteo
- `weather-svg-creator` skill (`.claude/skills/weather-svg-creator/SKILL.md`) — creates SVG card, writes output
See `orchestration-workflow/orchestration-workflow.md` for the complete flow diagram.

### Agent Teams System (Experimental)
Self-contained demo in `agent-teams/` showing the experimental agent teams feature with a parallel time-orchestration workflow. Bootstrap prompt at `agent-teams/agent-teams-prompt.md`.

### Development Workflows
- `development-workflows/rpi/` — Research → Plan → Implement pattern with 8 specialized subagents (PM, UX, CTO, requirement parser, senior engineer, code reviewer, documentation analyst, constitutional validator) and 3 commands (`/rpi:research`, `/rpi:plan`, `/rpi:implement`)
- `development-workflows/cross-model-workflow/` — Claude Code + Codex dual-model workflow: Plan (Claude) → QA Review (Codex) → Implement (Claude) → Verify (Codex). Documents 4 bridging mechanisms (plugin, MCP, router)

### Skill Definition Structure
Skills in `.claude/skills/<name>/SKILL.md` use YAML frontmatter:
- `name`, `description` (for auto-discovery), `argument-hint`, `disable-model-invocation`, `user-invocable`
- `allowed-tools`, `model`, `context` (set to `fork` for isolated subagent), `agent`, `hooks`

Two skill patterns: **agent skills** (preloaded via agent's `skills:` field, `user-invocable: false`) vs **standalone skills** (invoked via `Skill` tool or `/` menu).

### Subagent Definition Structure
Subagents in `.claude/agents/*.md` use YAML frontmatter:
- `name`, `description` (use "PROACTIVELY" for auto-invocation), `tools`, `disallowedTools`
- `model` (haiku/sonnet/opus/inherit), `permissionMode` (e.g. `acceptEdits`, `bypassPermissions`), `maxTurns`
- `skills` (preloaded agent skills), `mcpServers`, `hooks`, `memory` (user/project/local)
- `background`, `effort` (low/medium/high/max), `isolation` (worktree), `color`

### Presentation System
Per-presentation agents handle slide decks (see `.claude/rules/presentation.md`):
- `presentation-vibe-coding` → `presentation/vibe-coding-to-agentic-engineering/`
- `presentation-claude-gemini` → `presentation/2026-04-25-gdg-kolachi-cli-claude-code-gemini/`
- `presentation-claude-code` → `presentation/claude-code-best-practice/`

### Hooks System
Cross-platform sound notification system in `.claude/hooks/`:
- `scripts/hooks.py` — Python handler for all 27 hook events, with agent-specific sound support
- `config/hooks-config.json` — shared team config (enable/disable per hook); `hooks-config.local.json` for personal overrides
- `sounds/` — per-event .mp3/.wav pairs (ElevenLabs TTS)
- 27 hooks registered: PreToolUse, PostToolUse, UserPromptSubmit, Notification, Stop, SubagentStart, SubagentStop, PreCompact, SessionStart, SessionEnd, Setup, PermissionRequest, TeammateIdle, TaskCompleted, ConfigChange, and more
- Special: git commits trigger `pretooluse-git-committing` sound
- Full docs: `.claude/hooks/HOOKS-README.md`

## Configuration

### Hierarchy
1. **Managed** (`managed-settings.json` / MDM plist / Windows Registry) — org-enforced, cannot override
2. Command line arguments — single-session overrides
3. `.claude/settings.local.json` — personal project settings (git-ignored)
4. `.claude/settings.json` — team-shared project settings
5. `~/.claude/settings.json` — global personal defaults
6. `hooks-config.local.json` overrides `hooks-config.json`

### Key Project Settings
- `CLAUDE_AUTOCOMPACT_PCT_OVERRIDE=80` — auto-compact at 80% context
- `plansDirectory: "./reports"` — plans stored in reports directory
- `outputStyle: "Explanatory"` — verbose tutorial-style output
- `Co-Authored-By: Claude` on all commits
- Custom spinner verbs and tips override built-in defaults
- Status line shows model, branch, context %, cost
- `enableAllProjectMcpServers: true`

### MCP Servers (`.mcp.json`)
- `playwright` — browser automation (`npx @playwright/mcp@0.0.70`)
- `context7` — documentation lookup (`npx @upstash/context7-mcp@2.1.8`)
- `deepwiki` — wiki search (`npx deepwiki-mcp@0.0.6`)

## Content Directories

- `best-practice/` — Authoritative reference docs: subagents, commands, skills, settings, memory, MCP, CLI flags, power-ups
- `reports/` — 13 deep-dive analyses: agent memory, advanced tool use, SDK vs CLI, LLM degradation, harness importance, spinner verbs, browser MCP comparison, settings scopes, etc.
- `tips/` — 8 curated tip collections from Boris Cherny (Claude Code creator) and Thariq (Anthropic), organized by date
- `videos/` — 8 video/podcast transcripts (Karpathy, Matt Pocock, Boris Cherny, etc.) with timestamps
- `tutorial/` — Beginner curriculum: day0 (setup Windows/Linux/macOS), day1 (Prompting → Agents → Skills)
- `implementation/` — Working examples showing how each concept is implemented in this repo
- `changelog/` — Version tracking per category

## Critical Patterns

### Subagent Orchestration
Subagents **cannot** invoke other subagents via bash. Use the Agent tool:
```
Agent(subagent_type="agent-name", description="...", prompt="...", model="haiku")
```
Be explicit about tool usage in subagent definitions — avoid vague terms like "launch."

### README Table Maintenance
Commands in `.claude/commands/workflows/` update README tables for development workflows, agent collections, and skill collections. Best-practice change tracking workflows in `.claude/commands/workflows/best-practice/`.

## Answering Best Practice Questions

Always search this repo first (`best-practice/`, `reports/`, `tips/`, `implementation/`, `README.md`) before relying on training knowledge or external sources. This repo is the authoritative source.

## Workflow Best Practices

- Keep CLAUDE.md under 200 lines per file for reliable adherence
- `.claude/rules/*.md` with `paths:` frontmatter are lazy-loaded only when matching files are touched; without frontmatter they load into every session like CLAUDE.md
- Use commands for workflows instead of standalone agents
- Create feature-specific subagents with skills (progressive disclosure) rather than general-purpose agents
- Perform manual `/compact` when context approaches the auto-compact threshold (80% in this project)
- Start with plan mode for complex tasks
- Use human-gated task list workflow for multi-step tasks
- Break subtasks small enough to complete in well under the compact threshold

### Debugging
- `/doctor` for diagnostics
- Run long-running terminal commands as background tasks for better log visibility
- Use browser automation MCPs (Playwright, Chrome DevTools) for Claude to inspect console logs
- Provide screenshots when reporting visual issues

## Git Commit Rules

Create **separate commits per file** — do NOT bundle multiple file changes into a single commit. Each file gets its own commit with a descriptive message specific to that file's changes.

## Documentation

See `.claude/rules/markdown-docs.md` for documentation standards:
- Keep files focused — one topic per file
- Use relative links between docs, not absolute GitHub URLs
- Include back-navigation link at top of best-practice and report docs
- When adding a new concept or report, update the corresponding table in README.md
