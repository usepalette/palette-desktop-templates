---
type: index
read_when:
  - Before building, changing or choosing a component
---

# Components

Which component to use for what. The components themselves live in the code or the library; this page holds when to use each one, when not to, and what we decided not to build. Rules that span components are in [`../../rules/`](../../rules/README.md).

> **Not filled in yet.** Say "fill in the components" and an agent lists the components it finds in the code or the library and drafts a line for each, for you to check.

**Components live in:** [repo and path, and the library file]
**Where to see them running:** [Storybook link, docs site or local command]

## The components

| Component | Use it for | Don't use it for |
|---|---|---|
| [Name] | [the job it does] | [the case where another component fits better] |

## A doc per component

A component that needs more than its package documentation gets a doc here, named for it, such as `menu.md`, with a link from its row. The doc says how the component is used in the product and the rules that apply to it alone. Under a heading "Designed, not shipped" it says what is designed and not built yet, so a scope can link to it.

## Adding a component

- **Look first.** Check this list, the repo and the other designers' `drafts/` for something that already does the job.
- **Extend before adding.** A variant, a slot or a property on an existing component comes before a new one.
- **Add a variant only for a real use case,** not one that might come up.
- **When it ships,** add its row here and any settled call to the rules.

## Not building

Components or patterns we decided against, and why, so nobody builds them again.

_None yet._
