---
title: Roadmap
summary: Now, next and later, from the projects in Linear and the specs in your docs, with a view for customers.
category: product
order: 3
tags: [roadmap, product, linear]
request: "Make our roadmap as now, next and later from the Linear projects and the specs, with a customer view I can share."
type: artifact
artifact_kind: page
version: 2611101
author: Søren Clausen
updated: 2026-11-10
also: [marketing]
---

# Roadmap

Now, next and later, from the projects in Linear and the specs in your docs, with a view for customers.

## What it makes

One page that answers what comes when: four numbers, then the projects in three columns, now, next and later. Each project opens to why it is on the roadmap and who asked for it. The projects in build show their progress, owner, date and confidence.

The page leaves out the status of the week and who works on what. The Projects overview holds those.

On the first share, the process writes a customer version beside the page: quarters only, with no owners, no confidence and no dates inside a quarter. When a customer asks when, the answer comes from that version, always after a preview.

## The request

> Make our roadmap as now, next and later from the Linear projects and the specs, with a customer view I can share.

Said in the person's own words.

## What it reads

- **Linear or Jira**: the projects. Status, progress, target dates, owners.
- **Notion or Google Docs**: the specs, for the reason behind each project.
- **The `projects/` folder**: the projects the team keeps in the workspace. The process reads it and never changes it.
- **HubSpot**: the customers who asked for each project, from the CRM notes.
- **Slack**: the product channel, for decisions that move a project.

Every source is optional. Without HubSpot, the list of who asked comes from the team's feedback folder. Without specs, the reason is typed.

## What lands in the workspace

In the folder the person picks, for example `spaces/product/`:

```
roadmap.html             the page
processes/roadmap.md     how the page is written, refreshed and shared
```

The process gets a row in `processes/README.md`. The first share adds `roadmap-customers.html` beside the page.

## How it stays current

Ask for the roadmap, or press Refresh on the page. Both run `processes/roadmap.md` on the page. Only the parts the template writes change. Lines the team changed stay as they are. Once the customer version exists, each run offers to refresh it too.

## Example

[`preview.html`](preview.html) is the page after a run, with made-up content for Halden, a made-up software company.

> When a customer asks when, I send the customer view. It says the quarter and nothing I will regret.
>
> Anna Moen, Head of product, Tromsø Digital (made up)
