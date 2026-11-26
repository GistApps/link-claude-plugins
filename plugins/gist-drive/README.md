# Gist Drive

Find, organize and share the files and folders in your Gist Drive from a
conversation with Claude. Ask Claude to locate a document by name, list what
is in a folder or shared with you, tidy files into folders, share an item with
a teammate, or get a download link.

## Use it

1. Add the plugin, then connect **Gist Drive** from the plugin's
   Connectors tab and sign in with your GistLink account.
2. Choose the organization Claude may act in. The connection only reaches
   Drive, with your own permissions.
3. Ask things like "Find the signed contract for Acme" or "Move last month's
   invoices into the Finance folder."

Skills included:

- **find-file**: searches by name and view, and confirms the right item with
  its folder path.
- **organize-files**: plans folder moves, shows the plan, then creates folders
  and moves items.

## Data

The plugin sends your requests and the file and folder details you work with
to your GistLink account through `https://mcp.gist.link/drive/mcp`. File
contents are only reachable through short-lived download links you ask for.
It stores nothing itself. See the [privacy policy](https://gist.link/privacy)
and the [connector documentation](https://developers.gist.link/mcp/connectors/drive/).
