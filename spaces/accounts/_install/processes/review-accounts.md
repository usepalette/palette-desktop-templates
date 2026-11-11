---
type: process
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
read_when:
  - "Someone asks where the accounts stand, who has gone quiet or what is past due"
  - "Before a meeting where the team goes through its accounts"
---

# Review accounts

Where every account stands, grouped by stage, with the next steps that are past due and the accounts that have gone quiet. It reads the list of customers and each brief, and changes nothing without a yes.

## When to run this

- Someone asks where the accounts stand: "where do our accounts stand?", "who has gone quiet?", "what's in onboarding?"
- Before a meeting where the team goes through its accounts, when [`company/how-we-work.md`](../../../company/how-we-work.md) lists one under Rituals.

## Steps

1. **Read the list.** The Customers table in [`customers/README.md`](../../../customers/README.md): one row per account, with its stage, owner and Now line. Leave out the archived accounts at the bottom, unless the person asks for them.
2. **Read the stage from its home.** When [`company/tools.md`](../../../company/tools.md) says a CRM owns stage, read it there and note the date. If the CRM can't be reached, use the brief's `stage` and say how old it is.
3. **Open each brief,** `customers/<name>/README.md`: the Now line, the newest Activity line (the last touch), the Health status and flag, and the open questions and task links. Read the linked tasks in the task home for their due dates.
4. **Show the accounts by stage,** in the order Lead, Engaged, Onboarding, Active, Paused, or in the CRM's own order when it owns stage. One line per account: the name, the owner, the last touch, the next step and its date, and the health when there is a read.
5. **Then what needs attention,** most urgent first:
   - a next step whose date has passed, or an account with no next step at all
   - an account with no touch for longer than the rhythm its Activity shows
   - a Health status of At risk, or a flag
   - a stage the signals contradict
   - a date coming up in a brief's Timeline, such as a renewal
   - a row in the table that disagrees with its brief, or a folder in `customers/` with no row
6. **Answer a narrower question by filtering.** "Who has gone quiet?" is only the quiet ones; "what's in onboarding?" is only that stage.
7. **Propose the fixes, and make each one after a yes:** a table row, a stage, a Now line, a task's date. A change in the CRM or the tracker is a write in that tool: show the exact change first.
8. **Keep the review in the conversation.** When it was for a team meeting, its note goes where [`company/meetings.md`](../../../company/meetings.md) says the work of a space goes: a meetings folder in this space, made from the shared meeting mold the first time.

## Done when

- Every live account is in the review, with its stage, last touch and next step.
- What needs attention is listed, most urgent first.
- Nothing was changed without a yes.
