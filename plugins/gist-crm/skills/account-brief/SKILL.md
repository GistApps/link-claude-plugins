---
name: account-brief
description: Prepare a brief on a customer from Gist CRM. Use when the user asks who someone is, wants background before a call or meeting, or asks for the status of an account, contact, company or deal.
---

To prepare an account brief:

1. Identify the record. With an email address, call `find_by_email`; otherwise `search_contacts` or `search_companies` by name. If several match, ask which one.
2. Pull the full picture with `get_contact` (customer 360) or `get_company`.
3. Add open deals with `list_deals` filtered to that contact or company, and recent history with `list_activities`.
4. Write the brief in this order:
   - who they are (name, title, company, owner)
   - open deals: title, stage, amount, expected close
   - last three interactions with dates
   - open tasks and anything overdue
   - one or two suggested talking points drawn from the history
5. Amounts are stored in minor units with a currency: show 125000 USD as $1,250.00.
