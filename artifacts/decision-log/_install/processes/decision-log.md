---
type: process
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
cadence: weekly
template: decision-log@2611101
---

# Decision log

Writes the team's decisions into [`../decision-log.html`](../decision-log.html) from the workspace's logs, Slack and the meeting notes, and adds a new decision to the docs tool's decisions page after a yes.

## When to run this

- On Friday, for the decisions of the week.
- When someone asks: "build our decision log", "refresh the decision log", "update the decision log".
- When someone wants one decision added: "log this decision", "add this to the decision log", or a pasted thread with "decided". Go to **Add one decision**.
- When someone presses Refresh on the page.

## Where it goes

- **Decisions page:** [The decisions page in the docs tool, if the team keeps one. The first run asks, and writes the answer here. "None" if there is none.]
- **Channels:** [The Slack channels the team decides in, for example #product and #marketing.]

## Sources

- **The workspace's `log.md` files**: the decisions each scope records, in `company/`, the projects and the spaces. Read them only. Never create or change a `log.md`.
- **Slack**: the threads in the channels above where something was decided. The thread, who said it, the replies.
- **Meeting notes**: the decisions marked in the notes in the workspace, for example in `meetings/`.
- **Notion or Google Docs**: the decisions page, when the team keeps one.
- **Linear or Jira**: the issues and projects a decision touched, for the link.

Every source is optional. Check which ones are connected or present. For a missing one, say what it would add, for example "connect Slack and the threads where something was decided fill the log". Without Slack, the log comes from the logs, the meeting notes and the decisions page. A decision can always be typed in. Never invent an entry.

## How the page is built

- Read the page only down to the `end of content` comment. The script and the style after it never change.
- Write only inside elements with `data-slot`. Everything outside a slot is the team's: never change it.
- The slots:
  - `quarter` and `sources` in the toolbar: the quarter, and the sources with the time.
  - `headline`: one sentence on the quarter's decisions, one on what comes up for review.
  - `numbers`: decisions this quarter, this week, up for review, reversed this quarter.
  - `filters`: the **All** pill, then one pill per area that has entries. The spacer and the search field at the end stay as they are.
  - `this-week`: the decisions taken in the last seven days.
  - `up-for-review`: the decisions whose review date is in the next four weeks, or has passed without a review.
  - `reversed`: the decisions reversed this quarter.
  - `earlier`: every other decision, newest first. It holds earlier quarters too.
- Each decision is one row that opens (`<details class="row">`). The summary holds what was decided (`.t`), the date it was decided or its state (`.tr`), why in one sentence (`.s`), and who, where and the review date (`.m`). The detail holds **Options on the table** and **What followed**, then one block for each state change.
- The page is a log. A run adds entries and never rewrites the title, why, who, where, options or what followed of an earlier entry. Only an entry's state changes:
  - **Up for review:** the row moves to `up-for-review` with "Review on" and the date in `.m`, and `.tr` says "Holds".
  - **Reviewed:** add a block "Reviewed on" with the date and the outcome. If it holds, the row moves back to `earlier`.
  - **Reversed:** add a block "Reversed on" with the date, the reason and the decision that replaces it. Add "Reversed on" and the date to `.m`. The row moves to `reversed`. The new decision is a new row.
- A row moves between slots and keeps its `id`. A decision is on the page once.
- Each row has an `id`: the quarter it was decided in and a short slug of its title, for example `2026-q4-client-approvals-q1`. The `id` never changes: comments on the shared page attach to it.
- Each row has `data-tags` with the area it belongs to: the space or project whose log holds it, or the team that decided it, for example `Product,Launch`. Use the exact values of the pills. Each tag on a row has a pill, and each pill has a row.
- An element with `data-kept="YYYY-MM-DD"` was changed at someone's request. Never rewrite it. If its source changed since, say so.
- When someone asks to correct an entry, correct it and add `data-kept` with today's date.
- The page is shared as one file. A source links to its web address, never to a file in the workspace. Never add a stylesheet, a script, a font or an image from outside the page.
- `period` in the comment at the top of the page is the quarter the numbers count, for example `2026-Q4`.

## Steps

1. **Find the quarter.** It is the quarter of today, unless the person names another.
   - `period` is empty: this is the first run. Ask which channels the team decides in and whether there is a decisions page. Fill in **Where it goes** above. Read the whole quarter so far, and go to step 3.
   - `period` is this quarter: this is a refresh. Go to step 3.
   - `period` is an earlier quarter: go to step 2.
2. **Start the new quarter.** Move the rows in `this-week` and `reversed` to the top of `earlier`, with their state blocks. Rows in `up-for-review` stay until their review. In `earlier`, a row from an earlier year shows the year in its date, for example "21 Oct 2025".
3. **Read the sources** since the last run, or the whole quarter on the first run. Do not widen the period without asking. Say which sources answered and which did not.
4. **Find the decisions.** Take only what was decided, not what was discussed. A decision without a who is a discussion and does not go in. A decision already on the page is not added twice.
5. **Add the new entries.** Each one is a row in `this-week`, or in `earlier` when it is older than seven days. Fill what, why, who, where, the options, what followed and the review date when one was named. Mark a part no source gave as "Not known yet".
6. **Update the states.** Move rows into and out of `up-for-review` by their review date. Add the reviews and the reversals the sources show, as **How the page is built** says. Move rows older than seven days from `this-week` to `earlier`.
7. **Write the other slots.** The headline, the numbers, the filters, the quarter and the sources with the time.
8. **Show what changed** against the page before this run, one line per change, and save after a yes.
9. **Stamp the page.** Set `period`, `last_updated` and `last_updated_by` in the comment at the top. Set `template` to the value in this process's frontmatter.
10. **Update the shared page.** If the page is shared from Palette, offer to update the shared copy too.

### Add one decision

11. **Read what the person gives**: a thread link, a meeting note or a sentence. Find what was decided, by whom, and the reason given. Without a who, say that it is a discussion, and stop.
12. **Draft the entry** on the row's shape: what, why, who, where, the options, what followed, a review date if one was named, and its area. Show it as it will read on the page. The person corrects the wording.
13. **Add it after a yes.** Put the row in `this-week`, or in `earlier` when it is older than seven days. Update the headline and the numbers, add a pill if its area is new, and stamp the page as in step 9.
14. **Add it to the decisions page after a yes.** If **Where it goes** names a decisions page, show the entry as it will read there. Add it after a yes.
15. **Say the decision back** in one line. Then offer step 10.

## Done when

- Every decision of the quarter that the sources show is on the page, with its who.
- The states match the sources: reviews and reversals carry their date and reason.
- `period` names this quarter.
- A new decision is on the page, and on the decisions page when there is one, or the person said not to add it there.

## Rules

- Never write to the docs tool or update a shared page without a preview and a yes.
- Never rewrite an earlier entry. A state change is added with its date and reason.
- Never delete a reversed decision. It stays, marked reversed, with the date and the reason.
- Never reword the decision itself. The why can be tightened.
- A decision has a who. Without a name, it is a discussion and does not go in.
- An entry without its source is never added as a fact.
