---
type: process
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
cadence: weekly
template: team-capacity@2611092
---

# Team capacity

Writes the coming week's capacity into [`../team-capacity.html`](../team-capacity.html) from the task tool and the calendar, and makes the moves the person accepts in the task tool after a yes.

## When to run this

- On Friday, for the week that starts on Monday.
- When someone asks: "show the team's capacity", "who has room next week", "refresh the team capacity", "rebalance the week", "move some of Tobias's work".
- When someone presses Refresh on the page.

## The team

- **People:** [Not set yet. The first run asks who is on the team, and writes the names here.]
- **Task tool:** [The Linear or Jira team, project or cycle the work comes from.]
- **A day of work:** [What an estimate is in days, for example 1 point is half a day. A working day is 8 hours unless the team says otherwise.]

## Sources

- **Linear or Jira**: the issues in the week's cycle, with their assignees and estimates. The moves are made here.
- **Google Calendar**: time off, and the hours in meetings per person.

Every source is optional. Check which ones are connected. For a missing one, say what it would add, for example "connect Google Calendar and time off and meetings fill themselves". Without estimates, count issues instead of days, and say so in the headline. Without the calendar, everyone is in all week, and the sources line says so. Never invent a number.

## How the page is built

- Read the page only down to the `end of content` comment. The script and the style after it never change.
- Write only inside elements with `data-slot`. Everything outside a slot is the team's: never change it.
- An element with `data-kept="YYYY-MM-DD"` was changed at someone's request. Never rewrite it. If its source changed since, say so.
- When someone asks to change a line, change it and add `data-kept` with today's date.
- The slots:
  - `week` and `sources`: the toolbar. The week with its dates, and the sources with the time of the run.
  - `headline`: who is over, in one sentence, then one sentence on the totals and the issues nobody has.
  - `numbers`: four tiles. Days available, days planned, over (the key tile) and with room.
  - `by-day`: one `.lrow` per person. The name and the role with the hours in meetings (`.who`), then one `.cell` per working day. A cell's `--w` is the share of the day planned. Add `over` when the work is more than the day, and `out` with the text "Out" when the person is off. `data-tip` says the day and the number, for example "Mon: 1.4 days of work, 0.4 over". The `.tr` is the week's balance: "3 days over", "Full" or "2 days free", with `over` when over.
  - `moves`: one row per suggested move. The title (`.t`) "Give “issue” from A to B", the move (`.tr`) "A → B", and the issue key and the days (`.m`). After a move is made, add "Moved" and the day to `.m`.
  - `unassigned`: one row per issue that nobody has. The title, then the issue key, the days and who it fits (`.m`).
  - `footer`: the template line, and the moves made with the time.
- The page is shared as one file. An issue links to its web address, never to a file in the workspace. Never add a stylesheet, a script, a font or an image from outside the page.
- Each row has an `id`: the week and its key, for example `w46-hal-1447` for an issue and `w46-tobias-falk` for a person. Keep the `id` of a row that stays: comments on the shared page attach to it.
- `period` in the comment at the top of the page is the week the page shows, for example `2026-W46`.

## Steps

1. **Find the week.** It is the coming week, Monday to Friday. On a Monday, it is the week that starts that day. The person can name another week.
   - `period` is empty: this is the first run. Ask who is on the team, where the work comes from and what an estimate is in days. Fill in **The team** above, and go to step 3.
   - `period` is this week: this is a refresh. Go to step 3.
   - `period` is an earlier week: go to step 2.
2. **Start the new week.** Clear every slot. The page shows one week, so the earlier week is not kept. Rows with `data-kept` go with their week.
3. **Read the sources** for the week. Say which ones answered and which did not.
4. **Work out the week.** For each person, the days available are the working days minus time off and meeting hours. The days planned are the estimates of the issues assigned to them. Spread each person's work over the days they are in.
5. **Write the slots.** The headline, the four numbers, one row per person by day, the suggested moves and the issues nobody has. Propose moves smallest issues first, only to people with the days and the skill for it. The toolbar gets the week and the sources with the time.
6. **Show what changed** against the page before this run, one line per change, and save after a yes.
7. **Stamp the page.** Set `period`, `last_updated` and `last_updated_by` in the comment at the top. Set `template` to the value in this process's frontmatter.
8. **Make the moves after a yes.** List the people over and the people with room, with the days. Show each move as it will be made in the task tool: the issue, from whom, to whom, and why. Make only the moves the person accepts.
9. **Write the moves onto the page.** Add "Moved" and the day to each move made, and write the moves made with the time in the `footer` slot. Then do steps 3 to 6 again, so the numbers show the week after the moves. Say in one line who is still over, if anyone.
10. **Update the shared page.** If the page is shared from Palette, offer to update the shared copy too.

## Done when

- Every slot shows the coming week, or says which source was missing.
- `period` names the coming week.
- Each suggested move is made or turned down, or the person said not to make moves.

## Rules

- Never move an issue or update a shared page without a preview and a yes.
- Never move an issue to someone who is out on the days it needs.
- Say when the numbers rest on missing estimates.
- A number that no source gave stays "–". It is never invented.
