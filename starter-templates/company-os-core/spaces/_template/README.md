---
type: index
owner: "[Owner]"
status: draft
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
---

# [Space]

> **Mold.** This folder is copied to add a space; don't fill it in here. The steps are in the `README.md` one level up, under "Add a space".
>
> In the copy: put in the name, the owner and the one-line purpose the person gave you, and add the rows this space needs to the table below. Preserve the four `_template.md` files as molds, but apply the space's chosen edit policy to them. Follow the root page-state procedure before removing this box.

[One line: what this space is for, and what it holds.]

Company-wide rules live in the root [`AGENTS.md`](../../AGENTS.md) and always apply. How to think and behave *in this space* is in this folder's [`AGENTS.md`](AGENTS.md).

## You need to…

| You need to… | Go to |
|---|---|
| Understand how to think and work in this space | [`AGENTS.md`](AGENTS.md) |
| Load the reference this work builds on, before starting | [`foundations/`](foundations/README.md) |
| Know how a domain is thought about here | [`playbooks/`](playbooks/README.md) |
| Do something step by step | [`processes/`](processes/README.md) |
| Produce a recurring output in this space's format | [`templates/`](templates/README.md) |
| Capture how something is done here | Say "let me explain how we do this"; **Capturing how the work is done** below says where it goes |
| Record a correction about working here | [`lessons.md`](lessons.md) |
| Record a decision or a change | [`log.md`](log.md) |
| [A task specific to this space] | [where it lives] |

## Structure

```
[space]/
├── README.md        # this front door
├── AGENTS.md        # how to think and behave here (delete it if the root rules are enough)
├── CLAUDE.md · GEMINI.md   # thin pointers so each agent loads AGENTS.md
├── foundations/     # what is known here: the reference to load before working
├── playbooks/       # how to think: one file per domain
├── processes/       # how things are done: step-by-step checklists
├── templates/       # the fill-in formats for recurring outputs
├── lessons.md       # what to do differently here
└── log.md           # what happened here
```

This is a starting shape. Add subfolders as real work arrives (`meetings/` with the first meeting note, for example), each with its own `README.md`, and remove the ones this space doesn't need. Don't create empty stubs to fill the tree.

## Capturing how the work is done

When someone explains, pastes or points at how something is done here, it becomes one file in one of the four folders. One explanation often holds two of these (the thinking and the steps): split it into two files that link to each other.

| What you have | It is a | Goes in |
|---|---|---|
| Settled facts to load before working | foundation | `foundations/<topic>.md` |
| A point of view: what matters, how to choose, what good looks like | playbook | `playbooks/<domain>.md` |
| Steps in an order, with a trigger and a finished state | process | `processes/<name>.md` |
| A format to fill in for a recurring output | template | `templates/<output>.md` |

Write the file from that folder's `_template.md`, in the words of the people who do the work, and add a row to that folder's `README.md`. Never add principles, steps or rules nobody gave you; a gap stays a gap, marked as an open question at the bottom of the file.

## What lives elsewhere

| For… | Go to |
|---|---|
| What the whole company shares: the brand, the products, the market, the tools | [`company/`](../../company/README.md) |
| The projects that belong to this space | [`projects/`](../../projects/README.md) |
| The customers this work touches | [`customers/`](../../customers/README.md) |
| How to work with a teammate | [`people/`](../../people/README.md) |
| Tasks and issues | the task home named in [`company/tools.md`](../../company/tools.md) |

One fact, one home: read and link across the OS instead of copying.
