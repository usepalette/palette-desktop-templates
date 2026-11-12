---
title: Team capacity
summary: Who has room next week and who has too much, from the calendar and the work assigned in Linear.
category: team
order: 3
tags: [capacity, planning, linear, calendar]
request: "Show me the team's capacity for next week from the calendar and Linear, and suggest what to move."
type: artifact
artifact_kind: page
version: 2611101
updated: 2026-11-10
also: [product]
---

# Team capacity

Who has room next week and who has too much, from the calendar and the work assigned in Linear.

## What it makes

One page that holds the coming week. Four numbers, then one row per person with a box per working day, filled by the work planned for it. The people who are over and the people with room are named at the top. Below are the suggested moves and the issues that nobody has, each with who it fits.

Every Friday the page shows the next week, and the week before goes. A move you accept is made in Linear, always after a preview, and the page shows it as made.

## The request

> Show me the team's capacity for next week from the calendar and Linear, and suggest what to move.

Said in the person's own words.

## What it reads

- **Linear or Jira**: the issues in the cycle, with their assignees and estimates.
- **Google Calendar**: time off, and the hours in meetings per person.

Every source is optional. Without estimates, the page counts issues instead of days and says so. Without the calendar, everyone is in all week.

## What lands in the workspace

In the folder the person picks, for example `spaces/product/`:

```
team-capacity.html             the page
processes/team-capacity.md     how the page is written, refreshed and rebalanced
```

The process gets a row in `processes/README.md`.

## How it stays current

Ask for next week's capacity, or press Refresh on the page. Both run `processes/team-capacity.md` on the page. Only the parts the template writes change. Lines the team changed stay as they are.

## Example

[`preview.html`](preview.html) is the page after a run, with made-up content for Halden, a made-up software company.

> It shows the two people who are over before the week starts, which is when it is still cheap to fix.
>
> Elin Kvist, Engineering manager, Solv (made up)
