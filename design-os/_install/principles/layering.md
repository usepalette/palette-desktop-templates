---
type: doc
read_when:
  - Anything opens on top of anything else
---

# Layering

> **Not confirmed yet.** A starter set. Change it until it says what the team believes, then delete this box.

How UI is put on top of UI without the person losing their place.

## A layer is a detour

Something on top of the view is a separate moment: open it, do the thing, close it. There is no navigation inside a layer. The reasons to layer are reading a piece of information, adding something or editing something.

## The layer stack

- **Base** — The content of the view
- **Raised** — Surfaces that group or emphasise content inside the view
- **Floating** — Buttons and navigation that sit over the content without blocking it
- **Modal** — Dialogs, sheets and popovers, over everything, with a scrim when they block

## A sheet and a dialog are one thing

The screen size decides how it is shown: a sheet from the bottom on a phone, a centred dialog on a larger screen. A popover anchored to a control is a large-screen pattern and becomes a sheet on a phone.

## Interrupt only for what matters

A quiet notification for information the person does not have to act on, which goes away on its own. A blocking dialog for what they must decide or acknowledge, such as a destructive action.

## Go deeper, not sideways

A dialog may open a smaller dialog or a popover. A small layer that opens a larger one feels wrong, because focus should narrow as the person goes deeper.

## Every layer says how it closes

Sheets close by swiping or tapping outside, unless the person has to make a choice. Popovers close by clicking outside. Notifications close themselves.
