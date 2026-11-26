---
name: find-file
description: Find a file or folder in Gist Drive. Use when the user asks where a document is, wants a file by name or topic, or asks what is in a folder, shared with them, starred or recently changed.
---

To find a file:

1. Pick the view that matches the request and call `search_files`:
   - by name or topic: `filter.search`
   - "shared with me", "starred", "recent", "in the trash": the matching filter flag
   - "in folder X": find the folder first, then `filter.parentId`
2. If nothing matches, retry once with a shorter or alternative search term before reporting no results.
3. When several items match, list up to five with name, type, last update and owner, and ask which one.
4. For the chosen item, call `get_folder_path` and reply with its full path so the user can recognise it.
5. Only call `get_download_link` when the user wants to open or download the file. Say the link expires shortly.
