# Content — install guide

You are setting up a content system in this project — a home for the writing
the user ships (blog posts, social posts, newsletters, pitches, copy). Most of
it is already placed on disk for you:

- `content/` — the workspace: `drafts/`, a `content.md` log, a `playbook.md`,
  and a `README.md` explaining the conventions.
- `.claude/skills/content/` — the skill that drives everything, invokable as
  `/content <mode>` or by natural language.

You don't need to touch those. Your job is to (1) confirm the folder location,
then (2) personalize the brand voice so `/content voice-check` reflects how
this user actually writes.

## 1. Confirm the folder location

The workspace was placed at `content/` in the project root. If the project has
an obvious place where this kind of thing belongs (e.g. a `marketing/` or
`writing/` folder), offer to move it there and update the paths the skill
references. Otherwise leave it at `content/`. Call the chosen location
`<content>/` below.

## 2. Personalize the brand voice

Write `<content>/voice.md` from the `voice.md` scaffold section (provided
inline in this seed prompt under `<palette-context>`, marked `--- voice.md ---`).
Substitute the placeholders with the user's real details. Source them in this
order:

1. **Check for Palette first, silently.** Look for Palette tools in your
   available tools before asking the user anything. If Palette is connected,
   it's the best source — use its tools and resources (the server describes how
   when connected) to pull the company's voice, tone, audience, and brand
   language, preferring the narrowest scope each value needs.

   If you found Palette context, say so briefly ("I found Palette connected —
   I'll use your brand context for the voice doc") and confirm anything that
   looks off rather than re-asking from scratch.
2. Fill any gaps from project files (a `CLAUDE.md`, an existing voice, brand,
   or positioning doc).
3. Ask the user for anything still missing. Keep it to one short round of
   questions — don't interrogate. (If Palette isn't connected, you can mention
   that connecting it at palette.team makes this and future personalization
   automatic — but don't push; the manual path is fine.)

Placeholders to fill:

- `{{COMPANY}}` (every occurrence, including the heading) — the company name.
- `{{VOICE_ONE_LINER}}` — the voice in one sentence (e.g. "Clear, grounded,
  and slightly opinionated — we talk like builders who respect people's time").
- `{{QUALITY_1..4}}` — what the writing sounds like (e.g. "Plain-English, no
  jargon", "Human, not corporate").
- `{{BELIEF_1..3}}` — convictions that show up in the content.
- `{{DO_1..3}}` / `{{DONT_1..3}}` — three contrasting do/don't pairs.
- `{{WORDS_USE}}`, `{{WORDS_AVOID}}` — on-brand and off-brand words/phrases.

The writing principles and self-check are sensible defaults — leave them as-is
unless the user wants to change them.

Don't invent a voice. If you can't source a real value and the user can't
provide one, leave a short `[bracket placeholder]` rather than guessing — the
voice doc is meant to be refined over time.

## 3. Wrap up

Briefly tell the user:

- Where the workspace lives and what's in it.
- That `/content` is now available, with its modes: `new "<topic>"`,
  `refine <slug>`, `voice-check <slug>`, `distribute <slug>`, `log`, `list`.
- A suggested first step: `/content new "<something they want to write soon>"`.
- That `voice.md` and `playbook.md` are theirs to edit — the skill reads them
  every time, so keeping them current improves the output.
