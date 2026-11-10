---
type: doc
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: everyone
read_when:
  - "This file exists: the workspace is still being set up"
---

# Setup

This workspace starts as a blank structure. **While this file exists, the workspace is still being set up.** This page says what "set up" means, how to get there and when to delete this file. It keeps no progress of its own: the pages are the progress. With the person, talk about setting up the workspace, never about this file.

## Where things stand

Setup is done when five things are: the four core pages, then a first space.

| What | Where | Done when |
|---|---|---|
| The company | `company/README.md` | the page has no box at its top |
| Tools | `company/tools.md` | the page has no box at its top |
| Voice | `company/brand/voice.md` | the page has no box at its top |
| Messaging | `company/brand/messaging.md` | the page has no box at its top |
| A first space | [`spaces/README.md`](spaces/README.md) | the list of spaces on that page has a space in it |

A page whose box says "Not confirmed yet" is written but not done: the next step for it is that a person reads it. A required page that is missing is not done: report it and restore it within an authorized repair, or ask how the setup should change. A deliberately declined first space may be skipped; a missing folder alone is not a decline.

To say where setup stands, count what is done: "2 of 5 done". When only the first space is left, say so: "4 of 5 done. The last one is a first space." Never keep a tally in this file.

## How to run it

1. **Start with the person.** If they have no folder in `people/` yet, get them set up first: [`people/README.md`](people/README.md) → Getting started here.
2. **Ask for the fastest source,** unless they already gave you one: then use it and don't ask. A website address, a deck or a document that describes the company, or what another AI tool already knows about it. Draft every core page that source supports. Ask questions only for what is still missing. They can paste it or drop a file in. Follow [the import procedure](.agents/import.md) for destinations and review. In setup, asking to set up the workspace is the yes for the core pages: draft them on their pages, where they stay "Not confirmed yet" until the person has read them. Anything else the source holds (customers, projects, colleagues) goes through the import proposal first.
3. **Know what the workspace is for.** If it is not clear, ask: the whole company, one team, or one project within the company. This is always professional team work, not a personal-project template. The core pages keep the company and brand context; the initial team or project goes in its own space or project folder.
4. **Work through the core**, in the order above unless the person wants another. Draft related pages together when one source supports them. Each page's box says what belongs there.
5. **Show the drafts and confirm a named batch.** The person may approve all the pages they have seen in one reply, or review them separately. Follow [page states](.agents/page-states.md): preserve owners, leave optional unknowns visible, and don't confuse review with a record's lifecycle.
6. **Use the company's name.** When the company page is confirmed, put the name in the three files that carry `[Company]`: the heading of `AGENTS.md`, the root `README.md` (its heading, its first lines and the tree) and the heading of `company/README.md`. Put the one-line description on the root `README.md`, delete the box on that page and set its `status` to `active`: its own box says the same.
7. **End with a first space.** Offer it when the four pages are done. If the person's actual task already requested a space earlier, do that task and count the existing space here. Ask which area of work the person spends most of their time in. Then show what you would make (the name of the space, one line on what it is for, and who owns it) and get a yes if those specifics have not already been approved. With that authorization, make that one space with the steps in [`spaces/README.md`](spaces/README.md) → Add a space. Only one, and only for the area they named: other spaces are made when someone asks for them. Do not turn a finite project into a space just to finish setup; the person may decline the space. Once the four core pages are confirmed and the space exists or has been declined, setup is over: do what "When to delete this file" says, below.
8. **Their task comes first.** If they came to do something else, do it. Then say in one line where setup stands and offer the next step. One offer, at the end; skip it for capture-only requests, people who have declined offers, or people who said setup is not theirs.
9. **Anyone can help; nobody has to.** Setup belongs to whoever is here, and it can be done in any order, by any number of people. If someone says setup is not theirs, don't offer it to them again, and note that in their own `lessons.md`.

## Later

Everything else fills in when the work reaches it, by the same rule as any blank page: how we work, the glossary, the brand design, products, the ideal customer, competitors, the starter templates, colleagues, more spaces, customers and projects. `company/meetings.md` fills itself in the first time someone logs a meeting.

## When to delete this file

- **All five are done,** or the four pages are done and the person said no to a space. Tell the person the workspace is set up, and delete this file. From then on a blank page is offered only when a task runs into it.
- **Someone says the workspace is set up, or that this is enough.** Check that they mean the workspace and not only themselves, then delete this file.

Don't suggest deleting this file yourself. "I'll do the rest another day" means setup goes on: leave the file where it is.

Either way, add one line to the root `log.md` with the date, saying that setup ended. If the company page was never confirmed, `[Company]` stays in the three headings until it is; nothing else needs changing when this file goes.
