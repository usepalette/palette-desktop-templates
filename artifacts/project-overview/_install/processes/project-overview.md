---
type: process
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
cadence: weekly
template: project-overview@2611092
---

# Projects overview

Writes where every project stands this week into [`../project-overview.html`](../project-overview.html), and shares the stakeholder version after a yes.

## When to run this

- On Monday, for the week that starts that day.
- When someone asks: "make me a projects overview", "refresh the projects overview", "update the projects overview", "share the overview", "send the projects page to the board", "give someone the stakeholder view".
- When someone presses Refresh on the page.

## Where it goes

- **Stakeholder version:** `project-overview-stakeholders.html`, beside the page. The first share makes it.
- **Readers:** [Who gets the stakeholder version, for example the people above and beside the team. The first share asks, and writes the answer here.]

## Sources

- **Linear or Jira**: the projects. Progress, target dates, status, owners and open issues.
- **The `projects/` folder** at the root of the workspace: the projects the team keeps there, with their owners and dates. Read it only. Never create or change a file in it.
- **GitHub**: the pull requests merged this week, per project.
- **Slack**: the updates in the project channels, and the pinned one.
- **Notion or Google Docs**: the specs the projects link to.

Every source is optional. Check which ones are connected. For a missing one, say what it would add, for example "connect Linear and the projects fill themselves". Without GitHub, leave out the pull-request counts. Without Slack, ask the person for the pinned update, or leave it "Not filled in yet". Never invent a line.

## How the page is built

- Read the page only down to the `end of content` comment. The script and the style after it never change.
- Write only inside elements with `data-slot`. Everything outside a slot is the team's: never change it.
- An element with `data-kept="YYYY-MM-DD"` was changed at someone's request. Never rewrite it. If its source changed since, say so.
- When someone asks to change a line, change it and add `data-kept` with today's date.
- The slots:

  | Slot | What it holds |
  |---|---|
  | `week` | The day of the run, for example `Monday 9 November`. |
  | `sources` | The sources that answered, with the time. |
  | `headline` | One sentence on the projects this week, and one on the main risk. |
  | `numbers` | Three tiles: on track, at risk, delivered. |
  | `projects` | One row per project, which opens to its detail. |
  | `milestones` | The milestones this week and next, done or not. |
  | `pinned-update` | The pinned update from the project channel, as written. |
  | `who-is-on-what` | One table row per person: the project and the work this week. |
  | `waiting-on` | Who outside the team the projects wait on, and since when. |
  | `what-changed` | What changed since last week: progress, status, delivered. |
  | `footer` | When the stakeholder version was last written, and for whom. |

- Each project is a row that opens (`details.row`). The summary holds the name (`.t`), the progress (`.tr` and `.bar`, with `warn` when it is at risk), the blocker in one sentence when there is one (`.s`), and the owner, the stage and the target date (`.m`). The detail holds **This week** (issues closed, pull requests merged), **Open** (open issues and the open risk) and **Sources** (the project in the task tool, the spec, the channel).
- Every other row is a title (`.t`), a day or a state (`.tr`), one sentence if needed (`.s`) and its project or person (`.m`).
- The page answers what is happening now. Leave out what comes next and later: the Roadmap holds that. A project shows here once work on it has started, and until a week after it is delivered.
- Each row has an `id`:
  - A project: `p-` and its key in the task tool, or a short slug of its name, for example `p-portals-2`.
  - A milestone, the pinned update and a change: the week and a short slug, for example `w45-go-no-go`.
  - A wait: `waiting-` and a short slug, for example `waiting-legal-data-agreement`. A person: `person-` and their name, for example `person-anna-moen`.
  - Keep the `id` of a row that stays: comments on the shared page attach to it.
- `period` in the comment at the top of the page is the week the page shows, for example `2026-W45`.
- The page is shared as one file. A source links to its web address, never to a file in the workspace. Never add a stylesheet, a script, a font or an image from outside the page.

### The stakeholder version

- `data-internal` marks what stays inside the team: the view pills, **Who is on what**, **Waiting on** and **What changed**.
- The stakeholder version is `project-overview-stakeholders.html`, beside the page. It is a copy of the page with every element marked `data-internal` removed. Its comment at the top says `type: doc`, `title: Projects overview for stakeholders` and the date it was written.

## Steps

1. **Find the week.** It is this week, unless the person names another.
   - `period` is empty: this is the first run. Go to step 3.
   - `period` is this week: this is a refresh. Go to step 3.
   - `period` is an earlier week: go to step 2.
2. **Start the new week.** Note each project's progress and status as the page shows it. **What changed** compares against these. Take out milestones older than this week, and projects delivered more than a week ago.
3. **Read the sources** for this week and next. Say which ones answered and which did not.
4. **Write the slots.** The headline, the three numbers, the projects with their detail, the milestones, the pinned update as written, who is on what, who the team waits on, and what changed since last week. The toolbar gets the day and the sources with the time.
5. **Show what changed** against the page before this run, one line per change, and save after a yes.
6. **Stamp the page.** Set `period`, `last_updated` and `last_updated_by` in the comment at the top. Set `template` to the value in this process's frontmatter.
7. **Refresh the stakeholder version.** If `project-overview-stakeholders.html` exists, show what changes in it and write it again after a yes.
8. **Share after a yes.** When someone asks to share the overview, write `project-overview-stakeholders.html` if it does not exist. Ask who gets it when nobody said, and fill in **Where it goes** above. Show it, and share it after a yes, as a link from Palette or as a mail. Write who got it and the date in the `footer` slot, and say in one line what was sent.
9. **Update the shared page.** If the page is shared from Palette, offer to update the shared copy too.

## Done when

- Every slot shows this week, or says which source was missing.
- `period` names this week.
- The stakeholder version is current, or there is none yet.

## Rules

- Never share the page itself outside the team. Share the stakeholder version.
- Never share, send or update a shared page without a preview and a yes.
- The pinned update goes as written. It is the team's voice.
- Never write a number that no source gave. Leave the tile "–" and say which source was missing.
- Never create or change a file in `projects/`. Each project's detail lives in its row on this page.
