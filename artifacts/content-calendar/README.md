---
title: Content calendar
summary: What goes out, when, on which channel and in what state, by week and by month, with the overdue pieces and the launch content.
category: marketing
order: 1
tags: [content, marketing, notion, calendar]
connectors: [notion, google-calendar, linear, slack]
request: "Build the content calendar for November from the Notion database, the launch dates and the marketing issues, by week and by month."
type: artifact
artifact_kind: page
version: 2611092
author: Silja Hürlimann
updated: 2026-11-09
---

# Content calendar

What goes out, when, on which channel and in what state, by week and by month, with the overdue pieces and the launch content.

## What it makes

One page that holds the month, in two views. Four numbers first, with the launch pieces on the key tile. The Week view shows the week by day, each piece with its channel, owner and state, and the pieces that are overdue. The Month view shows the month week by week. Every piece opens to its brief and a link to its draft.

On Monday the week's plan goes to the marketing channel, and each owner of an overdue piece gets one line. Both go after a preview.

## The request

> Build the content calendar for November from the Notion database, the launch dates and the marketing issues, by week and by month.

Said in the person's own words.

## What it reads

- **Notion or Google Docs**: the content database. Pieces, channels, owners, states, dates and briefs.
- **Google Calendar**: the launch and event dates the content is planned around.
- **Linear or Jira**: the marketing issues, for the pieces tracked there.
- **Slack**: the marketing channel, where the plan goes.

Every source is optional. Without the content database, the pieces are typed on the page. Without the calendar, the launch dates are typed.

## What lands in the workspace

In the folder the person picks, for example `spaces/marketing/`:

```
content-calendar.html             the page
processes/content-calendar.md     how the page is written, refreshed and posted
```

The process gets a row in `processes/README.md`.

## How it stays current

Ask for the content calendar, or press Refresh on the page. Both run `processes/content-calendar.md` on the page. Only the parts the template writes change. Lines the team changed stay as they are.

## Example

[`preview.html`](preview.html) is the page after a run, with made-up content for Halden, a made-up software company.

> The overdue list on Monday morning is the honest version of our content plan.
>
> Line Dahl, Head of marketing, Solv (made up)
