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
with backlinks. The files stay readable in any other editor, and an existing Obsidian
vault can be opened as is.

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

### Search and shortcuts

`⌘K` searches the names and the contents of the notes, and runs actions such as a new
task or a new project. Keyboard shortcuts cover the frequent actions.

![The search palette](screenshots/search.png)

### GitHub sync

The vault can be synchronized both ways with a GitHub repository, through the Git of your
Mac. Conflicts never lose anything: both versions are kept. It requires Git and a GitHub
authentication already set up on your Mac (SSH key or `gh auth login`).

### English and French

The interface is available in English and French.

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
