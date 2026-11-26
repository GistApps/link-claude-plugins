---
name: catch-up
description: Catch the user up on Gist Teams. Use when the user asks what they missed, what is happening in a channel or team, what needs their attention, or what is on their plate.
---

To catch the user up:

1. Call `my_home` for unread channels and direct messages, recent activity, cards assigned to the user and pending check-ins.
2. For a specific channel, find it with `list_teams` / `get_team`, then read it with `get_channel`. For a direct message, use `list_conversations` and `get_conversation`.
3. Summarize per channel or conversation: decisions made, questions waiting on the user, and action items with owners. Skip small talk.
4. List the user's assigned cards that are overdue or due soon (`get_card` for details when needed).
5. To find an older discussion, use `search_messages` with a short keyword.

Offer to reply with `send_message`, but only post after the user approves the exact text.
