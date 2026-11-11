---
type: template
owner: "[Owner]"
status: draft
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
---

# Design links

> **Mold.** The format of a project's index of design files and prototypes; don't fill it in here. Copy it into the project as `projects/<name>/design/design-links.md` when the first design file or prototype is linked. A project without a design folder makes it first: [`README.md`](README.md) → Folders a project makes later.
>
> In the copy: everything from **Fill in** down, with its own full frontmatter as `type: doc` ([`README.md`](README.md) → How templates work). Write only what you were given, and delete a table the project has nothing for.

Where a project's design files and prototypes are, who owns each, and which design system they build on. The design tool is the source of truth: this page links to the files and never copies them.

## How to write this

- **Load first:** the project's `README.md`, and the design space's pages when the workspace has a design space.
- **Links, not exports.** A file or a prototype is linked where it lives. A snapshot goes into the project only when someone asks for one.
- **No credentials.** If a prototype needs a login, say where the login is kept, never the login itself.
- **Reasoning the files can't hold,** such as why a flow was chosen, goes on its own page in the project's design folder, named for its subject. A design choice with consequences for the whole project is a decision record.
- **Quality bar:** anyone on the project finds the current file for a screen in one click, and knows who to ask about it.

## Fill in

_The format itself, with a bracket in every slot. Copy from here down into the new document._

# [Project name]: design links

## Design files

| File | What it covers | Owner | Link |
|---|---|---|---|
| [The file's name] | [the flows or screens it holds] | [name] | [url] |

## Prototypes

| Prototype | What it tests | Audience | Link |
|---|---|---|---|
| [The prototype's name] | [the question it answers] | [the team, the customer, or test participants] | [url] |

## Design system

- **Name:** [the design system the project builds with]
- **Source of truth:** [a link to the repo, the library or the docs]
- **Notes:** [what the project reuses, and what it adds]
