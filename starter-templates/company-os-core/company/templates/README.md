---
type: index
owner: Shared
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
---

# Templates

Fill-in formats for the outputs the whole company produces again and again. A template gives the shape; the files in [`../brand/`](../brand/README.md), [`../products/`](../products/README.md) and [`../market/`](../market/README.md) give the content. That is why they are kept apart: change the voice once, and every future output follows.

## Templates

Three starter formats ship with the workspace. Each is usable as it stands; change it to how the company makes that output, or delete it.

| Template | Use it for | Loads |
|---|---|---|
| [`one-pager.md`](one-pager.md) | The company or one product on a single page | messaging, the product's file, voice, design |
| [`social-post.md`](social-post.md) | A post under a person's name or the company's | the author's tone of voice, voice |
| [`customer-story.md`](customer-story.md) | What changed for a customer, told with their approval | the customer's folder, voice, messaging |

## How templates work

- **The template is the source of truth for shape.** Improve the template and every future output inherits the change.
- **Each template says what to load.** Its **How to write this** section names the files to read first, so the rules are not repeated in every template.
- **Copy, don't edit in place.** Copy the part under **Fill in** to where the work lives (a project folder, a customer folder, a scratchpad), then fill it in. A Markdown output starts with its own full frontmatter (`type: doc` or the fitting type, known owner, status, date, acting person and edit policy); do not copy template metadata unchanged. Follow [page states](../../.agents/page-states.md) for its review box. The brackets in the original template are its format: they stay.

## Add a template

When the same output has been made twice, save its format:

1. Copy [`_template.md`](_template.md) to a file named for the output.
2. Write **How to write this** from what made the good ones good, and the **Fill in** part from their structure. Keep the shape, never an old example's names, numbers or wording.
3. Stamp the frontmatter, follow [page states](../../.agents/page-states.md) for review, and add a row to the table above. A format inferred from examples remains unconfirmed until reviewed; its reusable slots remain after confirmation.

Delete the templates the company doesn't use, and remove their rows.

## Company-wide or one space's?

A format the whole company uses belongs here. A format that belongs to one area of work lives in that space, in its own `templates/` folder under [`spaces/`](../../spaces/README.md).
