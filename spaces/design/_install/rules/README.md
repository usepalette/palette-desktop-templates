---
type: index
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
read_when:
  - You are designing or building a UI and need the settled calls
  - You are reviewing a design
---

# Rules

The settled calls: the specific decisions that come out of real design work and should hold next time without being argued again. The principles in [`../principles/`](../principles/README.md) explain how to think. These record what we decided.

Read the files for the areas your work touches, not all of them. A toolbar change reads controls, spacing and components. Rules about a single component live in that component's doc in [`../design-system/components/`](../design-system/components/README.md).

## Areas

| Area | Covers |
|---|---|
| [`components.md`](components.md) | Which design system part to use, and in which size |
| [`controls.md`](controls.md) | Buttons, menus, inputs, confirming |
| [`spacing.md`](spacing.md) | Padding, gaps, dividers, grids |
| [`surfaces.md`](surfaces.md) | Colour on colour, shadows, borders |
| [`typography.md`](typography.md) | Text styles and how text sits together |
| [`icons.md`](icons.md) | Icon set, style, size and placement |
| [`motion.md`](motion.md) | How things move when they change |

Add a file when an area has no home here, such as `navigation.md`, or `figma.md` for how the team builds its design files, and add its row. Delete a file the team will never use.

## Adding a rule

Put it in the file for its area, newest first: **the rule in bold, in one sentence**, then the date and who made the call, then a sentence or two on why. The reason is what makes the rule hold when someone wants to break it. Add a line to the space's `log.md`.

```
**A divider is inset, never the full width of the column.** *(2026-03-14, [Name])* A line between rows starts and ends on the same inset as the content beside it, so the list lines up with what is inside the boxes around it.
```

A rule that reverses an older one says so, and the older one is deleted. When two rules seem to disagree, the newer date wins until someone settles it.

When a rule has grown into a way of thinking, move it into the principle it belongs to and delete it here. A rule about one person's preference belongs in that person's `lessons.md`.
