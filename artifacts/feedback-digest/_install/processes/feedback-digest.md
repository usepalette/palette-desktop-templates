---
type: process
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
cadence: weekly
template: feedback-digest@2611101
---

# Feedback digest

Sorts the week's customer feedback into themes in [`../feedback-digest.html`](../feedback-digest.html), and links or files an issue for each theme after a yes.

## When to run this

- On Friday, for the week that ends that day.
- When someone asks: "sort this week's feedback", "make the feedback digest", "refresh the feedback digest", "update the feedback digest".
- When someone asks for the issues: "create the issues from the feedback", "link the themes", "file this feedback". Run the steps for the week, then step 8.
- When someone presses Refresh on the page.

## Where it goes

- **New issues:** [Not set yet. The first time issues are filed, ask which team or project in Linear or Jira takes them, and write the answer here.]

## Sources

- **Slack**: the feedback channel and the customer channels.
- **HubSpot**: the support inbox and the CRM notes. Who wrote, and for which customer.
- **Transcripts**: the customer calls of the week.
- **A space with a `user-feedback/` folder**: that folder, when the workspace has one (`spaces/*/user-feedback/`). The feedback the team collected there by hand.
- **Linear or Jira**: the issues and projects the themes point to.

Every source is optional. Check which ones are connected or present. For a missing one, say what it would add, for example "connect HubSpot and the support inbox counts too". Without the support tool, build the digest from Slack and the calls, and say in the toolbar what it did not read. A theme without an issue says "No issue yet". Never invent a quote, a count or a customer.

That folder belongs to its space. Read it, and never create, change or move a file in it.

## How the page is built

- Read the page only down to the `end of content` comment. The script and the style after it never change.
- Write only inside elements with `data-slot`. Everything outside a slot is the team's: never change it.
- An element with `data-kept="YYYY-MM-DD"` was changed at someone's request. Never rewrite it. If its source changed since, say so.
- When someone asks to change a line, change it and add `data-kept` with today's date.
- The page is shared as one file. A source links to its web address, never to a file in the workspace. Never add a stylesheet, a script, a font or an image from outside the page.
- `period` in the comment at the top of the page is the week the page shows, for example `2026-W45`.

| Slot | What it holds |
|---|---|
| `week` | The week, for example "Week 45". |
| `sources` | The sources that answered, and the day and time. Name a source that did not answer. |
| `headline` | An `h1` on the top theme, and one `p` on what moved since last week. |
| `numbers` | Three tiles: pieces of feedback, customers, themes. The first is the key tile. |
| `themes` | This week's themes, the largest first. |
| `over-time` | Every theme of the last six weeks, with its count per week. |
| `footer` | The template line, and when the issues were last filed. |

- A theme row is a `<details class="row">` that opens. The summary has the theme (`.t`), its count this week (`.tr`) and the chevron. Under it, `.m` holds the customers, the trend and the issue id or "No issue yet". Then `.bar`, with `--w` the count against the largest theme and `data-tip` "count, share". The `.detail` holds up to three quotes: `.k` is the customer and the source, `.x` is the quote. The first row is `open`.
- A row that groups small themes, such as "Billing, export and mobile", goes last.
- An over-time row has the theme (`.t`) and its trend (`.tr`): Rising, Falling, Steady, New or Gone. Its `.m` has one span per week, oldest first, such as "W44 9", then the issue id. Show six weeks at most. A theme with no piece in six weeks leaves the slot.
- Ids: a theme row is the week and a slug of the theme, for example `w45-client-approvals`. An over-time row is `t-` and the slug, for example `t-client-approvals`. Keep the `id` of a row that stays: comments on the shared page attach to it.
- Keep a theme's name from week to week, so its counts line up. When the team renames a theme, keep its ids.

## Steps

1. **Find the week.** It is the week that ends today, unless the person names another.
   - `period` is empty: this is the first run. Go to step 3.
   - `period` is this week: this is a refresh. Go to step 3.
   - `period` is an earlier week: go to step 2.
2. **Start the new week.** The week before stays in **Over time**: check that its counts are there. Then clear `week`, `sources`, `headline`, `numbers` and `themes`. Its quotes stay in the issues they went to.
3. **Read the sources** for the week. Say which ones answered and which did not. Do not widen the week without asking.
4. **Sort the feedback into themes.** Match each piece to a theme in **Over time** before you make a new one. Count the pieces and the customers. Keep the clearest quotes, with the customer, the source and the date. Take each theme's issue from **Over time** or from the task tool.
5. **Write the slots.** The headline, the three numbers, the themes, this week's count and trend in **Over time**, the week and the sources with the time.
6. **Show what changed** against the page before this run, one line per change, with the old and the new value. Save after a yes.
7. **Stamp the page.** Set `period`, `last_updated` and `last_updated_by` in the comment at the top. Set `template` to the value in this process's frontmatter.
8. **Link or file the issues after a yes.** If **Where it goes** is not set, ask, and write the answer there. For each theme, search the task tool for an open issue or project on the same thing. Show one list: each theme, the issue it matches or the title of a new one, and the quotes and customers that go in. After a yes:
   - Link a match. Add this week's quotes and customers to it as a comment.
   - Create a new issue for a theme with no match. Put the quotes and the customers in its description.
   - Where the task tool keeps customer requests, attach the customers there too.
   - Write the issue id into the theme's `.m` and its over-time row. Write "Issues filed" and the time in the `footer` slot.
   - Say in one line what was linked and what was created.
9. **Update the shared page.** If the page is shared from Palette, offer to update the shared copy too.

## Done when

- Every slot shows this week, or says which source was missing.
- **Over time** has this week's count for every theme.
- `period` names this week.
- Every theme has an issue id, "No issue yet", or the person said not to file it.

## Rules

- Never create an issue, comment on one or update a shared page without a preview and a yes.
- Never create an issue that duplicates an open one. Search first.
- A quote is the customer's own words. Shorten it, never reword it.
- Quotes go into the issue as quotes, with the customer and the date.
- A number that is unknown stays marked as missing. It is never invented.
- A source that answered before and not now: keep its old lines, marked with the date of the earlier run.
- Never change the files of a space. The page is the only file this process writes.
