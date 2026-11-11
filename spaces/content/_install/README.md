---
type: index
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
template: content@2611111
---

# Content

The writing the company ships, from the first draft to the link once it is out: blog posts, LinkedIn posts, newsletters, pitches and copy. Every piece starts from one takeaway and the company's own facts, sounds like the company, and has a plan for reaching people.

Company-wide rules live in the root [`AGENTS.md`](../../AGENTS.md) and always apply. How to think and behave *in this space* is in this folder's [`AGENTS.md`](AGENTS.md).

## Get started

While `SETUP.md` exists in this folder, the space is still being set up. Say "set up the content space" and tell the agent what you have: the channels you write for and how often, where your pieces get published, and two or three pieces you were happy with. One channel is enough to start.

Each page you have not set up yet opens with a box saying so. The box tells the agent what to do with the page and goes once a person has read it.

## You need to…

| You need to… | Go to |
|---|---|
| Understand how to think and work in this space | [`AGENTS.md`](AGENTS.md) |
| Write a piece: "help me write a LinkedIn post about…" | [`processes/start-a-piece.md`](processes/start-a-piece.md) |
| Tighten a draft: "tighten this draft", "this is too long" | [`processes/refine-a-piece.md`](processes/refine-a-piece.md) |
| Check a piece against the voice: "does this sound like us?" | [`processes/check-the-voice.md`](processes/check-the-voice.md) |
| Plan where a piece goes: "where should this go?" | [`processes/plan-distribution.md`](processes/plan-distribution.md) |
| Record a piece that went out: "we published this today" | [`processes/publish-a-piece.md`](processes/publish-a-piece.md) |
| See what is being written, and what went out where | [`pieces/`](pieces/README.md) |
| Know how we approach content, and the length and cadence of each channel | [`playbooks/content.md`](playbooks/content.md) |
| Know how the company sounds | [`company/brand/voice.md`](../../company/brand/voice.md) |
| Capture how something is done here | Say "let me explain how we do this"; **Capturing how the work is done** below says where it goes |
| Record a correction about working here | [`lessons.md`](lessons.md) |
| Record a decision or a change | [`log.md`](log.md) |

## Structure

```
content/
├── README.md        # this front door
├── AGENTS.md        # how to think and behave here: the posture, and the rules that add to the root's
├── CLAUDE.md · GEMINI.md   # thin pointers so each agent loads AGENTS.md
├── SETUP.md         # present only while the content space is being set up
├── pieces/          # one file per piece, and the list of every piece with its channel, status and link
├── playbooks/       # how we think about content, one file per domain
├── processes/       # start a piece, refine it, check the voice, plan distribution, publish
├── lessons.md       # what to do differently here
└── log.md           # what happened here
```

Add a folder when real work needs one, such as a folder of formats once the team has a format it fills in again and again (**Capturing how the work is done** below says how). Each new folder gets its own `README.md`.

## How a piece moves

1. **Start.** A piece starts from its channel and one takeaway, as a file in `pieces/` with `status: draft` and a row in the list.
2. **Refine.** It is tightened against the playbook: the takeaway early, concrete examples, a fifth cut.
3. **Check the voice.** It is read against the company's voice, and each flag quotes the line it breaks. When its author says it is ready for someone else to read, its status becomes `in-review`.
4. **Plan distribution.** Where it lives, where it is shared and what else it becomes.
5. **Publish.** Its status, date and link are set in the piece and in the list.

Each step is a process in [`processes/`](processes/README.md), and each one also runs on its own when someone asks. A piece can skip a step, but an agent never publishes or sends one without a yes.

## Capturing how the work is done

When someone explains, pastes or points at how something is done here, it becomes one file. One explanation often holds two of these (the thinking and the steps): split it into two files that link to each other.

| What you have | It is a | Goes in |
|---|---|---|
| A point of view: what matters, how to choose, what good looks like | playbook | `playbooks/<domain>.md` |
| Steps in an order, with a trigger and a finished state | process | `processes/<name>.md` |
| A format for a piece the team writes again and again, such as a newsletter issue | template | `templates/<output>.md`, in a folder made with its first file from Core's [`spaces/_template/templates/`](../_template/templates/README.md) |
| Settled facts to load before writing, such as a style sheet | foundation | `foundations/<topic>.md`, in a folder made the same way from [`spaces/_template/foundations/`](../_template/foundations/README.md) |

Write the file from that folder's mold, in the words of the people who do the work, and add a row to that folder's `README.md`. Never add principles, steps or rules nobody gave you; a gap stays a gap, marked as an open question at the bottom of the file. A format the whole company uses goes in [`company/templates/`](../../company/templates/README.md) instead.

## What lives elsewhere

| For… | Go to |
|---|---|
| How the company sounds, and how a person sounds for a piece under their name | [`company/brand/voice.md`](../../company/brand/voice.md), with that person's `people/<name>/tone-of-voice.md` on top of it |
| The lines the company uses about itself, and its proof points | [`company/brand/messaging.md`](../../company/brand/messaging.md) |
| What the company sells | [`company/products/`](../../company/products/README.md) |
| Who we write for | [`company/market/ideal-customer.md`](../../company/market/ideal-customer.md) |
| A format the whole company reuses: a social post, a customer story, a one-pager | [`company/templates/`](../../company/templates/README.md) |
| A campaign or a launch with a start and an end | [`projects/`](../../projects/README.md) |
| A customer, and their approval to be named | [`customers/`](../../customers/README.md) |
| Where pieces are published, and where images and video live | [`company/tools.md`](../../company/tools.md) |
| Tasks and issues | the task home named in [`company/tools.md`](../../company/tools.md) |
| Launch formats, when the workspace has a GTM space | `spaces/gtm/templates/launch/` |

One fact, one home: read and link across the OS instead of copying.
