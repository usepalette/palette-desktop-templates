---
title: Design OS
summary: A design space for your workspace, with the team's principles, settled rules, process, design system and explorations in one folder.
category: design
order: 1
tags: [design, design-system, ui, ux, figma]
request: "Set up a design space for our team: we design in Figma and in code, the design system is in our app repo, and our design docs are in Notion."
type: space
folder: design
version: 2611091
author: Palette
license: MIT
updated: 2026-11-09
---

# Design OS

A design space for your workspace, with the team's principles, settled rules, process, design system and explorations in one folder.

Built for design teams that work with AI agents, so a call one designer settles holds in the next designer's work.

## What you get

- **Starter principles** for philosophy, progressive disclosure, page structure, layout, layering, typography, writing in the product, and naming. Your team changes them until they say what you believe.
- **Rules for settled calls**, one file per area: components, controls, spacing, surfaces, typography, icons, and motion. Each rule is dated with the reason for it, so it isn't argued again.
- **A design process** from exploring a problem to a scope engineering builds from, plus design reviews that write back what they settle.
- **Design system pages** for foundations and components, written from your code or design library. They say what each part is for and never copy token values, so they don't go out of date with what ships.
- **Shared drafts**, one folder per exploration with who owns it and where it stands, so agents build on a teammate's earlier work instead of starting over.
- **Lessons and a log for design.** Corrections land in the space's `lessons.md` and what happened in its `log.md`. What repeats is proposed as a rule, and a person approves it.

## The request

> Set up a design space for our team: we design in Figma and in code, the design system is in our app repo, and our design docs are in Notion.

Said in the person's own words. A repo alone is enough to start.

## What it reads

- **GitHub or a local folder** — the product and design system repos, for the foundations and components.
- **Figma** — the design files and the library, when the team designs in a design tool.
- **Notion or Google Docs** — the existing design docs, sorted into the space after a yes.

Without a design file, the space works from code. Without existing docs, the starter principles and process are the first version.

## What lands in the workspace

The space installs as `spaces/design/`. An earlier `spaces/design/` is replaced; Palette Desktop takes a checkpoint first, so you can undo.

```
spaces/design/
├── README.md        # the front door
├── AGENTS.md        # how to design here; adds to the root rules
├── CLAUDE.md · GEMINI.md   # pointers so each agent loads AGENTS.md
├── SETUP.md         # present only while the space is being set up
├── principles/      # how the team thinks about design
├── rules/           # the settled calls, one file per area
├── process/         # exploring, scoping and reviewing a design
├── design-system/   # foundations and components
├── drafts/          # one folder per exploration
├── repos.md         # the repos and design files, and how agents reach them
├── lessons.md       # what to do differently here
└── log.md           # what happened here
```

Nothing is placed outside `spaces/design/`.

## How setup works

After install, a session adds Design to your list of spaces and starts its setup. Tell it what you have:

- Whether you design in a design tool, in code, or both.
- Where your design system lives: a repo, a library, or a link.
- Where your product lives: a repo or a design file.
- Where your existing design docs are, if you have any.

The agent records where your team designs, checks it can reach your repos and design files, writes the design system pages from your code or library, and shows you where each existing doc would go before it writes anything. Pages it writes stay marked "Not confirmed yet" until someone on the team has read them.

## Part of your workspace

- Your workspace's rules still apply. The space's own `AGENTS.md` adds how to design, and agents read it whenever they work in the space.
- Designers use their profile in `people/`, like every teammate.
- The space links to your brand and products in `company/` instead of copying them.

## Design from the same guidance

Agents working on design read the space's rules for the area before they touch a UI.

- "Review this screen against our rules and principles."
- "We just settled that icons are always outlined. Add it as a rule."
- "Explore a new settings section from the problem up."
- "Break this design down into a scope for engineering."

Everything is plain markdown you can read and edit, with or without Palette.
