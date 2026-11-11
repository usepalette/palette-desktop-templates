---
type: template
owner: "[Owner]"
status: draft
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
---

# Decision record

> **Mold.** The format of one decision on a project; don't fill it in here. [`processes/record-a-decision.md`](../processes/record-a-decision.md) copies it into a project as `projects/<name>/decisions/NNNN-<slug>.md`, numbered.
>
> In the copy: everything from **Fill in** down, with the frontmatter described below. Write only what you were given: a section you have nothing for keeps its brackets, and a line you worked out yourself ends with "(to confirm)". Once accepted, a record is history and is never rewritten.

Why a project did something one way: the context, the options, the call, the reasons, and what follows from it. Written so that someone six weeks later understands the choice without asking.

## How to write this

- **Frontmatter of the copy:** the full block (`type: decision`, the project's owner and edit policy, today and the person you are working for), plus `date`, the day it was decided, quoted. `status` is `draft` while the decision is only proposed and `active` once it is accepted.
- **When a later record supersedes it,** only three things change: `status: archived`, with `archived` (the date), `replaced_by` (the newer record) and `reason` added to the frontmatter, and its Status line says "superseded by NNNN". Nothing else in it is rewritten.
- **Load first:** the project's `README.md`, the meeting note or the thread where it was decided, and any earlier record it changes.
- **The reasons are the point.** The context, the options and the consequences are what nobody can rebuild later. Name the trade-offs that were accepted.
- **Quality bar:** someone who was not there understands what was chosen, what was given up and what to revisit. Everyone named under "Decided by" took part in the decision.

## Fill in

_The format itself, with a bracket in every slot. Copy from here down into the new document._

# NNNN — [Short title]

- **Date:** YYYY-MM-DD
- **Status:** [proposed, accepted, or superseded by NNNN]
- **Decided by:** [names]

## Context

[What is going on that needs a decision: the constraints, the deadlines, the earlier choices it builds on.]

## Options considered

1. [An option, in one line]
2. [Another option, in one line]

## Decision

[The option chosen, in one or two sentences.]

## Why

[The reasoning, and the trade-offs accepted: the part that is hardest to rebuild later.]

## Consequences

[What follows: what gets easier, what gets harder, what moves in or out of scope, and what to revisit, and when.]
