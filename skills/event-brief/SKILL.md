---
name: event-brief
description: "Turns a planner's notes into a one-page event brief: purpose, date, venue, guest count, budget ceiling, must-haves, decision makers, and open questions. Use when a planner starts a new event, a wedding, or a conference and wants everything in one place before planning."
license: MIT
---

# Event brief

Put the facts of one event on one page, so every later document starts from the same details.

## Ask first

1. Event type and purpose, in the host's words.
2. Date or date range, location or venue, and expected guest count. Unknowns stay `[confirm]`.
3. Budget ceiling, and who approves spending.
4. Must-haves and deal-breakers, and the people who make final decisions.

## Steps

1. Write each known fact once, with its source ("from the venue contract", "from the couple").
2. List every fact that is still open as a question, with the person who can answer it.
3. Note known constraints: accessibility, dietary needs reported by guests, cultural or religious requirements, travel, weather.
4. List the vendors and roles the event will likely need, without naming specific businesses.

## Output

1. **Event at a glance**: type, purpose, date, venue, guest count, budget ceiling.
2. **Decision makers**.
3. **Must-haves and deal-breakers**.
4. **Constraints**.
5. **Open questions**: question, who answers, by when.
6. **Roles to fill**.

Offer a planning timeline next with the `event-planning-timeline` skill.

## Guardrails

- Real details only: use the dates, times, counts, names, prices, and terms the planner gives you. Never invent vendor names, prices, deposits, availability, contract terms, or venue facts. Write `[confirm: what and with whom]` instead.
- Confirm with real people: mark every item a vendor, the venue, a speaker, or a guest has to confirm, and say who confirms it. A draft is not a confirmation.
- Guest privacy: work with counts, roles, groups, or initials. Do not ask for guest contact details or health information. If the planner pastes them, replace them with placeholders and say that you did.
- Accessibility and dietary needs: never guess or assume a guest's needs. Ask guests directly, give them a way to tell the planner, and confirm with the venue and caterer.
- Safety and venue rules: capacity, fire and emergency procedures, permits, alcohol, and food safety come from the venue and local authorities. Flag them for the planner to check. Do not state them as fact.
- Accuracy: add up every budget total and check every timeline for overlaps and travel time. Mark anything you are not sure of with `[verify]`.
- The planner decides: you draft. The planner confirms, signs, pays, and sends.
