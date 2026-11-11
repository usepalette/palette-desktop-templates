# accounts

The accounts space inside the company OS: how the team works its accounts, from the sales approach to preparing a call, reading an account's health and reviewing every account. The accounts themselves are customer folders in the root [`customers/`](../../customers/README.md). **Company-wide rules live in the root [`AGENTS.md`](../../AGENTS.md) and always apply**; this file adds how to think and behave here. For what lives where, see [`README.md`](README.md).

## Posture

Work as someone on the team who knows every account and how the team sells. Understand the customer's world before talking about ours. This space exists so that what one person learns about an account, or about selling, is there for the next call, whoever takes it.

## Before account work

The root rules say who the person is and what to read first. Then, in this order:

1. **If `SETUP.md` exists in this folder, read it.** The accounts space is still being set up. Setup never blocks the task the person came with.
2. **For work on one account**, read its brief, `customers/<name>/README.md`, then its meeting notes as far as the task needs. [`company/tools.md`](../../company/tools.md) says which tool owns its stage, contacts and usage: read that tool when you can reach it.
3. **For a call, a follow-up or a plan**, read [`playbooks/sales-approach.md`](playbooks/sales-approach.md) as well.

## Rules

- **The sales approach shapes every call brief.** What to ask, how to qualify and which next step to land come from [`playbooks/sales-approach.md`](playbooks/sales-approach.md), chosen for the account, never a generic list. While it still says **Not filled in yet**, say so and use only the lines that are written.
- **The brief stays short and scannable.** It is the one page someone reads to understand an account: under about 120 lines, with the detail in the meeting notes. What they care about is one line per theme. A snapshot such as How they work is replaced when it changes, never added to.
- **Open questions are a working list.** Remove an item when it is answered or done. A task lives in the task home named in [`company/tools.md`](../../company/tools.md), and the brief links to it.
- **Never invent people, dates or signals.** A bracket is better than a confident guess. A value read from a tool carries its source and the date it was checked.
- **Only a real engagement gets a folder.** Meetings have happened, a shared channel exists, or they have signed: [`customers/README.md`](../../customers/README.md) → When to create a folder.
- **One home per fact.** When a CRM owns stage or contacts, the brief links to the record and shows a dated snapshot; never keep a second copy. A change there is a write in the CRM: show it first, and make it after a yes.
- **Start from the company context.** What we sell, who it is for and how we describe it are in [`company/products/`](../../company/products/README.md), [`company/market/ideal-customer.md`](../../company/market/ideal-customer.md) and [`company/brand/messaging.md`](../../company/brand/messaging.md). Link to them; never copy them here.
- **Follow a process when one exists, and use the template when one exists.** Check [`processes/README.md`](processes/README.md) and [`templates/README.md`](templates/README.md).

## Where to read for a task

| When the task is… | Read |
|---|---|
| Setting up the accounts space | `SETUP.md` if it exists |
| Adding an account | [`customers/README.md`](../../customers/README.md) → Add a customer |
| Logging a call or a meeting | [`company/meetings.md`](../../company/meetings.md), then the brief: the Now line, Activity, and the Plan, Health or Timeline when the call changed them |
| Preparing a call | [`processes/prepare-a-call.md`](processes/prepare-a-call.md) |
| Reading how an account is doing | [`processes/read-account-health.md`](processes/read-account-health.md) |
| Reviewing the accounts, or finding the ones that have gone quiet | [`processes/review-accounts.md`](processes/review-accounts.md) |
| Writing an account's plan | [`templates/account-plan.md`](templates/account-plan.md) |
| Qualifying a lead, or deciding what to ask | [`playbooks/sales-approach.md`](playbooks/sales-approach.md) |
| Writing to a customer | [`company/brand/voice.md`](../../company/brand/voice.md), and `people/<name>/tone-of-voice.md` when it goes out under someone's name |

## Updating this space

- A better way of selling, or a question that worked → the sales approach, shown to the person first and written after their yes. A better way of doing something → the process.
- What we learned about one customer → their brief, never here.
- A correction about working here → [`lessons.md`](lessons.md). A decision or a change → [`log.md`](log.md).
- A rule the person states for working here → this file, under **Rules**. What is here and where things go → [`README.md`](README.md).

Keep this file short. Detail belongs in the pages it links to.
