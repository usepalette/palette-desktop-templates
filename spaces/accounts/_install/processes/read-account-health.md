---
type: process
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
read_when:
  - "Someone asks how an account is doing"
  - "A renewal, a review or a hard call is coming up"
---

# Read account health

How an account is doing, read from the signals that show it and written into the **Health** section of its brief. It also says when the signals no longer match the account's stage.

## When to run this

- Someone asks how an account is doing: "how is [customer] doing?", "refresh [customer]'s health".
- Before a renewal, a review or a call where it matters, or when [`review-accounts.md`](review-accounts.md) flags an account.

## Steps

1. **Find the account** in [`customers/`](../../../customers/README.md). Health is read for an account with a folder; when there is none, say so.
2. **Find the sources.** [`company/tools.md`](../../../company/tools.md) says which tool owns usage (product analytics), which owns contacts and stage (a CRM), and where conversations happen (email, chat).
3. **Read each signal from its source,** and note the source and the date you read it:
   - **Product usage:** the analytics tool, through its connector. Without one, the latest meeting note or what the person tells you, named as the source. Active, Inactive or Unknown.
   - **Communication:** the brief's Activity and the latest meeting notes, and the email or chat tool when it is connected. Recent, Stale or None.
   - **Engagement:** the meeting notes and Activity: who comes to the calls, how fast they answer, whether they do what they said. High, Medium or Low.

   A source you can't reach keeps its last value and date, or Unknown when there is none. Never fill a signal from a guess.
4. **Write the Health section.** Replace the section with the new read; when the brief has none, copy the format from [`../templates/account-health.md`](../templates/account-health.md). Set the status and the flag, and stamp the brief's `last_updated` and `last_updated_by`.
5. **Check the stage.** When the signals contradict it, such as Active with communication None, or Paused with a call last week, say so in the flag and offer to change the stage. After a yes, change it in the brief and in its row in [`customers/README.md`](../../../customers/README.md). When a CRM owns stage, the change is made in the CRM: show the exact change first, as the root rules say for a write in a tool, then copy the new value into the brief's `stage` with its `source` and `source_checked`.
6. **Say what changed:** the status, each signal that moved, and the flag.

## Done when

- Every signal has a value, a source and the date it was checked, or says Unknown.
- The status and the flag are set.
- A stage the signals contradict has been raised, and changed only after a yes.
