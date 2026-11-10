---
type: index
owner: "[Owner]"
status: draft
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
read_when:
  - "You're starting a session"
  - "You're writing anything in the company's name"
---

# [Company]

> **Not filled in yet.** Say "help me fill in the company page" and it gets written with you.
>
> 1. Take it from the about page of the website, a pitch deck, or what the person tells you. Ask what the company does, for whom, and which values it actually uses when it decides something. Keep it to one page: it is read at the start of every session.
> 2. Write only what you are given. End a line you worked out yourself with "(to confirm)", and leave a slot you have nothing for in its brackets.
> 3. For drafted or inferred content, keep this box and change its first line to "**Not confirmed yet.**" Directly supplied facts need no second approval; use the root page-state procedure.
> 4. Delete this box when the page holds only what a person stated themselves, or when a person confirms it, alone or in a clearly named batch they have reviewed. Then set `status: active`. Follow `.agents/page-states.md` at the workspace root; preserve the owner, and leave brackets for what nobody knows yet.

## What we do

[Two or three sentences: what the company makes or does, for whom, and what makes it different.]

- **Stage and size:** [stage, number of people, where the team is based]
- **Working language:** [the language the pages in this workspace are written in]

## Why we exist

[One or two sentences: the mission, and where the company is heading.]

## Values

- [A value, and what it means in how we work]
- [A value, and what it means in how we work]
- [A value, and what it means in how we work]

## The rest of this folder

Everything else about the company lives in small files next to this page, one topic each. Open the one the task needs; don't load them all.

| When you… | Read |
|---|---|
| Need the rituals, the channels, who decides what, or who owns what | [`how-we-work.md`](how-we-work.md) |
| Log a meeting, or need to know how meetings are noted | [`meetings.md`](meetings.md) |
| Need to know which tool owns a fact, or where tasks live | [`tools.md`](tools.md) |
| Meet an internal word you don't know | [`glossary.md`](glossary.md) |
| Write anything that leaves the company | [`brand/voice.md`](brand/voice.md) and [`brand/messaging.md`](brand/messaging.md) |
| Make anything a person will look at | [`brand/design.md`](brand/design.md) |
| Describe, explain or sell a product or service | [`products/`](products/README.md) |
| Need to know who we sell to, or how we compare with an alternative | [`market/`](market/README.md) |
| Produce an output the company has a format for | [`templates/`](templates/README.md) |

```
company/
├── README.md         # this page: the company on one page
├── how-we-work.md    # rituals, channels, decisions, areas and owners
├── meetings.md       # how meetings are noted, and where a note goes
├── tools.md          # which tool owns which fact
├── glossary.md       # internal words
├── brand/            # how we sound, what we say, how we look
├── products/         # one file per product or service
├── market/           # who we sell to, and who we are up against
└── templates/        # the formats the whole company reuses
```

## Adding to this folder

- **One topic, one file.** When something about the company doesn't fit an existing file, it gets its own file here, named for its subject (`pricing.md`, `strategy.md`, `partners.md`), and a row in the table above. Give it the same style as the pages next to it: a box at the top, and a bracket in every slot that says what goes there.
- **Everyone's context, not one area's.** If the whole company needs it, it belongs here. If it belongs to one area of work (go-to-market, product, design, content, …), it lives in that area's space under [`spaces/`](../spaces/README.md), which links here instead of copying.
- **Its own lessons and log.** Corrections about how the company describes itself go in [`lessons.md`](lessons.md), and changes to what it says about itself go in [`log.md`](log.md). What applies across the whole workspace goes in the root pair.
- **Delete what you don't use.** A company with no competitors to track, or no shared formats yet, removes that folder: ask for it, so its rows, links and the steps that depend on it are updated in the same change (`.agents/conventions.md` → Changing structure, at the workspace root).
