---
title: Weekly update
summary: The week's update to the team and the people above it, written from Linear, GitHub, Slack and the calendar.
category: team
order: 1
tags: [weekly, team, slack, linear]
connectors: [linear, github, slack, google-calendar]
request: "Write this week's update for the team from Linear, GitHub, Slack and the calendar, and show me before it goes out."
type: artifact
artifact_kind: page
version: 2611092
author: Silja Hürlimann
updated: 2026-11-09
also: [product]
---

# Weekly update

The week's update to the team and the people above it, written from Linear, GitHub, Slack and the calendar.

## What it makes

One page that holds this week: four numbers, then what shipped, what was decided, what is at risk, next week and who is out. Each line links to its issue, pull request or thread. Every Friday the new week goes on top, and the week before moves into **Earlier weeks**.

A wording change someone asks for is kept through every refresh. The update goes to the team's channel or by mail, always after a preview.

## The request

> Write this week's update for the team from Linear, GitHub, Slack and the calendar, and show me before it goes out.

Said in the person's own words.

## What it reads

- **Linear or Jira**: the issues that moved this week. Done, in progress, blocked, and who.
- **GitHub**: the pull requests merged this week, with their authors.
- **Slack**: the decisions and the threads worth a line, and where the update goes.
- **Google Calendar**: next week. What is booked and who is out.

Every source is optional. Without Slack, the person posts the update themselves. Without GitHub, the shipped lines come from the task tool alone.

## What lands in the workspace

In the folder the person picks, for example `spaces/product/`:

```
weekly-update.html             the page
processes/weekly-update.md     how the page is written, refreshed and posted
```

The process gets a row in `processes/README.md`.

## How it stays current

Ask for this week's update, or press Refresh on the page. Both run `processes/weekly-update.md` on the page. Only the parts the template writes change. Lines the team changed stay as they are.

## Example

[`preview.html`](preview.html) is the page after a run, with made-up content for Halden, a made-up software company.

> Friday used to be an hour of digging through Linear and Slack. Now the update is on screen by nine and I change two lines.
>
> Mia Berg, Head of product, Nordlys (made up)
