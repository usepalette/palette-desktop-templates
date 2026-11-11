---
type: process
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
cadence: ""
---

# Synthesise feedback

Turns several raw sources into the smallest useful set of painpoints and feature requests, each linked to its evidence. It runs when a problem keeps coming up, or when someone wants a slice of feedback sorted.

## When to run this

- "We keep hearing this", "what are customers saying about onboarding?", "turn this month's feedback into painpoints".
- After an interview that raised several problems or asks.
- Before a spec or a thesis, when the evidence it needs is still raw.

## Steps

1. **Load the playbook.** Read [`../playbooks/feedback-synthesis.md`](../playbooks/feedback-synthesis.md): its rules decide what graduates.
2. **Choose the sources.** Use the topic, company, tag or files the person gave. With none, list the recent feedback and interviews and ask which slice to take.
3. **Read every selected source in full,** then search the painpoints and requests that exist before proposing anything new.
4. **Show an evidence table,** one row per distinct underlying job or problem:

   | Candidate | Sources | Companies | Explicit ask? | Graduation |
   |---|---:|---:|---|---|
   | [Short problem] | [count] | [count] | yes or no | raw only, request or painpoint |

   Say so when one blocking interview is the only evidence.
5. **Propose, for each candidate:** the item it belongs to, if one exists; whether to create, update, merge or leave it raw; the severity and frequency, or the priority signal, each with a one-sentence reason; and the counter-signal or the limits of the claim. Synthesis is judgement: write nothing before a yes.
6. **Write what was agreed.**
   - Check who can read the destination before customer material goes in. Anonymise names, quotes and links that may not cross to that audience.
   - Respect each file's `edit_policy`: a yes to write is not a yes to edit an `owner-only` file. Ask its owner.
   - Create or update painpoints and requests from the molds in their folders, with their `owner`, `edit_policy` and stamps filled in like a capture. Keep `source_files` complete and relative, and the verbatim quotes as they are.
   - Update every company profile the change touches.
   - Link discovery, strategy, specs or the tracker only where they exist.
7. **Rebuild the dashboard** with [rebuild the feedback dashboard](rebuild-feedback-dashboard.md).
8. **Say what you did:** what was created, updated or merged, and what was deliberately left raw.

## Done when

- Every agreed painpoint and request exists once, with complete `source_files`.
- The company profiles link them.
- The dashboard shows them.
