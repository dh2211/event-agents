---
name: event-planning-timeline
description: "Builds a planning timeline that counts back from the event date, with tasks, owners, deadlines, and vendor booking windows. Use when a planner asks for a wedding planning timeline, a conference countdown, a task list by month, or a planning schedule."
license: MIT
---

# Planning timeline

Work back from the event date to today, so nothing lands too late.

## Ask first

1. Event date and today's date.
2. The brief from the `event-brief` skill, or the event type, size, and venue status.
3. What is already booked or done.
4. Who is on the planning team, and what each person owns.

## Steps

1. Count back from the event date in phases: booking, details, confirmations, final week, day before.
2. Put venue and date-critical bookings first. Do not state how far ahead a vendor type books up. Write `[confirm lead time with vendor]`.
3. Give every task one owner and one deadline. If the deadline has already passed, flag it at the top.
4. Add confirmation tasks: final counts, dietary and accessibility details from guests, vendor arrival times, payments due.
5. Check that tasks for one person do not pile up in the same week. Say where they do.

## Output

A table by phase: task, owner, deadline, depends on, status. Then a list of overdue or tight items. Offer a day-of schedule next with the `event-run-of-show` skill.

## Guardrails

- Real details only: use the dates, times, counts, names, prices, and terms the planner gives you. Never invent vendor names, prices, deposits, availability, contract terms, or venue facts. Write `[confirm: what and with whom]` instead.
- Confirm with real people: mark every item a vendor, the venue, a speaker, or a guest has to confirm, and say who confirms it. A draft is not a confirmation.
- Guest privacy: work with counts, roles, groups, or initials. Do not ask for guest contact details or health information. If the planner pastes them, replace them with placeholders and say that you did.
- Accessibility and dietary needs: never guess or assume a guest's needs. Ask guests directly, give them a way to tell the planner, and confirm with the venue and caterer.
- Safety and venue rules: capacity, fire and emergency procedures, permits, alcohol, and food safety come from the venue and local authorities. Flag them for the planner to check. Do not state them as fact.
- Accuracy: add up every budget total and check every timeline for overlaps and travel time. Mark anything you are not sure of with `[verify]`.
- The planner decides: you draft. The planner confirms, signs, pays, and sends.
