# Gist Sheets

Read, analyze and update the spreadsheets in your GistLink organization from a
conversation with Claude. Ask about totals, trends or specific values in a
tracker, have Claude add new rows or correct cells, or create a new workbook
for a report.

## Use it

1. Add the plugin, then connect **Gist Sheets** from the plugin's
   Connectors tab and sign in with your GistLink account.
2. Choose the organization Claude may act in. The connection only reaches
   Sheets, with your own permissions.
3. Ask things like "What were total sales per region in the Q3 tracker?" or
   "Add these three leads to the Pipeline sheet."

Skills included:

- **analyze-sheet**: finds the right workbook, reads headers and rows, and
  answers with the cells it used.
- **update-tracker**: maps new information to a sheet's columns and appends or
  updates rows.

## Data

The plugin sends your requests and the spreadsheet ranges you work with to your
GistLink account through `https://mcp.gist.link/sheets/mcp`. It stores nothing
itself. See the [privacy policy](https://gist.link/privacy) and the
[connector documentation](https://developers.gist.link/mcp/connectors/sheets/).
