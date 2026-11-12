---
title: GTM
summary: A go-to-market space for your workspace, with your strategy, your sales story, the playbooks for selling, content and launches, and a launch kit in one folder.
category: marketing
also: [sales]
order: 5
tags: [gtm, sales, marketing, launch, playbooks]
request: "Set up a go-to-market space for us: our positioning doc and sales deck are in Google Drive, our sales calls are recorded in Gong, and we launch on the blog, on LinkedIn and in our Slack community."
type: space
folder: gtm
contents:
  - folder: foundations
    description: The GTM strategy and the sales story
  - folder: playbooks
    description: How the team sells, writes and launches
  - folder: processes
    description: Reviewing GTM work before it is shared
  - folder: templates
    description: "The launch kit: the messaging brief and a format for each piece"
  - folder: research
    description: Market research, discovery and competitive deep dives
  - file: lessons.md
    description: What to do differently here
  - file: log.md
    description: What happened here
version: 2611111
license: MIT
updated: 2026-11-11
---

# GTM

A go-to-market space for your workspace, with your strategy, your sales story, the playbooks for selling, content and launches, and a launch kit in one folder.

Built for founders and commercial teams that work with AI agents, so the story one person settles is the story every call, post and launch tells.

## What you get

- **A strategy and a sales story.** How you go to market: the motion, the channels, the phase you are in and your bets. Then the story you tell in a sales call, with its discovery questions and objections. Setup fills them in with you.
- **Playbooks for selling, content and launches**, a starter point of view your team changes until it says how you work: discovery before the demo, one idea per piece, and launch tiers that match the effort to what shipped.
- **A launch kit**: a messaging brief agreed before anything is written, then a format for each piece, from the changelog entry and the community post to the landing page and the video script. Each one says how to write it.
- **A review before work goes out**, against your voice, your messaging and your strategy. It names the line a piece breaks and the page that says so.
- **Research in one place**, dated, so the next campaign starts from what the team already knows.
- **Lessons and a log for GTM.** Corrections land in the space's `lessons.md` and what happened in its `log.md`. What repeats is proposed for a playbook, and a person approves it.

## The request

> Set up a go-to-market space for us: our positioning doc and sales deck are in Google Drive, our sales calls are recorded in Gong, and we launch on the blog, on LinkedIn and in our Slack community.

Said in the person's own words. A sales deck alone is enough to start.

## What it reads

- **Google Drive, Notion or Google Docs**: the positioning doc, the sales deck, the strategy and past launch posts, sorted into the workspace after a yes.
- **Your website**: the lines the company already uses about itself, for the voice and messaging pages while they are empty.
- **Gong, Granola or your call notes**: the problem in your customers' own words, for the sales story.
- **Linear, Jira or GitHub**: what shipped, for a launch's messaging brief.

Every source is optional. Without documents, one round of questions fills in the strategy and the sales story, and the starter playbooks and launch kit are the first version.

## What lands in the workspace

The space installs as `spaces/gtm/`. An earlier `spaces/gtm/` is replaced; Palette Desktop takes a checkpoint first, so you can undo.

```
spaces/gtm/
├── README.md        # the front door
├── AGENTS.md        # how to do go-to-market work here; adds to the root rules
├── CLAUDE.md · GEMINI.md   # pointers so each agent loads AGENTS.md
├── SETUP.md         # present only while the space is being set up
├── foundations/     # the GTM strategy and the sales story
├── playbooks/       # how the team sells, writes and launches
├── processes/       # reviewing GTM work before it is shared
├── templates/       # the launch kit: the messaging brief and a format for each piece
├── research/        # market research, discovery and competitive deep dives
├── lessons.md       # what to do differently here
└── log.md           # what happened here
```

Nothing is placed outside `spaces/gtm/`.

## How setup works

After install, a session adds GTM to your list of spaces and starts its setup. Tell it what you have:

- How you sell today: founder-led, inbound, outbound or through the product.
- The channels you use, such as LinkedIn, events, a newsletter or a community.
- Your sales deck or pitch, for the sales story.
- Where your existing GTM docs are, if you have any: positioning, strategy, past launches.

The agent writes the strategy and the sales story from what you give it, offers to fill in your voice, messaging and ideal customer while those pages are still empty, and shows you where each existing doc would go before it writes anything. Pages it writes stay marked "Not confirmed yet" until someone on the team has read them.

## Part of your workspace

- Your workspace's rules still apply. The space's own `AGENTS.md` adds how to do go-to-market work, and agents read it whenever they work in the space.
- Your voice, messaging, ideal customer, competitors and products stay in `company/`. The space reads them instead of copying them.
- Customers live in `customers/`, campaigns and launches in `projects/`, and the people who sell and write in `people/`, with how each of them writes.
- With a Content or an Accounts space in the workspace, setup asks which one keeps the content or the sales playbook, so your team has one of each.

## Go to market from the same story

Agents working on GTM read your strategy, the playbook for the work and your brand pages before they write a word.

- "Prepare me for tomorrow's call with this customer, from their brief and our sales playbook."
- "We ship the new integration next week. Which tier is it, and which pieces do we need?"
- "Write the messaging brief for this launch from the pull request and what customers asked for."
- "Review this blog post against our voice and messaging before it goes out."

Everything is plain markdown you can read and edit, with or without Palette.
