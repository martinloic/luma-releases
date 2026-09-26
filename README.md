# Luma

Luma is a desktop app for notes, tasks and calendar, stored as plain Markdown files in a
folder of your choice, with optional sync to a GitHub repository.

This repository only hosts the downloads. The source code is not public.

![A project note in Luma, with links, tasks, priorities, due dates and time spent](screenshots/notes.png)

## Download

Get the latest version from the [Releases](https://github.com/martinloic/luma-releases/releases/latest) page.

- macOS on Apple Silicon (M1 and later): `Luma-<version>-arm64.dmg`
- Intel Macs, Windows and Linux are not supported yet.

## Features

### Notes in plain Markdown

Your notes are Markdown files in a folder you choose (a vault), browsed as a tree. The
editor saves as you type and supports task lists, tables and `[[links]]` between notes,
with backlinks. A handle next to each line moves it elsewhere in the note. The files stay
readable in any other editor, and an existing Obsidian vault can be opened as is.

### Projects and tasks

A project is a folder, and a task is a Markdown checkbox line in any note, with an optional
priority and due date ([Obsidian Tasks](https://publish.obsidian.md/tasks/) format). The
task view gathers the tasks of the whole vault: overdue, today, later and undated.

![The task view, with overdue, today and later tasks](screenshots/tasks.png)

The same tasks can be sorted in an Eisenhower matrix, by importance (priority) and
urgency (due date).

![The Eisenhower matrix](screenshots/matrix.png)

### Calendar and daily notes

A month view shows the tasks on their due date. A click on a day opens its daily note,
or creates it.

![The month calendar with tasks and daily notes](screenshots/calendar.png)

### Focus

A Pomodoro timer of 15, 25 or 50 minutes, on a task or on nothing in particular. The time
spent is added to the task line itself (`⏱ 1h15m`).

![The focus view during a session](screenshots/focus.png)

### Focus history

Every focus session is kept in the vault. The History view shows, for a day, a week or a
month, the focus time per project, the tasks done and the sessions of each day. A click on
a session or a task opens its note at the task.

![The history of a week, with the time per project, the tasks done and the sessions](screenshots/history.png)

### Search and shortcuts

`⌘K` searches the names and the contents of the notes, and runs actions such as a new
task or a new project. Keyboard shortcuts cover the frequent actions.

![The search palette](screenshots/search.png)

### GitHub sync

The vault can be synchronized both ways with a GitHub repository, through the Git of your
Mac. Each sync commit lists the files it changed. Conflicts never lose anything: both
versions are kept. It requires Git and a GitHub authentication already set up on your Mac
(SSH key or `gh auth login`).

### English and French

The interface is available in English and French.

## Limitations

Luma is young, and some things are not there (yet):

- **One vault at a time**: no list of vaults or switching between them.
- **Calendar**: month view only, no week or day view. No events with times, no Google,
  Outlook or iCloud calendars, no drag and drop of tasks between days.
- **Tasks**: no recurring tasks, no start or scheduled dates, no Kanban view.
- **Focus**: 15, 25 or 50 minutes only, no long breaks, a single end chime. Sessions
  cannot be edited or entered by hand, and the history has no charts or export. The time
  spent before version 0.2.0 is not in the history.
- **Links**: embedded notes (`![[note]]`) and block links are kept in the file but not
  displayed. Standard Markdown links to notes are not followed. No graph view.
- **Renaming outside Luma**: renaming or moving notes in Finder or through Git does not
  update the `[[links]]` pointing to them. Rename and move notes in Luma.
- **GitHub sync**: Git must be installed on your Mac, and only GitHub repositories can be
  cloned. No version history or restore from Luma (Git keeps it). No sync on quit.
- **Languages**: English and French only.

## First launch on macOS

Luma is not signed with an Apple Developer certificate yet, so macOS blocks the first
launch:

1. Open the DMG and drag Luma into Applications.
2. Open Luma: macOS says it cannot verify the app. Close the message.
3. Open System Settings > Privacy & Security, scroll down, and click **Open Anyway** next
   to the message about Luma.
4. Confirm. The next launches open normally.

## License

Luma is free to use, but it is not open source. See [LICENSE](LICENSE).
