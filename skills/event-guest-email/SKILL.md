---
name: event-guest-email
description: "Writes guest emails and messages: save-the-dates, invitations, RSVP requests, reminders, logistics, and thank-yous, with a way for guests to share access and dietary needs. Use when a planner asks for an invitation, an RSVP reminder, a logistics email, an agenda email, or a thank-you note."
license: MIT
---

# Guest email

Write clear messages that tell guests what they need and ask them what the planner needs to know.

## Ask first

1. Which message: save-the-date, invitation, RSVP request, reminder, logistics, change notice, or thank-you.
2. The confirmed details: date, time, venue, dress code, RSVP deadline and method, parking and transport.
3. Tone and who it is from.

## Steps

1. Put the key details at the top: what, when, where, and what the guest must do.
2. Use only confirmed details. Mark anything else `[confirm]` and say it must be filled before sending.
3. In RSVP and invitation messages, ask guests to share any access or dietary needs, and say who will see that information.
4. Address guests with a merge placeholder such as `[guest name]`. Do not ask for or store a guest list here.
5. For a change notice, state what changed first, then what stays the same.
6. Write a short subject line and a plain-text version.

## Output

Subject line, message, and a checklist: every detail confirmed, RSVP method works, access and dietary question included where it applies.

## Guardrails

- Real details only: use the dates, times, counts, names, prices, and terms the planner gives you. Never invent vendor names, prices, deposits, availability, contract terms, or venue facts. Write `[confirm: what and with whom]` instead.
- Confirm with real people: mark every item a vendor, the venue, a speaker, or a guest has to confirm, and say who confirms it. A draft is not a confirmation.
- Guest privacy: work with counts, roles, groups, or initials. Do not ask for guest contact details or health information. If the planner pastes them, replace them with placeholders and say that you did.
- Accessibility and dietary needs: never guess or assume a guest's needs. Ask guests directly, give them a way to tell the planner, and confirm with the venue and caterer.
- Safety and venue rules: capacity, fire and emergency procedures, permits, alcohol, and food safety come from the venue and local authorities. Flag them for the planner to check. Do not state them as fact.
- Accuracy: add up every budget total and check every timeline for overlaps and travel time. Mark anything you are not sure of with `[verify]`.
- The planner decides: you draft. The planner confirms, signs, pays, and sends.
