---
type: index
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
---

# Design

The design team's home: how the team thinks about design, the calls it has settled, how the work is done and what the design system is, with a folder for each exploration. What one designer settles here is written down where the next one will read it.

Company-wide rules live in the root [`AGENTS.md`](../../AGENTS.md) and always apply. How to think and behave *in this space* is in this folder's [`AGENTS.md`](AGENTS.md).

## Get started

While `SETUP.md` exists in this folder, the space is still being set up. Say "set up the design space" and tell the agent what you have: whether you design in a design tool, in code or both, where your design system and product live, and where your existing design docs are. A repo is enough to start.

Each page you have not set up yet opens with a box saying so. The box tells the agent what to do with the page and goes once a person has read it.

## You need to…

| You need to… | Go to |
|---|---|
| Understand how to think and work in this space | [`AGENTS.md`](AGENTS.md) |
| Know how we think about a design | [`principles/`](principles/README.md) |
| Find a call we settled and should not argue again | [`rules/`](rules/README.md), in the file for its area |
| Explore a problem, scope a design for engineering or review one | [`process/`](process/README.md) |
| Choose colours, spacing, type, radii or motion | [`design-system/foundations/`](design-system/foundations/README.md) |
| Choose a component | [`design-system/components/`](design-system/components/README.md) |
| Find a repo or a design file, and how agents reach it | [`repos.md`](repos.md) |
| Start an exploration, or find one a teammate started | [`drafts/`](drafts/README.md) |
| Write the words on a screen | [`principles/writing-in-the-product.md`](principles/writing-in-the-product.md) |
| Record a correction about working here | [`lessons.md`](lessons.md) |
| Record a decision or a change | [`log.md`](log.md) |

## Structure

```
design/
├── README.md        # this front door
├── AGENTS.md        # how to think and behave here: the posture, and the rules that add to the root's
├── CLAUDE.md · GEMINI.md   # thin pointers so each agent loads AGENTS.md
├── SETUP.md         # present only while the design space is being set up
├── principles/      # how we think: philosophy, disclosure, page structure, layout, layering, type, words, naming
├── rules/           # the settled calls, one file per area, each dated with the reason for it
├── process/         # exploring a problem, scoping a design, reviewing one
├── design-system/   # foundations and components
├── drafts/          # one folder per exploration: who owns it, where it is, where it stands
├── repos.md         # the repos and design files the team works in, and how agents reach them
├── lessons.md       # what to do differently here
└── log.md           # what happened here
```

Add a folder when real work needs one, such as `design-system/patterns/` when the first pattern settles. Each new folder gets its own `README.md`.

## How the guidance fits together

Each kind of guidance has its own folder, from the most general to the most specific.

- **[`principles/`](principles/README.md)** — How we think about a design. Defaults, broken on purpose and with a reason
- **[`rules/`](rules/README.md)** — The settled calls, one file per area, each dated with the reason for it
- **[`process/`](process/README.md)** — How the work is done, from exploring a problem to a scope engineering builds from, and how a design is reviewed
- **[`design-system/`](design-system/README.md)** — What we build with: foundations and components, explained here and shipped from the repo

The guidance moves upward as it settles. A correction lands in this space's `lessons.md`. When it holds across more than one piece of work, it becomes a rule. When a rule has turned into a way of thinking, it moves into the principle it belongs to. Agents propose each move and a person approves it.

The code is the authority on what exists. These pages say why, when and what was decided. When a page and the code disagree, one of them changes on purpose and the log says which.

## How the learning moves between people

- **Work starts where the team designs.** An exploration is a design file or a branch in the real repo, tracked in [`drafts/`](drafts/README.md) by a `README.md` that says who owns it, what it is, where it is and where it stands.
- **What it teaches goes up.** A settled call becomes a rule in `rules/`. A correction goes into this space's `lessons.md`. Agents do this at the end of a session, so nobody has to remember to.
- **Everyone reads the same files.** Every agent reads the rules for the area it works in before it designs, so a rule settled by one designer holds in the next designer's work.
- **What repeats moves up a level.** When the same lesson appears more than once, an agent proposes a rule. When a rule has become a way of thinking, it proposes moving it into a principle.
- **Reviews are where the team meets the guidance.** A design is reviewed against the rules, and what the review settles is written back as a rule the same day.

## What lives elsewhere

| For… | Go to |
|---|---|
| A designer: who they are and how to work with them | [`people/`](../../people/README.md), like every teammate |
| The brand's look and voice | [`company/brand/`](../../company/brand/README.md) |
| What the company sells | [`company/products/`](../../company/products/README.md) |
| Design work with a start, an end and more than one person | [`projects/`](../../projects/README.md) |
| Production code | the repo, listed in [`repos.md`](repos.md), never this workspace |
| Design files, large images, video | the tool they are made in, linked from here |
| Tasks and issues | the task home named in [`company/tools.md`](../../company/tools.md) |

One fact, one home: read and link across the OS instead of copying.
