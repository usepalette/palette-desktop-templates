---
title: Decision log
summary: Every decision the team took, with the why, the who and the thread it came from, in one place.
category: team
order: 2
tags: [decisions, slack, notion]
request: "Build our decision log from the #product and #marketing threads, the meeting notes and the Decisions page, and keep it updated."
type: artifact
artifact_kind: page
version: 2611101
author: Christian Lomholt
updated: 2026-11-10
also: [product, marketing]
---

# Decision log

Every decision the team took, with the why, the who and the thread it came from, in one place.

## What it makes

One page that holds every decision: four numbers for the quarter, then this week, up for review, reversed and earlier. Each decision opens to the options on the table, what followed, and each review or reversal with its date. Filter by area, or search as you type.

The page is a log. A run adds decisions and never rewrites one. A review or a reversal is added with its date and its reason. Every Friday the week's new decisions go on top. At a new quarter, the quarter before moves into **Earlier**.

To add one decision, share its thread, a meeting note or a sentence. The draft shows first, and it goes on the page after a yes. It goes on the team's decisions page in the docs tool too, after a yes.

## The request

> Build our decision log from the #product and #marketing threads, the meeting notes and the Decisions page, and keep it updated.

Said in the person's own words.

## What it reads

- **The workspace's `log.md` files**: the decisions each scope records. The page reads them and never changes them.
- **Slack**: the threads where something was decided. The thread, who said it, the replies.
- **Meeting notes**: the decisions marked in the notes in the workspace.
- **Notion or Google Docs**: the decisions page, when the team keeps one.
- **Linear or Jira**: the projects a decision touched, for the link.

Every source is optional. Without Slack, the log comes from the logs, the meeting notes and the decisions page. A decision can always be typed in.

## What lands in the workspace

In the folder the person picks, for example `company/`:

```
decision-log.html             the page
processes/decision-log.md     how the page is built, refreshed and added to
```

The process gets a row in `processes/README.md`.

## How it stays current

Ask to refresh the decision log, or press Refresh on the page. Both run `processes/decision-log.md` on the page. Only the parts the template writes change. Decisions already on the page keep their words, and lines the team changed stay as they are.

## Example

[`preview.html`](preview.html) is the page after a run, with made-up content for Halden, a made-up software company, and its product and marketing teams.

> A new PM read it on her first day and stopped asking why things are the way they are.
>
> Sara Aalto, CPO, Kappa (made up)
