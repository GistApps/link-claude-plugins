---
name: organize-files
description: Reorganize files and folders in Gist Drive. Use when the user wants to tidy up, group files into folders, rename items, clean up old files or share a folder with someone.
---

To organize files:

1. List the items involved with `search_files` (for a folder, use `filter.parentId`).
2. Propose a plan: folders to create, items to move or rename, items to trash. Show it as a short list and get the user's go-ahead before changing anything.
3. Apply it in this order: `create_folder`, then `move_items` (batch ids per destination), then `rename_item`.
4. Use `trash_items` only for items the user explicitly agreed to remove; mention they can be restored with `restore_items`.
5. To share, call `share_item` with the person's email (or the whole organization) and the role the user asked for: viewer unless they said editor.
6. Finish with a summary of what changed and where things are now.
