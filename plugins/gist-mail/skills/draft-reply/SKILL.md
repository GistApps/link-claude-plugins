---
name: draft-reply
description: Draft or send an email reply from Gist Mail. Use when the user asks to reply to, answer, follow up on or write an email, or to send a message from their Gist Mail mailbox.
---

To draft a reply:

1. Find the thread (`search_threads` with `filter.search`) and read it with `get_thread`.
2. Write the reply: answer every question asked, match the thread's language and tone, and keep it short. Leave placeholders like [date] for facts you do not know rather than guessing.
3. Save it with `save_draft`, passing the thread's `mailbox_uuid` and `thread_uuid` so it is threaded as a reply. Show the user the draft text.
4. Send only when the user explicitly says to send. Then call `send_email` with the saved `draft_uuid` and report that it was queued.
5. For edits, update the same draft by passing its `draft_uuid` to `save_draft`.

For a new message (not a reply), confirm the recipients' addresses before saving the draft.
