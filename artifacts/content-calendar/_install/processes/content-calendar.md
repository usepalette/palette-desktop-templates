---
type: process
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
cadence: weekly
template: content-calendar@2611092
---

# Content calendar

Writes the month's content into [`../content-calendar.html`](../content-calendar.html) from the team's tools, posts the week's plan and reminds the owners of overdue pieces after a yes.

## When to run this

- On Monday, for the week that starts that day.
- When someone asks: "build the content calendar", "refresh the content calendar", "what goes out this week", "post the content plan", "chase the overdue pieces".
- When someone presses Refresh on the page.

## Where it goes

- **Channel:** [Not set yet. The first run asks where the week's plan goes, and writes the answer here.]
- **Reminders:** [How an owner of an overdue piece hears about it, for example a direct message in Slack.]
- **Content database:** [The Notion or Google Docs database the pieces come from.]

## Sources

- **Notion or Google Docs**: the content database. The pieces, with their channel, owner, state, date, brief and the web address of the draft.
- **Google Calendar**: the launch and event dates the content is planned around.
- **Linear or Jira**: the marketing issues, for the pieces tracked there.
- **Slack**: the marketing channel, where the plan goes, and the owners to remind.

Every source is optional. Check which ones are connected. For a missing one, say what it would add, for example "connect Notion and the pieces fill themselves". Without the content database, the person tells you the pieces: write them as rows with `data-kept`, so a refresh keeps them. Without the calendar, ask for the launch dates. Never invent a piece or a number.

## How the page is built

- Read the page only down to the `end of content` comment. The script and the style after it never change.
- Write only inside elements with `data-slot`. Everything outside a slot is the team's: never change it.
- An element with `data-kept="YYYY-MM-DD"` was changed at someone's request. Never rewrite it. If its source changed since, say so.
- When someone asks to change a line, change it and add `data-kept` with today's date.
- The page has two views, Week and Month. A section with `data-view="Week"` shows in the Week view, and one with `data-view="Month"` in the Month view. A section without `data-view` shows in both. Keep the pills that switch them.
- The slots:
  - `month` and `sources`: the toolbar. The month, and the sources with the time of the run.
  - `headline`: one sentence on the month, then one on the numbers and what comes next, such as a launch.
  - `numbers`: four tiles. Pieces planned, published, for the launch (the key tile) and overdue.
  - `week-title` and `days`: the week, Monday to Sunday. One `.day` per day, with the date (`b`) and the weekday. Add `weekend` on Saturday and Sunday. Each piece on the day is a `.piece` with its title (`.pt`) and "channel, owner, state" (`.pm`). Add `launch` for launch content and launch dates, and `late` for an overdue piece. A day with nothing has "Nothing planned" in `.empty`.
  - `overdue`: every piece past its date and not published, from any month. The title, the date it was due (`.tr`), and the channel and owner (`.m`). After a reminder, add "Reminded" and the date to `.m`.
  - `month-title` and `weeks`: one row per week that has most of its days in the month. The week and its dates, the number of pieces (`.tr`), one sentence on what goes out (`.s`), and how many are for the launch (`.m`).
  - `briefs`: one row that opens per piece in the month, by date. The summary holds the title, the day and the date (`.tr`), and the channel, owner, state, "Launch" and the issue key (`.m`). The detail holds the brief and the draft. If the draft lives in a docs tool, link to it with its `https://` address. Otherwise write "No draft yet."
  - `footer`: the template line, and where and when the plan was posted.
- The page is shared as one file. A piece links to its web address, never to a file in the workspace. Never add a stylesheet, a script, a font or an image from outside the page.
- Each row has an `id`: the month and the source key, for example `nov-mkt-208`. A piece without a key uses a short slug of its title, for example `nov-three-ways-agencies-share-work`. An overdue row starts with `late-`, a week row is the week (`w46`), and a day is the month and the date (`nov-09`). Keep the `id` of a row that stays: comments on the shared page attach to it.
- `period` in the comment at the top of the page is the month the page shows, for example `2026-11`.

## Steps

1. **Find the month and the week.** The week is Monday to Sunday and holds today. The month is the month of that Monday. The person can name another week or month.
   - `period` is empty: this is the first run. Ask where the plan goes, how owners are reminded and which database holds the pieces. Fill in **Where it goes** above, and go to step 3.
   - `period` is this month: this is a refresh. Go to step 3.
   - `period` is an earlier month: go to step 2.
2. **Start the new month.** Clear every slot. The page shows one month, so the earlier month is not kept. Keep a row with `data-kept` only if its piece is still overdue or falls in the new month.
3. **Read the sources** for the month. Say which ones answered and which did not.
4. **Write the slots.** The headline, the four numbers, the week by day, the overdue pieces, the month week by week and a brief for every piece. The toolbar gets the month and the sources with the time.
5. **Show what changed** against the page before this run, one line per change, and save after a yes.
6. **Stamp the page.** Set `period`, `last_updated` and `last_updated_by` in the comment at the top. Set `template` to the value in this process's frontmatter.
7. **Post the week's plan after a yes.** If the page is older than a day, do steps 3 to 6 first. Show the post as it will read in the channel: one line per piece with the day, the title, the channel, the owner and the state. Write "Posted to" with the channel and the time in the `footer` slot.
8. **Remind the owners after a yes.** List the overdue pieces by owner. Show each message before it goes: one message per owner, with their pieces and the dates they were due. Add "Reminded" and the date to each overdue row.
9. **Update the shared page.** If the page is shared from Palette, offer to update the shared copy too.

## Done when

- Every slot shows this month and this week, or says which source was missing.
- `period` names this month.
- The plan is posted and the owners are reminded, or the person said not to.

## Rules

- Never post, send a reminder or update a shared page without a preview and a yes.
- Never post a piece's brief. The plan has the days, the titles, the channels, the owners and the states only.
- Send one reminder per owner, never one per piece.
- A launch can also have its own page, made with the Launch plan template. Never read or copy from a launch page. The content calendar reads only its own sources.
