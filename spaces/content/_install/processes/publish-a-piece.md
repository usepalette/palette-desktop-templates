---
type: process
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
cadence: ""
---

# Publish a piece

Records a piece that went out: its status, the date and the link, in the piece and in the list. It runs when a piece is published, and to record one that went out without a file here.

## When to run this

- Someone says a piece went out: "we published this today", "log the article we published", "this went out on LinkedIn", with the link.
- Someone asks you to post, schedule or send a piece through a connected tool.

## Steps

1. **Find the piece.** Match the title or the topic against [`pieces/README.md`](../pieces/README.md). If two could match, or none does, ask. A piece written somewhere else gets a row and no file, unless the person wants its text kept here.
2. **Get what is missing.** The date it went out, the channel and the link. Write the date out as `YYYY-MM-DD`, never "today", and never invent a link or a date.
3. **Publishing through a tool waits for a yes.** If the person asks you to post, schedule or send the piece, show the exact text, the account or list it goes to, and when. Post only after their yes, then read back what was published and take the link from it.
4. **Update the piece.** In its frontmatter: `status: published`, `date` (the day it went out), `link`, `last_updated` and `last_updated_by`. The file keeps its name, so no link to it breaks.
5. **Update the list.** In its row in `pieces/README.md`: the day it went out, `published` and the link. Keep the table newest first: move the row if the new date changes its place.
6. **Offer what comes next.** If the piece has no distribution plan yet, offer one with [`plan-distribution.md`](plan-distribution.md): a great piece nobody sees is a wasted piece.

## Done when

- The piece says `status: published`, with the date and the link.
- Its row in `pieces/README.md` shows the same date, status and link.
- Nothing was posted, scheduled or sent without the person's yes.
