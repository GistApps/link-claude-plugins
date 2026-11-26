---
name: create-task
description: Create or update a task card on a Gist Teams board. Use when the user wants to add a task, to-do or action item, assign work to someone, set a due date, or move a card along a board.
---

To create a task:

1. Find the team (`list_teams`, `get_team`) and the board (`get_board`) the task belongs on. Ask if more than one board fits.
2. Pick the column: the board's first column (backlog or to-do) unless the user named one.
3. Call `create_card` with a short action-oriented title, a description with the context and acceptance details, and the assignee and due date when given (`get_team` lists members).
4. To progress existing work, use `move_card` to another column, `update_card` for assignee, due date or labels, and `comment_on_card` for notes.
5. Reply with the card title, board and column, assignee and due date.
