---
type: doc
owner: "[Owner]"
status: draft
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
read_when:
  - You are laying out a whole screen
---

# Page structure

> **Not confirmed yet.** A starter set. Change it until it says what the team believes, then delete this box.

How a screen is divided into header, content and navigation.

## Three zones, three containers

A screen has a header, a content area and navigation. They are three separate containers, each with its own sizing and behaviour.

## The header belongs to the view

The header says where the person is, holds the back action and carries the view's primary action. Navigation is global: it moves the person between views and is the same on every one.

## The content does one job

The content resolves to a list, a grid or a simple combination of two, such as a chart above a list. When three or four kinds of content compete, split the view into tabs or pages. Something that starts a different task opens a new view, or a layer when it is a quick detour.

## Sticky headers belong to the page

The page's header sticks. Headings inside the scrolling content do not.

## State belongs to the whole view

A view loads, then resolves to data, empty or error, and each is a state of the whole view. Inline state is for buttons, dialogs and input fields. Never show several spinners at once: if several things load into one view, the view is loading until they all settle.
