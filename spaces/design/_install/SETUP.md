---
type: doc
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
read_when:
  - "This file exists: the design space is still being set up"
---

# Setup

**While this file exists, the design space is still being set up.** This page says how to set it up and when to delete this file. It keeps no progress of its own: the pages are the progress. With the person, talk about setting up the design space, never about this file.

This is the design space's setup only. A `SETUP.md` at the root of the workspace is the company's setup: separate from this one, and not finished by it.

## Before the steps

The person needs a profile in the root [`people/`](../../people/README.md); the root rules make one if they have none. Then ask once for what they have, unless they already said: whether the team designs in a design tool, in code or in both, the design files and repos they work in, where the design system lives, and where their existing design docs are. Whatever they have is enough to start.

## The steps

1. **Say where the design happens.** Fill in the line in [`AGENTS.md`](AGENTS.md) → Where the design happens with the person's answer.
2. **Reach the files and the repos.** Check you can read each one. A design file needs the design tool's connector for agents; a repo needs the folder. If you cannot reach one, walk the person through [`repos.md`](repos.md) → Give agents access. Fill in a row and the notes for each from what it says itself.
3. **Read the design system.** Write [`design-system/README.md`](design-system/README.md), [`foundations/`](design-system/foundations/README.md) and [`components/`](design-system/components/README.md) from the code or the design library, following each page's box. Never copy token values: they live in the code or the library. A team with no design system yet starts from its product, and the pages list what it repeats as a first proposal for one.
4. **Sort the existing docs.** Show the person where each piece would go, per [`AGENTS.md`](AGENTS.md) → Bringing design material in, and write after their yes. A team with no docs skips this step.

Show the pages you wrote and ask the person to read them. A page they agree with loses its "Not confirmed yet" box.

## Not part of setup

The starter pages in [`principles/`](principles/README.md) and [`process/`](process/README.md) are there to be changed as the team works. Rules arrive as calls are made. Neither needs to be done before the space is used.

## When to delete this file

When the four steps are done, or when someone says the design space is set up, delete this file and add one line to this space's [`log.md`](log.md) saying that setup ended and what was left open. "I'll do the rest another day" means setup goes on: leave the file where it is.

If the person came to do something else, do that first. Then say in one line where setup stands and offer the next step.
