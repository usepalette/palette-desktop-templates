---
name: content
description: Create and manage written content — blog posts, LinkedIn posts, newsletters, pitches, copy. Drafts, voice checks against your brand, distribution plans, and a log of what you've shipped. Use when the user wants to start a piece, refine a draft, check copy against their voice, plan where content goes, log something they published, or list their content. Invokable as /content with a mode, or just by asking ("help me write a post about X", "does this sound like us?", "where should this go?").
---

# Content

Manage the user's written content — blog posts, LinkedIn/social posts,
newsletters, pitches, landing copy, changelogs. Everything lives under the
`content/` folder (drafts, a `content.md` log, a `voice.md` brand voice, and a
`playbook.md`). If you can't find it at the project root, search for a
`content/` folder before asking the user where it is.

The skill has modes. Match the user's intent to one — the explicit form is
`/content <mode> <args>`, but infer the mode from natural language too.

Slugs are kebab-cased titles (`Why we rebuilt onboarding` →
`why-we-rebuilt-onboarding`). When a mode takes a `<slug>` and the user gives a
title or topic, resolve it against the files in `content/drafts/`; if it's
ambiguous or missing, ask before creating anything.

## new `<topic>`

Create a new draft at `content/drafts/YYYY-MM-DD-<slug>.md` using the template
in `content/drafts/README.md`. Before writing:

- Ask for (or infer) the **target channel** — LinkedIn, blog, newsletter,
  pitch, etc. Format and length follow from it (see `content/playbook.md`).
- Pin down the **one takeaway** — the single thing the reader should leave
  with. If the user can't name it, help them find it before drafting prose.
- Match their voice (see **Voice & context** below).
- Pull in company/product context for examples and claims rather than
  inventing them.

Then add a row to `content/content.md` (date, title, channel, status = Draft).

## refine `<slug>`

Read the existing draft and tighten it against `content/playbook.md`:

- Lead with the insight or problem, not the backstory.
- One clear takeaway, surfaced early.
- Concrete examples over abstract claims; strong verbs over adjective piles.
- Cut, don't pad — aim to remove ~20% on the first pass.

Push back if the piece doesn't have a spine. A shorter piece that says one
thing well beats a longer one that says five things vaguely.

## voice-check `<slug>`

Read the draft and `content/voice.md`, then run the voice self-check against
the copy. Flag, with the specific line quoted:

- Hype, corporate-speak, or consulting-speak.
- Avoided words/phrases (check the list in `voice.md`).
- Vague claims without specifics; adjective-heavy writing.
- "Feature soup" — listing capabilities instead of workflows/outcomes.
- Anything that contradicts the brand's personality or positioning.

For each flag, quote the line in `voice.md` it violates and suggest a fix.
If `voice.md` is missing or still has placeholders, say so and check against
general principles instead.

## distribute `<slug>`

Read the draft and produce a distribution plan (in chat unless asked to save):

- **Primary channel** — where it lives.
- **Amplification** — communities, threads, Slack groups, partners to share in.
- **Repurpose** — what else this becomes (a blog post → 3 LinkedIn posts; a
  case study → a talk). Be specific about the spin-offs.

Pull the channel norms and cadence from `content/playbook.md`.

## log `<url?>`

Log a piece you've shipped. Ask for date, title, channel, and the link, then
update its row in `content/content.md` (status → Shipped, add the URL). If no
row exists yet, add one.

## list

Show everything from `content/content.md` plus any active drafts in
`content/drafts/`. Group by status (Draft / In review / Shipped). If the user
asks something narrower ("what's still in draft?", "what shipped this month?"),
filter to that.

## Voice & context

Content should sound like the user and fit the channel — a LinkedIn post, a
long-form blog, and a cold pitch each need a different register. Before
writing or refining prose:

- Read `content/voice.md` — the source of truth for tone, principles, and the
  words to use and avoid. Match it.
- Read `content/playbook.md` for how the team approaches content, channel
  norms, and distribution.
- Look for company/product context in the project (a `CLAUDE.md`, positioning
  or product docs) to ground claims and examples.
- If the Palette MCP is available, pull organization and personal context from
  it for background and voice rather than guessing.

## Guidelines

- One clear takeaway per piece. The reader should be able to say what the
  point was afterwards.
- Useful first, promotional second. If someone learns something even without
  buying, the piece did its job.
- Concrete beats abstract. Specific numbers, real examples, strong verbs.
- Don't invent stats, quotes, or customer names. If a number isn't sourced,
  cut it or flag it for the user to confirm.
- Distribution is half the job — a great piece nobody sees is a wasted piece.
