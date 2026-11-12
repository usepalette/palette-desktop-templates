---
title: Marketing scoreboard
summary: Signups, leads, visits and paying teams against the year goal, by month, with where they came from and the pace.
category: marketing
order: 2
tags: [metrics, marketing, weekly]
request: "Set up the marketing scoreboard from HubSpot and PostHog with our year goal, and refresh it every Monday."
type: artifact
artifact_kind: page
version: 2611101
updated: 2026-11-10
also: [team]
---

# Marketing scoreboard

Signups, leads, visits and paying teams against the year goal, by month, with where they came from and the pace.

## What it makes

One page that holds the year against its goal: how far it is, where it should be, and where it ends at this pace. Then the month in four numbers, each with its change on last month and its source, the months as a chart for each measure, where the signups came from and the notes on the month. Each month of the year opens to its numbers and their sources.

The goals are the team's. They come from the goals page, or the person types them once. A number no source gives is typed when asked, marked as typed, and kept through every refresh. Every Monday a three-line note on what moved goes to the marketing channel, always after a preview.

## The request

> Set up the marketing scoreboard from HubSpot and PostHog with our year goal, and refresh it every Monday.

Said in the person's own words.

## What it reads

- **HubSpot**: qualified leads, paying teams, trial to paid.
- **PostHog**: signups, website visits, where they came from.
- **Notion or Google Docs**: the goals page, for the year goal.

Every source is optional. Without the goals page, the person types the goals once. Without a source for a number, the person types it on Monday, and the page marks it as typed.

## What lands in the workspace

In the folder the person picks, for example `spaces/marketing/`:

```
marketing-scoreboard.html             the page
processes/marketing-scoreboard.md     how the page is written, refreshed and posted
```

The process gets a row in `processes/README.md`.

## How it stays current

Ask for the Monday numbers, or press Refresh on the page. Both run `processes/marketing-scoreboard.md` on the page. Only the parts the template writes change. The goals, the typed numbers and the notes stay as they are.

## Example

[`preview.html`](preview.html) is the page after a run, with made-up content for Halden, a made-up software company.

> One page on Monday with where the year should be and where it ends at this pace. That is the whole meeting.
>
> Priya Nair, Growth lead, Lumen (made up)
