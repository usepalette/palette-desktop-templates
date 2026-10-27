---
type: index
---

# Design OS

The shared home of a design team that works with agents. It holds how the team thinks about design, the calls it has settled, how the work is done and what the design system is. Everything is plain markdown, so people and agents read the same files.

What one designer settles here is written down where the next one will read it. A call made in one person's exploration is a rule the same day, and every agent reads the rules before it touches a UI.

Agents read [`AGENTS.md`](AGENTS.md) first. This page is the map.

## Get started

Open this folder in Palette, or in any agent that reads `AGENTS.md`, and say:

> Set this up with me. We design in [Figma, code or both]. Our design system is in [repo, library or link], our product is in [repo or design file], and our existing design docs are in [link, folder or file].

Give whatever you have. A repo is enough to start. The agent follows [`SETUP.md`](SETUP.md) and goes through these in order.

- **You** — A folder in `people/` that says how you like to work
- **Where you design** — In a design tool, in code or both, written into [`AGENTS.md`](AGENTS.md) so every agent works the same way
- **Your repos and design files** — Listed in [`repos.md`](repos.md), with the access the agent needs to read them
- **Your design system** — The token groups and components, read from your code or library into [`design-system/`](design-system/README.md)
- **Your existing docs** — Sorted into principles, rules, the design system, process and code, shown to you before anything is written
- **The starter principles** — Read by your team and changed until they say what you believe

Each page you have not set up yet opens with a box saying so. The box tells the agent what to do with the page and goes once a person has read it.

## How the guidance fits together

Each kind of guidance has its own folder, from the most general to the most specific.

- **[`principles/`](principles/README.md)** — How we think about a design. Defaults, broken on purpose and with a reason
- **[`rules/`](rules/README.md)** — The settled calls, one file per area, each dated with the reason for it
- **[`process/`](process/README.md)** — How the work is done, from exploring a problem to a scope engineering builds from, and how a design is reviewed
- **[`design-system/`](design-system/README.md)** — What we build with: foundations and components, explained here and shipped from the repo

The guidance moves upward as it settles. A correction lands in the nearest `lessons.md`. When it holds across more than one piece of work, it becomes a rule. When a rule has turned into a way of thinking, it moves into the principle it belongs to. Agents propose each move and a person approves it.

The code is the authority on what exists. These pages say why, when and what was decided. When a page and the code disagree, one of them changes on purpose and the log says which.

## Structure

```
design-os/
├── SETUP.md             # how an agent sets this workspace up with you; deleted when setup is done
├── principles/          # how we think: philosophy, disclosure, page structure, layout, layering, type, words, naming
├── rules/               # the settled calls, one file per area, each ending in its checks
├── process/             # exploring a problem, scoping a design, reviewing one
├── design-system/       # foundations and components
├── people/              # one folder per designer, with their drafts
├── repos.md             # the repos and design files the team works in, and how agents reach them
├── README.md            # this map
├── AGENTS.md            # how agents work here (the source of truth)
├── CLAUDE.md · GEMINI.md · .vibe/   # thin pointers so each agent loads AGENTS.md
├── lessons.md           # what to do differently next time, team-wide
└── log.md               # what happened and what was decided, team-wide
```

Add a folder when real work needs one: `design-system/patterns/` when the first pattern settles, `projects/` when work outgrows one person's draft, `brand/` for how the team looks outside the product. Each new folder gets its own `README.md`.

## Where things live

| It is about… | It lives in |
|---|---|
| How we think about design | [`principles/`](principles/README.md) |
| A call we settled and should not argue again | [`rules/`](rules/README.md), in the file for its area |
| Exploring a new product, section or screen from the problem up | [`process/exploration.md`](process/exploration.md) |
| Breaking a design down for engineering | [`process/scope-documents.md`](process/scope-documents.md) |
| Reviewing a design against our guidance | [`process/reviews.md`](process/reviews.md) |
| Colours, spacing, type, radii, motion | [`design-system/foundations/`](design-system/foundations/README.md) |
| Which component to use, and when | [`design-system/components/`](design-system/components/README.md) |
| How a repo's code is written | that repo's own instruction files, noted in [`repos.md`](repos.md) |
| The words on a screen | [`principles/writing-in-the-product.md`](principles/writing-in-the-product.md) |
| A repo or a design file: where it is, what it holds | [`repos.md`](repos.md) |
| A designer and how to work with them | `people/<name>/README.md` |
| Something one designer is exploring | `people/<name>/drafts/<subject>/` |
| What to do differently, what happened | the nearest `lessons.md` and `log.md` |
| Production code | the repo, never this workspace |
| Design files, large images, video | the tool they are made in, linked from here |
| Tasks and issues | the team's tracker, linked from the draft that the work belongs to |

## How the learning moves between people

- **Work starts where the team designs.** An exploration is a design file or a branch in the real repo, tracked in its designer's `drafts/` folder by a `README.md` that says what it is, where it is and where it stands.
- **What it teaches goes up.** A settled call becomes a rule in `rules/`. A correction goes into the nearest `lessons.md`. Agents do this at the end of a session, so nobody has to remember to.
- **Everyone reads the same files.** Every agent reads the rules for the area it works in before it designs, so a rule settled by one designer holds in the next designer's work.
- **What repeats moves up a level.** When the same lesson appears in more than one place, an agent proposes a rule. When a rule has become a way of thinking, it proposes moving it into a principle.
- **Reviews are where the team meets the guidance.** A design is reviewed against the rules, and what the review settles is written back as a rule the same day.
