---
title: Content
summary: A content space for your workspace, with every piece from first draft to published link, written to your playbook and checked against your brand voice.
category: marketing
order: 6
tags: [content, writing, blog, linkedin, newsletter]
request: "Set up a content space for our team: we post on LinkedIn every week, write for our blog once a month, and send a newsletter from Substack."
type: space
folder: content
version: 2611111
author: Palette
license: MIT
updated: 2026-11-11
---

# Content

A content space for your workspace, with every piece from first draft to published link, written to your playbook and checked against your brand voice.

Built for teams that write with AI agents, so every piece says one useful thing, sounds like the company and claims only what the company can stand behind.

## What you get

- **Every piece in one list**, one file each, with its channel, where it stands and the link once it is out. Agents check the list before they write, so the same piece isn't written twice.
- **A content playbook** for how the team writes: one takeaway per piece, useful first and promotional second, concrete over abstract, and the length and cadence of each channel you use. Your team changes it until it says how you write.
- **A voice check** that reads a piece against your brand voice and quotes the line each flag breaks. A piece under someone's name also reads their own tone of voice.
- **Distribution planned with the piece:** where it lives, where it is shared and what else it becomes.
- **Five processes you start in plain words:** start a piece, refine it, check the voice, plan where it goes, and record it once it is published.
- **Lessons and a log for content.** Corrections land in the space's `lessons.md` and what happened in its `log.md`. What repeats is proposed for the playbook or the voice, and a person approves it.

## The request

> Set up a content space for our team: we post on LinkedIn every week, write for our blog once a month, and send a newsletter from Substack.

Said in the person's own words. One channel is enough to start.

## What it reads

- **Your company pages** — the voice, the messaging, the products and the ideal customer in `company/`, for how a piece sounds and what it can claim.
- **Your projects and customers** — the real work a piece is written from. A customer is named only with their approval.
- **LinkedIn, your blog and your newsletter** — the pieces already out, through a connector or a link, listed after a yes.
- **Notion or Google Docs** — drafts in progress, brought in after a yes.

Without a brand voice yet, setup offers to write it with you from pieces you were happy with. Without published pieces, the list starts empty.

## What lands in the workspace

The space installs as `spaces/content/`. An earlier `spaces/content/` is replaced; Palette Desktop takes a checkpoint first, so you can undo.

```
spaces/content/
├── README.md        # the front door
├── AGENTS.md        # how to write here; adds to the root rules
├── CLAUDE.md · GEMINI.md   # pointers so each agent loads AGENTS.md
├── SETUP.md         # present only while the space is being set up
├── pieces/          # one file per piece, and the list of every piece
├── playbooks/       # how the team thinks about content
├── processes/       # start, refine, check the voice, plan distribution, publish
├── lessons.md       # what to do differently here
└── log.md           # what happened here
```

Nothing is placed outside `spaces/content/`.

## How setup works

After install, a session adds Content to your list of spaces and starts its setup. Tell it what you have:

- The channels you write for, and how often.
- Where your pieces get published: the blog, the newsletter tool, the accounts.
- Two or three pieces you were happy with, if your brand voice isn't written yet.
- Drafts or published pieces to bring in.

The agent fills in your channels and cadence in the content playbook, records where you publish in `company/tools.md`, offers to write your brand voice with you while that page is empty, and shows you where each existing piece would go before it writes anything. The playbook stays marked "Not confirmed yet" until someone on the team has read it.

## Part of your workspace

- Your workspace's rules still apply. The space's own `AGENTS.md` adds how to write, and agents read it whenever they work in the space.
- The voice is your company's, in `company/brand/voice.md`, the same for every team. A piece under someone's name also reads their own tone of voice in `people/`.
- The space links to your messaging, products and ideal customer in `company/`, and uses its formats for a social post and a customer story, instead of copying them.
- With a GTM space in the workspace, launch pieces follow its launch formats.

## Write from the same voice

Agents read your voice and the playbook before they write a word, and nothing goes out without your yes.

- "Help me write a LinkedIn post about why we rebuilt onboarding."
- "Does this sound like us?"
- "Where should this go, and what else can it become?"
- "We published the onboarding post today. Here's the link."

Everything is plain markdown you can read and edit, with or without Palette.
