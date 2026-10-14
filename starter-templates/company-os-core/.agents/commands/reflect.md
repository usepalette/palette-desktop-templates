---
type: command
owner: Shared
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: everyone
description: "Go through the lessons.md and log.md files and propose what to merge, move, promote into a guide or drop. Suggests only"
argument-hint: "[a folder; leave out for the whole workspace]"
---

# Reflect

The pass that keeps the memory files short and makes what was learned stick. A lesson that keeps coming back becomes a line in the guide agents read every time, and leaves `lessons.md`.

**It only suggests.** Show each change and let a person approve it. Never rewrite a rule in an `AGENTS.md`, delete history from a `log.md`, or touch a folder you may not edit, on your own.

Say "tidy the lessons", or name the command, with a folder if only that folder is meant. Run it when a `lessons.md` passes about twenty lines, after a heavy session, or weekly.

## 1. Tidy

For each `lessons.md` and `log.md` in scope:

- **Merge** lines that say the same thing. When a lesson replaced an older one, the older one goes.
- **Shorten** a lesson that tells the story of a session: keep the rule, its scope and one clause of why, in two sentences at most.
- **Real dates:** turn "yesterday" and "last week" into `YYYY-MM-DD`.
- **Right file:** a rule sitting in a `log.md`, or history sitting in a `lessons.md`, moves to the other.
- **Right scope:** a line about one person in a shared file, or a company-wide rule in a person's file, moves to the narrowest place that benefits.
- **Right home:** a lesson that is really a fact or a format (a word the company avoids, how a note is laid out) belongs on the page that holds it. Fix the page; leave at most a pointer.
- **Contradictions:** show two lessons that disagree. Don't pick; ask.

## 2. Promote and retire

- **Promote** a lesson that has come up more than once, or that every session needs: into a rule in an `AGENTS.md`, a line in a `README.md`, a playbook, or a person's "How to work with me". Then remove it from `lessons.md`.
- **Retire** a lesson that has already become a rule, or that is stale and never came back. Say why.

## What you show

```
## Reflect — {scope} — {date}

### Tidy ({count})
- {file}: {merge | shorten | date | wrong file | wrong scope | wrong home | contradiction} → {the change}

### Promote ({count})
- "{lesson}" → into {guide}, out of {lessons.md} — {why}

### Retire ({count})
- "{lesson}" in {file} → drop — {already a rule | stale}
```

Change only what the person says yes to. Stamp `last_updated` and `last_updated_by` (the person, never an agent) on every file you change.
