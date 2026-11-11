---
type: template
owner: "[Owner]"
status: draft
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
---

# Timeline

> **Mold.** The format of a project's timeline; don't fill it in here. [`processes/start-a-project.md`](../processes/start-a-project.md) copies it into a project as `projects/<name>/timeline.md`.
>
> In the copy: everything from **Fill in** down, with its own full frontmatter as `type: doc` ([`README.md`](README.md) → How templates work). Write only what you were given: never invent a phase or a date, a slot you have nothing for keeps its brackets, and a line you worked out yourself ends with "(to confirm)".

The project's phases with their dates, the other dates the plan has to respect, and what could move them. The milestones stay in the project's `README.md`.

## How to write this

- **Load first:** the project's `README.md`: its `start`, `end` and `phase`, and its Milestones table.
- **One home per date.** A milestone lives in the README's Milestones table, never here. The names of the phases are the words the README's `phase` field uses: when a phase starts, `phase` changes to its name.
- **Quality bar:** every phase ends in an outcome someone can check, and every risk says what it would move.

## Fill in

_The format itself, with a bracket in every slot. Copy from here down into the new document._

# [Project name]: timeline

## Phases

| Phase | Start | End | Outcome |
|---|---|---|---|
| [A phase, such as discovery, build or launch] | YYYY-MM-DD | YYYY-MM-DD | [what is true when it ends] |

## Key dates

Dates the plan has to respect that are not milestones: a holiday, a freeze, a review the project waits on.

| Date | Event | Notes |
|---|---|---|
| YYYY-MM-DD | [The event] | [why it matters to the plan] |

## Risks to the timeline

- **[A risk]** — [what it could move, and what the team does about it]
