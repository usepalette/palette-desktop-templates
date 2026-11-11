# Setting up Accounts

What the agent does in the session that installs this template. Read it with the template's README.

The app placed the Accounts space at `spaces/accounts/`, the home inside the company OS for how the team works its accounts. It holds the team's sales approach (`playbooks/`), the steps for preparing a call, reading an account's health and reviewing every account (`processes/`), and the formats for an account's plan and health (`templates/`). The accounts themselves are the workspace's customers, one folder each in `customers/`, made the way `customers/README.md` says; the install adds none. Nothing was placed outside `spaces/accounts/`.

It ships as a **first version**: the sales approach is a starter playbook marked "Not filled in yet", with brackets for the team's own questions and signals; the processes work from day one; the two formats in `templates/` are molds. There is no sample data.

## What to do

1. **Say what it is.** Tell the person in one or two sentences what the Accounts space is: how the team sells and works its accounts, on top of the customer folders the workspace already keeps. Don't read `AGENTS.md` or the README to them.

2. **If the install replaced an accounts space,** the app says so in its message. Say in one line that the earlier `spaces/accounts/` was replaced and that the checkpoint before the install still holds it. Offer to bring back pages from it, such as its `lessons.md`, `log.md` or its sales approach, and copy them only after a yes. Never copy them without asking.

3. **Register the space**, the way `spaces/README.md` → Add a space, steps 7 and 8, describes. The space is already in place: don't copy `spaces/_template/` and don't recreate any of its files.
   - Its name is Accounts, its folder `spaces/accounts/`, and what it is for: how the team works its accounts, with the sales approach, call prep, account health and reviews. Its edit policy is `team`.
   - Its owner is the person installing unless they name someone else. Ask in the same round as the setup questions in step 6, not as a question of its own.
   - Add its row to the list of spaces in `spaces/README.md`, the area and its owner to **Areas and owners** in `company/how-we-work.md`, and one dated line to `spaces/log.md`. If either list already has a row for Accounts, which happens when this install replaced an accounts space, update that row; never add a second one. If **Areas and owners** already lists the area this space serves, such as sales, with no space in it, put `spaces/accounts/` in that row instead of adding one.
   - Point the customer pages to the space, so work that starts from a customer finds the team's approach. In `customers/README.md` → You need to…, the **Prepare for a call** row goes to `spaces/accounts/processes/prepare-a-call.md`, the **See where every customer stands** row adds `spaces/accounts/processes/review-accounts.md`, and one new row, for knowing how a customer is doing, goes to `spaces/accounts/processes/read-account-health.md`. In its **Conventions**, the line on a customer that goes quiet changes to how this space works: a customer that goes quiet keeps its folder at the **Paused** stage, and only one that leaves or says no gets `status: archived`, with its row moved to the bottom of the table. Stamp the page.

4. **Keep one sales playbook.** Read the list of spaces in `spaces/README.md`. If another space there already keeps a page on how the team sells, such as a GTM space's `spaces/<space>/playbooks/sales.md`, show the person what each page says, side by side, and ask which one is the home, in the same round as the questions in step 6. After the answer:
   - The space whose page is not the home links to the home from its `README.md` and `AGENTS.md`, and every page there that linked to its own copy links to the home instead. In this space, those are the pages that link to `playbooks/sales-approach.md`.
   - Offer to move into the home what only the other copy says. The copy is removed only after a yes, with its row in its folder's `README.md`.
   - This space reads two parts of the sales approach by name: **What we sell** and **Discovery questions**. When the other space's page is the home and has no part by that name, move that part into the home under the same name before this copy goes, so call prep still finds it.

   When no other space keeps one, skip this step without mentioning it.

5. **Stamp every page.** In each page under `spaces/accounts/` that has frontmatter, `[Owner]` becomes the owner, `last_updated` becomes today and `last_updated_by` becomes the person you are working for. Leave the molds as they are: `playbooks/_template.md`, `processes/_template.md` and `templates/_template.md`, and the two formats `spaces/accounts/templates/account-plan.md` and `spaces/accounts/templates/account-health.md`, whose slots are filled when a brief gets the section. Never change `template` in `spaces/accounts/README.md`: the app reads it to find the space and its version.

6. **Start the accounts setup now**, following `spaces/accounts/SETUP.md` as written. The person's profile is the one in the root `people/`; if they have none yet, the root rules make it. Then ask once for what the request didn't already say: how the team sells (the questions they ask, the signals that make a lead worth pursuing, what they won't do), which tool keeps the pipeline and the contacts, the accounts they are working on now, and where an existing sales playbook is, if there is one. Whatever they have is enough to start: one account is fine. Show what you would write, and where, and write after their yes; never invent a customer, a contact, a stage or a signal.

   A `SETUP.md` at the workspace root is the company's setup, separate from this one. If it is still running, the accounts space now counts as its first space. `company/tools.md` is one of its pages: fill only the rows the person gave you facts for, and leave its box to the company's setup.

7. **Sum up the first pass:**
   - Where the space is listed, and who owns it.
   - What you filled in, and which pages still say "Not filled in yet" or "Not confirmed yet" and need a person to read them.
   - That the accounts live in `customers/`: "we just signed a new customer" adds one, and "here are my notes from the call" logs a call and updates the brief.
   - How the space grows: a better way of selling goes into the sales approach after a yes, a correction into the space's `lessons.md`, and what happened into its `log.md`.

## Notes

- The root `AGENTS.md` always applies; `spaces/accounts/AGENTS.md` adds how to work accounts, and the `CLAUDE.md` and `GEMINI.md` beside it point to it.
- Accounts are customers like any other: their folders live in the root `customers/`, never in the space. Core's `new-customer` adds one and `new-meeting` logs a call. The space adds a **Plan** and a **Health** section to a brief when there is something real to put in them.
- A CRM keeps what it owns. `company/tools.md` says which tool owns stage and contacts; the brief links to the record and keeps a dated snapshot, never a second copy.
- `spaces/accounts/SETUP.md` is deleted when the accounts setup is done. Until then, the next agent to work in the space picks setup up where it stands.
