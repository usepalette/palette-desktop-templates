---
type: index
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
template: project@2611111
---

# Project

How the team runs its projects: the steps to start one and record its decisions, how the team works on a project, and the formats a project's pages use. Each project lives in [`projects/`](../../projects/README.md), one folder each, made the way the workspace makes every project. This space holds how it is run.

Company-wide rules live in the root [`AGENTS.md`](../../AGENTS.md) and always apply. How to think and behave *in this space* is in this folder's [`AGENTS.md`](AGENTS.md).

## Get started

While `SETUP.md` exists in this folder, the space is still being set up. Say "set up the project space" and tell the agent what you have: whether you run client engagements, internal projects or both, which pages a new project gets, who sits on the other side of your projects, and where your tasks live. Any one of those is enough to start.

The formats in [`templates/`](templates/README.md) open with a box that says they are molds: a project copies them, and they are never filled in here. The two playbooks open with a box until the team has written how it works.

## You need to…

| You need to… | Go to |
|---|---|
| Understand how to think and work in this space | [`AGENTS.md`](AGENTS.md) |
| Start a project | Say "we're starting a new project"; the steps are in [`processes/start-a-project.md`](processes/start-a-project.md) |
| Record a decision on a project, or a change of scope | Say "we decided …" or "record this decision"; the steps are in [`processes/record-a-decision.md`](processes/record-a-decision.md) |
| Log a meeting on a project | Say "log this meeting"; the note goes in the project's meetings folder, as [`company/meetings.md`](../../company/meetings.md) says |
| See where a project stands | its `README.md` in [`projects/`](../../projects/README.md): the **Now** line, then the milestones |
| See where every project stands | the Active table in [`projects/README.md`](../../projects/README.md), or the Projects overview page when the workspace has one |
| Know how the team works on a project | [`playbooks/ways-of-working.md`](playbooks/ways-of-working.md) |
| Bring someone onto a project | [`playbooks/joining-a-project.md`](playbooks/joining-a-project.md) |
| Write a brief, goals, a stakeholder map, a scope, a timeline or another project page | its format in [`templates/`](templates/README.md) |
| Close a project | Say "that project is done"; the steps are in [`projects/README.md`](../../projects/README.md) → Close a project |
| Capture how something is done here | Say "let me explain how we do this"; **Capturing how the work is done** below says where it goes |
| Record a correction about running projects here | [`lessons.md`](lessons.md) |
| Record a decision or a change about how projects are run | [`log.md`](log.md) |

## Structure

```
project/
├── README.md        # this front door
├── AGENTS.md        # how to think and behave here: the posture, and the rules that add to the root's
├── CLAUDE.md · GEMINI.md   # thin pointers so each agent loads AGENTS.md
├── SETUP.md         # present only while the project space is being set up
├── playbooks/       # how the team works on a project, and how someone joins one
├── processes/       # starting a project, recording a decision
├── templates/       # the formats a project's pages use: brief, goals, stakeholder map, scope, timeline, …
├── lessons.md       # what to do differently here
└── log.md           # what happened here
```

Add a folder when real work needs one, and give it its own `README.md`. Don't create empty stubs to fill the tree.

## How a project runs here

A project is a folder in `projects/`. This space is how the team runs it, from the first day to the last.

1. **Start.** "We're starting a new project": the project is made the way the workspace makes every project, then gets the extras this team uses and `space: project` in its frontmatter ([`processes/start-a-project.md`](processes/start-a-project.md)).
2. **Run.** Each meeting gets a note in the project's meetings folder. Each real decision gets a dated `Decision:` line in the project's `README.md`, and a numbered record when it has real options or consequences ([`processes/record-a-decision.md`](processes/record-a-decision.md)). A change of scope gets a row in the scope's change log. The **Now** line says where the project stands this week.
3. **Close.** "That project is done": the project is closed the way the workspace closes every project, with a short retro. What the team would do differently comes back here, to [`lessons.md`](lessons.md).

A project run this way looks like this. The extras are the ones the project uses, and the last three folders are made when their first file arrives, never empty:

```
projects/<name>/
├── README.md        # the front page: the Now line, scope, milestones, people, decisions
├── meetings/        # one note per meeting
├── brief.md · goals.md · stakeholders.md · scope.md · timeline.md   # the extras, copied from templates/
├── decisions/       # the numbered decision records
├── research/        # interviews and findings
└── design/          # links to the design files and prototypes
```

## Capturing how the work is done

When someone explains, pastes or points at how a project is run here, it becomes one file in one of these folders. One explanation often holds two of them (the thinking and the steps): split it into two files that link to each other.

| What you have | It is a | Goes in |
|---|---|---|
| A point of view: what matters, how to choose, what good looks like | playbook | `playbooks/<domain>.md` |
| Steps in an order, with a trigger and a finished state | process | `processes/<name>.md` |
| A format to fill in for a page projects make again and again | template | `templates/<output>.md` |
| Settled facts to load before working | foundation | `foundations/<topic>.md`, a folder made with its first file from the workspace's space mold, [`spaces/_template/foundations/`](../_template/foundations/README.md) |

Write the file from that folder's `_template.md`, in the words of the people who do the work, and add a row to that folder's `README.md`. Never add principles, steps or rules nobody gave you; a gap stays a gap, marked as an open question at the bottom of the file.

## What lives elsewhere

| For… | Go to |
|---|---|
| The projects themselves | [`projects/`](../../projects/README.md), one folder each |
| A customer: their brief and their key people | [`customers/`](../../customers/README.md) |
| A teammate: who they are and how to work with them | [`people/`](../../people/README.md) |
| The company's rituals, its channels and who owns what | [`company/how-we-work.md`](../../company/how-we-work.md) |
| How meetings are noted, and where a note goes | [`company/meetings.md`](../../company/meetings.md) |
| A word the whole company uses | [`company/glossary.md`](../../company/glossary.md) |
| Tasks and issues | the task home named in [`company/tools.md`](../../company/tools.md) |
| Contracts, statements of work, invoices and rates | the restricted place named in [`company/tools.md`](../../company/tools.md); a project links to them and never holds the details |

One fact, one home: read and link across the OS instead of copying.
