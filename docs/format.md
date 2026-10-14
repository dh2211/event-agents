# Why the kit uses Agent Skills

This page explains why event-agents ships as Agent Skills folders instead of prompts, a plugin for one tool, or an app.

## What a planner needs from the format

A planner should be able to read every instruction the AI follows, change it to fit their events, and use it in whichever AI tool they already pay for. A planning team should be able to keep its own copy in a shared folder. Nothing should need a server, an account, or code.

## Why Agent Skills fits

An Agent Skill is a folder with a `SKILL.md` file: YAML frontmatter with a `name` and a `description`, then Markdown instructions. The [specification](https://agentskills.io/specification) is short and open.

Claude Code, Codex, Cursor, Grok, and OpenCode all document loading this layout ([install.md](install.md) links each page). We have not yet tested the skills live in any of them.

The agent sees only each skill's name and description until a request matches, then loads the full instructions. Nine skills cost little context when they're idle, so you can install all of them.

Markdown is the whole format. A planner with no coding background can open `event-run-of-show/SKILL.md`, see why every arrival time is marked to confirm, and change the columns.

## What we gave up

- **Tool-specific features.** We use only the fields in the specification, so every tool reads the same file the same way.
- **A guided app.** Skills rely on the agent to ask for missing details, and quality depends on the model behind it.
- **Shared reference files.** Each skill holds what it needs, including its own copy of the Guardrails section. That duplicates a few lines, but you can install one skill alone and it still works.

## What an agent is here

An agent file in `agents/` is a short role description: a `name`, a `description`, the list of skills it uses, and the order to use them in. The know-how stays in the skills, so the agents never drift from them. The Markdown-with-frontmatter shape matches Claude Code's custom subagents, and other tools can take the body as a prompt.
