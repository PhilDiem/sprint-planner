# Sprint Planner

A lightweight, single-file sprint planning tool for teams. No build step, no dependencies – just open in a browser.

## Features

- **Tasks with Subtasks** – Each task can have unlimited subtasks. All fields available on both levels.
- **Assignee** – Free-text assignee with autocomplete (previously used names).
- **Estimates** – Free-text: `3`, `4h`, `2d`, `5 SP`. Hours are normalized to days (8h = 1d) in reports.
- **Status** – Click the circle to cycle: To Do → In Progress → Done.
- **Progress Bars** – Subtask completion rolls up as a percentage bar on the parent task.
- **Assignee Filter** – Filter the task list by assignee.
- **Sprint Goal** – A multiline text field at the top. Included in export/import.
- **Markdown Export** – Download your sprint as `.md`, ready to paste into Slack or save.
- **Markdown Import** – Restore tasks from a previously exported file.
- **Report** – Modal with per-assignee breakdown: tasks, subtasks, estimates, progress bars.
- **Report Export** – Download the report as markdown too.
- **Persistence** – Everything saved to `localStorage` automatically.
- **Themes** – Light, Dark, and Unicorn (rainbow) mode. Choice is saved.

## Usage

1. Open `index.html` in any modern browser.
2. Add a sprint goal, then start adding tasks.
3. Click the status circle to mark progress.
4. Use **Export MD** to share the plan, **Report** to see per-person stats.

## Example

```
Sprint Planner                [Light|Dark|Unicorn]
                              [Export] [Import] [Report]

Sprint Goal: Deliver the checkout MVP by Friday

Filter: [All Assignees ▼]
[Task title...] [Assignee...] [Est...] [Add]

  ○ API Design            Alex   3h   --- 50% ---
    ○ GET /users          Alex   1h
    ✓ POST /users         Anna   1h
    ☐ Tests               Alex   1h
  ○ Setup CI/CD                  2d   ---  0% ---
  ✓ Planning done                 -   ---100% ---
```

## Tech

- **Zero dependencies** – Pure HTML, CSS, and Vanilla JavaScript.
- **Single file** – Everything in `index.html`.
- **localStorage** – No server, no database.
- **Responsive** – Works on desktop and mobile.
