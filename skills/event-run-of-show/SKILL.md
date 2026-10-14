---
name: event-run-of-show
description: "Writes a minute-by-minute run of show for the event day, with setup, vendor arrivals, program, cues, owners, and teardown. Use when a planner asks for a day-of timeline, run of show, run sheet, wedding day schedule, or conference agenda for staff."
license: MIT
---

# Run of show

Give everyone working the day one schedule they can follow.

## Ask first

1. Venue access times: earliest setup, latest teardown, from the venue contract.
2. Program: ceremony, sessions, meal, speeches, entertainment, with any fixed times.
3. Vendors and their agreed arrival and departure times.
4. Who runs the day, and who is the backup contact.

## Steps

1. Start at venue access and end at the venue's out time. Never schedule outside them.
2. List each block with start, end, location, what happens, owner, and cue.
3. Add travel time between locations and buffers before key moments. Check that no two blocks overlap for the same person or room.
4. Mark every arrival time as `[confirm with vendor]` until the planner says it is confirmed.
5. Add a contact column with roles only ("caterer lead"), not phone numbers, unless the planner provides them for this sheet.
6. Note where the `event-mc-script` skill should provide announcements.

## Output

A table: time, end, location, item, owner, cue, confirmed (yes or no). Then a short list for the final check: unconfirmed times, tight buffers, venue rules to check.

## Guardrails

- Real details only: use the dates, times, counts, names, prices, and terms the planner gives you. Never invent vendor names, prices, deposits, availability, contract terms, or venue facts. Write `[confirm: what and with whom]` instead.
- Confirm with real people: mark every item a vendor, the venue, a speaker, or a guest has to confirm, and say who confirms it. A draft is not a confirmation.
- Guest privacy: work with counts, roles, groups, or initials. Do not ask for guest contact details or health information. If the planner pastes them, replace them with placeholders and say that you did.
- Accessibility and dietary needs: never guess or assume a guest's needs. Ask guests directly, give them a way to tell the planner, and confirm with the venue and caterer.
- Safety and venue rules: capacity, fire and emergency procedures, permits, alcohol, and food safety come from the venue and local authorities. Flag them for the planner to check. Do not state them as fact.
- Accuracy: add up every budget total and check every timeline for overlaps and travel time. Mark anything you are not sure of with `[verify]`.
- The planner decides: you draft. The planner confirms, signs, pays, and sends.
