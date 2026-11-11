---
type: index
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
template: product@2611111
---

# Product

The product team's home for evidence and reasoning: what users say, the questions still open, the claims about how the product wins, and the specs that come out of them. Every conclusion here links back to the signal behind it.

**This space covers:** [one product, a product area, a platform or a portfolio, by name, with a link to its file in `company/products/`]. Setup fills in this line.

Company-wide rules live in the root [`AGENTS.md`](../../AGENTS.md) and always apply. How to think and behave *in this space* is in this folder's [`AGENTS.md`](AGENTS.md).

## Get started

While `SETUP.md` exists in this folder, the space is still being set up. Say "set up the product space" and tell the agent what you have: what the space covers, where feedback arrives, which tools hold the work, and where your existing research, specs and strategy are. A product name is enough to start.

The playbook is a first version, and says so in a box at its top. The box goes once someone on the team has read it.

## You need to…

| You need to… | Go to |
|---|---|
| Understand how to think and work in this space | [`AGENTS.md`](AGENTS.md) |
| Save what a user said, an interview or an explicit ask | Say "a customer just told me…" or "capture this feedback": [`processes/capture-feedback.md`](processes/capture-feedback.md) |
| Find the pattern across several pieces of feedback | Say "we keep hearing this": [`processes/synthesise-feedback.md`](processes/synthesise-feedback.md) |
| See the feedback by company, type, sentiment or tag | Open [`user-feedback/index.html`](user-feedback/index.html) |
| Bring the dashboard up to date | Say "rebuild the feedback dashboard": [`processes/rebuild-feedback-dashboard.md`](processes/rebuild-feedback-dashboard.md) |
| Share a sourced recap with a team, a customer or a stakeholder | Say "recap the feedback on [a company or a topic]": [`processes/share-feedback.md`](processes/share-feedback.md) |
| Frame a question nobody can answer yet | [`discovery/`](discovery/README.md) |
| Write down a claim about how the product wins | [`strategy/`](strategy/README.md) |
| Write a spec for one buildable piece of work | Say "write this up for engineering": [`processes/write-a-spec.md`](processes/write-a-spec.md) |
| Check the evidence before something is shared | Say "review this spec": [`processes/review-product-work.md`](processes/review-product-work.md) |
| Record what a teammate is pushing for, or a roadmap sync | [`team-input/`](team-input/README.md) |
| Know when feedback becomes a request or a painpoint | [`playbooks/feedback-synthesis.md`](playbooks/feedback-synthesis.md) |
| Capture how something is done here | Say "let me explain how we do this"; **Capturing how the work is done** below says where it goes |
| Record a correction about working here | [`lessons.md`](lessons.md) |
| Record a decision or a change | [`log.md`](log.md) |

## Structure

```
product/
├── README.md        # this front door
├── AGENTS.md        # how to think and behave here: the posture, and the rules that add to the root's
├── CLAUDE.md · GEMINI.md   # thin pointers so each agent loads AGENTS.md
├── SETUP.md         # present only while the product space is being set up
├── user-feedback/   # what users say: feedback, interviews, requests, painpoints, companies, recaps, the dashboard
├── discovery/       # open questions, each with a plan to learn the answer
├── strategy/        # durable claims about how the product wins
├── specs/           # briefs for one buildable piece of work, linked to their evidence
├── team-input/      # what each person is pushing for now, and the roadmap sync format
├── playbooks/       # how to think: how feedback is synthesised
├── processes/       # how things are done: capture, synthesise, rebuild, share, spec, review
├── lessons.md       # what to do differently here
└── log.md           # what happened here
```

Add a folder when real work needs one, such as a meetings folder with the first meeting note. Each new folder gets its own `README.md`.

## How signal moves

```text
raw feedback ──┬──> explicit ask ──> feature request ──┐
               │                                       │
interviews ────┴──> repeated problem ──> painpoint ─────┼──> discovery or spec
                                                       │
team input + competitor evidence ──────────────────────┴──> strategy
```

Not every quote becomes a painpoint, and not every painpoint becomes a feature. The links stay visible, so the team judges the evidence instead of trusting a summary. Competitor evidence comes from [`company/market/competitors/`](../../company/market/competitors/README.md).

## Capturing how the work is done

When someone explains, pastes or points at how something is done here, it becomes one file. One explanation often holds two of these (the thinking and the steps): split it into two files that link to each other.

| What you have | It is a | Goes in |
|---|---|---|
| A point of view: what matters, how to choose, what good looks like | playbook | `playbooks/<domain>.md` |
| Steps in an order, with a trigger and a finished state | process | `processes/<name>.md` |
| A format for an output this space makes again and again | format | the mold of the folder that output lives in; a new kind of output gets its own folder, with a `README.md` and a mold |
| Settled facts about the product, or its words | company page | [`company/products/`](../../company/products/README.md) or [`company/glossary.md`](../../company/glossary.md), linked from here |

Write the file from its folder's mold, in the words of the people who do the work, and add a row to that folder's `README.md`. Never add principles, steps or rules nobody gave you; a gap stays a gap, marked as an open question at the bottom of the file.

## What lives elsewhere

| For… | Go to |
|---|---|
| What the product is, who it is for and how it is described | [`company/products/`](../../company/products/README.md) |
| An internal word, a feature name or an abbreviation | [`company/glossary.md`](../../company/glossary.md) |
| A competitor or an alternative: what they ship, where they are ahead | [`company/market/competitors/`](../../company/market/competitors/README.md) |
| Who the company sells to | [`company/market/ideal-customer.md`](../../company/market/ideal-customer.md) |
| How to work with a teammate | [`people/`](../../people/README.md), like every teammate |
| A customer's brief and meeting notes | [`customers/`](../../customers/README.md) |
| Work with a start, an end and more than one person, such as a launch | [`projects/`](../../projects/README.md) |
| Tasks, issues, the roadmap and delivery dates | the tracker named in [`company/tools.md`](../../company/tools.md) |
| Where feedback arrives, and the product analytics | the tools named in [`company/tools.md`](../../company/tools.md) |

One fact, one home: read and link across the OS instead of copying.
