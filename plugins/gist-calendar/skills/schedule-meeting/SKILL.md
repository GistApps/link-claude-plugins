---
name: schedule-meeting
description: Schedule a meeting in Gist Calendar. Use when the user wants to set up, book, move or find a time for a meeting or event with one or more people.
---

To schedule a meeting:

1. Collect what is missing: attendees' emails, duration, the date range, and the title. Default to 30 minutes within working hours (09:00-17:00 in the user's timezone) when not stated.
2. Call `find_busy_times` for the attendees and the user over the range, and `list_events` for the user's own calendar.
3. Propose up to three free slots that suit everyone, earliest first, with times in the user's timezone.
4. After the user picks one, call `create_event` with title, start/end, timezone and attendees. Say that attendees will receive an invitation.
5. To move an existing meeting, use `update_event`; for a recurring series ask whether to change this occurrence, following ones or all. Use `cancel_event` only after the user confirms.
