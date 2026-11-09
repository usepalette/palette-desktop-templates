---
type: process
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
template: sprint-review@2611094
---

# Sprint review

Writes the review of each cycle into [`../sprint-review.html`](../sprint-review.html) from the team's tools, carries the open issues into the next cycle and posts the review, each after a yes.

## When to run this

- At the end of each cycle, for the cycle that ends that day. Cycles vary in length, so there is no fixed day.
- When someone asks: "write the sprint review", "refresh the sprint review", "post the review", "close the cycle", "carry over the open items".
- When someone presses Refresh on the page.

## Where it goes

- **Channel:** [Not set yet. The first run asks, and writes the answer here.]
- **Task tool and team:** [The tool and the team whose cycles the review reads, for example Linear, team HAL.]

## Sources

- **Linear or Jira**: the cycle. The planned issues, done, carried, added, the assignees and the estimates. The five cycles before it, for the chart on the first run.
- **GitHub**: the pull requests merged in the cycle, with their authors. They give the things worth showing.
- **Slack**: the team channel, for the highlights people mentioned.

Every source is optional. Check which ones are connected. For a missing one, say what it would add, for example "connect Linear and the numbers fill themselves". Without the task tool, the numbers, the chart, carried over, added and per person stay "Not filled in yet". Without GitHub, the review counts issues only, and the things worth showing come from Slack or from the person. Never invent a line.

## How the page is built

- Read the page only down to the `end of content` comment. The script and the style after it never change.
- Write only inside elements with `data-slot`. Everything outside a slot is the team's: never change it. The one exception is the target note on the first run, below.
- An element with `data-kept="YYYY-MM-DD"` was changed at someone's request. Never rewrite it. If its source changed since, say so.
- When someone asks to change a line, change it and add `data-kept` with today's date.
- The slots:

| Slot | What it holds |
|---|---|
| `cycle` | The toolbar button: the cycle, for example "Cycle 23". |
| `sources` | The sources that answered, and the day and time. |
| `headline` | An `h1` with the cycle and the share done, and one `p`: what went out, and what carried into the next cycle. |
| `numbers` | Four tiles: done, carried over, added, and the share done against the target. The last tile is `key`. |
| `planned-done` | The chart: six columns, the oldest on the left. Each has a grey `plan` bar and a done bar. |
| `planned-done-axis` | One label per column: "14 of 18" and the cycle. |
| `carried-over` | The issues that move to the next cycle, each with its reason. |
| `added` | The issues added after the cycle started. Group them by subject, for example "Three bugs from the beta". |
| `worth-showing` | Three things the team can show, from the merged pull requests. |
| `earlier-cycles` | One row per earlier cycle, the newest on top. |
| `per-person` | The table body in the Per person view: one `tr` per person with planned, done and carried. |
| `footer` | Where the carried issues went, and where and when the review was posted. |

- Each row is a title (`.t`), one sentence (`.s`) and its sources (`.m`): the issue key or the pull request, and the person. In carried over, the sentence is the reason.
- The chart: a column has `data-tip="Cycle 23: 18 planned, 14 done, 78%"` and `tabindex="0"`. `--v` is the count divided by the top of the scale. The top is the largest planned count of the six, rounded up to the next multiple of 5. When the top changes, set `--v` again on all six columns, not only the newest. Only the newest column and its label have the class `now`.
- The note under the chart is the team's. It holds the target, for example "The target is 85% done." The `key` tile reads the target from it. It is the one place outside a slot that the process writes: the first run writes the target there once, after asking. After that, only a person changes it.
- Each row has an `id`: the cycle and its source key, for example `c23-hal-1430` or `c23-pr-1440`. A row without a key uses a short slug of its title, for example `c23-beta-bugs`. A person's `tr` uses the cycle and the name, for example `c23-sara-lind`. An earlier cycle uses only the cycle, for example `c22`. Keep the `id` of a row that stays: comments on the shared page attach to it.
- The page is shared as one file. A source links to its web address, never to a file in the workspace. Never add a stylesheet, a script, a font or an image from outside the page.
- `period` in the comment at the top of the page is the cycle the page shows, for example `cycle-23`.

## Steps

1. **Find the cycle.** It is the cycle that ends today, or the last one that ended, unless the person names another.
   - `period` is empty: this is the first run. Ask where the review goes and what the target is. Fill in **Where it goes** above, write the target in the note under the chart, and go to step 3.
   - `period` is this cycle: this is a refresh. Go to step 3.
   - `period` is an earlier cycle: go to step 2.
2. **Start the new cycle.** Move the earlier cycle to the top of **Earlier cycles** as one row: "Cycle 22: " and its headline, with the date it ended. Shift the chart one column to the left: drop the oldest column and its label, and take `now` off the last one. Then clear the other slots. Rows with `data-kept` belong to the earlier cycle: they leave with it, and the new cycle starts without them.
3. **Read the sources** for the cycle. Say which ones answered and which did not. Do not widen the cycle without asking.
4. **Write the slots.** The headline is one sentence on the cycle and one on what carried. Then the four numbers, the newest column of the chart (and `--v` on every column if the top of the scale changed), carried over, added, worth showing and per person. On the first run, fill the five earlier columns from the task tool; a cycle it does not have shows "–". If no source names three things worth showing, ask for them in one question. The toolbar gets the cycle and the sources with the time.
5. **Show what changed** against the page before this run, one line per change, with the old and the new value. Save after a yes.
6. **Stamp the page.** Set `period`, `last_updated` and `last_updated_by` in the comment at the top. Set `template` to the value in this process's frontmatter.
7. **Carry the open issues after a yes.** Check that every carried issue is in the next cycle, and that its reason is on the issue. Show the list of what is missing: the issues to move, and the reason to add to each as a comment. Move them and add the reasons after a yes. Write "The carried items are in cycle 24." in the `footer` slot.
8. **Post after a yes.** Show the post as it will read in the channel: the headline, the four numbers, the things worth showing and the carried list, with their links. Write "Posted to" with the channel and the time in the `footer` slot.
9. **Update the shared page.** If the page is shared from Palette, offer to update the shared copy too.

## Done when

- Every slot shows this cycle, or says which source was missing.
- `period` names this cycle.
- Every carried issue is in the next cycle with its reason, or the person said to leave it.
- The review is posted, or the person said not to post it.

## Rules

- Never move an issue, comment on an issue, post or update a shared page without a preview and a yes.
- A carry-over reason is a fact from the issue: its history, a comment or a blocking link. Never guess. If the issue does not say, ask.
- A number that no source gave stays "–". It is never invented.
- A source that does not answer on a refresh leaves its rows as they are. Say so in the `sources` line.
- Write every line for the team. Never copy a line from another page, such as the weekly update or the release notes.
- A line changed at someone's request is posted as changed. It is never written again at posting time.
