---
name: daily-agenda
description: Summarize the user's Gist Calendar schedule. Use when the user asks what is on their calendar, what their day or week looks like, when they are free, or whether they have conflicts.
---

To brief the user on their schedule:

1. Work out the window in the user's timezone (today, tomorrow, this week) and call `list_events` with `filter.timeMin`/`timeMax` as ISO 8601 timestamps. Follow `pageInfo` if `hasNextPage` is true.
2. List events in time order: start-end, title, location or meeting link, and whether the user has not yet responded.
3. Point out overlaps, back-to-back stretches with no break, and free gaps of 30 minutes or more.
4. For invitations still awaiting a response, offer to answer with `respond_to_event`.
5. Keep it short; use `get_event` only when the user asks about one event's details.
