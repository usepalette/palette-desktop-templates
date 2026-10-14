---
type: index
owner: Shared
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
---

# Projects

One folder per project. A project folder holds the brief, the milestones, the decisions and the meeting notes. **Tasks and issues have one home**, the tracker or shared fallback named in [`company/tools.md`](../company/tools.md). A project folder holds context and task links, not a second checklist.

## You need to…

| You need to… | Go to |
|---|---|
| Start a project | Say "we're starting a new project"; the steps are under **Start a project** |
| Understand where a project stands | its `README.md`: the **Now** line, then the milestones |
| Log a meeting | Say "log this meeting"; the note goes in `<project>/meetings/` and the README is updated |
| Record a decision | a dated `Decision:` line in the project README's **Decisions** section |
| Close a project | Say "that project is done"; the steps are under **Close a project** |
| Run it the way this kind of work is done here | the playbooks and templates of the space it belongs to, under [`spaces/`](../spaces/README.md) |
| Record a correction about how this folder works | [`lessons.md`](lessons.md) |

## The project folder

Copied from [`_template/`](_template/README.md):

```
<project>/
├── README.md       # the brief: what and why, scope, milestones, people, decisions
└── meetings/       # one file per meeting
```

Plus whatever the work produces: designs, research, drafts. Add folders as real files arrive, each with its own `README.md`.

## Start a project

1. **Check it doesn't exist.** If `projects/<name>/` exists, open it instead.
2. **Copy [`_template/`](_template/README.md)** to `projects/<name>/`, whole: the `README.md` and `meetings/` with its two files. The folder is named for the project's scope, in kebab-case; the README heading keeps the readable name.
3. **Write only what you were given.** Fill the heading, the one-liner and the **Now** line. Milestones and people go in when the person names them: delete the bracketed rows you have no real values for, and never invent a milestone or a date. A line you worked out yourself ends with "(to confirm)".
4. **Stamp the frontmatter:** `owner`, `status` (`draft` while exploring, `active` once committed), `phase`, `health`, `customer` and `space` when there is one, `start`, `end`, `tracker`, `last_updated` is today, `last_updated_by`. Write every date quoted. Use `health: unknown` until an assessment is supplied. Fill the project name, known owner, chosen edit policy, date and attribution in `meetings/README.md` too; preserve `meetings/_template.md` as a mold. Follow [page states](../.agents/page-states.md) for the review box: project lifecycle and confirmation are independent.
5. **Add the row** to the Active table below, replacing the "None yet" row if it is the first.
6. **Link the customer both ways** when there is one: the project's Links table gets the customer's brief, and the customer README's **Projects** section gets a line linking the project.

## Close a project

A project never closes on its own. It closes when a person says so.

1. **Read the folder** and note what is still open: milestones that are not `done`, unresolved questions and linked tasks.
2. **Resolve open items.** If closing was already clearly requested and nothing consequential is unresolved, proceed. Otherwise show the outstanding choices as one batch: done, dropped, or moved to the task home or another project. Don't invent their outcome.
3. **Ask for a short retro**, and accept "skip": what went well that we should repeat, what we would do differently, and what is left that someone should know about.
4. **Update the brief.** Frontmatter: `status: archived`, `archived: "YYYY-MM-DD"` (ask for the date; don't assume today) and `reason:` (completed, or decided against and why). Set each milestone to its true final status. Replace the **Now** line with one sentence on how it ended, and add a `## Retro` section with the answers.
5. **Move the row** from Active to Archived, with the close date. Update the customer's **Projects** line if there is one.
6. **Capture what was learned.** Each "do differently" answer becomes a line in the right `lessons.md` (the nearest existing parent pair, the relevant space's or the root), and [`log.md`](log.md) gets one line saying the project closed and how.

Nothing is deleted: the folder stays where it is, so no link breaks. Reopening is the reverse.

## Projects

### Active

| Project | Customer | Phase | Health | Owner | Updated |
|---|---|---|---|---|---|
| _None yet._ | | | | | |

### Archived

| Project | Customer | Closed | How it ended |
|---|---|---|---|
| _None yet._ | | | |

## Conventions

- **`status` says where the project stands:** `draft` (exploring, nothing committed), `active` (committed and in flight), `archived` (finished, or decided against). Update the field in the same session the project changes state, and move its row.
- **`health`** is `unknown` until assessed, then `on-track`, `at-risk`, `off-track` or `paused`. **`phase`** is your own vocabulary (discovery, design, build, launch, …).
- **`customer`** is the folder name under `customers/` when the project is for one, and the two link both ways. **`space`** is the folder name under `spaces/` of the area the project belongs to. Both stay empty when there is none.
- **`tracker`** is the link to the board, the project in the task tool, or the one shared fallback task file. `start` and `end` are the project dates, quoted.
- A milestone's status is `planned`, `in-progress`, `done` or `delayed`.
- Decisions are dated lines in the README's **Decisions** section, newest on top.
