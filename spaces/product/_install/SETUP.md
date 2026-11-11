---
type: doc
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
read_when:
  - "This file exists: the product space is still being set up"
---

# Setup

**While this file exists, the product space is still being set up.** This page says how to set it up and when to delete this file. It keeps no progress of its own: the pages are the progress. With the person, talk about setting up the product space, never about this file.

This is the product space's setup only. A `SETUP.md` at the root of the workspace is the company's setup: separate from this one, and not finished by it.

## Before the steps

The person needs a profile in the root [`people/`](../../people/README.md); the root rules make one if they have none. Then ask once for what they have, unless they already said: what the space covers, where feedback arrives today, which tools hold the work (a tracker, analytics, a support or research tool), where their existing research, specs and strategy are, and what they want to do first. Whatever they have is enough to start. One person working alone, no tracker and feedback captured by hand are all fine: a tool the team doesn't have is written "not used", never guessed.

## The steps

1. **Say what the space covers.** One product, a product area, a platform or a portfolio, by name. Write it in place of the brackets in the "This space covers" line of [`README.md`](README.md), and delete "Setup fills in this line." after it.
2. **Describe the product where the company keeps it.** If [`company/products/`](../../company/products/README.md) has no file for the product yet, offer to add one, following that page's **Add a product**, after a yes; a portfolio gets one file per product. Link the file from the line in step 1. If [`company/glossary.md`](../../company/glossary.md) still says **Not filled in yet**, offer to start it with the product's own words, such as its feature names and abbreviations, following its box, after a yes.
3. **Record where feedback arrives.** The support tool, the channels, the calls or the research tool, or "captured by hand". Write it as a "Product feedback" row in [`company/tools.md`](../../company/tools.md). Feedback reaches this space through [capture feedback](processes/capture-feedback.md), one piece or a batch at a time.
4. **Record the live systems.** The tracker the specs link to is the **Tasks and issues** row of [`company/tools.md`](../../company/tools.md); add a row for the product analytics and for any research tool. "Not used" is an answer. If that page still says **Not filled in yet**, offer to fill it, following its box, after a yes.
5. **Bring in what exists.** Show the person where each piece of existing feedback, research, specs and strategy would go, per [`AGENTS.md`](AGENTS.md) → Bringing product material in, and write after their yes. A team with nothing to bring skips this step.
6. **Choose the first workflow.** Unless the person already said, ask which helps most now: capturing feedback, finding a pattern, framing a question, writing a thesis or writing a spec. Start it, or say the words that start it.

Show the pages you wrote and ask the person to read them. A page they agree with loses its "Not confirmed yet" box.

## Not part of setup

The playbook in [`playbooks/`](playbooks/README.md) and the processes in [`processes/`](processes/README.md) are a first version, there to be changed as the team works. Feedback, discovery questions, theses and specs arrive with the work. None of it needs to be done before the space is used.

## When to delete this file

When the six steps are done, or when someone says the product space is set up, delete this file and add one line to this space's [`log.md`](log.md) saying that setup ended and what was left open. "I'll do the rest another day" means setup goes on: leave the file where it is.

If the person came to do something else, do that first. Then say in one line where setup stands and offer the next step.
