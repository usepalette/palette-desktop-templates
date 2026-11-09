---
title: Sprint review
summary: "The cycle's review: planned against done, what carried over and why, what was added, and what is worth showing."
category: product
order: 2
tags: [sprint, cycle, linear, github]
connectors: [linear, github, slack]
request: "Write the review of the cycle that just ended from Linear and GitHub: planned against done, carry-over with reasons, the highlights, per person."
type: artifact
artifact_kind: page
version: 2611093
author: Christian Lomholt
updated: 2026-11-09
---

# Sprint review

The cycle's review: planned against done, what carried over and why, what was added, and what is worth showing.

## What it makes

One page that holds the cycle: four numbers, planned against done for the last six cycles, then what carried over with the reason, what was added and three things worth showing. A second view shows planned, done and carried per person. At the end of each cycle the new cycle goes on top, the chart moves one cycle on, and the cycle before moves into **Earlier cycles**.

After a yes, the carried issues go into the next cycle with their reasons, and the review goes to the team's channel.

## The request

> Write the review of the cycle that just ended from Linear and GitHub: planned against done, carry-over with reasons, the highlights, per person.

Said in the person's own words.

## What it reads

- **Linear or Jira**: the cycle. Planned, done, carried, added, the assignees and the estimates.
- **GitHub**: the pull requests merged in the cycle, with their authors.
- **Slack**: the team channel, for the highlights people mentioned, and where the review goes.

Every source is optional. Without GitHub, the review counts issues only, and the person names the highlights. Without Slack, the person posts the review themselves.

## What lands in the workspace

In the folder the person picks, for example `spaces/product/`:

```
sprint-review.html             the page
processes/sprint-review.md     how the page is written, refreshed and posted
```

The process gets a row in `processes/README.md`.

## How it stays current

Ask for the review at the end of a cycle, or press Refresh on the page. Both run `processes/sprint-review.md` on the page. Only the parts the template writes change. Lines the team changed, and the target under the chart, stay as they are.

## Example

[`preview.html`](preview.html) is the page after a run, with made-up content for Halden, a made-up software company.

> Planned against done over three cycles, with the reasons. The retro got shorter and better.
>
> Mei Lund, Engineering lead, Aalto & Co (made up)
