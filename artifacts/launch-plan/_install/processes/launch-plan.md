---
type: process
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
cadence: weekly
template: launch-plan@2611092
---

# Launch plan

Writes one page per launch into [`../launches/`](../launches/README.md) from the team's tools, and posts the launch status to the launch channel after a yes.

## When to run this

- Once a week for each launch that has not shipped.
- When someone asks for a new launch: "make me a launch plan", "start a launch plan for Portals 2.0 on 26 November".
- When someone asks for a refresh: "refresh the launch plan", "update the launch plan".
- When someone asks for the status: "post the launch status", "where is the launch", "launch update". Go to **Post the status**.
- When someone presses Refresh on a launch page.

## Where it goes

- **Launch channel:** each launch's channel is in its row in [`../launches/README.md`](../launches/README.md). A new launch asks for it.
- **Readers:** [Who reads the status, for example product, marketing, success and sales.]

## Sources

- **Linear or Jira**: the launch project. Items per workstream, owners, dates and states.
- **Notion or Google Docs**: the content database. The comms pieces, their briefs and their drafts.
- **GitHub**: the release. What ships, and the pull requests still in review.
- **Google Calendar**: the dates (go or no-go, freeze, launch, review), and who is out before a date.
- **Slack**: the launch channel, to post the status.

Every source is optional. Check which ones are connected. For a missing one, say what it would add, for example "connect Linear and the checklist fills itself". Without a launch project, type the checklist from the person's list. Without the content database, type the pieces. Without Slack, the person posts the status themselves. Never invent an item, a date or an owner.

## How the page is built

- Each launch is one page, `launches/<slug>.html`, copied from `launches/_template.html`. The slug comes from the launch's name, for example `portals-2.html`. The page is never the mold: never fill in `_template.html`.
- Read a page only down to the `end of content` comment. The script and the style after it never change.
- Write only inside elements with `data-slot`. Everything outside a slot is the team's: never change it.
- The slots:
  - `launch` and `sources` in the toolbar: the launch's name, and the sources with the time.
  - `headline`: the days to the launch in the title. Then the next date, what has to happen first, and how many items are done.
  - `numbers`: days to go, items done of the total, items at risk.
  - `timeline`: every key date from the first to the launch review, oldest first. A date that has passed says "Done".
  - `at-risk`: each item at risk, with why in one sentence.
  - `workstreams`: one `<section class="section off" data-view="Workstreams">` per workstream. Its heading is the name and the count done, for example "Product, 5 of 7". Keep `off` and `data-view` on each section.
  - `comms`: each comms piece.
  - `footer`: "Status posted to" with the channel and the time, after a post.
- A row is a title (`.t`), a date or a state (`.tr`), one sentence where it helps (`.s`), and the owner, date and source (`.m`).
- Each comms piece is a row that opens (`<details class="row">`). The summary holds the piece (`.t`), its state (`.tr`), and the channel, owner and date (`.m`). The detail holds **Brief** and **Draft**: a link to the draft's web address when it lives in a docs tool, or its state in words.
- At risk is a fact, never an opinion: an item overdue, blocked or waiting in its source, or owned by someone who is out before its date.
- Each section and row has an `id`. A workstream section is `workstream-` and its slug. A row is its section's prefix and the source key, or a short slug of its title: `date-go-no-go`, `risk-load-time-fix`, `item-load-time-fix`, `piece-launch-post`. Keep the `id` of a row that stays: comments on the shared page attach to it.
- An element with `data-kept="YYYY-MM-DD"` was changed at someone's request. Never rewrite it. If its source changed since, say so.
- When someone asks to change a line, change it and add `data-kept` with today's date.
- The page is shared as one file. A source links to its web address, never to a file in the workspace. Never add a stylesheet, a script, a font or an image from outside the page.

## Steps

1. **Find the launch.** Use the launch the person names, or the page where Refresh was pressed. If the person names none, read [`../launches/README.md`](../launches/README.md): when one launch has not shipped, use it; otherwise ask which, and list them. A launch with no row is a new launch: go to step 2. Otherwise go to step 3.
2. **Start a new launch.** Ask for what the request did not give: the name, the date, the launch channel and the launch project.
   - Copy `../launches/_template.html` to `../launches/<slug>.html`. Set `title` in the comment at the top to the launch's name.
   - Add the launch's row to `../launches/README.md`: the name with a link to its page, the date, the owner, the channel and "Active". Replace the `_None yet._` row with the first launch.
3. **Read the sources** for this launch. Do not widen the launch's scope without asking. Say which sources answered and which did not.
4. **Write the slots.** Four workstreams (product, marketing, support and sales) unless the launch project has others. Mark a part that no source gave as "Not known yet".
5. **Show what changed** against the page before this run, one line per change, and save after a yes. Update the launch's date and status in `../launches/README.md` if they changed.
6. **Mark a shipped launch.** When the launch date has passed and the release is out, the headline says it shipped and on which date. Set `status: archived` in the comment at the top, as Core's conventions say for finished work, and "Shipped" in its row. The page stays. Refresh it again only when someone asks.
7. **Stamp the page.** Set `last_updated` and `last_updated_by` in the comment at the top. Set `template` to the value in this process's frontmatter.
8. **Update the shared page.** If the page is shared from Palette, offer to update the shared copy too.

### Post the status

9. **Refresh first** with steps 3 to 7 when the page is older than a day.
10. **Write the status**: what is done per workstream, what is at risk and why, and the next date. Show it as it will read in the launch channel, with each line's link.
11. **Post after a yes.** Write "Status posted to" with the channel and the time in the `footer` slot. Say it in one line.
12. **Update the shared page** as in step 8.

## Done when

- Every slot shows the launch as its sources hold it today, or says which source was missing.
- The launch has its row in `../launches/README.md`, with the current date and status.
- The status is posted, or the person said not to post it.

## Rules

- Never post or update a shared page without a preview and a yes.
- At risk is a fact: overdue, blocked, or an owner out before the date. Never an opinion.
- The next date comes from the calendar.
- A line without its source is never posted as a fact.
- One page per launch. Never write one launch's content into another launch's page or into the mold.
- A shipped launch's page stays. Never delete it.
