---
type: playbook
owner: "[Owner]"
status: draft
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
read_when:
  - "You are capturing feedback, an interview or an explicit ask"
  - "You are turning several sources into feature requests or painpoints"
  - "You are reviewing product evidence"
---

# Feedback synthesis

> **Not confirmed yet.** A first version. Change it until it says how the team judges feedback, then delete this box.

How raw feedback and interviews become honest feature requests and recurring painpoints, with the sources, the attribution, the quotes and the counter-signal kept in view. Load it before capturing or synthesising feedback.

## How we think about it

The goal is not more files. It is to keep raw signal as it came, find the few patterns that matter, and keep the evidence visible, so the team judges the evidence instead of trusting a summary.

```text
raw feedback ──┬──> explicit ask ──> feature request
               │
               └──> repeated or blocking problem ──> painpoint
user interview ┘
```

Every derived file carries `source_files`, pointing to the material it came from.

## Principles

### When a signal graduates

| Signal | Action |
|---|---|
| One comment, no explicit ask | Keep it as raw feedback |
| A specific capability is requested | Create or update a feature request |
| The same underlying pain appears in at least two independent sources | Create or update a painpoint |
| A structured interview shows a clearly blocking problem | A painpoint may stand on that one source; say so |
| Two sources use different words for the same job | Merge them into the item that exists |
| Two sources touch the same part of the product but different jobs | Keep them apart |

When unsure, keep the raw sources apart. Merging later is easier than splitting a false pattern.

### Scoring

A painpoint is scored on two axes:

- **Severity** (`low`, `medium` or `high`): the impact when the problem occurs
- **Frequency** (`occasional`, `recurring` or `blocking`): how often the work is affected

Don't score emotional volume. A quiet blocker can matter more than a loud annoyance.

A feature request carries a **priority signal** (`low`, `medium` or `high`). It is the strength of the evidence, not a place on the roadmap. Weigh the strength and urgency of the ask, the number and relevance of independent sources, and the fit with the theses in [`../strategy/`](../strategy/README.md). Record tensions. Never raise a score because a source is senior or loud.

### Attribution

- A quote comes from `## Their words`, or from a source captured with `capture_mode: verbatim`. Mark a cut with an ellipsis.
- A paraphrase is labelled as a paraphrase.
- Keep `source_url` in the raw source, so a later reviewer can trace the evidence.
- Context and impact can be your reading of the source, but they are never written as the source's own words.
- An unknown identity stays unknown. Never guess a company or a person.

### Data boundaries

- Include only the product context everyone who reads the space may see.
- Keep restricted raw material, secrets and needless personal details in their access-controlled source. Link to it, anonymise or summarise.
- Never weaken a source's permissions by copying it into a page, a recap or the dashboard that more people read.

### Tags

- Use the tags that already exist before adding one.
- Write them in lowercase kebab-case.
- A tag names the product area, the workflow or the friction, never the company.
- Keep the set small enough to stay useful.

## Approach

1. Read every selected source in full.
2. List the distinct pains and the explicit asks.
3. Search the painpoints and requests that exist for the same underlying job.
4. Group sources only when the job and the impact are really the same.
5. Keep the verbatim words under `## Their words`.
6. Keep facts, interpretation and counter-signal apart.
7. Propose what to create or update before writing anything.
8. Update the company profiles, then rebuild the dashboard.
