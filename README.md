- `C-z` - "undo" state - Use this command when you get into a weird state that seems to break Evil mode. Also make sure CAPS lock is not active.
- `SPC .` - Switch open buffer.
- `SPC ,` - Switch open buffer in current project.


# Org Mode

- `SPC m l l` - major mode link - `org-insert-link` - Insert a new link, OR edit an existing link.
  - For a normal link, select HTTP, then press escape, followed by `y` to paste the URL.
- `SPC m x` - make x - `org-toggle-checkbox`

## Org Agenda

## Tables



### Task Management

- `SPC o a t` - org agenda tasks - View all open tasks

#### From the org-agenda view:

- `RET` - Open the .org file containing the TODO entry at point
- `J` - Priority down
- `K` - Priority up

#### Directly from the .org file containing TODO entries:

- `RET` (on a task) - Toggle between `TODO` and `DONE`
- `SPC m p p ?` - major put priority - Assign a priority (A, B, C) to a task

- `SPC m l l` - 'org-insert-link' - Create a new file and link to it from here (it wants the file extension or protocol first I think, probably `org`, followed by the path)


# Code Editing

- `z a` - Expand or collapse the currently open code block (`z o` or `z c` to explicitly open or close).
- `g c c` - Comment or uncomment the current line of code.
- `K` - `lsp-describe-thing-at-point`
- `g d` - Go to definition
- `C-o` - (better-jumper-jump-backward) - Navigate outward (back)
- `C-i` - (better-jumper-jump-forward) - Navigate inward (forward)



# Keep these repos synced

- Doom Config
- 2B
- swe-toolbox
