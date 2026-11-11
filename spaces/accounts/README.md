---
title: Accounts
summary: An accounts space for your workspace, with your sales approach, call prep, account health and a review of every account, built on your customer folders.
category: sales
order: 1
tags: [accounts, sales, customer-success, calls]
request: "Set up an accounts space for our sales team: deals and contacts live in HubSpot, our calls are recorded in Gong, and our sales playbook is a Google Doc."
type: space
folder: accounts
version: 2611111
author: Palette
license: MIT
updated: 2026-11-11
---

# Accounts

An accounts space for your workspace, with your sales approach, call prep, account health and a review of every account, built on your customer folders.

Built for sales and customer success teams that work with AI agents, so what one person learns about an account is there for the next call, whoever takes it.

## What you get

- **Your sales approach** for before, during and after a call: the questions to ask about the problem you solve, the signals that qualify a lead, and what you don't do. It links to your products, your ideal customer and your messaging instead of copying them.
- **A brief before every call**, with where the account stands, who is on the call, what they care about, what to ask and the next step to land. It is written from the account's brief, its last two meetings and your sales approach.
- **A health read for each account**: usage, communication and engagement, each with its source and the date it was checked, and a flag when the signals no longer match the account's stage.
- **A plan for the accounts that need one**: what you are trying to achieve, your current bet and the risks, in the account's brief where every call brief reads it.
- **A review of every account**, grouped by stage, with the next steps that are past due and the accounts that have gone quiet. Nothing changes without your yes.
- **Lessons and a log for selling.** Corrections land in the space's `lessons.md` and what happened in its `log.md`. A question that worked is proposed for the sales approach, and a person approves it.

## The request

> Set up an accounts space for our sales team: deals and contacts live in HubSpot, our calls are recorded in Gong, and our sales playbook is a Google Doc.

Said in the person's own words. One account you are working on now is enough to start.

## What it reads

- **A CRM such as HubSpot, Salesforce, Pipedrive or Attio** — the stage, the contacts and the deals, when your workspace says the CRM owns them. A brief links to the record and keeps a dated snapshot, never a second copy.
- **Call notes** — from a notetaker or a call recorder, logged as each customer's meeting notes.
- **Email, chat and the calendar** — the last touch with an account, and who is coming to a call.
- **Product analytics** — usage, for an account's health, when the tool is connected.
- **Notion or Google Docs** — an existing sales playbook, sorted into your sales approach after a yes.

Without a CRM, the customer briefs hold the stage and the contacts. Without an existing playbook, the starter sales approach is the first version.

## What lands in the workspace

The space installs as `spaces/accounts/`. An earlier `spaces/accounts/` is replaced; Palette Desktop takes a checkpoint first, so you can undo.

```
spaces/accounts/
├── README.md        # the front door
├── AGENTS.md        # how to work accounts here; adds to the root rules
├── CLAUDE.md · GEMINI.md   # pointers so each agent loads AGENTS.md
├── SETUP.md         # present only while the space is being set up
├── playbooks/       # the sales approach
├── processes/       # preparing a call, reading an account's health, reviewing every account
├── templates/       # the formats for an account's plan and health
├── lessons.md       # what to do differently here
└── log.md           # what happened here
```

Nothing is placed outside `spaces/accounts/`. The accounts themselves stay in your workspace's `customers/`, one folder each, and the space brings no sample accounts.

## How setup works

After install, a session adds Accounts to your list of spaces and starts its setup. Tell it what you have:

- How your team sells: the questions you ask, the signals that make a lead worth pursuing, and what you won't do.
- Which tool keeps your pipeline and contacts: a CRM, or none.
- The accounts you are working on now.
- Where your existing sales playbook is, if you have one.

The agent writes your sales approach with you, records which tool owns the stage and the contacts, and adds your first accounts to `customers/` once you have seen the list. It also points the rows for call prep and account reviews in `customers/README.md` at the space, so work that starts from a customer finds your approach, and makes a quiet account Paused rather than archived. If another space already has a sales playbook, it shows you both and asks which one the team keeps. Pages it writes stay marked "Not confirmed yet" until someone on the team has read them.

## Part of your workspace

- Your workspace's rules still apply. The space's own `AGENTS.md` adds how to work an account, and agents read it whenever they work in the space.
- Your accounts are your workspace's customer folders, each with its brief and its meeting notes. The space adds a plan and a health read to a brief when there is something real to put in it.
- Adding an account and logging a call use your workspace's own steps: "we just signed a new customer", "here are my notes from the call".
- The space links to your products, your ideal customer and your messaging in `company/` instead of copying them.

## Every call from the same approach

Agents read the account's brief and your sales approach before a call brief, a health read or a review.

- "Prepare me for Thursday's call: where we are, who's coming and what to ask."
- "Here are my notes from the call. Log them and update the plan."
- "How are our onboarding accounts doing?"
- "Which accounts have gone quiet, and which next steps are past due?"

Everything is plain markdown you can read and edit, with or without Palette.
