---
name: draft-ticket-reply
description: Summarize a Gist Support ticket and draft a reply or internal note. Use when an agent asks to answer, respond to, summarize or follow up on a support ticket.
---

To draft a ticket reply:

1. Read the ticket with `get_ticket`: the requester, every message in order, status, priority and tags.
2. Summarize it in two or three lines: the problem, what has been tried, and what the customer is waiting for.
3. Draft the reply: acknowledge the issue, answer or give the next step, and say when they will hear back. Match the customer's language. Do not promise refunds, credits or dates the agent has not confirmed.
4. Show the draft and ask whether to send it publicly, post it as an internal note, or edit it.
5. On approval, call `reply_to_ticket` with `isPublic` true (customer-visible, `includeSignature` true) or false (internal note). Then offer to update the status with `set_ticket_status`, for example to pending.
