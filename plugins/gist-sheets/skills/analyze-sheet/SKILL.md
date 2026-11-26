---
name: analyze-sheet
description: Analyze or summarize data in a Gist Sheets spreadsheet. Use when the user asks about totals, trends, averages, lookups or anomalies in a spreadsheet, tracker or report stored in Gist Sheets.
---

To analyze a spreadsheet:

1. Find the workbook with `search_workbooks` unless the user gave an id. If several titles match, ask which one.
2. Call `get_workbook` to see its worksheets and their row/column counts. Pick the worksheet the question is about.
3. Read the header row with `get_values` (rowStart 0, rowEnd 0, columnStart 0, columnEnd = columnCount - 1) so you know what each column holds.
4. Read the data with `read_rows`, following `hasNextPage` until you have the rows you need. For a small, known area use `get_values` instead.
5. Compute the answer yourself from the values. Treat empty cells as missing, not zero, and mention it when they affect the result.
6. Reply with the answer first, then the worksheet and A1 range you used (for example `Q3!B2:B41`). Show a short table only when it helps; never paste whole sheets.

Indexes are 0-based: row 0 is spreadsheet row 1 and column 0 is column A.
