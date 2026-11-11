---
type: doc
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
read_when:
  - "This file exists: the content space is still being set up"
---

# Setup

**While this file exists, the content space is still being set up.** This page says how to set it up and when to delete this file. It keeps no progress of its own: the pages are the progress. With the person, talk about setting up the content space, never about this file.

This is the content space's setup only. A `SETUP.md` at the root of the workspace is the company's setup: separate from this one, and not finished by it. The voice page in step 3 is one of its core pages, so filling it in here moves that setup on as well.

## Before the steps

The person needs a profile in the root [`people/`](../../people/README.md); the root rules make one if they have none. Then ask once for what they have, unless they already said: the channels the team writes for and how often, where pieces get published, two or three pieces the company was happy with if the voice page in step 3 is still empty, and drafts or published pieces to bring in. Whatever they have is enough to start: one channel is fine.

## The steps

1. **Say which channels the team writes for, and how often.** Fill in **Content types** in [`playbooks/content.md`](playbooks/content.md) with the person's answer: a row for each channel the team uses, with its length, where it goes and how often. Delete the rows for channels the team doesn't use and add the ones it has. A length or a cadence nobody knows yet keeps its bracket. If the person names communities, groups or partners the team shares in, fill in **Where we share** too.
2. **Say where pieces get published.** For each tool the team publishes with, such as the blog's tool, the newsletter tool or a scheduling tool, add a row to [`company/tools.md`](../../company/tools.md) saying which pieces live there. Adding the rows does not confirm the rest of that page. A channel that is only an account, such as a LinkedIn profile, needs no row.
3. **Check the voice.** Read [`company/brand/voice.md`](../../company/brand/voice.md) and look at the box at its top.
   - **No box:** the voice is in place. Nothing to do.
   - **Not confirmed yet:** it is written and waits for a person to read it. Offer to go through it with them.
   - **Not filled in yet:** offer to fill it in now. After a yes, follow that page's own box: start from the two or three pieces the person was happy with, which go under **Pieces that sound like us**, then ask in one round for what they don't show:
     - the voice in one line, the way you would brief a new writer → **In one line**
     - what we sound like → **What we sound like**
     - what we believe, and three pairs of do and don't → **What we sound like** as well, each as a quality and what it means on the page, since the page has no section of its own for them
     - words to use, and words to avoid → **Words**

     Write only what the person gives you, in their words.
4. **Bring in what is already written.** Follow the root import procedure, [`.agents/import.md`](../../.agents/import.md): show one table with each piece and where it would go, and wait for a yes. A published piece becomes a row in [`pieces/README.md`](pieces/README.md) with its date, title, channel, `published` and its link; its text stays where it was published unless the person wants it kept here. A draft in progress becomes a piece copied from [`pieces/_template.md`](pieces/_template.md), with `status: draft`. A team with nothing to bring in skips this step.

Show the pages you wrote and ask the person to read them. A page they agree with loses its "Not confirmed yet" box.

## Not part of setup

The principles and the approach in [`playbooks/content.md`](playbooks/content.md) are a first version, there to be changed as the team writes. The processes in [`processes/`](processes/README.md) work from day one. Neither needs to be done before the space is used.

## When to delete this file

When the four steps are done, or when someone says the content space is set up, delete this file and add one line to this space's [`log.md`](log.md) saying that setup ended and what was left open. "I'll do the rest another day" means setup goes on: leave the file where it is.

If the person came to do something else, do that first. Then say in one line where setup stands and offer the next step.
