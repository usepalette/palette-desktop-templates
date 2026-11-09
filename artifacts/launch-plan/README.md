---
title: Launch plan
summary: "One launch on one page: the countdown, the checklist per workstream, the comms pieces and the timeline, from Linear, the docs, GitHub and the calendar."
category: marketing
order: 3
tags: [launch, marketing, product, calendar]
request: "Make the launch plan for Portals 2.0 on 26 November: the checklist per workstream from Linear, the pieces from the content calendar, the dates from the calendar."
type: artifact
artifact_kind: page
version: 2611092
author: Lars Ettrup
updated: 2026-11-09
also: [product]
---

# Launch plan

One launch on one page: the countdown, the checklist per workstream, the comms pieces and the timeline, from Linear, the docs, GitHub and the calendar.

## What it makes

One page per launch, in three views. **Overview** has the days to go, the timeline to the launch review and what is at risk. **Workstreams** has a checklist per workstream, with owners and dates. **Comms** has every piece with its channel, owner and state. Each piece opens to its brief and a link to its draft.

The page is refreshed every week until the launch ships. Then it says shipped, and it stays. The status goes to the launch channel: done per workstream, at risk and why, and the next date, always after a preview.

## The request

> Make the launch plan for Portals 2.0 on 26 November: the checklist per workstream from Linear, the pieces from the content calendar, the dates from the calendar.

Said in the person's own words.

## What it reads

- **Linear or Jira**: the launch project. Items per workstream, owners, dates.
- **Notion or Google Docs**: the content database, for the comms pieces and their drafts.
- **GitHub**: the release, for what ships.
- **Google Calendar**: the dates. Go or no-go, freeze, launch, review.
- **Slack**: the launch channel, to post the status.

Every source is optional. Without a launch project, the checklist is typed from the person's list. Without the content database, the pieces are typed.

## What lands in the workspace

In the folder the person picks, for example `spaces/marketing/`:

```
launches/
├── _template.html          the mold for a new launch
├── README.md               the list of launches
└── portals-2.html          one page per launch, made by the process
processes/launch-plan.md    how a launch page is made, refreshed and posted
```

The install lands `_template.html` and `README.md`. The process makes each launch's page and adds its row to `launches/README.md`. The process gets a row in `processes/README.md`.

## How it stays current

Ask for a launch plan with the launch's name and date, or ask to refresh one, or press Refresh on a launch page. Each runs `processes/launch-plan.md` on that launch's page. Only the parts the template writes change. Lines the team changed stay as they are.

## Example

[`preview.html`](preview.html) is a launch page after a run, with made-up content for Halden, a made-up software company, and its product and marketing teams.

> Four workstreams, one page, a countdown. For the first time the launch did not live in my head.
>
> Mikkel Sørensen, Product marketing, Bergen Studio (made up)
