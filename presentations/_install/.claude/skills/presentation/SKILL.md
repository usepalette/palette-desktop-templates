---
name: presentation
description: Create and manage presentations of any kind — sales pitches, product reviews, team updates, conference talks, internal decks. Drafts, HTML slide decks, and a log of past presentations. Use when the user wants to start a new presentation, refine a draft, generate slides, log one they gave, or list their decks. Invokable as /presentation with a mode, or just by asking ("help me build a deck for X", "turn this draft into slides", "log the talk I gave at Y").
---

# Presentation

Manage the user's presentations — whatever the occasion: a sales pitch, a
product review, a team or all-hands update, a conference talk, an internal
deck. Everything lives under the `presentations/` folder (drafts, slide
decks, the log of past presentations). If you can't find it at the project
root, search for a `presentations/` folder before asking the user where it is.

The skill has modes. Match the user's intent to one — the explicit form is
`/presentation <mode> <args>`, but infer the mode from natural language too.

## new `<title>`

Create a new presentation draft at `presentations/drafts/YYYY-MM-DD-<slug>.md`
using the template in `presentations/drafts/README.md`. Ask for event name,
date, duration, and audience if not given. Pull in company/product context
(see **Context & voice** below) for relevant background.

## draft `<slug>`

Read the existing draft and help refine it — flesh out the outline, suggest
talking points, tighten the narrative. Match the user's voice (see **Context
& voice**). Push back if the flow doesn't hold together; a presentation that
doesn't have a spine is worse than a shorter one that does.

## slides `<slug>`

Read the draft markdown and generate an HTML deck at
`presentations/slides/<slug>.html`, based on `presentations/slides/template.html`.

- Follow the draft's outline closely.
- Keep slides minimal — few words per slide. Detail goes in the speaker
  notes (`data-notes="..."`), not on the slide.
- Use the `.big`, `.center`, `.highlight`, `.columns` classes where they fit.
- Check `presentations/snippets.md` for reusable slides (about me, about the
  company, the team, CTA) and drop them in where the draft calls for them.
- Fill the title slide's `PRESENTATION_TITLE`, `PRESENTER_NAME`, `EVENT_NAME`,
  and `EVENT_DATE` placeholders from the draft's frontmatter.

## log `<url?>`

Log a completed presentation. Ask for date, title, audience/event, and any
notes, then add a row to `presentations/presentations.md`.

## list

Show all presentations from `presentations/presentations.md` plus any active
drafts in `presentations/drafts/`.

## Context & voice

Presentations should sound like the user and fit the audience — a sales
prospect, an exec review, a team standup, and a conference crowd each need a
different register. Before writing draft prose or slide copy:

- Look for a voice/tone doc in the project (`voice.md`, `knowledge/voice.md`,
  a brand `voice.md`, or similar) and match it.
- Look for company/product context (a `CLAUDE.md`, a context or positioning
  doc, `presentations/snippets.md`) to ground claims and examples.
- If the Palette MCP is available, pull organization and personal context
  from it for background and voice rather than guessing.

## Guidelines

- Lead with one clear takeaway. Whether it's a pitch, a review, or a talk, the
  audience should be able to say what the point was afterwards.
- Fewer slides > more slides. One idea per slide.
- Short phrases and visuals on the slide; the substance is in what you *say*.
- Don't invent stats or quotes. If a number isn't sourced, cut it.
