---
type: index
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
template: accounts@2611111
---

# Accounts

How the team works its accounts: the sales approach, preparing a call, reading an account's health and reviewing every account. The accounts themselves are not here: each one is a customer folder in [`customers/`](../../customers/README.md), with its brief and its meeting notes. This space is how the team works them.

Company-wide rules live in the root [`AGENTS.md`](../../AGENTS.md) and always apply. How to think and behave *in this space* is in this folder's [`AGENTS.md`](AGENTS.md).

## Get started

While `SETUP.md` exists in this folder, the space is still being set up. Say "set up the accounts space" and tell the agent what you have: how your team sells, which tool keeps your pipeline and contacts, and the accounts you are working on now. One account is enough to start.

Each page you have not set up yet opens with a box saying so. The box tells the agent what to do with the page and goes once a person has read it.

## You need to…

| You need to… | Go to |
|---|---|
| Understand how to think and work in this space | [`AGENTS.md`](AGENTS.md) |
| Know how the team sells: the thinking, what to ask, what qualifies a lead | [`playbooks/sales-approach.md`](playbooks/sales-approach.md) |
| Prepare for a call with a customer or a lead | [`processes/prepare-a-call.md`](processes/prepare-a-call.md). Say "prepare me for my call with [customer]" |
| Know how an account is doing | [`processes/read-account-health.md`](processes/read-account-health.md). Say "how is [customer] doing?" |
| See where every account stands, and what has gone stale | [`processes/review-accounts.md`](processes/review-accounts.md). Say "where do our accounts stand?" |
| Add an account | Say "we just signed a new customer"; the steps are in [`customers/README.md`](../../customers/README.md) → Add a customer |
| Log a call or a meeting | Say "here are my notes from the call"; [`company/meetings.md`](../../company/meetings.md) says where the note goes |
| Write what we are trying to achieve with an account | [`templates/account-plan.md`](templates/account-plan.md) |
| Understand one account fast | its brief, `customers/<name>/README.md`: the **Now** line, then its Plan and Health |
| Capture how something is done here | Say "let me explain how we do this"; **Capturing how the work is done** below says where it goes |
| Record a correction about working here | [`lessons.md`](lessons.md) |
| Record a decision or a change | [`log.md`](log.md) |

## The accounts

Each account is a folder in [`customers/`](../../customers/README.md), made by the workspace's own steps when someone says "we just signed a new customer": the brief, `customers/<name>/README.md`, and one note per meeting in `customers/<name>/meetings/`. Your team may say accounts or clients; the folder stays `customers/`. A folder starts when there is real engagement. A name in the CRM with no conversation behind it stays in the CRM.

A brief grows with the relationship. This space adds four sections to it, each only when there is something real to put in it, after **What they care about** and in this order:

| Section | What it holds | How it is written |
|---|---|---|
| **Plan** | What we are trying to achieve with them, what we are doing about it now, and what could get in the way | the format in [`templates/account-plan.md`](templates/account-plan.md) |
| **Health** | How the account is doing: usage, communication and engagement, each with its source and the date it was checked | the format in [`templates/account-health.md`](templates/account-health.md), kept current by [`read-account-health`](processes/read-account-health.md) |
| **How they work** | Their tools, their rhythm and how their team is organised | three lines, **Tools**, **Rhythm** and **Team**, replaced when they change, never added to |
| **Timeline** | The dates that shape the relationship: when they signed, went live, renew | one dated line per milestone, in date order |

Material made for the customer to see, such as a proposal or a summary, goes in `customers/<name>/shareables/`, a folder made with its own `README.md` when there is a first thing to share. Heavy files stay in the drive [`company/tools.md`](../../company/tools.md) names, linked from there.

## Stages

An account's stage is the `stage` field in its brief. When [`company/tools.md`](../../company/tools.md) says a CRM owns stage, the CRM's value is the real one, and the brief shows it with the date it was checked. Without a CRM, these are the stages:

| Stage | What it means |
|---|---|
| **Lead** | We have been in touch, with no shared interest yet |
| **Engaged** | Conversations are happening, and the interest is mutual |
| **Onboarding** | They have signed and are getting started |
| **Active** | They use the product, and we are in regular contact |
| **Paused** | They went quiet: no recent activity |

An account that leaves, or says no, is archived: `status: archived` in its brief, and its row moves to the bottom of the table in [`customers/README.md`](../../customers/README.md). The folder stays as the record.

## Structure

```
spaces/accounts/
├── README.md        # this front door
├── AGENTS.md        # how to think and behave here: the posture, and the rules that add to the root's
├── CLAUDE.md · GEMINI.md   # thin pointers so each agent loads AGENTS.md
├── SETUP.md         # present only while the accounts space is being set up
├── playbooks/       # how the team sells: the sales approach
├── processes/       # preparing a call, reading an account's health, reviewing every account
├── templates/       # the formats for an account's Plan and Health sections
├── lessons.md       # what to do differently here
└── log.md           # what happened here
```

Add a folder when real work needs one, such as a meetings folder for the team's account reviews, the first time one is noted. Each new folder gets its own `README.md`.

## How what we learn is shared

- **One brief per account, read by everyone.** What one person learns on a call goes into the meeting note and the brief the same day, so the next person to call them starts from it.
- **Every call brief starts from the same approach.** The team asks the questions it agreed on, and qualifies a lead by the same signals.
- **What a call teaches about selling goes up.** A question that worked, or a red flag that proved true, is proposed for the sales approach, and a person approves it.
- **A correction about working here** goes into this space's [`lessons.md`](lessons.md), and what happened into its [`log.md`](log.md).

## Capturing how the work is done

When someone explains, pastes or points at how something is done here, it becomes one file in one of these folders. One explanation often holds two of these (the thinking and the steps): split it into two files that link to each other.

| What you have | It is a | Goes in |
|---|---|---|
| A point of view: what matters, how to choose, what good looks like | playbook | `playbooks/<domain>.md` |
| Steps in an order, with a trigger and a finished state | process | `processes/<name>.md` |
| A format to fill in for a recurring output | template | `templates/<output>.md` |
| Settled facts to load before working, such as how the team splits its accounts | foundation | `foundations/<topic>.md`, in a folder copied the first time from the root's [space mold](../_template/foundations/README.md) |

Write the file from that folder's `_template.md`, in the words of the people who do the work, and add a row to that folder's `README.md`. Never add principles, steps or rules nobody gave you; a gap stays a gap, marked as an open question at the bottom of the file.

## What lives elsewhere

| For… | Go to |
|---|---|
| The accounts: one folder each, with the brief and the meeting notes | [`customers/`](../../customers/README.md) |
| What we sell | [`company/products/`](../../company/products/README.md) |
| Who we sell to, and who is not a fit | [`company/market/ideal-customer.md`](../../company/market/ideal-customer.md) |
| How we describe ourselves, and the proof we can quote | [`company/brand/messaging.md`](../../company/brand/messaging.md) |
| Who else they could choose | [`company/market/competitors/`](../../company/market/competitors/README.md) |
| Which tool owns stage, contacts and usage, and where tasks live | [`company/tools.md`](../../company/tools.md) |
| How meetings are noted | [`company/meetings.md`](../../company/meetings.md) |
| Work for a customer with a start and an end, such as an onboarding or a pilot | [`projects/`](../../projects/README.md) |
| A teammate: who they are and how to work with them | [`people/`](../../people/README.md) |
| A format the whole company uses, such as a one-pager or a customer story | [`company/templates/`](../../company/templates/README.md) |

One fact, one home: read and link across the OS instead of copying.
