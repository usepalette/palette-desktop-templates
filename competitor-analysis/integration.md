# Competitor Analysis — install guide

You are setting up structured competitor tracking in this project. The
skill files are already placed for you in the appropriate provider
directories — you don't need to touch them. Your job is to gather the
missing details from the user, then write the contextual files into the
project.

## 1. Where should the market folder live?

Suggest `gtm/foundations/market/` as the default. If the project already
has an established research, strategy, or market folder (look for
`research/`, `strategy/`, or `market/` in the project root or under
`gtm/`), suggest installing there instead. Defer to the user's choice.

Call the chosen path `<market>/` for the rest of these instructions.

## 2. What is the user's product/company name?

If the Palette MCP is available, pull this from organization context
rather than asking. Otherwise ask. Call this value `<product>`.

## 3. Which competitors should we seed?

Ask the user for 2–5 competitors they want to track first. They don't
need to be exhaustive — this is a starting point, and `/add-competitor`
exists for adding more later.

If the Palette MCP is available you can suggest competitors yourself
based on the user's product context, but always confirm the list before
writing.

## 4. Then write

For each file below, substitute the markers as listed.

### `<market>/landscape.md`

Copy the contents of the inline `landscape.md` shown in the Contextual
files section of this message — not any existing `landscape.md` in the
project. Substitute:

- `{{PRODUCT}}` → `<product>` (every occurrence)
- `{{COMPETITORS}}` → a bulleted markdown list of the seeded competitors,
  one per line, linking each to its profile (e.g. `- [Glean](competitors/glean.md)`)
- `{{TODAY}}` → today's date in `YYYY-MM-DD`

### `<market>/competitors/<slug>.md` (one per seeded competitor)

Copy the contents of the inline `competitors/_template.md` shown in
the Contextual files section of this message. Substitute:

- `{{COMPETITOR_NAME}}` → the competitor's display name
- `{{TODAY}}` → today's date in `YYYY-MM-DD`

Leave all sections as the placeholder text — the next step offers to
fill them in via research. Don't pre-fill from general knowledge; for
competitive docs an empty placeholder is better than a confident-sounding
hallucination.

The slug should be a lowercase, hyphenated form of the name (`Microsoft
365 Copilot` → `microsoft-365-copilot`).

## 5. Offer to research the seeded competitors

The scaffolded profiles are placeholders. Ask the user whether to run
the `competitor-research` skill on the seeded competitors now, or skip
and let them invoke `/add-competitor` (or research manually) later.

Frame it roughly like:

> I've scaffolded the profiles but they're empty placeholders. Want me
> to research them now? This takes a minute or two per competitor and
> uses web search. Or I can skip and you can run research later.

If the user says yes, invoke the `competitor-research` skill once per
seeded competitor, updating each `<market>/competitors/<slug>.md` in
place. After researching all of them, update `<market>/landscape.md`'s
tier table and threat assessment to reflect what you learned — that's
the load-bearing synthesis.

If the user says skip (or to research only some), respect that and move
on. They can run `/add-competitor` on any seeded name later to fill it
in — the skill will detect the existing placeholder and confirm before
replacing it.

## 6. Wrap up

Summarize:

- Which files you wrote, with full paths.
- Whether the profiles were researched or left as placeholders. If
  placeholders, remind the user they can run `/add-competitor <name>`
  on any seeded competitor to fill it in later.
- That `/add-competitor` is now available — they can use it to add more
  competitors without re-running this workflow.
- That the install created a checkpoint they can revert to from the
  timeline if they want to start over.
