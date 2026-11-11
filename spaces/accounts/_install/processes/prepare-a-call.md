---
type: process
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
read_when:
  - "Someone has a call coming up with a customer or a lead"
---

# Prepare a call

A brief for one call: where the account stands, who is on the call, what they care about, what to ask and the next step to land. It is written from the account's brief, its last two meetings and the team's sales approach, so it sounds like the team and not like a generic playbook.

## When to run this

- Before a call with a customer or a lead: "prepare me for my call with [customer]", "prep the [customer] call".

## Steps

1. **Find the account.** Match the name to a folder in [`customers/`](../../../customers/README.md), or to the `domain` in a brief, and ask when two could fit. With no folder yet, as before a first call, work from what the person tells you and what is public about the company, such as its website and recent news when you can reach the web, then go to step 4. Don't make a folder for a call that hasn't happened: the meeting note after it does, when there is real engagement.
2. **Read the brief,** `customers/<name>/README.md`: the **Now** line, Key people, What they care about, the sections this space adds when it has them (**Plan**, **Health**, How they work, Timeline), Open questions and task links, and Activity.
3. **Read the last two meeting notes.** Follow the newest lines in Activity: a call held for a project has its note in `projects/<project>/meetings/`.
4. **Read what a tool owns.** When [`company/tools.md`](../../../company/tools.md) says a CRM owns stage or contacts, read the record and note the date. When the calendar is connected, the invite says who is coming; a live-context connector, when there is one, adds what changed since the last note. If a tool can't be reached, say so and use the brief's dated snapshot.
5. **Read the sales approach,** [`playbooks/sales-approach.md`](../playbooks/sales-approach.md): the questions, the qualification signals and what we don't do, and the company pages its **What we sell** links to, as far as the call needs them. While it still says **Not filled in yet**, use the lines that are written, never its brackets, and say in one line that the team's own questions are not in yet.
6. **Write the brief in the conversation,** in these parts:
   - **Where we are:** the stage, the relationship in two or three lines, and the open questions
   - **Who is on the call:** each person's role and their part in the relationship, such as champion, sponsor or user
   - **What they care about:** from the brief, in their words
   - **What to ask:** three to five discovery questions from the sales approach, chosen for this account's stage and open questions, never a generic list
   - **Watch out for:** what the Health section flags, the Plan's risks, and any follow-up we owe them
   - **The next step:** one specific action to land on the call, as the sales approach says

   Every line comes from what you read. Mark a line you worked out yourself "(to confirm)", and leave out a part you have nothing for.
7. **Keep it only if asked.** Then save it in the person's `people/<name>/scratchpad/` as `YYYY-MM-DD-<customer>-call.md`, with a line in the scratchpad's index. After the call, offer to log it: "here are my notes from the call" writes the meeting note and updates the brief.

## Done when

- The person has the brief before the call, with every part there was material for.
- Each line traces to the brief, a meeting note, a tool or the sales approach; nothing is invented.
- Nothing was saved unless the person asked.
