---
name: log-interaction
description: Record a customer interaction in Gist CRM. Use when the user describes a call, meeting or email with a customer and wants it logged, wants to update a deal after it, or wants a follow-up task created.
---

To log an interaction:

1. Find the contact (and their deal, if one was discussed) with `search_contacts` or `find_by_email`, then `list_deals`. Create the contact with `create_contact` only if the user confirms they are new.
2. Call `log_activity` with kind `call`, `meeting`, `email` or `note`, a concise body (what was discussed, decisions, next steps), `occurredAt`, and the contact, company and deal uuids that apply.
3. If the deal moved forward or stalled, propose the stage change; after the user agrees, call `move_deal` (see `list_pipelines` for stage uuids). Use `update_deal` for amount or close-date changes.
4. For each follow-up, call `log_activity` with kind `task` and a `dueAt` date.
5. Reply with a short summary of everything recorded.
