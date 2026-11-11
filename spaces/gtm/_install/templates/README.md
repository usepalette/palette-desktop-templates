---
type: index
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
---

# Templates — GTM

Reusable **fill-in formats** for this space's recurring outputs: the modular partner to [`playbooks/`](../playbooks/README.md). A playbook tells you what to do and how to think; a template gives you the exact format to fill in. Read the playbook to decide, then copy the template to produce.

Codify a repeatable output once as a template, and every future one comes out consistent: same structure, same quality bar, no reinventing.

## How templates work

- **The template is the source of truth for shape.** Extend it and every future output inherits the change.
- **They compose with the context.** A template says which pages to load first (this space's foundations, the company's brand pages), so outputs stay consistent without repeating the rules in every file.
- **Copy, don't edit in place.** Copy the format under **Fill in** to where the work lives (a project's folder, the Content space, a scratchpad), then fill it in. Markdown outputs need their own full frontmatter, with the fitting type, owner, status, date, acting person and edit policy; follow `.agents/page-states.md` at the workspace root. The original template's brackets stay.

**This space's, or everyone's?** A format the whole company uses belongs in the company's shared [`templates/`](../../../company/templates/README.md), such as its one-pager, its social post and its customer story, not here.

## Templates

| Template | Use it for |
|---|---|
| [`launch/`](launch/README.md) | The launch kit: the messaging brief, agreed first, then a format for each piece, from the changelog entry to the video script. Used with [`playbooks/launch.md`](../playbooks/launch.md) |

The launch formats ship as starter formats, usable as they stand. Change each one to how the team makes that piece, and delete its box once the team has made the format its own.

Copy [`_template.md`](_template.md) when a new format is written, such as a proposal or a sales deck, and list it here. Formats for one kind of work can share a folder of their own, like `launch/`, with its own README.
