---
type: template
owner: "[Owner]"
status: draft
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
---

# Goals

> **Mold.** The format of a project's goals; don't fill it in here. [`processes/start-a-project.md`](../processes/start-a-project.md) copies it into a project as `projects/<name>/goals.md`.
>
> In the copy: everything from **Fill in** down, with its own full frontmatter as `type: doc` ([`README.md`](README.md) → How templates work). Write only what you were given: a slot you have nothing for keeps its brackets, and a line you worked out yourself ends with "(to confirm)".

What the project is trying to change, how the team will know it did, and what it is not trying to do.

## How to write this

- **Load first:** the project's `README.md`, and its brief when it keeps one.
- **Outcomes, not features.** An outcome is a change for the people the project is for, never a thing the project ships.
- **Every outcome has a metric,** with its value today, a target, and how it is measured. A baseline nobody has measured stays in brackets until someone does: never estimate one.
- **Quality bar:** at the end of the project, anyone can read this page and say whether each outcome was reached.

## Fill in

_The format itself, with a bracket in every slot. Copy from here down into the new document._

# [Project name]: goals

## Outcomes

What the project is trying to achieve: a change in the world, not features shipped.

- **[Outcome]** — [the change it makes, and why it matters to the people the project is for]
- **[Another outcome]** — [the change it makes, and why it matters]

## Non-goals

What people might assume is in play and is not, so the scope stays honest.

- [A non-goal]

## Success metrics

| Metric | Baseline | Target | How we measure |
|---|---|---|---|
| [What is measured] | [its value today] | [where it should be, and by when] | [the source: a tool, a report, a survey] |
