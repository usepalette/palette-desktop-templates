---
type: process
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
cadence: weekly
template: competitor-watch@2611101
---

# Competitor watch

Writes the competitors' week, where we stand and their profiles into [`../competitor-watch.html`](../competitor-watch.html), and posts the digest to marketing and sales after a yes.

## When to run this

- On Friday, for the week that ends that day.
- When someone asks: "write the competitor watch", "refresh the competitor watch", "update the competitor watch", "what did the competitors do".
- When someone asks to post it: "post the competitor digest", "send the watch". Run the steps for the week, then step 7.
- When someone presses Refresh on the page.

## Where it goes

- **Channels:** [Not set yet. The first run asks for the marketing and sales channels, and writes the answer here.]
- **Readers:** [Who reads it, for example marketing, sales and support.]

## Sources

- **Web**: the competitors' changelogs, pricing pages, blogs and posts.
- **Slack**: the competitors channel and the mentions elsewhere.
- **Transcripts**: the sales calls where a competitor came up.
- **Notion or Google Docs**: the team's competitors page, for the profiles.
- **A space with a `competitors/` folder**: the profiles the team keeps in a space, when the workspace has one. Find the space in `spaces/README.md`, or as `spaces/*/competitors/`.

Every source is optional. Check which ones are connected or present. For a missing one, say what it would add, for example "connect the call recorder and the sales mentions fill themselves". Without the calls, the sales mentions are empty and the toolbar says so. Never invent a move, a price or a quote.

The profiles come from the first of these that has them: the space, the competitors page, then the page itself. A space and a competitors page belong to the team. Read them, and never create, change or move a file in them. With neither, the profiles live on this page: the first run makes them from the web, and the team keeps them here.

## How the page is built

- Read the page only down to the `end of content` comment. The script and the style after it never change.
- Write only inside elements with `data-slot`. Everything outside a slot is the team's: never change it. The view pills are outside the slots.
- An element with `data-kept="YYYY-MM-DD"` was changed at someone's request. Never rewrite it. If its source changed since, say so.
- When someone asks to change a line, change it and add `data-kept` with today's date.
- The page is shared as one file. A source links to its web address, never to a file in the workspace. Never add a stylesheet, a script, a font or an image from outside the page.
- `period` in the comment at the top of the page is the week the page shows, for example `2026-W45`.

| Slot | View | What it holds |
|---|---|---|
| `week` | | The week, for example "Week 45". |
| `sources` | | The sources that answered, and the day and time. Name a source that did not answer. |
| `headline` | | An `h1` on the move that matters most, and one `p` on the week. |
| `numbers` | | Three tiles: moves, competitors, moves that matter. The last is the key tile. |
| `moves` | This week | The week's moves, rated. |
| `what-to-say` | This week | What to say when a customer brings up a move. |
| `earlier-weeks` | This week | One row per earlier week, the latest first. |
| `where-we-stand` | Where we stand | One table: us against each competitor. |
| `profiles` | Profiles | One profile per competitor. |
| `footer` | | The template line, and where and when the digest was posted. |

- A move row is the move, with the competitor first (`.t`), its rating (`.tr`), one or two sentences on what it is and why it matters to us (`.s`), and its sources (`.m`). Matters first, then Watch, then Note.
  - **Matters**: it changes a deal or our plans, or customers name it.
  - **Watch**: it could matter if it grows.
  - **Note**: worth knowing, nothing to do.
- A what-to-say row is "When a customer brings up …" (`.t`), what to say in two sentences at most (`.s`), and who says it (`.m`). Write one for each move rated Matters or Watch.
- An earlier-weeks row is "Week 44: " and that week's headline (`.t`), and the date of its Friday (`.m`).
- The where-we-stand table has one row per capability. Our column comes first with `class="em"`, then one column per competitor. A cell is Yes, Partly, — or a date.
- A profile is a `<details class="row">` that opens. The summary has the name (`.t`) and the chevron, one line on what they are and where they are strongest (`.s`), and the price and the last move (`.m`). The `.detail` has `.k` and `.x` pairs: Who they sell to, Where they win, Where we win, Recent moves and Sources. When the profile comes from a space or the competitors page, Sources names it.
- Ids: a move is the week, the competitor and a slug, for example `w45-portalio-approvals`. A what-to-say row adds `say`, for example `w45-say-portalio-approvals`. An earlier week is `w44`. A profile is `c-` and the competitor, for example `c-portalio`. A table row is `f-` and the capability. Keep the `id` of a row that stays: comments on the shared page attach to it.

## Steps

1. **Find the week.** It is the week that ends today, unless the person names another.
   - `period` is empty: this is the first run. Take the list of competitors from the space or the competitors page, or ask. Ask where the digest goes, and fill in **Where it goes** above. Go to step 3.
   - `period` is this week: this is a refresh. Go to step 3.
   - `period` is an earlier week: go to step 2.
2. **Start the new week.** Move the earlier week to the top of **Earlier weeks** as one row: "Week 44: " and its headline, with the date of its Friday. Then clear `week`, `sources`, `headline`, `numbers`, `moves` and `what-to-say`. **Where we stand** and **Profiles** carry over.
3. **Read the sources** for the week. For each competitor: the changelog, the pricing page, the blog and the posts. Then the Slack mentions and the calls. Say which ones answered and which did not. Do not widen the week without asking.
4. **Write the slots.**
   - The moves, rated, and what to say for each move rated Matters or Watch. Check each claim about a competitor against its move.
   - Where we stand: change a cell only when a move changed it.
   - The profiles: from the space or the competitors page when there is one, else from the page. Add the week's moves to Recent moves, and update the price and the last move.
   - The numbers, the headline, the week and the sources with the time.
5. **Show what changed** against the page before this run, one line per change, with the old and the new value. If a move changes a profile that a space or a competitors page holds, say so, so the team can update it there. Save after a yes.
6. **Stamp the page.** Set `period`, `last_updated` and `last_updated_by` in the comment at the top. Set `template` to the value in this process's frontmatter.
7. **Post after a yes.** Show the post as it will read in the channels: the moves rated Matters first, then Watch, then the count of Note. Each move has its source link. What to say comes last. Post to the channels in **Where it goes**. Write "Posted to" with the channels and the time in the `footer` slot. Say it in one line.
8. **Update the shared page.** If the page is shared from Palette, offer to update the shared copy too.

## Done when

- Every slot shows this week, or says which source was missing.
- Each move rated Matters or Watch has a what-to-say row.
- `period` names this week.
- The digest is posted, or the person said not to post it.

## Rules

- Never post or update a shared page without a preview and a yes.
- A move needs a source. A rumour without one stays off the page and out of the post.
- What to say never names a competitor's weakness without a fact behind it.
- A price or a number that is unknown stays marked as missing. It is never invented.
- A source that answered before and not now: keep its old lines, marked with the date of the earlier run.
- A line changed at someone's request is posted as changed. It is never written again at posting time.
- Never change the files of a space or the team's competitors page. The page is the only file this process writes.
