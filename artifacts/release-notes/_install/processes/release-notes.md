---
type: process
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
cadence: weekly
template: release-notes@2611102
---

# Release notes

Writes the week's release notes for customers into [`../release-notes.html`](../release-notes.html) from the team's tools, with the internal lines kept apart. After a yes, it publishes them and tells the customers who asked.

## When to run this

- On Friday, for the week that ends that day.
- When someone asks: "write this week's release notes", "refresh the release notes", "publish the release notes", "post what shipped", "tell the customers who asked".
- When someone presses Refresh on the page.

## Where it goes

- **Changelog:** [Not set yet. The first run asks where the changelog lives, and writes the answer here.]
- **Announcements channel:** [Not set yet. The first run asks, and writes the answer here.]
- **Mail:** [The list for a release mail. It is used only when someone asks for a mail.]
- **Areas:** [The product areas customers know, for example Portals and Notifications. The first run proposes them from the task tool.]

## Sources

- **GitHub**: the pull requests merged this week, with their title, author and description.
- **Linear or Jira**: the issues closed this week, for the area and the customer requests linked to them.
- **Slack**: the feedback channel, for who asked for each thing or reported each bug.

Every source is optional. Check which ones are connected. For a missing one, say what it would add, for example "connect the feedback channel and each line says who asked". Without GitHub, write the lines from the closed issues. Without the feedback channel, the lines have no "Asked for by", and the run says so. Never invent a line.

## How the page is built

- Read the page only down to the `end of content` comment. The script and the style after it never change.
- Write only inside elements with `data-slot`. Everything outside a slot is the team's: never change it.
- An element with `data-kept="YYYY-MM-DD"` was changed at someone's request. Never rewrite it. If its source changed since, say so.
- When someone asks to change a line, change it and add `data-kept` with today's date.
- The slots:

| Slot | What it holds |
|---|---|
| `week` | The toolbar button: the week, for example "Week 45". |
| `sources` | The sources that answered, and the day. |
| `headline` | An `h1` with the week's main change in customer words, and one `p` on the rest. |
| `areas` | The filter pills: "All", then one pill per area that has a row on the page. |
| `new`, `improved`, `fixed` | The customer lines, one row each. |
| `internal` | One row per customer line, with its pull requests, issue keys and who did it. The small fixes are one row. |
| `earlier-weeks` | One row that opens per earlier week, the newest on top. |
| `footer` | Where and when the notes were published, and the notes to customers. |

- A customer row is a title (`.t`), one sentence on what changes for the customer (`.s`), and `.m`: the area, then "Asked for by" or "Reported by" with the customers. A fix that needs no sentence has none.
- An internal row is the change in the team's words (`.t`), its kind (`.tr`: New, Improved or Fixed) and `.m`: the pull requests, the issue keys and the people.
- An earlier week is a `details.row`: the summary holds "Week 44: " and its headline, the date of its Friday (`.tr`) and the chevron. The `.detail` holds one `.k` and `.x` pair per kind, with the week's customer lines.
- Every row has `data-tags` with the exact values of its area pills, for example `data-tags="Portals"`. A row that covers several areas, such as the small fixes or an earlier week, lists them all: `data-tags="Portals,Notifications"`. Never write a pill that no row has.
- `data-internal` marks what only the team sees: the `internal` section, every "Asked for by" and "Reported by" span, and anything that names a pull request, an issue key or a person on the team. Customer names stay internal, because the changelog is public.
- Each row has an `id`: the week and its issue key, for example `w45-hal-1398`. A row without a key uses a short slug of its title, for example `w45-small-fixes`. An internal row adds `-internal`, for example `w45-hal-1398-internal`. An earlier week uses only the week, for example `w44`. Keep the `id` of a row that stays: comments on the shared page attach to it.
- The page is shared as one file. A source links to its web address, never to a file in the workspace. Never add a stylesheet, a script, a font or an image from outside the page.
- `period` in the comment at the top of the page is the week the page shows, for example `2026-W45`.

## The customer version

`release-notes-customers.html`, next to the page, is the page for customers. The first publish makes it, and every publish after that writes it again.

- It is a copy of the page without every element that has `data-internal`. Remove a pill that no row keeps.
- Set its `<title>` to "Release notes for customers", and remove the `template` line from its top comment, so the app does not take it for the page.
- Never edit it by hand. Change the page and publish again.

## Steps

1. **Find the week.** It is the week that ends today, unless the person names another.
   - `period` is empty: this is the first run. Ask where the changelog lives and which channel gets the announcement, propose the areas, fill in **Where it goes** above, and go to step 3.
   - `period` is this week: this is a refresh. Go to step 3.
   - `period` is an earlier week: go to step 2.
2. **Start the new week.** Move the earlier week to the top of **Earlier weeks** as one row that opens: "Week 44: " and its headline, with the date of its Friday. Its detail holds the week's customer lines by kind, with their wording as published: take them from `release-notes-customers.html`, which holds what went out, not from the page, which can hold edits made after publishing. If the week was never published, take the page's lines, add "Not published" to the row, and mark the row `data-internal`, so no customer version shows lines nobody approved. Take `data-internal` off only when the week is published. Its internal lines and the customer names do not move. Then clear the other slots.
3. **Read the sources** for the week. Say which ones answered and which did not.
4. **Write the slots.** Sort each change into new, improved or fixed. Write each line for customers: what they can do now, in plain words, with no pull request, issue key or code term. Group the fixes a customer would not notice into one row, for example "Six more small fixes". Find who asked for each line in the feedback and the issues. Then write the internal rows, the pills, the headline, and the toolbar with the week and the sources.
5. **Show what changed** against the page before this run, one line per change, and save after a yes.
6. **Stamp the page.** Set `period`, `last_updated` and `last_updated_by` in the comment at the top. Set `template` to the value in this process's frontmatter.
7. **Publish after a yes.** Show the customer version as it will publish, without the internal parts. After a yes, post it to the changelog and the announcements channel. Send the mail only when someone asks for it, and only after a yes for the mail. Write "Published to" with the places and the time in the `footer` slot. Then write `release-notes-customers.html`.
   - An earlier week marked "Not published" can be published later. Show its lines as they will publish. After a yes, take `data-internal` and "Not published" off its row, and publish them the same way.
8. **Tell the customers who asked.** For each customer in an "Asked for by" or "Reported by" span, draft a short note: it thanks them and holds only their lines. Show each note, and send it after a yes for that note. A note without a yes stays a draft. Add the count of notes sent to the `footer` slot, inside a `data-internal` span.
9. **Update the shared pages.** If the page or the customer version is shared from Palette, offer to update the shared copy too.

## Done when

- Every slot shows this week, or says which source was missing.
- Every row has `data-tags`, and every pill matches at least one row.
- `period` names this week.
- The notes are published and `release-notes-customers.html` is current, or the person said not to publish.
- Each customer who asked has a note sent or drafted, or the person said not to.

## Rules

- Never publish, post, mail, send a note or update a shared page without a preview and a yes.
- Internal lines never publish. The customer version never holds a pull request, an issue key, a team member's name or another customer's name.
- A note to a customer holds only the lines they asked for or reported.
- Never mail every customer without an explicit yes for the mail.
- A line without its source is never published as a fact.
- Write every line for customers. Never copy a line from another page, such as the weekly update or the sprint review.
- A line changed at someone's request is published as changed. It is never written again at publishing time.
