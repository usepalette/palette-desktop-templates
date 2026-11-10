---
type: process
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
cadence: weekly
template: goals-checkin@2611101
---

# Goals check-in

Writes the week's value, confidence and note for each key result of the quarter into [`../goals-checkin.html`](../goals-checkin.html). Posts the check-in to the company channel and writes the week to the goals page, each after a yes.

## When to run this

- On Friday, for the week that ends that day.
- When someone asks: "write the goals check-in", "refresh the goals check-in", "post the check-in", "share the goals update", "send the OKR update".
- When someone presses Refresh on the page.

## Where it goes

- **Channel:** [Not set yet. The first run asks, and writes the answer here.]
- **Goals page:** [The goals page in Notion or Google Docs, if there is one. The first run asks, and writes the link here.]
- **Readers:** [Who reads it, for example the whole company.]

## Sources

- **Notion or Google Docs**: the goals page. The objectives, key results, owners and targets, when the quarter starts.
- **Linear or Jira**: the projects behind the key results and their progress.
- **HubSpot**: the numbers behind the growth key results: paying teams, trial to paid.
- **PostHog**: the product numbers behind the key results: signups, usage, funnels.

Every source is optional. Check which ones are connected: a source counts only when its connector is connected, not because this list names it. For a missing one, say what it would add, for example "connect HubSpot and paying teams fill themselves". Without the goals page, the person types the goals once. A value no source gives is typed by the key result's owner when asked. Never invent a number.

## How the page is built

- Read the page only down to the `end of content` comment. The script and the style after it never change.
- Write only inside elements with `data-slot`. Everything outside a slot is the team's: never change it.
- The goals are the team's and sit outside the slots. Each objective is a `<section>` with the objective as its `h2`. Each key result is a row in it: the key result with its target (`.t`), the owner (the first `.m` span), and "How it is measured" in its detail. The row with `data-key` is the key result that decides the quarter. The empty page has one objective and one key result as placeholders in brackets.
- Write the goals only when the team gives them: on the first run and at a new quarter, from the goals page or from the person. At any other time, change a goal only when someone asks.
- A value no source gives is typed by the owner when asked. Write it into its slot with `data-kept` and today's date, and write "Typed in by" and the name in the `source` slot.
- The confidence and the note are the owner's. Write them with `data-kept` and the date the owner gave them.
- An element with `data-kept="YYYY-MM-DD"` was typed or changed at someone's request. Never rewrite it in the same week. If its source changed since, say so.
- When someone asks to change a line, change it and add `data-kept` with today's date.
- The slots for the whole page:

| Slot | What it holds |
|---|---|
| `week` | The week the page shows, in the toolbar. |
| `sources` | The sources that answered and the time. A source that did not answer is named here with the key results it left stale. |
| `headline` | The quarter and the week, for example "Q4 goals, week 45". Then one sentence: how many are on track, and the key result that decides the quarter. |
| `numbers` | Three tiles: on track, off track, and the key result with `data-key` against its target. |
| `earlier-quarters` | One row per closed quarter, newest first. It opens to each key result with its final value and "Met" or "Missed". |
| `footer` | The template line, then "Posted to" with the channel and the time, and whether the goals page got the week. |

- The slots in each key result row. The row's `id` says which key result they belong to.

| Slot | What it holds |
|---|---|
| `value` | This week's value, for example "104 of 120" or "72%". |
| `note` | The owner's one line for the week. |
| `confidence` | High, medium or low confidence, or "Done". |
| `change` | The change on last week, for example "+3 this week". |
| `source` | Where this week's value came from, or "Typed in by" and the name. |
| `progress` | The bar: `--w` is the share of the target, and `data-tip` says the value and the share. Low confidence is off track: the bar gets `warn`. |
| `weeks` | The earlier weeks of the quarter, newest first, one line each: "Week 44: 101, low confidence." and the note. |

- Each section and row has an `id`. An objective is the quarter and a short slug, for example `q4-growth`. A key result adds its own slug, for example `q4-growth-paying-teams`. A closed quarter is the quarter and the year, for example `q3-2026`. Keep the `id` of a row that stays: comments on the shared page attach to it.
- `period` in the comment at the top of the page is the week the page shows, for example `2026-W45`. The quarter is the one that holds the week's Friday.
- The page is shared as one file. A source links to its web address, never to a file in the workspace. Never add a stylesheet, a script, a font or an image from outside the page.

## Steps

1. **Find the week.** It is the week that ends this Friday, unless the person names another.
   - `period` is empty: this is the first run. Ask where the check-in goes and where the goals page is, and fill in **Where it goes** above. Go to step 3.
   - `period` is this week: this is a refresh. Go to step 4.
   - `period` is an earlier week of the same quarter: go to step 2.
   - `period` is in an earlier quarter: go to step 3.
2. **Start the new week.** In each key result, move the week to the top of its `weeks` slot as one line: the week, the value, the confidence and the note. Then clear `note`, `confidence` and `change`. Values with `data-kept` belong to the earlier week: they go into its line in `weeks` with the rest, and the new week starts without them. Go to step 4.
3. **Set the quarter's goals.** Ask for the new goals before you write anything: the objectives, the key results with their targets, the owners, how each one is measured, and the one that decides the quarter. Read them from the goals page when there is one, and show them for a yes.
   - If the page holds a closed quarter, add it to the top of `earlier-quarters` as one row: the quarter, how many key results were met, and each key result with its final value.
   - Replace the objective sections with the new goals, one section per objective and one row per key result. Mark the deciding key result with `data-key`.
4. **Read the sources** for the week. Say which ones answered and which did not. Do not widen the period without asking.
5. **Ask for what no source gives** in one message, grouped by owner: each value without a source, and each confidence and note, with last week's shown. If the person wants the owners asked directly, show each message and send it after a yes.
6. **Write the slots.** Each key result gets its value, change, source and bar, and the confidence and note its owner gave. Then the tiles, the headline, and the week and the sources with the time in the toolbar.
7. **Show what changed** against the page before this run, one line per change, with the old and the new value. Save after a yes.
8. **Stamp the page.** Set `period`, `last_updated` and `last_updated_by` in the comment at the top. Set `template` to the value in this process's frontmatter.
9. **Post after a yes.** Every key result needs a value and a confidence: ask for any that is missing. A missing note is fine. Show the post as it will read in the channel: the objectives as headings, and the key results as lines with the value, the confidence and the note. Write "Posted to" with the channel and the time in the `footer` slot.
10. **Write the week to the goals page after a yes.** If there is a goals page, show the row each key result gets: the week, the value, the confidence and the note. Write it after a yes, and say so in the `footer` slot.
11. **Update the shared page.** If the page is shared from Palette, offer to update the shared copy too. Say what went where in one line.

## Done when

- Every key result shows this week's value, or says which source was missing.
- Every key result has a confidence, or "Confidence not set".
- `period` names this week.
- The check-in is posted and the goals page has the week, or the person said not to.

## Rules

- Never post, send or write to the goals page without a preview and a yes.
- Never post a typed value as if a source gave it. Keep the "Typed in" mark.
- A key result without a confidence is posted as "not set", never guessed.
- A value without its source is never posted as a fact.
- Never change a goal at a refresh. Goals change at a new quarter, or when someone asks.
- A refresh changes the content, not the layout. Change the layout only when the person asks.
