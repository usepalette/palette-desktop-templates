---
type: index
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
template: gtm@2611111
---

# GTM

The go-to-market team's home: the strategy, the story the team tells, how it sells, writes and launches, and the formats for launch content. What one person settles about the story is written down where the next call, post and launch will read it.

Company-wide rules live in the root [`AGENTS.md`](../../AGENTS.md) and always apply. How to think and behave *in this space* is in this folder's [`AGENTS.md`](AGENTS.md).

## Get started

While `SETUP.md` exists in this folder, the space is still being set up. Say "set up the GTM space" and tell the agent what you have: how you sell today, the channels you use, your sales deck or pitch, and anything else you already have written down, such as a positioning doc, a strategy or past launch posts. A sales deck is enough to start.

Each page you have not set up yet opens with a box saying so. The box tells the agent what to do with the page and goes once a person has read it.

## You need to…

| You need to… | Go to |
|---|---|
| Understand how to think and work in this space | [`AGENTS.md`](AGENTS.md) |
| Know how we go to market: the motion, the channels, the phase, the bets | [`foundations/gtm-strategy.md`](foundations/gtm-strategy.md) |
| Tell the story in a sales call, a deck or a pitch | [`foundations/sales-narrative.md`](foundations/sales-narrative.md) |
| Prepare for a sales call, or follow one up | [`playbooks/sales.md`](playbooks/sales.md), then the customer's brief in [`customers/`](../../customers/README.md) |
| Write a post, an article or a newsletter | [`playbooks/content.md`](playbooks/content.md) |
| Plan a launch: its tier, its messaging and its pieces | [`playbooks/launch.md`](playbooks/launch.md), then [`templates/launch/`](templates/launch/README.md) |
| Make a launch piece: the brief, the changelog, a post, the landing page | [`templates/launch/`](templates/launch/README.md) |
| Check work against the brand, the messaging and the strategy before it is shared | Say "review this before I share it"; the steps are in [`processes/review-gtm-work.md`](processes/review-gtm-work.md) |
| Keep or find research: the market, discovery, a competitive deep dive | [`research/`](research/README.md) |
| Run a campaign or a launch with a start and an end | Say "we're starting a new project"; it lives in [`projects/`](../../projects/README.md) with `space: gtm` in its frontmatter |
| Add a customer or an account | Say "we just signed a new customer"; it lives in [`customers/`](../../customers/README.md) |
| Capture how something is done here | Say "let me explain how we do this"; **Capturing how the work is done** below says where it goes |
| Record a correction about working here | [`lessons.md`](lessons.md) |
| Record a decision or a change | [`log.md`](log.md) |

## Structure

```
gtm/
├── README.md        # this front door
├── AGENTS.md        # how to think and behave here: the posture, and the rules that add to the root's
├── CLAUDE.md · GEMINI.md   # thin pointers so each agent loads AGENTS.md
├── SETUP.md         # present only while the GTM space is being set up
├── foundations/     # what is known here: the GTM strategy and the sales story
├── playbooks/       # how to think: selling, content, launches
├── processes/       # how things are done: reviewing GTM work before it is shared
├── templates/       # the fill-in formats: the launch kit
├── research/        # what the team has found out, one dated file each
├── lessons.md       # what to do differently here
└── log.md           # what happened here
```

This is a starting shape. Add subfolders as real work arrives (a meetings folder with the first meeting note, for example), each with its own `README.md`, and remove the ones this space doesn't need. Don't create empty stubs to fill the tree.

## How the work fits together

- **[`foundations/`](foundations/README.md)**: what the team knows about how it goes to market. Loaded before producing anything
- **[`playbooks/`](playbooks/README.md)**: how the team thinks about selling, content and launches
- **[`templates/`](templates/README.md)**: the formats a piece is made from, starting with the launch kit
- **[`processes/`](processes/README.md)**: what is done step by step, such as the review before work is shared
- **[`research/`](research/README.md)**: what the team has found out, dated

A piece of work reads them in that order: the foundations and the company's brand pages, then the playbook to decide, then the format to produce, then the review before it goes out. The work itself lives where the root map says: a campaign or a launch is a project, a customer has its own folder, and a piece of content is written in the Content space when the workspace has one.

What the work teaches comes back here. A better way of thinking goes into its playbook, a format made twice becomes a template, a finding goes into research, a correction into [`lessons.md`](lessons.md), and what happened into [`log.md`](log.md). Agents propose each change and a person approves it.

## Capturing how the work is done

When someone explains, pastes or points at how something is done here, it becomes one file in one of these folders. One explanation often holds two of them (the thinking and the steps): split it into two files that link to each other.

| What you have | It is a | Goes in |
|---|---|---|
| Settled facts to load before working | foundation | `foundations/<topic>.md` |
| A point of view: what matters, how to choose, what good looks like | playbook | `playbooks/<domain>.md` |
| Steps in an order, with a trigger and a finished state | process | `processes/<name>.md` |
| A format to fill in for a recurring output | template | `templates/<output>.md` |
| Something the team found out | research | `research/YYYY-MM-DD-<topic>.md` |

Write the file from the mold in that folder (for research, follow **Add research** in [`research/README.md`](research/README.md)), in the words of the people who do the work, and add a row to that folder's `README.md`. Never add principles, steps or rules nobody gave you; a gap stays a gap, marked as an open question at the bottom of the file.

## What lives elsewhere

| For… | Go to |
|---|---|
| How the company sounds | [`company/brand/voice.md`](../../company/brand/voice.md) |
| What it says about itself: the positioning, the tagline, the proof points | [`company/brand/messaging.md`](../../company/brand/messaging.md) |
| How it looks, for anything visual | [`company/brand/design.md`](../../company/brand/design.md) |
| Who it sells to | [`company/market/ideal-customer.md`](../../company/market/ideal-customer.md) |
| Who it competes with | [`company/market/competitors/`](../../company/market/competitors/README.md) |
| What it sells | [`company/products/`](../../company/products/README.md) |
| A format the whole company uses: a one-pager, a social post, a customer story | [`company/templates/`](../../company/templates/README.md) |
| A customer or an account: the brief and the meeting notes | [`customers/`](../../customers/README.md) |
| A campaign or a launch | [`projects/`](../../projects/README.md), with `space: gtm` in the project's frontmatter |
| A piece of content: a post, an article, a changelog entry | the Content space when the workspace has one (`spaces/content/`); otherwise the project it belongs to, or the person's scratchpad until it has a home |
| A teammate, and how they write | [`people/`](../../people/README.md): their profile, and `people/<name>/tone-of-voice.md` |
| Which tool owns the pipeline, and where tasks live | [`company/tools.md`](../../company/tools.md) |

One fact, one home: read and link across the OS instead of copying.
