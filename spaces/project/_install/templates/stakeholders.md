---
type: template
owner: "[Owner]"
status: draft
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
---

# Stakeholder map

> **Mold.** The format of a project's stakeholder map; don't fill it in here. [`processes/start-a-project.md`](../processes/start-a-project.md) copies it into a project as `projects/<name>/stakeholders.md`.
>
> In the copy: everything from **Fill in** down, with its own full frontmatter as `type: doc` ([`README.md`](README.md) → How templates work). Keep the sections for the sides the project has. Write only what you were given: a slot you have nothing for keeps its brackets, and a line you worked out yourself ends with "(to confirm)".

Where each person on a project stands: how much they can change its course, how much it changes their work, and how the team keeps them involved. It adds to the People table in the project's `README.md` and never repeats it: names, roles and sides live there.

## How to write this

- **Load first:** the People table in the project's `README.md`, the teammates' profiles in [`people/`](../../../people/README.md), and the customer's key people in `customers/<name>/` when the project is for a customer.
- **The People table is the roster.** Everyone here is in it first. Someone missing there is added there before they get a row here, and a customer's person to the customer's key people too.
- **Influence** is how much a person can change the project's course. **Interest** is how much the project changes their work. Each is high, medium or low.
- **No contact details.** How to reach a teammate is in their profile; a customer's people are in the customer's folder.
- **Quality bar:** everyone with high influence has a clear way of being kept involved, and nobody with high interest hears about a change last.

## Fill in

_The format itself, with a bracket in every slot. Copy from here down into the new document._

# [Project name]: stakeholder map

## Customer

Who the work is for: the sponsor, the day-to-day contacts, and the people who sign off.

| Name | Influence | Interest | What they need from the project | How we keep them involved |
|---|---|---|---|---|
| [Name, as in the People table] | [high, medium or low] | [high, medium or low] | [what they care about, in their words where possible] | [the check-in, the update or the review they get, and from whom] |

## Team

Who is staffed on the project. Each name links to their profile in `people/`.

| Name | Influence | Interest | What they need from the project | How we keep them involved |
|---|---|---|---|---|
| [Name, as in the People table] | [high, medium or low] | [high, medium or low] | [what they need to do their part] | [the meetings and the channels they are in] |

## External

Partners, vendors, advisers, and anyone else in the loop.

| Name | Organisation | Influence | Interest | What they need from the project | How we keep them involved |
|---|---|---|---|---|---|
| [Name, as in the People table] | [their organisation] | [high, medium or low] | [high, medium or low] | [what they need, or what we need from them] | [how and when they hear from us] |
