---
name: account
description: Create and manage customer/prospect accounts — the working memory that doesn't fit a CRM field. Account briefs, meeting logs, health reads, pre-call prep, and a roster of who's live. Use when the user wants to start tracking an account, log a meeting or call, prep for an upcoming conversation, update an account's health, or see where everything stands. Invokable as /account with a mode, or just by asking ("log my call with Acme", "prep me for the Globex check-in", "who's gone quiet?").
---

# Account

Manage the user's accounts — the companies they're actively engaged with as a
prospect, customer, or design partner. Everything lives under the `accounts/`
folder (one folder per account, plus an `accounts.md` roster and an
`approach.md` sales approach). If you can't find it at the project root, search
for an `accounts/` folder before asking the user where it is.

The skill has modes. Match the user's intent to one — the explicit form is
`/account <mode> <args>`, but infer the mode from natural language too.

Slugs are kebab-cased company names (`Acme Corp` → `acme-corp`). When a mode
takes a `<slug>` and the user gives a company name, resolve it against the
folders in `accounts/`; if it's ambiguous or missing, ask before creating
anything.

## new `<company>`

Create a new account folder at `accounts/<slug>/` with `README.md` and
`health.md` from `accounts/_template/`. Fill what you can:

- Pull company facts (domain, location, size, people) from context — see
  **Context** below — rather than asking for what you can already find.
- Ask only for what's missing and actually needed to make the brief useful:
  who owns it internally, current stage, and why there's a folder at all
  (what's the engagement?).
- Don't invent facts. Leave `[bracket placeholders]` for anything unknown —
  the brief is meant to be filled in over time.

Then add a row to `accounts/accounts.md` (company, stage, owner, last touch =
today, next step). Don't create `meetings/` or `shareables/` yet — they're
added when there's something to put in them.

## meeting `<slug>`

Log a conversation. Create `accounts/<slug>/meetings/YYYY-MM-DD-<topic>.md`
using the meeting format below. Ask for (or read from what the user pastes)
the attendees, meeting type, key points, and follow-ups.

After writing the meeting file:

- Lift concrete action items into the account `README.md` **Open threads**.
- Update **History** and the **Timeline** if something material happened.
- Refresh the account's row in `accounts.md` (last touch = meeting date, next
  step from the follow-ups).

Meeting file format:

```markdown
# {Title} — {Mon DD, YYYY}

> {2-3 sentence summary — scannable without reading the rest}

**Attendees:** {names with roles}
**Type:** {Discovery / Onboarding / Check-in / Deep dive / ...}

## Key points
- {detailed notes}

## Follow-ups
- [ ] {concrete action items}
```

## prep `<slug>`

Build a pre-call brief. Read the account `README.md`, the latest few files in
`meetings/`, `health.md`, and `accounts/approach.md`. Produce (in chat, not a
file unless asked):

- **Where we are** — stage, the relationship arc in 2-3 lines, open threads.
- **Who's on the call** — known people and their roles/relationship.
- **What they care about** — pulled from the brief, in their language.
- **Discovery questions** — 3-5, drawn from `approach.md`, tailored to this
  account's open questions and stage. Not a generic list.
- **Risks / watch-outs** — anything in `health.md` or open threads to handle.
- **Suggested next step** — a specific action to land, per the approach.

Ground the brief in `approach.md` so it reflects how *this* user sells, not a
generic template. If `approach.md` is missing or still has placeholders, say
so and prep from the account files alone.

## health `<slug>`

Refresh `accounts/<slug>/health.md`. Update the signal table (product usage,
communication, engagement) with today's date, set the status, and flag
anything that needs attention. If signals contradict the README's stage (e.g.
"Active" but communication has gone stale), note the mismatch and offer to
update the stage.

## list

Read `accounts/accounts.md` and show the roster grouped by stage (Lead →
Outreach → Engaged → Onboarding → Active → Paused → Churned). Surface anything
that looks stale — a past-due next step, or no touch in a while. If the user
asks something narrower ("who's gone quiet?", "what's in onboarding?"), filter
to that.

## Context

Make briefs accurate without interrogating the user:

- Read existing account files before asking — `README.md`, recent meetings,
  `health.md`.
- Look for company/product context in the project (a `CLAUDE.md`, positioning
  or strategy docs) to ground the account and your prep.
- If the Palette MCP is available, pull organization, people, and account
  context from it (the server describes how to use its tools when connected)
  rather than guessing.
- `accounts/approach.md` is the source of truth for *how* the user sells —
  use it for discovery questions, qualification, and next steps in `prep`.

## Guidelines

- The account `README.md` is the one file someone reads to understand the
  account. Keep it under ~120 lines and scannable — detail lives in meeting
  files. "About them" is a snapshot that gets replaced, not appended.
- Open threads is a working list — remove items when done, don't let it grow
  into a graveyard.
- Don't invent people, dates, or signals. A `[bracket placeholder]` is better
  than a confident guess.
- Only create a folder when there's real engagement. A name with no context
  doesn't need one — say so rather than scaffolding an empty shell.
