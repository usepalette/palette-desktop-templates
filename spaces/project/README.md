---
title: Project
summary: How your team runs projects, with the steps to start one and record its decisions, the ways of working, and the formats for a brief, goals, scope and more.
category: team
also: [product]
order: 5
tags: [projects, delivery, clients, decisions]
request: "Set up a project space for how we run projects: we do client engagements and a few internal ones, our tasks are in Linear, and our briefs and statements of work are in Google Docs."
type: space
folder: project
contents:
  - folder: playbooks
    description: How the team works on a project, and how someone joins one
  - folder: processes
    description: Starting a project, recording a decision
  - folder: templates
    description: The formats a project's pages use, from the brief to the decision record
  - file: lessons.md
    description: What to do differently here
  - file: log.md
    description: What happened here
version: 2611111
license: MIT
updated: 2026-11-11
---

# Project

How your team runs projects, with the steps to start one and record its decisions, the ways of working, and the formats for a brief, goals, scope and more.

Built for teams that run projects with AI agents, for clients or for the company itself, so every project starts the same way and every decision keeps its reason.

## What you get

- **A way to start a project.** Each project gets its own folder in `projects/`, made the way your workspace makes every project. Then it gets the pages your team uses: a fuller brief, goals with metrics, a stakeholder map, a scope with a change log, and the phases.
- **Decisions with their reasons.** A real fork gets a numbered record with the context, the options and the consequences, and a dated line on the project's front page that links to it. A record is never rewritten: a change of mind is a new record.
- **Formats for the pages a project makes:** brief, goals, stakeholder map, scope, timeline, glossary, decision record, research interview, research findings and design links. Change a format once and every new project follows.
- **How your team works on a project:** the cadence, the channels, when people are available, how you decide and what done means, plus a page for bringing someone onto a project.
- **Rules agents follow on every project.** A meeting gets a note, a change of scope goes in the change log, and the project's **Now** line says where it stands this week.
- **Lessons and a log for how you run projects.** What a retro says you would do differently lands in the space's `lessons.md`, and what changed in how you work in its `log.md`.

## The request

> Set up a project space for how we run projects: we do client engagements and a few internal ones, our tasks are in Linear, and our briefs and statements of work are in Google Docs.

Said in the person's own words. Saying what kinds of projects you run is enough to start.

## What it reads

- **Your documents** — a statement of work, a proposal, a brief or kickoff notes, in Google Docs, Notion or a file, to draft a project's brief, goals and scope. You see where each piece would go before anything is written.
- **Your task tool** — Linear, Jira, Asana or the shared task list your workspace names, so each project links to its tasks. The tasks stay there.
- **Meeting notes and transcripts** — from your notetaker, or pasted, for the meeting notes and the decisions they settle.

Without documents, a project starts from what you tell the agent. A name and one line on what it is for are enough.

## What lands in the workspace

The space installs as `spaces/project/`. An earlier `spaces/project/` is replaced; Palette Desktop takes a checkpoint first, so you can undo.

```
spaces/project/
├── README.md        # the front door
├── AGENTS.md        # how to run a project here; adds to the root rules
├── CLAUDE.md · GEMINI.md   # pointers so each agent loads AGENTS.md
├── SETUP.md         # present only while the space is being set up
├── playbooks/       # how the team works on a project, and how someone joins one
├── processes/       # starting a project, recording a decision
├── templates/       # the formats a project's pages use, from the brief to the decision record
├── lessons.md       # what to do differently here
└── log.md           # what happened here
```

Nothing is placed outside `spaces/project/`.

The projects themselves live in `projects/`, one folder each, as in every workspace. The space holds how they are run: starting a project with it adds the pages your team uses and marks the project as one this space runs.

## How setup works

After install, a session adds Project to your list of spaces and starts its setup. Tell it what you have:

- Whether you run client engagements, internal projects or both.
- Which pages a new project gets beyond its front page: the brief, the goals, a stakeholder map, the scope, the phases.
- Who sits on the other side of your projects: a customer's people, a sponsor inside the company, partners.
- Where your tasks live.

The agent writes your answers where the space reads them and offers to start your first project. It also points the rows for starting a project and recording a decision in `projects/README.md` at the space, so a project started from there gets your team's pages. The two playbooks stay marked "Not filled in yet" until your team says how it works; nothing about how you work is made up.

## Part of your workspace

- Your workspace's rules still apply. The space's own `AGENTS.md` adds how to run a project, and agents read it whenever they work in the space.
- Each project lives in `projects/`, never in the space, and is closed the way your workspace closes every project, with a retro.
- Teammates stay in `people/`, customers and their people in `customers/`, and tasks in your task tool. The space links to them instead of copying.
- For one page with every project's status, add the **Projects overview** template. It reads `projects/` and never changes it.

## Run every project the same way

Agents working on a project read its front page and the space's rules before they change anything.

- "We're starting a new client project. Here's the statement of work."
- "We decided to move the launch by two weeks. Record it with the reason."
- "The customer added a second market to the scope. Update the scope and its change log."
- "Someone new joins the project on Monday. What should they read first?"

Everything is plain markdown you can read and edit, with or without Palette.
