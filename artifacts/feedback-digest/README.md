---
title: Feedback digest
summary: The week's customer feedback sorted into themes, with the quotes, the counts, the trend and the issue each one points to.
category: product
order: 5
tags: [feedback, customers, slack]
connectors: [slack, hubspot, transcripts, linear]
request: "Sort this week's feedback from #feedback, the support inbox and the calls into themes with quotes and counts, and link each theme to its issue."
type: artifact
artifact_kind: page
version: 2611092
author: Silja Hürlimann
updated: 2026-11-09
also: [marketing]
---

# Feedback digest

The week's customer feedback sorted into themes, with the quotes, the counts, the trend and the issue each one points to.

## What it makes

One page that holds this week's feedback: three numbers, then the themes, the largest first. Each theme shows its count, its customers, its trend and its issue, and opens to the best quotes. **Over time** shows each theme's count for the last six weeks, so a theme that rises or fades is easy to see.

For each theme, the process finds the issue it belongs to or files a new one, with the quotes and the customers attached. It always shows the list first and acts after a yes.

## The request

> Sort this week's feedback from #feedback, the support inbox and the calls into themes with quotes and counts, and link each theme to its issue.

Said in the person's own words.

## What it reads

- **Slack**: the feedback channel and the customer channels.
- **HubSpot**: the support inbox and the CRM notes.
- **Transcripts**: the customer calls of the week.
- **A space with a `user-feedback/` folder**: that folder, when the workspace has one. The page reads it and never changes it.
- **Linear or Jira**: the issues and projects the themes point to.

Every source is optional. Without the support tool, the digest is built from Slack and the calls and says what it did not read. A theme without an issue says so.

## What lands in the workspace

In the folder the person picks, for example `spaces/product/`:

```
feedback-digest.html             the page
processes/feedback-digest.md     how the page is written, refreshed and linked to issues
```

The process gets a row in `processes/README.md`.

## How it stays current

Ask for this week's feedback digest, or press Refresh on the page. Both run `processes/feedback-digest.md` on the page. Only the parts the template writes change. Lines the team changed stay as they are. Every Friday the new week replaces the themes, and its counts join **Over time**.

## Example

[`preview.html`](preview.html) is the page after a run, with made-up content for Halden, a made-up software company.

> The themes with the counts over four weeks settled an argument we had been having for a month.
>
> Noor Haddad, Head of product, Fjord (made up)
