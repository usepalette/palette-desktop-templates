---
type: process
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
cadence: monthly
template: roadmap@2611092
---

# Roadmap

Writes what comes when into [`../roadmap.html`](../roadmap.html): now, next and later, with a reason per project. After a yes, it writes the customer version beside the page and drafts the answer to a customer who asks when.

## When to run this

- On the first working day of the month.
- When someone asks: "make me a roadmap", "refresh the roadmap", "update the roadmap", "share the roadmap", "send the roadmap to a customer", "what do I tell a customer about this project".
- When someone presses Refresh on the page.

## Where it goes

- **Customer version:** `roadmap-customers.html`, beside the page. The first share makes it.
- **Readers:** [Who gets the customer version, for example customers who ask when. The first share asks, and writes the answer here.]

## Sources

- **Linear or Jira**: the projects. Status, progress, target dates, owners.
- **Notion or Google Docs**: the specs, for the reason behind each project and whether it has a spec yet.
- **The `projects/` folder** at the root of the workspace: the projects the team keeps there, with their goals and dates. Read it only. Never create or change a file in it.
- **HubSpot**: the customers who asked for each project, from the CRM notes.
- **Slack**: the product channel, for decisions that move a project or change its quarter.

Every source is optional. Check which ones are connected. For a missing one, say what it would add, for example "connect Linear and the projects fill themselves". Without HubSpot, the list of who asked comes from the team's feedback folder, if there is one. Without specs, ask the person for the reason, or leave it "Not filled in yet". Never invent a line.

## How the page is built

- Read the page only down to the `end of content` comment. The script and the style after it never change.
- Write only inside elements with `data-slot`. Everything outside a slot is the team's: never change it.
- An element with `data-kept="YYYY-MM-DD"` was changed at someone's request. Never rewrite it. If its source changed since, say so.
- When someone asks to change a line, change it and add `data-kept` with today's date.
- When someone asks to move a project to another column, move its row. Then offer to change its target in Linear or Jira: show the change, and make it after a yes.
- The slots:

  | Slot | What it holds |
  |---|---|
  | `quarter` | The quarter that **Now** covers, for example `Q4 2026`. |
  | `sources` | The sources that answered, with the day and the time. |
  | `headline` | One sentence on what comes when, and one on the quarters after. |
  | `numbers` | Four tiles: in build, next quarter, later, slipped. |
  | `now` | The projects in build this quarter. |
  | `next` | The projects with a spec or a quarter, after this one. |
  | `later` | The projects with no date yet. |
  | `footer` | When the customer version was last written. |

- Each project is a row that opens (`details.row`). The summary holds the name (`.t`), one sentence on what it is (`.s`), a line of facts (`.m`) and, in **Now**, the progress (`.tr` and `.bar`, with `warn` when it slipped). The detail holds **Why**, **Asked for by** and, when a customer asked, **Asked when**.
- The facts line: in **Now**, the owner, the target date and the confidence. In **Next**, the owner, the quarter and how many customers asked. In **Later**, "No date yet" and how many asked.
- The page answers what comes when. Leave out the status of the week, who works on what and the work of the week. The Projects overview holds those.
- Each project row has an `id`: `p-` and its key in the task tool, for example `p-hal-portals`. A project without a key uses a short slug of its name, for example `p-portals-2`. Keep the `id` when a project moves between columns: comments on the shared page attach to it.
- `period` in the comment at the top of the page is the quarter that **Now** covers, for example `2026-Q4`.
- The page is shared as one file. A source links to its web address, never to a file in the workspace. Never add a stylesheet, a script, a font or an image from outside the page.

### The customer version

- `data-internal` marks what stays inside the team: the owners, the confidence, the progress, the dates inside a quarter, the slipped count, who asked and when, and the sources line.
- The customer version is `roadmap-customers.html`, beside the page. It is a copy of the page with every element marked `data-internal` removed. Set `--n` on the tiles to the number of tiles left. Its comment at the top says `type: doc`, `title: Roadmap for customers` and the date it was written.
- Mark every new owner, confidence, progress bar, date inside a quarter and customer name with `data-internal` when you write it. A headline names a quarter, never a day; put a date in a sentence marked `data-internal`.

## Steps

1. **Find the quarter.** It is the quarter that today falls in.
   - `period` is empty: this is the first run. Go to step 3.
   - `period` is this quarter: this is a refresh. Go to step 3.
   - `period` is an earlier quarter: go to step 2.
2. **Start the new quarter.** Take the projects that are done out of **Now**. Move the projects planned for this quarter from **Next** to **Now**. Keep each row's `id`.
3. **Read the sources** for this quarter and the two after. Say which ones answered and which did not.
4. **Place each project.** **Now** is in build this quarter. **Next** has a spec or a quarter after this one. **Later** has neither. Write the reason from the spec, and who asked from HubSpot. Keep the **Asked when** lines that a project already has.
5. **Write the slots.** The headline, the four numbers and the three columns. The toolbar gets the quarter and the sources with the time.
6. **Show what changed** against the page before this run, one line per change: a project that moved column, a quarter that changed, a project that slipped. Save after a yes.
7. **Stamp the page.** Set `period`, `last_updated` and `last_updated_by` in the comment at the top. Set `template` to the value in this process's frontmatter.
8. **Refresh the customer version.** If `roadmap-customers.html` exists, show what changes in it and write it again after a yes. Write the date in the `footer` slot.
9. **Share after a yes.** When someone asks to share the roadmap:
   - For the whole roadmap: write `roadmap-customers.html` if it does not exist, and fill in **Where it goes** above. Show it, and share it after a yes, as a link from Palette or as the three columns in a short mail.
   - For a customer who asks about one project: find the project's column and quarter in the customer version. Draft the answer in two lines and show it. The person sends it, or it is sent after a yes.
   - Then add the customer, the date and what they were told to the project's **Asked when** line, marked `data-internal`. Write "Customer version written" with the date in the `footer` slot.
10. **Update the shared page.** If the page is shared from Palette, offer to update the shared copy too.

## Done when

- Every project the sources know is in **Now**, **Next** or **Later**, with a reason, or the row says which source was missing.
- `period` names this quarter.
- The customer version is current, or there is none yet.

## Rules

- Never share an owner, a confidence or a date inside a quarter with a customer. Give the quarter.
- A **Later** project has no date. Tell a customer "not planned yet", never a year.
- Never share the page itself outside the team. Share the customer version.
- Never share, send or update a shared page without a preview and a yes.
- Never write a number that no source gave. Leave the tile "–" and say which source was missing.
- Never change a project in Linear or Jira without a preview and a yes.
- Never create or change a file in `projects/`.
