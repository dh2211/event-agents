# Use the skills

After you [install the skills](install.md), ask your agent for what you need in plain English. The agent matches your request to a skill's description and loads it. You can also name the skill: "Use the event-budget-sheet skill to..."

## Brief it like a colleague

The skills ask for missing details, but a complete first request saves a round trip. Include:

- event type, date, and venue,
- guest count, as a number,
- what is already booked, with real quotes and contract dates,
- who decides,
- what guests have told you about access or dietary needs, as counts ("3 vegetarian, 1 wheelchair user"), not names.

## Start with the brief

Run the `event-brief` skill first. Keep the result and paste it at the start of later requests, so every document uses the same date, count, and budget.

## Requests that work well

- "Write a brief for a 90-guest backyard wedding on September 20. Budget ceiling is `[your budget]`. Tent not booked yet."
- "Build a planning timeline from today to the conference on March 3. Venue and catering are booked."
- "What should I ask a wedding photographer before booking?"
- "Here are my quotes so far. Lay them out in a budget sheet with totals and a payment schedule."
- "Seat 64 guests at 8 tables of 8. Groups and rules below."
- "Write an MC script for the awards dinner, timed to this run of show."
- "Write an RSVP reminder. Deadline is May 1, reply by the form link."

## Plan a whole event

Ask for the `event-planner-agent` workflow, or say: "Write the brief, then the timeline, vendor checklists, and budget." The agent stops after each step for you to approve or change it.

## Confirm before you send or sign

1. Search for `[confirm`, `[quote needed]`, `[verify]`, and `[from venue` and fill them in with real people.
2. Check budget totals and timeline times.
3. Read every guest message before you send it.
4. Get safety, capacity, and emergency details from the venue in writing.

## Keep guest data out

Don't paste guest emails, phone numbers, or health details. Use counts, groups, or initials. The skills replace personal details they see, but by then the text has reached the AI provider.
