# Competitor Analysis — install guide

You are setting up structured competitor tracking in this project. The
skill and slash command files are already placed under `.claude/` — you
don't need to touch those. Your job is to gather the missing details from
the user, then write the contextual files into the project.

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

Copy from the `landscape.md` contextual file. Substitute:

- `{{PRODUCT}}` → `<product>` (every occurrence)
- `{{COMPETITORS}}` → a bulleted markdown list of the seeded competitors,
  one per line, linking each to its profile (e.g. `- [Glean](competitors/glean.md)`)
- `{{TODAY}}` → today's date in `YYYY-MM-DD`

### `<market>/competitors/<slug>.md` (one per seeded competitor)

Copy from the `competitors/_template.md` contextual file. Substitute:

- `{{COMPETITOR_NAME}}` → the competitor's display name
- `{{TODAY}}` → today's date in `YYYY-MM-DD`

Pre-fill the **Positioning** section only if you have grounded,
verifiable information (Palette MCP, or cited public sources you can
point to). Don't fill it in from general knowledge — for competitive
docs, an empty placeholder is better than a confident-sounding
hallucination. Leave the other sections as the placeholder text so the
user knows what to fill in.

The slug should be a lowercase, hyphenated form of the name (`Microsoft
365 Copilot` → `microsoft-365-copilot`).

## 5. Wrap up

Summarize:

- Which files you wrote, with full paths.
- That `/add-competitor` is now available — they can use it to add more
  competitors without re-running this workflow.
- That the install created a checkpoint they can revert to from the
  timeline if they want to start over.
