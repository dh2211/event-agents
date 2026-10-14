# Company party: guests

Invented event: Northwind Studio's end-of-year party for 40 staff and guests. Skills used: `event-guest-email`, `event-seating-plan`.

## Request

> End-of-year dinner, Friday December 10, 2027, 19:00 to 23:00, at The Glasshouse restaurant, private room. RSVP by November 26 using the form link. Smart casual. From: the people team. Then, once RSVPs are in, seat 40 at 5 tables of 8.

## Invitation (event-guest-email)

**Subject:** You're invited: end-of-year dinner, Friday December 10

> Hi `[guest name]`,
>
> Join us for Northwind Studio's end-of-year dinner.
>
> **When:** Friday, December 10, 19:00 to 23:00
> **Where:** The Glasshouse, private room, `[confirm: address]`
> **Dress:** Smart casual
> **Please reply by November 26:** `[RSVP form link]`
>
> In the form, tell us about any dietary needs or anything that would make the evening easier for you, such as step-free access or a quieter seat. Only the people team and the restaurant will see this.
>
> Getting there: `[confirm: transport and parking from venue]`
>
> See you there,
> The people team

Checklist: address and transport confirmed with the venue, RSVP form link tested, access and dietary question included.

## Reminder (event-guest-email)

**Subject:** Reminder: reply by November 26 for the end-of-year dinner

> Hi `[guest name]`, a quick reminder to reply by Friday, November 26 for our dinner on Friday, December 10 at The Glasshouse. Reply here: `[RSVP form link]`. Let us know about any dietary or access needs in the form.

## Seating plan (event-seating-plan)

RSVPs as the planner gave them, in groups:

- Leadership: 4
- Design team: 12
- Engineering team: 14
- Operations: 6
- Partners and plus-ones: 4, seated with the person they came with

Rules: mix teams at each table; leadership not all at one table. Reported needs (from the form, counts only): 1 guest needs step-free access, 2 prefer a quieter seat.

| Table | Seats | Assigned | Notes |
| --- | --- | --- | --- |
| 1 | 8 | Leadership 1, Design 3, Engineering 3, Operations 1 | Nearest the step-free entrance `[confirm with venue]`; the guest who needs step-free access sits here |
| 2 | 8 | Leadership 1, Design 3, Engineering 3, Operations 1 | |
| 3 | 8 | Leadership 1, Design 2, Engineering 3, Operations 2 | Quieter corner `[confirm with venue]`; 2 guests who asked for a quieter seat |
| 4 | 8 | Leadership 1, Design 2, Engineering 3, Operations 2 | |
| 5 | 8 | Design 2, Engineering 2, Partners and plus-ones 4 | Move plus-ones next to their hosts once names are placed |

Count: 8 + 8 + 8 + 8 + 8 = 40. No table over capacity.

Conflicts: plus-ones should sit with the person they came with, so table 5 is a placeholder until the planner places names. Confirm the table layout matches the venue's floor plan.
