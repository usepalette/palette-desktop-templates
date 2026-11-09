---
type: process
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
cadence: weekly
template: marketing-scoreboard@2611093
---

# Marketing scoreboard

Writes the month's marketing numbers against the year goal into [`../marketing-scoreboard.html`](../marketing-scoreboard.html), and posts a three-line note on what moved after a yes.

## When to run this

- On Monday, for the month the page shows.
- When someone asks: "refresh the scoreboard", "Monday numbers", "what moved this week", "update the marketing scoreboard".
- When someone presses Refresh on the page.

## Where it goes

- **Channel:** [Not set yet. The first run asks, and writes the answer here.]
- **Readers:** [Who reads it, for example the marketing team and the founders.]

## Sources

- **HubSpot**: qualified leads, paying teams, trial to paid, and the signups that came from LinkedIn, referrals and the newsletter.
- **PostHog**: signups, website visits, and where the signups came from.
- **Notion or Google Docs**: the goals page, for the year goal.

Every source is optional. Check which ones are connected: a source counts only when its connector is connected, not because this list names it. For a missing one, say what it would add, for example "connect HubSpot and qualified leads fill themselves". A number no source gives is typed by the person when asked. Never invent a number.

## How the page is built

- Read the page only down to the `end of content` comment. The script and the style after it never change.
- Write only inside elements with `data-slot`. Everything outside a slot is the team's: never change it.
- The goals are the team's and sit outside the slots: the line after the share (`#year-goal`) and the note under each chart (`#goal-signups`, `#goal-leads`, `#goal-visits`, `#goal-paying-teams`). The empty page has them as `[year goal]` and `[monthly goal]`. Fill them only when the person gives the goals, on the first run or at a new year. Later runs read them. If the goals page says something else, say so and ask.
- A number no source gives is typed by the person when asked. Write it into its slot with `data-kept` and today's date, and show it as typed: "Typed in" on a tile, "typed in by" and the name in a month's detail.
- An element with `data-kept="YYYY-MM-DD"` was typed or changed at someone's request. Never rewrite it. If its source changed since, say so.
- When someone asks to change a line, change it and add `data-kept` with today's date.
- The slots:

| Slot | What it holds |
|---|---|
| `month` | The month the page shows, in the toolbar. |
| `sources` | The sources that answered and the time. A source that did not answer is named here with the part it left stale. |
| `headline` | One sentence on the pace, then one with the numbers: how far, how much is left, where the year ends at this pace. |
| `year-share` | The share of the year's signup goal reached so far. |
| `year-track` | The track: `--w` is the share, `--pace` is where the year should be. Its `data-tip` says both in words. |
| `year-pace` | Signed up so far, and where the year should be after this month. |
| `numbers` | The four tiles: signups, qualified leads, website visits, paying teams. Each has the change on last month and its source. |
| `signups-by-month`, `leads-by-month`, `visits-by-month`, `paying-teams-by-month` | One column per month for each measure, with the goal as the dashed line (`.goal`, `--g`). The page's month is `now`, the months after it are `come`. Each column's `data-tip` says the month and the number. |
| `months-axis` | The twelve months. The page's month is `now`. |
| `signup-sources` | Where the month's signups came from, one row per channel, with its source and a bar for its share. |
| `notes` | Notes on the month that people gave, one row each with its author. |
| `months` | Each month of the year so far, newest first: a row that opens to the four numbers with their sources, and the month's notes. |
| `footer` | The template line, then "Posted to" with the channel and the time. |

- Each row is a title (`.t`), a number or a state (`.tr`), its sources (`.m`) and, for a share, a bar (`.bar`). A month's row opens to one `.k` and `.x` pair per number.
- Each row has an `id`: the month and a short slug, for example `m2026-10-linkedin`. A month's row is the month alone, for example `m2026-10`. Keep the `id` of a row that stays: comments on the shared page attach to it.
- The chart's pills switch the measure: each pill's `data-show` matches the `data-view` of a chart and its note. Only the first chart and note are shown when the page opens; the others have the class `off`.
- `period` in the comment at the top of the page is the month the page shows, for example `2026-10`.
- The page is shared as one file. A source links to its web address, never to a file in the workspace. Never add a stylesheet, a script, a font or an image from outside the page.

## Steps

1. **Find the month.** It is the month in progress. On the first Monday of a month, it is still the month that just ended, so that run writes its final numbers.
   - `period` is empty: this is the first run. Ask where the note goes, and fill in **Where it goes** above. Take the year goals from the goals page, or ask for them, and fill in the goals on the page. Go to step 3.
   - `period` is this month: this is a refresh. Go to step 3.
   - `period` is an earlier month: go to step 2.
2. **Start the new month.** Finish the earlier month's row in `months` with its final numbers, and move its notes into the row's detail. A closed month never changes after this. Then clear `numbers`, `signup-sources` and `notes`. Rows and tiles with `data-kept` belong to the earlier month: they leave with it, and the new month starts without them. If the new month starts a new year, ask for the year's goals first, fill them in, and clear the charts.
3. **Read the sources** for the month. Say which ones answered and which did not. Do not widen the period without asking.
4. **Ask for the typed numbers** in one message: every number no source gave, with last week's value next to it. Write each answer with `data-kept` and today's date. A number nobody gives stays as it was, marked with the date of its last run, or "–".
5. **Write the slots.** Where the year should be is the goal times the share of the year gone by the end of the page's month. Where it ends at this pace is the year so far, over the months gone, times twelve. Write the month's row in `months` with every number and its source. The toolbar gets the month and the sources with the time.
6. **Show what changed** against the page before this run, one line per change, with the old and the new value. Save after a yes.
7. **Stamp the page.** Set `period`, `last_updated` and `last_updated_by` in the comment at the top. Set `template` to the value in this process's frontmatter.
8. **Post after a yes.** Write three lines: the number that moved most, the pace against the goal, and the one thing to watch. Show the post as it will read in the channel. Write "Posted to" with the channel and the time in the `footer` slot. Say what went where in one line.
9. **Update the shared page.** If the page is shared from Palette, offer to update the shared copy too.

## Done when

- Every slot shows the month, or says which source was missing.
- Every typed number has its date and its mark.
- `period` names the month.
- The note is posted, or the person said not to post it.

## Rules

- Never post or update a shared page without a preview and a yes.
- Never post a typed number without its mark.
- The pace uses the goal on the page, never a guess.
- A number without its source is never posted as a fact.
- A refresh changes the content, not the layout. Change the layout only when the person asks.
