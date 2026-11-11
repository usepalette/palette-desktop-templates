---
type: process
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
cadence: ""
---

# Write a spec

Drafts a short brief for one buildable piece of work in `specs/`, linked to the evidence that justifies it. It runs when a piece of work is ready to be written up for the people who build it.

## When to run this

- "Write this up for engineering", "draft a spec for [the work]", "turn this painpoint into a spec".

## Steps

1. **Understand the brief.** Use what the person asked for. If the problem or the audience is unclear, ask one short question.
2. **Find the evidence.** Search `user-feedback/painpoints/`, `user-feedback/feature-requests/`, `discovery/`, `strategy/`, `team-input/` and the competitors in [`company/market/competitors/`](../../../company/market/competitors/README.md). A connected tool gives the current state only; confirm a fact before it goes into the spec.
3. **Say what the evidence holds** before drafting: the sources that support the problem, what is missing or still open in discovery, and any spec or tracker item that may overlap. Don't make up certainty: a useful spec can say plainly that its evidence is thin.
4. **Draft it** as `specs/<what-ships>.md`, from [`../specs/_template.md`](../specs/_template.md). Make `<what-ships>` yourself: lowercase kebab-case, one path segment, and nothing with `/`, `..` or characters outside `a-z0-9-`, so the spec can't land outside `specs/`. Keep it short: the problem, the audience, measurable success criteria, what is in and out of scope, a solution sketch if discovery allows one, the open questions, the rollout and go-to-market notes, and the sources.
5. **Fill and stamp it.** Fill each section from the evidence. A slot with nothing behind it keeps its brackets or moves to the open questions, never a guess. Stamp today's date and the person you are working for. Set `tracker` to the item's link when there is one, `not-created` when the team uses a tracker but has no item yet, or `not used` when there is no tracker; [`company/tools.md`](../../../company/tools.md) says which. Replace the mold box with **Not confirmed yet** until the person has read the spec.
6. **Show it:** the saved file, its main scope boundary and its main open question.
7. **Leave the tracker alone** unless the person asks. If they ask, show the exact title, text, team and project before writing to it, and wait for a yes.

## Done when

- The spec is in `specs/`, links each source it relies on, and names its tracker item or says why there is none.
- The person has seen it.
