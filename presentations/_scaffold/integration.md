# Presentations — install guide

You are setting up a presentation system in this project — it works for any
kind of deck (sales pitch, product review, team update, conference talk).
Most of it is already placed on disk for you:

- `presentations/` — the workspace: `drafts/`, `slides/` (with a polished,
  self-contained `template.html`), and a `presentations.md` log of past
  presentations.
- `.claude/skills/presentation/` — the skill that drives everything,
  invokable as `/presentation <mode>` or by natural language.

You don't need to touch those. Your job is to (1) confirm the folder
location, then (2) personalize the reusable slide snippets so the user's
intro, company, and team slides are ready to drop into any deck.

## 1. Confirm the folder location

The workspace was placed at `presentations/` in the project root. If the
project has an obvious place where this kind of thing belongs (e.g. a
`workflows/` or `content/` folder), offer to move it there and update the
paths the skill references. Otherwise leave it at `presentations/`. Call the
chosen location `<presentations>/` below.

## 2. Personalize the slide snippets

Write `<presentations>/snippets.md` from the `snippets.md` scaffold section
(provided inline in this seed prompt under `<palette-context>`, marked
`--- snippets.md ---`). Substitute the placeholders with the user's real
details. Source them in this order:

1. If the Palette MCP is available, pull organization and personal context
   from it — company name, tagline, what it does, the team, the user's role.
2. Fill any gaps from project files (a `CLAUDE.md`, a positioning/voice doc).
3. Ask the user for anything still missing. Keep it to one short round of
   questions — don't interrogate.

Placeholders to fill:

- `{{PRESENTER_NAME}}`, `{{PRESENTER_ROLE}}`, `{{PRESENTER_BACKGROUND}}`,
  `{{PRESENTER_FOCUS}}` — the "About me" slide.
- `{{COMPANY}}` (every occurrence, including the heading), `{{COMPANY_TAGLINE}}`,
  `{{COMPANY_POINT_1..3}}` — the company slide.
- `{{TEAM_COLUMN_1}}`, `{{TEAM_COLUMN_2}}` — two balanced columns of
  `<li><span class="highlight">Name</span> — role</li>` items. If you don't
  have a real team, drop the team snippet entirely rather than inventing one.
- `{{CONTACT_LINE}}` — the closing CTA (email · social handle, etc.).

Don't invent facts. If you can't source a real value and the user can't
provide one, leave a short `[bracket placeholder]` rather than guessing —
the snippets are meant to be edited over time anyway.

## 3. Wrap up

Briefly tell the user:

- Where the workspace lives and what's in it.
- That `/presentation` is now available, with its modes: `new <title>`,
  `draft <slug>`, `slides <slug>`, `log`, `list`.
- A suggested first step: `/presentation new "<a deck they need soon>"`.
- That `snippets.md` holds their reusable intro/company/team/CTA slides and
  is theirs to edit.
