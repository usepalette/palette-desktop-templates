---
type: index
read_when:
  - You need to know what the design system is, where it lives or how it is structured
---

# Design system

What we build with. The design system itself lives in its repo, its design library or both (see [`../repos.md`](../repos.md)). These pages hold what the code cannot say: what each part is for, when to use it, and what we decided.

> **Not filled in yet.** Say "fill in the design system pages" and an agent reads the package or the library and writes this page, [`foundations/`](foundations/README.md) and [`components/`](components/README.md) for you to check. A team without a design system yet starts from the product: the agent lists the values and components it repeats, as a first proposal for one.

## Where it lives

| What | Where |
|---|---|
| Source of truth | [repo and path, and the package name if it is published] |
| Who uses it | [the apps that import it, and how: a workspace package, a published version, copied files] |
| Documentation | [Storybook, a docs site, or the folder of docs in the repo] |
| Design file | [the Figma library or design tool file, if there is one] |

## How it is structured

[The layers, from the values up, for example tokens, then primitives, then composed components, then patterns. What each layer holds, and which layers app code is allowed to use.]

## The folders

- **[`foundations/`](foundations/README.md)** — The values every component is built on: colour, spacing, type, radius, elevation, motion, icons
- **[`components/`](components/README.md)** — Which component to use for what, and a doc for each component that needs more than its package documentation

When the team settles how components combine into a whole view, such as a settings page or a list with a detail view, add `patterns/` with one page per pattern.

## How these pages change

- **What ships wins on what exists.** When a page here and the code or library disagree, fix one of them on purpose and log which in the root `log.md`.
- **Never copy values here.** A token's value, a prop list or a component's code lives in the code or the library, so these pages cannot go out of date with it. They name the token and say what it is for.
- **A component designed here first** gets a doc in `components/` with a section "Designed, not shipped", and the doc changes when it ships.
- **Where the design file and the code differ,** say which one is right, and which one changes.
