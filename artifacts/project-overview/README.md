---
title: Projects overview
summary: "Every project the team runs on one page: status, milestones, the pinned update, who is on what and what changed."
category: product
order: 1
tags: [projects, status, linear, github]
connectors: [linear, github, slack, notion]
request: "Build the projects overview from Linear, GitHub and Slack: status, milestones this week, the pinned update, and who we wait on."
type: artifact
artifact_kind: page
version: 2611093
author: Brian Kyed
updated: 2026-11-09
also: [team]
---

# Projects overview

Every project the team runs on one page: status, milestones, the pinned update, who is on what and what changed.

## What it makes

One page that answers what is happening now, in three views:

- **Projects**: three numbers, then every project with its progress, owner, stage and date. The one at risk shows in the warning colour. Each project opens to its week, its open issues and its sources. Then the milestones this week and next, and the pinned update.
- **Team**: who is on what, and who outside the team the projects wait on.
- **What changed** since last week.

The page leaves out what comes next and later. The Roadmap holds that.

On the first share, the process writes a stakeholder version beside the page: the projects, the milestones and the pinned update, without the team's views. It goes to the people above and beside the team, always after a preview.

## The request

> Build the projects overview from Linear, GitHub and Slack: status, milestones this week, the pinned update, and who we wait on.

Said in the person's own words.

## What it reads

- **Linear or Jira**: the projects. Progress, target dates, status, owners and open issues.
- **The `projects/` folder**: the projects the team keeps in the workspace. The process reads it and never changes it.
- **GitHub**: the pull requests merged this week, per project.
- **Slack**: the updates in the project channels, and the pinned one.
- **Notion or Google Docs**: the specs the projects link to.

Every source is optional. Without GitHub, the pull-request counts are left out. Without Slack, the pinned update is typed on the page.

## What lands in the workspace

In the folder the person picks, for example `spaces/product/`:

```
project-overview.html             the page
processes/project-overview.md     how the page is written, refreshed and shared
```

The process gets a row in `processes/README.md`. The first share adds `project-overview-stakeholders.html` beside the page.

## How it stays current

Ask for the projects overview, or press Refresh on the page. Both run `processes/project-overview.md` on the page. Only the parts the template writes change. Lines the team changed stay as they are. Once the stakeholder version exists, each run offers to refresh it too.

## Example

[`preview.html`](preview.html) is the page after a run, with made-up content for Halden, a made-up software company.

> I send the stakeholder view to the board. They stopped asking for a deck.
>
> Tom Rask, VP product, Bergen Studio (made up)
