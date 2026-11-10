---
title: Release notes
summary: What shipped this week, written for customers from the pull requests and the issues, with the internal version a click away.
category: product
order: 4
tags: [release, changelog, github]
request: "Write this week's release notes for customers from the merged PRs and the closed issues, and tell me who asked for each thing."
type: artifact
artifact_kind: page
version: 2611102
author: Kaspar-Jon Dremstrup
updated: 2026-11-10
also: [marketing]
---

# Release notes

What shipped this week, written for customers from the pull requests and the issues, with the internal version a click away.

## What it makes

One page that holds the week for customers: new, improved and fixed, each line in plain words with its area. Filters show one area at a time. Below, the team's internal version lists the pull requests, the issue keys and who did each one, and every line says which customers asked for it. Every Friday the new week goes on top, and the week before moves into **Earlier weeks**.

After a yes, the notes go to the changelog and the announcements channel, and by mail when asked. The first publish also writes `release-notes-customers.html`, the page without the internal parts. Each customer who asked for something gets a short note, also after a yes.

## The request

> Write this week's release notes for customers from the merged PRs and the closed issues, and tell me who asked for each thing.

Said in the person's own words.

## What it reads

- **GitHub**: the pull requests merged this week, with their title, author and description.
- **Linear or Jira**: the issues closed this week, for the area and the customer requests.
- **Slack**: the feedback channel, for who asked for each thing, and the announcements channel to publish to.

Every source is optional. Without GitHub, the notes are written from the closed issues. Without the feedback channel, the lines do not say who asked, and the run says so.

## What lands in the workspace

In the folder the person picks, for example `spaces/product/`:

```
release-notes.html             the page
processes/release-notes.md     how the page is written, refreshed and published
```

The process gets a row in `processes/README.md`. The first publish adds `release-notes-customers.html` next to the page.

## How it stays current

Ask for this week's release notes, or press Refresh on the page. Both run `processes/release-notes.md` on the page. Only the parts the template writes change. Lines the team changed stay as they are. Each publish writes the customer version again.

## Example

[`preview.html`](preview.html) is the page after a run, with made-up content for Halden, a made-up software company.

> Fourteen PRs became four lines customers understand, and it told me who to send them to.
>
> Ola Nygaard, Product marketing, Kappa (made up)
