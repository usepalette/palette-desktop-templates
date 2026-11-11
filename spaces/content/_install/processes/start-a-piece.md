---
type: process
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
cadence: ""
---

# Start a piece

Turns a request for a piece into a first draft, saved in `pieces/` with its channel, its one takeaway and its row in the list. It runs whenever someone asks for writing that goes out.

## When to run this

- Someone asks for a piece that goes out: "help me write a LinkedIn post about…", "draft a blog post on…", "we need this month's newsletter".
- A line or two asked for in passing, such as a reply to a comment, can stay in the conversation. Offer once to keep it as a piece.

## Steps

1. **Find the channel.** Take it from the request, or ask. The channel decides the length and the shape: its line in [`playbooks/content.md`](../playbooks/content.md) → Content types.
2. **Find the one takeaway.** The one thing the reader should leave with, in a sentence. If the person can't name it, help them find it before writing any prose: offer two or three from what they said, and let them pick.
3. **Look for what has been said.** Search [`pieces/README.md`](../pieces/README.md) and the pieces for the same topic. Build on an earlier piece or take another angle, and note it under **Notes**.
4. **Read the voice.** [`company/brand/voice.md`](../../../company/brand/voice.md) for how we sound, and [`company/brand/messaging.md`](../../../company/brand/messaging.md) for facts and names, never to paste a tagline in. For a piece under a person's name, their `people/<name>/tone-of-voice.md` comes first and the company voice sits under it. Who the reader is: [`company/market/ideal-customer.md`](../../../company/market/ideal-customer.md).
5. **Gather the material.** Claims and examples come from `company/` (the products, the proof points in the messaging), the projects in `projects/` and what the person tells you. A customer is named only with their approval, recorded in their folder in `customers/`. Never invent a number, a quote or a name.
6. **Use a format when one fits.** A social post follows [`company/templates/social-post.md`](../../../company/templates/social-post.md), and a customer story [`company/templates/customer-story.md`](../../../company/templates/customer-story.md). When the workspace has a GTM space, a piece for a launch follows its launch formats in `spaces/gtm/templates/launch/`.
7. **Make the file.** Copy [`pieces/_template.md`](../pieces/_template.md) to `pieces/YYYY-MM-DD-<slug>.md`, with today's date and the working title in kebab-case: "Why we rebuilt onboarding" becomes `why-we-rebuilt-onboarding`. Set `owner` to the person who asked for the piece, unless they name someone else, and set `channel`, `last_updated` and `last_updated_by`. Keep `status: draft`, fill in the takeaway, who it is for and who it goes out as, and delete the **Mold** box.
8. **Write the draft.** Lead with the insight or the problem, one idea per paragraph, concrete examples over claims, at the channel's length. Do the work with what you have: a first draft is worth more than a list of questions. Note each source under **Notes**, and mark anything you inferred "(to confirm)".
9. **Add its row** at the top of the table in [`pieces/README.md`](../pieces/README.md): the date, the title linked to the file, the channel, `draft`, and an empty link.
10. **Hand it over.** Show the draft in the reply, with one line on what would make it better. Then one offer: refine it, check the voice, or plan where it goes.

## Done when

- The piece is in `pieces/` with its channel, its takeaway, a first draft and `status: draft`.
- Its row is at the top of `pieces/README.md`.
- Every number, quote and name in it has a source under **Notes**, or a "(to confirm)" mark.
- The person has seen the draft.
