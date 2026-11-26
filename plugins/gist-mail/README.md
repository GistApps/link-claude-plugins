# Gist Mail

Work through your GistLink inbox with Claude. Search threads, summarize long
conversations, sort and label messages, and draft replies that you can review
before anything is sent. Claude only sends an email when you ask it to.

## Use it

1. Add the plugin, then connect **Gist Mail** from the plugin's Connectors
   tab and sign in with your GistLink account.
2. Choose the organization Claude may act in. The connection only reaches
   Mail, with your own mailboxes and permissions.
3. Ask things like "What needs my reply today?" or "Draft a reply to Dana's
   pricing question."

Skills included:

- **triage-inbox**: groups unread threads by what they need from you and
  offers to archive, label or star them.
- **draft-reply**: reads the thread and saves a draft in your voice; it sends
  only after you say so.

## Data

The plugin sends your requests and the messages you work with to your GistLink
account through `https://mcp.gist.link/mail/mcp`. Emails you choose to send
are delivered by Gist Mail to their recipients. The plugin stores nothing
itself. See the [privacy policy](https://gist.link/privacy) and the
[connector documentation](https://developers.gist.link/mcp/connectors/mail/).
