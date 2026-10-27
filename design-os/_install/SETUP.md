---
type: doc
read_when:
  - "This file exists: the workspace is still being set up"
---

# Setup

**While this file exists, the workspace is still being set up.** This page says how to set it up and when to delete this file. It keeps no progress of its own: the pages are the progress. With the person, talk about setting up the workspace, never about this file.

## Before the steps

Make the person's folder if they have none: [`people/README.md`](people/README.md) → Add a person. Then ask once for what they have, unless they already said: whether the team designs in a design tool, in code or in both, the design files and repos they work in, where the design system lives, and where their existing design docs are. Whatever they have is enough to start.

## The steps

1. **Say where the design happens.** Fill in the line in [`AGENTS.md`](AGENTS.md) → Where the design happens with the person's answer.
2. **Reach the files and the repos.** Check you can read each one. A design file needs the design tool's connector for agents; a repo needs the folder. If you cannot reach one, walk the person through [`repos.md`](repos.md) → Give agents access. Fill in a row and the notes for each from what it says itself.
3. **Read the design system.** Write [`design-system/README.md`](design-system/README.md), [`foundations/`](design-system/foundations/README.md) and [`components/`](design-system/components/README.md) from the code or the design library, following each page's box. Never copy token values: they live in the code or the library. A team with no design system yet starts from its product, and the pages list what it repeats as a first proposal for one.
4. **Sort the existing docs.** Show the person where each piece would go, per [`AGENTS.md`](AGENTS.md) → Bringing material in, and write after their yes. A team with no docs skips this step.

Show the pages you wrote and ask the person to read them. A page they agree with loses its "Not confirmed yet" box.

When the person gives the team's name, put it in the heading of `AGENTS.md` and `README.md`.

## Not part of setup

The starter pages in [`principles/`](principles/README.md) and [`process/`](process/README.md) are there to be changed as the team works. Rules arrive as calls are made. Neither needs to be done before the workspace is used.

## When to delete this file

When the four steps are done, or when someone says the workspace is set up, delete this file and add one line to the root `log.md` saying that setup ended and what was left open. "I'll do the rest another day" means setup goes on: leave the file where it is.

If the person came to do something else, do that first. Then say in one line where setup stands and offer the next step.
