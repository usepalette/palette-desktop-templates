---
type: index
owner: "[Owner]"
status: draft
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: everyone
---

# [Company] OS

> **Not filled in yet.** Say "help me get set up in this workspace" and it gets written with you.
>
> 1. This page is the map of the workspace, not a description of the company. It needs two things, and both come from `company/README.md`: the company's name, in the heading and in the tree, and the one-line description.
> 2. Write them here when a person has confirmed the company page, and delete this box in the same step: they confirmed both there.

**[One line: what the company does.]**

The shared, AI-readable home for how [Company] works and what is active. One folder of markdown that people and agents read the same way. Start with the company, one team or one project; this is always professional team work, with shared company and brand context.

This page is the map: what is where, and where a thing goes. New here? Open [`welcome.html`](welcome.html) to see how working here goes. Agents read [`AGENTS.md`](AGENTS.md) first; it holds the rules and points back to this page for the map.

## Structure

```
[company]-os/
├── company/          # who we are: the company on one page, brand, products, market, shared templates
├── people/           # one folder per person: how to work with them
├── spaces/           # one folder per area of work: go-to-market, product, design, content, operations, …
├── customers/        # one folder per customer, client or account: the brief and the meeting notes
├── projects/         # one folder per project: brief, milestones, decisions, meetings
│
├── README.md         # this map
├── welcome.html      # the page anyone new opens first: what this workspace is and how it works
├── AGENTS.md         # how agents behave here (the source of truth)
├── SETUP.md          # present only while setup is in progress
├── .agents/          # for agents: file conventions, and one page per command (add a person, log a meeting, check the workspace, …)
├── .claude/commands/ # pointers that make those commands show up in the command menu
├── CLAUDE.md · GEMINI.md · .vibe/   # thin pointers so each agent loads AGENTS.md
├── lessons.md        # what to do differently next time
└── log.md            # what happened, and what was decided
```

## How the folders fit together

- **`company/` is what everyone shares.** The company on one page, then one small file per topic: how we work, the tools, the glossary, the brand, the products, the market, and the formats everyone reuses. If the whole company needs it, it lives here.
- **A space is an area of work with its own rules and memory.** Turn one into whatever you need: go-to-market, product, design, content, operations. It can be a team's home, a discipline several people share, or a body of work; it doesn't have to be a team. Each space has its own front door, its own rules, its own lessons and its own log. If it belongs to one area of work, it lives in that space, and a space links to `company/` instead of copying from it.
- **`people/`, `customers/` and `projects/` cut across the spaces.** A person, a customer and a project each get one folder, whichever spaces they touch. There is no separate team folder: a team that needs a home gets a space.

Every content folder has a `README.md` explaining what belongs there. The root, top-level content folders, spaces and people also have `lessons.md` and `log.md`; deeper folders use the nearest existing pair. The root and every space carry an `AGENTS.md` as well, with thin pointer files beside it so each agent loads it. Collections of repeated items carry a `_template` to copy. Technical host folders are exceptions. Text in [brackets] marks unknowns or reusable slots, and a review box marks unfinished content; navigation and procedures work from day one.

## Where things live

One table, for finding a thing and for filing one. Nobody has to find the file themselves: say what you want, and it is filed by this table.

| It is about… | It lives in |
|---|---|
| What the company does, why, its stage and what it values | [`company/README.md`](company/README.md) |
| Rituals, channels, who decides what and who owns what | [`company/how-we-work.md`](company/how-we-work.md) |
| How meetings are noted, and where a meeting note goes | [`company/meetings.md`](company/meetings.md) |
| Which tool owns which fact, and where tasks live | [`company/tools.md`](company/tools.md) |
| An internal word | [`company/glossary.md`](company/glossary.md) |
| How the company sounds | [`company/brand/voice.md`](company/brand/voice.md) |
| The lines the company uses about itself | [`company/brand/messaging.md`](company/brand/messaging.md) |
| The logo, the colours, the look | [`company/brand/design.md`](company/brand/design.md) |
| What the company sells | [`company/products/`](company/products/README.md): one file per product |
| Who it sells to, and who it competes with | [`company/market/`](company/market/README.md) |
| A format the company reuses: a one-pager, a post, a customer story | [`company/templates/`](company/templates/README.md) |
| A person: who they are and how to work with them | `people/<name>/README.md`; the roster is in [`people/`](people/README.md) |
| How a person writes | `people/<name>/tone-of-voice.md` |
| A note someone keeps for themselves | `people/<name>/notes/`, made the first time it is needed |
| A draft or an experiment with no home yet | `people/<name>/scratchpad/` |
| An area of work, and how the work there is done | `spaces/<space>/`; the list is in [`spaces/`](spaces/README.md) |
| A customer, client or account | `customers/<name>/`; the list is in [`customers/`](customers/README.md) |
| A project | `projects/<name>/`; the list is in [`projects/`](projects/README.md) |
| What to do differently next time, and what happened or was decided | the nearest existing `lessons.md` and `log.md` for that work; company-wide ones in [`lessons.md`](lessons.md) and [`log.md`](log.md) |
| How working here goes, for anyone new | [`welcome.html`](welcome.html) |
| Tasks and issues | the tracker named in `company/tools.md`, or its one shared local fallback when no tracker is used |
| Images, video and other heavy files | not here: the drive or tool named in `company/tools.md` |
| Anything private or confidential: pay, health, contracts, personal matters | ask before saving: confirm the intended audience and an appropriately restricted destination; never assume a person's folder is private |
| Anything no row above covers: hiring, the office, finance, legal, … | a new page, folder or space of its own, proposed first. Until that is agreed, the person's `scratchpad/`. Never the root |

## Keep what you use

Every page says what belongs on it, and nothing in the workspace is sample content. Bring in what you already have (documents, a shared drive, what another AI tool knows about your work) and it gets filed where the table above says.

Optional collections can be removed when the team does not need them. Ask for the change so their listings, links and dependent procedures are updated together. Company and brand context stay useful even when the workspace begins with one team or project; missing required setup pages are a repair to make, not completed setup.

## How it stays healthy

Every meaningful session ends with a line in the right `lessons.md` or `log.md`. People, spaces, customers and projects are created from their `_template`, never from scratch. A workspace check finds broken links, stale listings and unconfirmed drafts; a reflect pass proposes how recurring lessons could become rules. Weekly checks are suggested, and are scheduled only on request. Scheduled checks report without making changes. The details are in [`AGENTS.md`](AGENTS.md).
