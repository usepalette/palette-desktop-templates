---
type: index
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
---

# Templates — Accounts

Reusable **fill-in formats** for this space's recurring outputs: the modular partner to [`playbooks/`](../playbooks/README.md). A playbook tells you what to do and how to think; a template gives you the exact format to fill in. Read the playbook to decide, then copy the template to produce.

Codify a repeatable output once as a template, and every future one comes out consistent: same structure, same quality bar, no reinventing.

## How templates work

- **The template is the source of truth for shape.** Extend it and every future output inherits the change.
- **They compose with the context.** A template says which files to load first (the customer's brief, this space's playbook), so outputs stay consistent without repeating the rules in every file.
- **Copy, don't edit in place.** Copy the format under **Fill in** to where the work lives, then fill it in. The two formats below are sections of a customer's brief, `customers/<name>/README.md`: the copy goes into the brief and takes no frontmatter of its own, and the brief's `last_updated` and `last_updated_by` change instead. A format for a document of its own gives the copy its full frontmatter, with the fitting type, owner, status, date, acting person and edit policy; follow `.agents/page-states.md` at the workspace root. The original template's brackets stay.

**This space's, or everyone's?** A format the whole company uses belongs in the company's shared [`templates/`](../../../company/templates/README.md), not here.

## Templates

| Template | Use it for |
|---|---|
| [`account-plan.md`](account-plan.md) | The **Plan** section of a customer's brief: what we are trying to achieve with them, the current bet and the risks |
| [`account-health.md`](account-health.md) | The **Health** section of a customer's brief: usage, communication and engagement, each with its source and the date it was checked |

Copy [`_template.md`](_template.md) when the next one is written, and list it here.
