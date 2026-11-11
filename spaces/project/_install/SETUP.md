---
type: doc
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
read_when:
  - "This file exists: the project space is still being set up"
---

# Setup

**While this file exists, the project space is still being set up.** This page says how to set it up and when to delete this file. It keeps no progress of its own: the pages are the progress. With the person, talk about setting up the project space, never about this file.

This is the project space's setup only. A `SETUP.md` at the root of the workspace is the company's setup: separate from this one, and not finished by it.

## Before the steps

The person needs a profile in the root [`people/`](../../people/README.md); the root rules make one if they have none. Then ask once for what they have, unless they already said: whether the team runs client engagements, internal projects or both, which pages a new project gets beyond its `README.md`, who sits on the other side of the team's projects, and where tasks live. Whatever they have is enough to start.

## The steps

1. **Say what kinds of projects the team runs.** Fill in the line in [`AGENTS.md`](AGENTS.md) → The projects this team runs with the person's answer: client engagements, internal projects or both.
2. **Choose the extras.** Show the extras in [`processes/start-a-project.md`](processes/start-a-project.md) → The extras, and ask which ones a new project gets by default. Fill in the line there with the answer. None is a fine answer: a project's `README.md` alone is a whole project.
3. **Name the sides.** Ask who sits on the other side of the team's projects: a customer's people, a sponsor inside the company, partners or vendors. Fit the sections of [`templates/stakeholders.md`](templates/stakeholders.md) to the answer: one for each side the team's projects have, named the way the team says it. A project's People table uses the same names in its Side column.
4. **Find the task home.** Read [`company/tools.md`](../../company/tools.md). When its Tasks row names a tracker or the shared task file, that is where a project's tasks live, and the project's `tracker` field links to them. If the page still says **Not filled in yet**, offer to fill in that row, following the page's own box, after a yes. Never start a task list in the space or in a project.
5. **Offer the first project.** Ask whether there is a project to start now, and after a yes run [`processes/start-a-project.md`](processes/start-a-project.md). A project already in [`projects/`](../../projects/README.md) can get the extras too, with the same process.

What the person says is written as they said it, and needs no second yes. A line you worked out yourself ends with "(to confirm)".

## Not part of setup

The two playbooks fill in as the team works: [`playbooks/ways-of-working.md`](playbooks/ways-of-working.md) when someone first says how the team runs a project, and [`playbooks/joining-a-project.md`](playbooks/joining-a-project.md) when someone first joins one. If the person tells you either during setup, write it there, following the page's own box. The formats in [`templates/`](templates/README.md) are there to be changed as the team runs projects. None of this needs to be done before the space is used.

## When to delete this file

When the five steps are done, or when someone says the project space is set up, delete this file and add one line to this space's [`log.md`](log.md) saying that setup ended and what was left open. A no to the first project still completes step 5. "I'll do the rest another day" means setup goes on: leave the file where it is.

If the person came to do something else, do that first. Then say in one line where setup stands and offer the next step.
