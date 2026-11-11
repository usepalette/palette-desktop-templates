---
type: template
owner: "[Owner]"
status: draft
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
---

# Scope

> **Mold.** The format of a project's scope; don't fill it in here. [`processes/start-a-project.md`](../processes/start-a-project.md) copies it into a project as `projects/<name>/scope.md`.
>
> In the copy: everything from **Fill in** down, with its own full frontmatter as `type: doc` ([`README.md`](README.md) → How templates work). The change log's bracketed row becomes "_None yet._" until the first change. Write only what you were given: a slot you have nothing for keeps its brackets, and a line you worked out yourself ends with "(to confirm)".

What the project delivers, what it does not, the assumptions the plan rests on, and every change since the scope was agreed.

## How to write this

- **Load first:** the project's `README.md` and its brief, and the statement of work or the proposal when there is one. Link a contract where it is kept; never copy its terms here.
- **The README keeps the headline.** Its Scope section keeps one line for in and one for out, and links here for the full lists.
- **A change is never silent.** A change to the scope is a decision: it gets a record ([`processes/record-a-decision.md`](../processes/record-a-decision.md)), a dated row in the change log linking the record, and the lists above change to match. The old version lives on in the change log.
- **Quality bar:** someone outside the team can tell from this page alone whether a request is in scope.

## Fill in

_The format itself, with a bracket in every slot. Copy from here down into the new document._

# [Project name]: scope

## In scope

- [What the project delivers]

## Out of scope or deferred

- [What the project does not do, and whether it could come later]

## Assumptions

- [What the plan takes as given: what someone else provides, what stays as it is, who is available]

## Change log

Every change since the scope was agreed, newest on top, each with the decision behind it.

| Date | Change | Reason | Decision |
|---|---|---|---|
| YYYY-MM-DD | [what changed] | [why] | [a link to the record in the project's decisions folder] |
