---
name: event-budget-sheet
description: "Lays out an event budget with categories, line items, quotes, deposits, due dates, and running totals, filled only with the planner's real numbers. Use when a planner asks for a wedding budget, conference budget, cost tracker, or payment schedule."
license: MIT
---

# Budget sheet

Give the planner a budget they fill with real quotes, and do the math for them.

## Ask first

1. Budget ceiling and who approves changes.
2. Quotes and contracts they already have, with amounts, deposits, and due dates.
3. Currency, and whether tax and service charges are included in the quotes.

## Steps

1. Lay out categories that fit the event (venue, food and drink, rentals, staff, decor, AV, entertainment, printing, transport, contingency).
2. For each line item, columns: vendor, quoted, contracted, deposit paid, balance, due date, status.
3. Fill only numbers the planner gave you. Leave every other cell blank with `[quote needed]`. Never suggest typical costs or averages.
4. Add up every column, show the total against the ceiling, and show the difference.
5. Add a contingency line as a percentage the planner chooses.
6. List payments due in date order.

## Output

The budget table with totals, the gap to the ceiling, and a payment schedule. Then: items still missing quotes, and any total you could not compute. Offer CSV so the planner can paste it into a spreadsheet.

## Guardrails

- Real details only: use the dates, times, counts, names, prices, and terms the planner gives you. Never invent vendor names, prices, deposits, availability, contract terms, or venue facts. Write `[confirm: what and with whom]` instead.
- Confirm with real people: mark every item a vendor, the venue, a speaker, or a guest has to confirm, and say who confirms it. A draft is not a confirmation.
- Guest privacy: work with counts, roles, groups, or initials. Do not ask for guest contact details or health information. If the planner pastes them, replace them with placeholders and say that you did.
- Accessibility and dietary needs: never guess or assume a guest's needs. Ask guests directly, give them a way to tell the planner, and confirm with the venue and caterer.
- Safety and venue rules: capacity, fire and emergency procedures, permits, alcohol, and food safety come from the venue and local authorities. Flag them for the planner to check. Do not state them as fact.
- Accuracy: add up every budget total and check every timeline for overlaps and travel time. Mark anything you are not sure of with `[verify]`.
- The planner decides: you draft. The planner confirms, signs, pays, and sends.
