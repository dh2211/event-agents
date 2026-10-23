# event-agents

EventPlannerKit: free, open-source Agent Skills that help event, wedding, and conference organizers draft planning timelines, vendor checklists, budget sheets, seating plans, MC scripts, and guest emails, built from their real dates, quotes, and constraints.

Each skill is a folder with a `SKILL.md` file in the open [Agent Skills](https://agentskills.io/specification) format. Claude Code, Codex, Cursor, Grok, OpenCode, and other agents that read that format document a folder for these files. You bring your own AI tool, install the skills once, then ask in plain English: "Build a run of show for a 120-guest wedding on June 14."

**Status: early.** The skills have not yet been tested live in any AI tool. The validator checks their format, not their output. Please tell us what you find.

## Quick start

1. Clone the repository:

   ```bash
   git clone https://github.com/dh2211/event-agents.git
   ```

2. Copy or link the `skills/` folders into the skills folder your agent reads. For Claude Code on macOS or Linux:

   ```bash
   mkdir -p ~/.claude/skills
   cp -R event-agents/skills/* ~/.claude/skills/
   ```

   [docs/install.md](docs/install.md) lists the folder for each agent, with links to each tool's documentation. You don't need Node.js or any other software to use the skills.

3. Start your agent and ask for what you need:

   > Here are my notes for a 200-person one-day conference on March 3. Write the brief, then a planning timeline from today.

   The agent picks the matching skills, asks for anything missing, and drafts.

## Skills

| Skill | What it makes |
| --- | --- |
| [event-brief](skills/event-brief/SKILL.md) | A one-page brief: facts with sources, decision makers, constraints, open questions |
| [event-planning-timeline](skills/event-planning-timeline/SKILL.md) | A countdown of tasks with owners and deadlines, from today to the event |
| [event-run-of-show](skills/event-run-of-show/SKILL.md) | A minute-by-minute day-of schedule with owners, cues, and confirmations |
| [event-vendor-checklist](skills/event-vendor-checklist/SKILL.md) | Questions to ask, terms to get in writing, and confirmations for one vendor type |
| [event-budget-sheet](skills/event-budget-sheet/SKILL.md) | A budget with line items, deposits, due dates, and totals from your real quotes |
| [event-seating-plan](skills/event-seating-plan/SKILL.md) | A draft table plan from your table sizes, groups, and rules, with conflicts listed |
| [event-mc-script](skills/event-mc-script/SKILL.md) | Welcome remarks, introductions, transitions, and announcements for the host |
| [event-guest-email](skills/event-guest-email/SKILL.md) | Save-the-dates, invitations, RSVP requests, reminders, logistics, and thank-yous |
| [event-contingency-plan](skills/event-contingency-plan/SKILL.md) | What could go wrong, who decides, the backup, and who tells whom |

## Agents

An agent here is a short role file that names the skills it uses and the order to use them in. It adds no new instructions about the work. Those live in the skills.

| Agent | Role |
| --- | --- |
| [event-planner-agent](agents/event-planner-agent.md) | Brief, timeline, vendor checklists, and budget, pausing for your approval at each step |
| [event-day-of-agent](agents/event-day-of-agent.md) | Run of show, MC script, and contingency plan for the final weeks |
| [event-guest-comms-agent](agents/event-guest-comms-agent.md) | Invitations, reminders, logistics emails, and seating |

You don't need the agents. Every skill works on its own.

## Examples

[examples/](examples/) has worked outputs written by following the skills. Events, people, vendors, and prices in them are invented.

- [Backyard wedding: planning](examples/backyard-wedding-planning.md). Brief, timeline, and a budget sheet.
- [One-day conference: the day](examples/one-day-conference-day-of.md). Run of show, MC script, and contingency plan.
- [Company party: guests](examples/company-party-guest-comms.md). Invitation with an access and dietary question, a reminder, and a seating plan.

## What the skills always do

Every skill ends with the same Guardrails section, and the validator fails if one is missing or different. The agent:

- uses only your real dates, counts, prices, and terms, and writes `[confirm: what and with whom]` otherwise,
- marks what a vendor, the venue, a speaker, or a guest has to confirm,
- works with guest counts, groups, or initials, not contact details or health information,
- never guesses access or dietary needs, and asks guests to tell you,
- leaves capacity, fire, emergency, permit, alcohol, and food-safety rules to the venue and local authorities,
- adds up budgets, checks timelines for overlaps, and marks unsure items `[verify]`,
- drafts, and leaves confirming, signing, paying, and sending to you.

## Confirm with real people

A draft is not a confirmation. Every price, deposit, and contract term comes from the vendor and the signed contract. Accessibility and dietary needs come from guests, confirmed with the venue and caterer. Safety and venue rules come from the venue and local authorities.

## Privacy

Your AI tool sends what you paste to its provider. Don't paste guest lists with contact details, health information, or signed contracts unless your tool's settings and your client allow it. Use counts, groups, or initials instead.

## Why Agent Skills

[docs/format.md](docs/format.md) explains the choice. In short, a skill is plain Markdown in a folder, several major agents already load the same folder layout, and you can read and edit every instruction.

## Documentation

- [Install for your agent](docs/install.md)
- [Use the skills](docs/usage.md)
- [Write a new skill](docs/authoring.md)
- [Why this format](docs/format.md)
- [Contributing](CONTRIBUTING.md)

## License

[MIT](LICENSE).
