---
name: update-tracker
description: Add or update rows in a Gist Sheets tracker or list. Use when the user wants to record new entries, log progress, fix values or keep a planning or tracking sheet in Gist Sheets up to date.
---

To update a tracker:

1. Locate the workbook (`search_workbooks`) and worksheet (`get_workbook`).
2. Read the header row with `get_values` and map each piece of information to a column. Ask when a value has no obvious column instead of inventing one.
3. New entries: call `append_rows` with one row per entry, cells in header order (`{"value": ...}`, or `{"formula": "=..."}` when the sheet uses formulas in that column).
4. Changes to existing entries: find the row with `read_rows`, then call `update_values` for just the cells that change, passing the workbook's current `revision` as `expectedRevision`. If it fails because the sheet changed, re-read and retry once.
5. Before overwriting or clearing cells that already hold data, tell the user what will change and get a yes.
6. Confirm what you wrote with the A1 range, for example "Added 3 rows at Pipeline!A42:F44".

Indexes are 0-based: row 0 is spreadsheet row 1 and column 0 is column A.
