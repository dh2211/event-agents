# Write a new skill

A skill is a folder with a `SKILL.md` file. This page explains how to add one that passes the validator and fits the kit.

## Decide whether it should be a skill

Add a skill when planners need a distinct document or procedure the current skills don't produce. If the request is a variation of an existing skill ("a run of show with two rooms"), improve that skill instead. Fewer, better skills are easier for the agent to choose between.

## Create the folder

```bash
mkdir skills/event-volunteer-briefing
```

The folder name is the skill name. It must start with `event-` and use only lowercase letters, digits, and single hyphens, at most 64 characters. The prefix keeps our skills from replacing your own skills with the same name when both sit in a shared folder. Agent file names in `agents/` start with `event-` for the same reason.

## Write the frontmatter

`SKILL.md` must start on line 1 with YAML frontmatter:

```markdown
---
name: event-volunteer-briefing
description: "Writes a briefing for event volunteers with roles, shifts, and who to ask. Use when a planner asks for volunteer instructions, a shift briefing, or a crew sheet."
license: MIT
---
```

- `name` must match the folder name.
- Put `description` in double quotes. Descriptions often contain a colon, and an unquoted colon makes the YAML invalid, so agents load the skill without its description.
- `description` must be 50 to 1,024 characters. Say what the skill makes, then "Use when" with the words a planner would type. The agent picks skills by this text alone.

Use only the fields from the [Agent Skills specification](https://agentskills.io/specification). Tool-specific fields work in one agent and are ignored or rejected in another.

## Write the body

Follow the shape of the existing skills:

1. A one-line purpose.
2. **Ask first.** The 3 or 4 inputs the skill needs. The agent asks only for missing ones.
3. The steps, as numbered commands. Name any method you rely on and say what it means in one line.
4. **Output.** The exact sections and order of the result.
5. **Guardrails.** Copy the section from any existing skill, word for word. The validator fails without it.

Keep `SKILL.md` under 500 lines. Move long reference material into a `references/` folder inside the skill and link it with a relative path. Keep links one level deep.

To point at another skill, write its name in backticks followed by "skill": "use the `event-budget-sheet` skill". Don't link to another skill's file. Planners can install one skill without the others, and a link would break. The validator checks that every name written this way exists.

## Write for planners and for the agent

- Plain English, short sentences, no jargon a new planner wouldn't know.
- Write instructions the agent can follow without guessing: "Add 10 minutes of buffer before each key moment", not "leave some buffer".
- Don't claim research findings without a source. Name the source if you rely on one.
- No em dashes. The validator rejects them.

## Add an example

Produce a real output by following your skill for one invented event, and add it to `examples/`. If you can't produce a good example by following the instructions, the instructions need work.

## Check it

```bash
npm run validate
npm test
```

Both run in CI on every pull request.
