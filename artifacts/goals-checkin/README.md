---
title: Goals check-in
summary: The quarter's goals with this week's numbers, a confidence per key result and a line on what changed.
category: team
order: 4
tags: [goals, okr, weekly]
request: "Set up our Q4 goals check-in from the goals page, Linear and HubSpot, and post it every Friday."
type: artifact
artifact_kind: page
version: 2611101
author: Lars Ettrup
updated: 2026-11-10
also: [marketing]
---

# Goals check-in

The quarter's goals with this week's numbers, a confidence per key result and a line on what changed.

## What it makes

One page that holds the quarter: three numbers, then each objective with its key results. Each key result shows this week's value, a progress line, the owner, the confidence, the change on last week and the source. A key result off track shows in the warning colour. It opens to how it is measured and its earlier weeks.

The goals are the team's. They come from the goals page, or the person types them once a quarter. Owners give the confidence and one line each week. At a new quarter, the page asks for the new goals first, and the closed quarter moves to **Earlier quarters** with each key result's final value.

The check-in goes to the company channel and back to the goals page, always after a preview.

## The request

> Set up our Q4 goals check-in from the goals page, Linear and HubSpot, and post it every Friday.

Said in the person's own words.

## What it reads

- **Notion or Google Docs**: the goals page. The objectives, key results, owners and targets.
- **Linear or Jira**: the projects behind the key results and their progress.
- **HubSpot**: the numbers behind the growth key results: paying teams, trial to paid.
- **PostHog**: the product numbers behind the key results: usage, funnels.

Every source is optional. Without the goals page, the person types the goals once a quarter. Without a source for a key result, its owner types the value, and the page marks it as typed.

## What lands in the workspace

In the folder the person picks, for example `company/`:

```
goals-checkin.html             the page
processes/goals-checkin.md     how the page is written, refreshed and posted
```

The process gets a row in `processes/README.md`.

## How it stays current

Ask for this week's check-in, or press Refresh on the page. Both run `processes/goals-checkin.md` on the page. Only the parts the template writes change. The goals, the typed values and the owners' lines stay as they are.

## Example

[`preview.html`](preview.html) is the page after a run, with made-up content for Halden, a made-up software company.

> Nine key results, one line each, every Friday. The whole company reads it in two minutes.
>
> Petra Kol, CEO, Lumen (made up)
