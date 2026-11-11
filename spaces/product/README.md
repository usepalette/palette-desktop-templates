---
title: Product
summary: A product space for your workspace, with what users say, the open questions, the strategy and the specs in one folder, each linked to its evidence.
category: product
order: 6
tags: [product, user-feedback, discovery, strategy, specs]
request: "Set up a product space for our team: feedback comes in through Intercom and our feedback channel in Slack, we track the work in Linear, and our research and specs are in Notion."
type: space
folder: product
version: 2611111
author: Palette
license: MIT
updated: 2026-11-11
---

# Product

A product space for your workspace, with what users say, the open questions, the strategy and the specs in one folder, each linked to its evidence.

Built for product teams that work with AI agents, from one person to a cross-functional team, so a claim in a spec can be traced back to what users actually said.

## What you get

- **A home for what users say.** Raw feedback, interviews, explicit requests and recurring painpoints, each linked to its source and its company, so the evidence doesn't become a pile of quotes.
- **A path from signal to decision.** Discovery questions, strategy theses and specs each have a clear job, and each one traces back to the evidence behind it.
- **A feedback dashboard.** One self-contained page that filters the signal by company, type, sentiment and tag. The markdown stays the source of truth, and the page is rebuilt from it.
- **Processes for the recurring work.** Capture feedback, find the pattern, share a sourced recap, write a spec and review the evidence, each started by saying what you need. A playbook says when a comment becomes a painpoint and how to score it.
- **Team input.** What each person is pushing for now, linked to their profile, and a format for roadmap syncs.
- **Lessons and a log for product.** Corrections land in the space's `lessons.md` and what happened in its `log.md`, so the next session starts from them.

## The request

> Set up a product space for our team: feedback comes in through Intercom and our feedback channel in Slack, we track the work in Linear, and our research and specs are in Notion.

Said in the person's own words. A product name is enough to start.

## What it reads

- **Slack or a support tool** — the channels and the inbox where feedback arrives, when the agent can reach them. Each piece is saved with its source.
- **Notion or Google Docs** — existing research, interview notes, specs and strategy, sorted into the space after a yes.
- **Linear or Jira** — the tracker your specs link to. The roadmap, the tasks and their status stay there.
- **Your product analytics** — when a claim needs what users actually do as evidence.

Without a connected tool, feedback is captured from what you paste or tell the agent. Without existing documents, the first piece of feedback you pass on starts the space.

## What lands in the workspace

The space installs as `spaces/product/`. An earlier `spaces/product/` is replaced; Palette Desktop takes a checkpoint first, so you can undo.

```
spaces/product/
├── README.md        # the front door
├── AGENTS.md        # how to do product work here; adds to the root rules
├── CLAUDE.md · GEMINI.md   # pointers so each agent loads AGENTS.md
├── SETUP.md         # present only while the space is being set up
├── user-feedback/   # feedback, interviews, requests, painpoints, companies, recaps and the dashboard
├── discovery/       # open questions, each with a plan to learn the answer
├── strategy/        # durable claims about how the product wins
├── specs/           # briefs for one buildable piece of work
├── team-input/      # what each person is pushing for, and the roadmap sync format
├── playbooks/       # how feedback is synthesised
├── processes/       # capture, synthesise, rebuild the dashboard, share, write a spec, review
├── lessons.md       # what to do differently here
└── log.md           # what happened here
```

Nothing is placed outside `spaces/product/`.

## How setup works

After install, a session adds Product to your list of spaces and starts its setup. Tell it what you have:

- What the space covers: one product, a product area, a platform or a portfolio.
- Where feedback arrives today, or that you capture it by hand.
- Which tools hold the work: a tracker, analytics, a support or research tool. None is required.
- Where your existing research, specs and strategy are, if you have any.

The agent records your tools on the workspace's tools page, offers to describe the product on your products page and to start the glossary while they are still empty, and shows you where each existing document would go before it writes anything. Pages it writes stay marked "Not confirmed yet" until someone on the team has read them.

## Part of your workspace

- Your workspace's rules still apply. The space's own `AGENTS.md` adds how to do product work, and agents read it whenever they work in the space.
- Product people use their profile in `people/`, like every teammate. What each of them is pushing for now goes in the space's `team-input/`.
- The space links to your products, glossary, competitors and tools in `company/` instead of copying them. A company that sends feedback and is also a customer links to its brief in `customers/`.
- Tasks, the roadmap and delivery dates stay in your tracker. The space holds the evidence and the reasoning behind them.

## Decide from the same evidence

Agents working on product read the evidence before they draw a conclusion.

- "A customer just told me exports keep timing out. Capture it."
- "What are customers repeatedly saying about onboarding, and what supports it?"
- "Write a spec for bulk export, grounded in the feedback and the strategy."
- "Review this spec before I share it."

Everything is plain markdown you can read and edit, with or without Palette.
