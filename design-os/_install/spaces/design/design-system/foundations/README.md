---
type: index
owner: "[Owner]"
status: draft
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
read_when:
  - You are choosing a colour, a space, a type style, a radius, a shadow or a motion value
---

# Foundations

The values every component is built on, and where they live in the code and the design library. This page explains the tokens. The values themselves live in the code or the library and are never copied here, so this page cannot go out of date with them. The settled calls about using them are in [`../../rules/`](../../rules/README.md).

> **Not filled in yet.** Say "fill in the foundations" and an agent reads the token files or the library's variables and writes this page for you to check.

**Tokens live in:** [repo and path to the token files, and the library's variable collections]
**How they reach the code:** [CSS custom properties, a theme object, a generated file, and how dark mode or themes switch]

## How tokens are named

[The naming pattern, for example semantic names that say the role (`surface-raised`) rather than the value (`gray-100`), and how the tiers relate: raw values, then semantic tokens, then component tokens.]

## The groups

| Group | What it is for | Where in code |
|---|---|---|
| Colour | [what the colour tokens cover: text, surfaces, borders, accents, states] | [path] |
| Spacing | [the scale, and which steps are for padding and which for gaps] | [path] |
| Type | [the text styles and when each is used] | [path] |
| Radius | [the radii and what gets which] | [path] |
| Elevation | [shadows and layering] | [path] |
| Motion | [durations and easings] | [path] |
| Icons | [the icon set, its style and how icons are imported] | [path] |

A group that needs more than a row gets a page of its own in this folder, named for the subject, such as `spacing.md`, and a link from its row.

## When a token is missing

Don't hardcode a value. Use the closest token and note the gap, or propose a new token in the design system and add a rule to the rule file for its area once it is agreed.
