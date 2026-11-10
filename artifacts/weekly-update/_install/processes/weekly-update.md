---
type: process
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
cadence: weekly
template: weekly-update@2611101
---

# Weekly update

Writes the week's update into [`../weekly-update.html`](../weekly-update.html) from the team's tools, and posts it after a yes.

## When to run this

- On Friday, for the week that ends that day.
- When someone asks: "write this week's update", "refresh the weekly update", "post the update".
- When someone presses Refresh on the page.

## Where it goes

- **Channel:** [Not set yet. The first run asks, and writes the answer here.]
- **Readers:** [Who reads it, for example the team and the people above it.]

## Sources

- **Linear or Jira**: the issues that moved this week. Done, in progress, blocked, and who.
- **GitHub**: the pull requests merged this week, with their authors.
- **Slack**: the decisions and the threads worth a line.
- **Google Calendar**: next week. What is booked and who is out.

Every source is optional. Check which ones are connected. For a missing one, say what it would add, for example "connect Linear and the shipped list fills itself". Fill its rows from the other sources, or leave them "Not filled in yet". Never invent a line.

## How the page is built

- Read the page only down to the `end of content` comment. The script and the style after it never change.
- Write only inside elements with `data-slot`. Everything outside a slot is the team's: never change it.
- An element with `data-kept="YYYY-MM-DD"` was changed at someone's request. Never rewrite it. If its source changed since, say so.
- When someone asks to change a line, change it and add `data-kept` with today's date.
- Each row is a title (`.t`), a day or a state (`.tr`), one sentence (`.s`) and its sources (`.m`). Group rows by subject, not by tool.
- The page is shared as one file. A source links to its web address, never to a file in the workspace. Never add a stylesheet, a script, a font or an image from outside the page.
- Each row has an `id`: the week and its source key, for example `w45-hal-1412`. A row without a key uses a short slug of its title. Keep the `id` of a row that stays: comments on the shared page attach to it.
- `period` in the comment at the top of the page is the week the page shows, for example `2026-W45`.

## Steps

1. **Find the week.** It is the week that ends today, unless the person names another.
   - `period` is empty: this is the first run. Ask where the update goes, fill in **Where it goes** above, and go to step 3.
   - `period` is this week: this is a refresh. Go to step 3.
   - `period` is an earlier week: go to step 2.
2. **Start the new week.** Move the earlier week to the top of **Earlier weeks** as one row: "Week 44: " and its headline, with the date of its Friday. Then clear the other slots. Rows with `data-kept` belong to the earlier week: they leave with it, and the new week starts without them.
3. **Read the sources** for the week. Say which ones answered and which did not.
4. **Write the slots.** The headline is one sentence on the week and one on what follows. Then the four numbers, shipped, decided, at risk, next week and out next week. The toolbar gets the week and the sources with the time.
5. **Show what changed** against the page before this run, one line per change, and save after a yes.
6. **Stamp the page.** Set `period`, `last_updated` and `last_updated_by` in the comment at the top. Set `template` to the value in this process's frontmatter.
7. **Post after a yes.** Show the post as it will read in the channel: Slack gets the headline and the rows as bullets with their links, a mail gets headings. Write "Posted to" with the channel and the time in the `footer` slot.
8. **Update the shared page.** If the page is shared from Palette, offer to update the shared copy too.

## Done when

- Every slot shows this week, or says which source was missing.
- `period` names this week.
- The update is posted, or the person said not to post it.

## Rules

- Never post or update a shared page without a preview and a yes.
- A line without its source is never posted as a fact.
- A line changed at someone's request is posted as changed. It is never written again at posting time.
