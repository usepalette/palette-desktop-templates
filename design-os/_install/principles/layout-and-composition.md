---
type: doc
read_when:
  - You are arranging elements, grouping them or setting space between them
---

# Layout and composition

> **Not confirmed yet.** A starter set. Change it until it says what the team believes, then delete this box.

How elements are arranged so a screen reads as one thing.

## Group by space before boxes

Things that belong together sit close together, and closeness already shows the group. A background or a border is for emphasis. Groups inside boxes inside boxes get heavy fast.

## Rows and columns show relationships

A row holds parallel things with the same role. A column holds a sequence or the attributes of one subject. Read the elements aloud: "and also" is a row, "and then" is a column.

## Layouts nest, and every container earns its place

A list row is a text group and an action group inside one horizontal layout. Each container owns its own padding and gaps. A sub-container is justified only when its elements need their own spacing, size or behaviour. This holds in the design file and in the code.

## Actions are not text

A button has its own weight and padding, so it sits in its own slot, never inline with labels. The space between two pieces of text is not the space between text and a button.

## Left-aligned by default

Text that runs to more than one line is left-aligned. Centre only short pairs on dialogs, empty states and large visual surfaces, and never mix alignments inside one group.

## One spacing scale

Every distance comes from the design system's spacing tokens. Text sits tighter to text than to the things around it, and padding grows with the size of the component.

## Lists and grids

Most screens are a list, a grid or both. In a grid, boxes side by side share a width and a gap.

## Start small, scale up

Design for the smallest screen first. Add columns when an item gets too wide to read, and set a maximum width on text.
