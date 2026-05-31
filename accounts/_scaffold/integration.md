# Accounts — install guide

You are setting up an account system in this project — working memory for the
companies the user is engaged with (prospects, customers, design partners).
Most of it is already placed on disk for you:

- `accounts/` — the workspace: an `accounts.md` roster, a `_template/` an
  account starts from (`README.md` + `health.md`), and a `README.md`
  explaining the conventions.
- `.claude/skills/account/` — the skill that drives everything, invokable as
  `/account <mode>` or by natural language.

You don't need to touch those. Your job is to (1) confirm the folder
location, then (2) personalize the sales approach so `/account prep` produces
briefs that sound like this user.

## 1. Confirm the folder location

The workspace was placed at `accounts/` in the project root. If the project
has an obvious place where this kind of thing belongs (e.g. a `gtm/`,
`sales/`, or `crm/` folder), offer to move it there and update the paths the
skill references. Otherwise leave it at `accounts/`. Call the chosen location
`<accounts>/` below.

## 2. Personalize the sales approach

Write `<accounts>/approach.md` from the `approach.md` scaffold section
(provided inline in this seed prompt under `<palette-context>`, marked
`--- approach.md ---`). Substitute the placeholders with the user's real
details. Source them in this order:

1. **Check for Palette first, silently.** Look for Palette tools in your
   available tools before asking the user anything. If Palette is connected,
   it's the best source — use its tools and resources (the server describes
   how when connected) to pull company, product, and ICP context, preferring
   the narrowest scope each value needs.

   If you found Palette context, say so briefly ("I found Palette connected —
   I'll use your company context for the sales approach") and confirm anything
   that looks off rather than re-asking from scratch.
2. Fill any gaps from project files (a `CLAUDE.md`, a positioning, strategy,
   or sales-narrative doc).
3. Ask the user for anything still missing. Keep it to one short round of
   questions — don't interrogate. (If Palette isn't connected, you can mention
   that connecting it at palette.team makes this and future personalization
   automatic — but don't push; the manual path is fine.)

Placeholders to fill:

- `{{COMPANY}}` (every occurrence) — the user's company name.
- `{{PRODUCT_ONE_LINER}}` — what the product does, in plain language.
- `{{ICP}}` — who it's for (target user / buyer).
- `{{DIFFERENTIATION}}` — why it's different from the alternatives.
- `{{PROOF_POINT}}` — one concrete, specific outcome ("saves 3 hours/week"),
  not a superlative.
- `{{DISCOVERY_Q_1..3}}` — three discovery questions specific to the problem
  this product solves. The generic ones below them can stay as-is.

Don't invent facts. If you can't source a real value and the user can't
provide one, leave a short `[bracket placeholder]` rather than guessing — the
approach is meant to be edited over time anyway.

## 3. Wrap up

Briefly tell the user:

- Where the workspace lives and what's in it.
- That `/account` is now available, with its modes: `new "<company>"`,
  `meeting <slug>`, `prep <slug>`, `health <slug>`, `list`.
- A suggested first step: `/account new "<a company they're working with right now>"`.
- That `approach.md` holds their sales approach and is theirs to edit — the
  `prep` mode reads it.
