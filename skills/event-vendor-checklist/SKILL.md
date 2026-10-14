---
name: event-vendor-checklist
description: "Writes a checklist for one vendor type: questions to ask before booking, what to get in writing, and what to confirm before the day. Use when a planner asks what to ask a caterer, venue, photographer, DJ, florist, AV company, or rental vendor, or wants a vendor tracking sheet."
license: MIT
---

# Vendor checklist

Help the planner ask the right questions and get the answers in writing.

## Ask first

1. Vendor type and the event it is for.
2. What the planner needs from this vendor.
3. Where they are: comparing quotes, booked, or final week.

## Steps

1. Write questions to ask before booking: availability for the date, what is included, what costs extra, deposits, payment schedule, cancellation and weather terms, insurance, setup and teardown needs.
2. List what must be in the signed contract. Do not tell the planner what a term usually is or should cost.
3. Write a confirmation list for the final weeks: arrival time, contact on the day, final counts, power and space needs, dietary or accessibility details passed on.
4. For comparing several vendors, give a blank comparison table the planner fills with real quotes.

## Output

Three checklists (before booking, in the contract, before the day) and an optional comparison table with every price cell blank. Offer the `event-budget-sheet` skill to track the quotes.

## Guardrails

- Real details only: use the dates, times, counts, names, prices, and terms the planner gives you. Never invent vendor names, prices, deposits, availability, contract terms, or venue facts. Write `[confirm: what and with whom]` instead.
- Confirm with real people: mark every item a vendor, the venue, a speaker, or a guest has to confirm, and say who confirms it. A draft is not a confirmation.
- Guest privacy: work with counts, roles, groups, or initials. Do not ask for guest contact details or health information. If the planner pastes them, replace them with placeholders and say that you did.
- Accessibility and dietary needs: never guess or assume a guest's needs. Ask guests directly, give them a way to tell the planner, and confirm with the venue and caterer.
- Safety and venue rules: capacity, fire and emergency procedures, permits, alcohol, and food safety come from the venue and local authorities. Flag them for the planner to check. Do not state them as fact.
- Accuracy: add up every budget total and check every timeline for overlaps and travel time. Mark anything you are not sure of with `[verify]`.
- The planner decides: you draft. The planner confirms, signs, pays, and sends.
