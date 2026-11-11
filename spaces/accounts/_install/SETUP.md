---
type: doc
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
read_when:
  - "This file exists: the accounts space is still being set up"
---

# Setup

**While this file exists, the accounts space is still being set up.** This page says how to set it up and when to delete this file. It keeps no progress of its own: the pages are the progress. With the person, talk about setting up the accounts space, never about this file.

This is the accounts space's setup only. A `SETUP.md` at the root of the workspace is the company's setup: separate from this one, and not finished by it.

## Before the steps

The person needs a profile in the root [`people/`](../../people/README.md); the root rules make one if they have none. Use what the workspace and its connected tools already say, and what the person has told you; then ask once for the rest: how the team sells (the questions they ask about the problem the product solves, the signals that make a lead worth pursuing, what the team won't do), which tool keeps the pipeline and the contacts, if any, the accounts they are working on now, and where an existing sales playbook is, if there is one. Whatever they have is enough to start: one account is fine.

## The steps

1. **Write the sales approach.** Fill [`playbooks/sales-approach.md`](playbooks/sales-approach.md) with the person, following its box: their discovery questions, their qualification signals and what the team won't do, in their words. Keep the starter thinking they agree with and change the rest. An existing sales playbook is material to bring in: show where each part would go, and write after their yes.
2. **Say which tool owns stage and contacts.** Write it in the **Customer records and pipeline** row of [`company/tools.md`](../../company/tools.md): the CRM and the fields it owns, or the customer briefs when there is no CRM. If that page still has its box, fill only this row and any other row the person gave you a fact for, such as where call notes come from, and leave the box: the rest of the page belongs to the company's setup. When there is a CRM, check that you can read it, and say so if you can't.
3. **Add the first accounts.** One folder per account with real engagement, the way [`customers/README.md`](../../customers/README.md) → Add a customer says. From a CRM, show the list you would add and wait for a yes; a name with no conversation behind it stays in the CRM. When the person says what the team is trying to achieve with an account, add a **Plan** section to its brief from [`templates/account-plan.md`](templates/account-plan.md).

Show the pages you wrote and ask the person to read them. A page they agree with loses its "Not confirmed yet" box.

The sales approach and every call brief read who the company sells to and what it sells. While [`company/market/ideal-customer.md`](../../company/market/ideal-customer.md) still says **Not filled in yet**, or [`company/products/`](../../company/products/README.md) has no product in it, offer to fill them, following each page's own box, after a yes.

## Not part of setup

Reading an account's health and reviewing every account run when someone asks for them, from the first day. The processes and the two formats work as they are: change them as the team works.

## When to delete this file

When the three steps are done, or when someone says the accounts space is set up, delete this file and add one line to this space's [`log.md`](log.md) saying that setup ended and what was left open. "I'll do the rest another day" means setup goes on: leave the file where it is.

If the person came to do something else, do that first. Then say in one line where setup stands and offer the next step.
