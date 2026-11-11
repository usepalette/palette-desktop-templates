# project

The project space inside the company OS: how the team runs its projects, with the steps to start one and record its decisions, how the team works on a project, and the formats a project's pages use. **Company-wide rules live in the root [`AGENTS.md`](../../AGENTS.md) and always apply**; this file adds how to think and behave here. For what lives where, see [`README.md`](README.md).

## Posture

Work as a teammate who understands the engagement and runs it well: who the project is for, what was agreed, what has changed since, and what has to happen next. Each project lives in its own folder in [`projects/`](../../projects/README.md); this space holds how the team runs one, so every project starts with the same pages, keeps its decisions with their reasons, changes its scope in the open, and shows anyone who opens it where it stands.

## Before project work

The root rules say who the person is and what to read first. Then, in this order:

1. **If `SETUP.md` exists in this folder, read it.** The project space is still being set up. Setup never blocks the task the person came with.
2. **For work on a project, read its `README.md` in [`projects/`](../../projects/README.md)**: the **Now** line, the milestones, the people and the decisions. Then the extras it keeps for the part the work touches, such as its brief or its scope, and its latest meeting notes when the history matters.
3. **Before writing a page a project makes again and again**, read its format in [`templates/`](templates/README.md).

## The projects this team runs

**This team runs [client engagements | internal projects | both].** Setup fills in this line. Until it is filled in, ask the person once and work the way they answer.

- **Client engagements** — The project is for a customer with a folder in [`customers/`](../../customers/README.md). Its `customer` field names that folder, the two link both ways, and the customer's people are the customer's key people there. The scope is what was agreed with the customer: a change to it is recorded with who agreed.
- **Internal projects** — The project is for the company. The person it is for inside the company, its sponsor, stands where a customer would, and agrees to a change of scope. `customer` stays empty.
- **Both** — Each project's `customer` field says which it is.

## Rules

- **Record a decision with its context and its consequences.** Every real decision on a project gets a dated `Decision:` line in the project's `README.md`. One with real options or consequences (a trade-off, a change of scope or priority, a change of mind) also gets a numbered record in the project's decisions folder: [`processes/record-a-decision.md`](processes/record-a-decision.md). A record is never rewritten: a change of mind is a new record that supersedes the old one. A suggestion is never written up as a decision.
- **A meeting gets a note.** A meeting about a project becomes one note in that project's meetings folder: say "log this meeting", and [`company/meetings.md`](../../company/meetings.md) says what else to update.
- **A change of scope goes in the scope's change log.** When the project keeps a scope page, the change gets a dated row in its change log, linking the decision record behind it. In every project, the in and out lists change to match. Never change a project's scope silently.
- **Keep the Now line current.** Before you finish work on a project, its **Now** line says where it stands this week and the next thing that has to happen. Change `phase` in its frontmatter and its row in the Active table of [`projects/README.md`](../../projects/README.md) when the phase changes, and `health` only when a person assesses it.
- **Use the formats in `templates/`.** A brief, goals, a stakeholder map, a scope, a timeline, a glossary, a decision record, a research note or the design links starts as a copy of its format. Never fill the format in place.
- **One home per fact.** The project's `README.md` is the summary: the Now line, the milestones, the people and the decisions live there and nowhere else. The extras add detail and link back. The stakeholder map adds influence and interest to the People table, never a second roster. Tasks live in the task home named in [`company/tools.md`](../../company/tools.md).
- **Start from the company context.** The company, its customers and its people are in [`company/`](../../company/README.md), [`customers/`](../../customers/README.md) and [`people/`](../../people/README.md). Link to them; never copy them into the space or into a project.
- **Follow a process when one exists.** Check [`processes/README.md`](processes/README.md); if there is a process for what you are doing, use it.

## Where to read for a task

| When the task is… | Read |
|---|---|
| Setting up the project space | `SETUP.md` if it exists |
| Starting a project, or adding the extras to one | [`processes/start-a-project.md`](processes/start-a-project.md) |
| Recording a decision, or a change of scope | [`processes/record-a-decision.md`](processes/record-a-decision.md) |
| Logging a meeting on a project | [`company/meetings.md`](../../company/meetings.md), then the project's meetings folder |
| Writing a project page from a format | its format in [`templates/`](templates/README.md) |
| How the team works on a project: its meetings, channels, decisions, what done means | [`playbooks/ways-of-working.md`](playbooks/ways-of-working.md) |
| Someone joining a project | [`playbooks/joining-a-project.md`](playbooks/joining-a-project.md) |
| Bringing a statement of work, a proposal or kickoff notes in | the root rules for bringing material in, then the formats it fills |
| Closing a project | [`projects/README.md`](../../projects/README.md) → Close a project |

## Updating this space

- A better way of working on a project → the playbook. A better way of doing something → the process.
- A format that changed → its file in `templates/`. New projects inherit the change; pages already copied keep theirs.
- A correction about running projects here → `lessons.md`. A decision or a change about how projects are run → `log.md`. What was decided on one project goes in that project, never here.
- A rule the person states for running projects → this file, under **Rules**. What is here and where things go → `README.md`.

Keep this file short. Detail belongs in the pages it links to.
