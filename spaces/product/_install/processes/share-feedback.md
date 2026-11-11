---
type: process
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
cadence: ""
---

# Share feedback

Drafts a short, sourced recap of the feedback on a company, a topic or a tag, from what this space already holds. It is saved or sent only after a yes.

## When to run this

- "Recap the feedback from [a company]", "what have users said about [a topic]? I need it for [the team, the customer, a stakeholder]".
- Before a meeting where the feedback on a topic will come up.

It works from the feedback already saved. A source that isn't saved yet goes through [capture feedback](capture-feedback.md) first.

## Steps

1. **Gather the sources.** For the company, topic or tag asked for, search the feedback, interviews, requests, painpoints and company profiles. Show a numbered list grouped by kind, newest first, and ask which to include.
2. **Read every selected file in full.** Quote only text under `## Their words`, or a raw source captured as `verbatim`. Never turn a summary or a paraphrase into a quote, and keep your reading of the sources apart from what they say.
3. **Check the audience.** Make sure whoever will read the recap may see the names, quotes and source details in it. Anonymise or leave out what they may not.
4. **Draft it,** with only the sections the selection supports:

   ```text
   [Company or topic]: product feedback recap ([date range])

   What users are trying to do
   - [The job or the context]

   What gets in the way
   - [The pain, with its severity and frequency when known]

   What they asked for
   - [The explicit ask, with its priority signal when known]

   Their words
   > "[Verbatim quote]"
   > [Person, company]

   Sources: [N feedback, M interviews, P painpoints, R requests]
   ```

   Keep it easy to scan. Never add a theme the selected sources don't hold.
5. **Ask where it goes.** Show the draft and offer three choices: keep it in the chat, save it in `user-feedback/recaps/`, or send it through a connected messaging tool. Before anything is sent, show the exact text and where it goes, and wait for a yes. Find out which tools are connected rather than assuming one.
6. **To save it,** name the file `YYYY-MM-DD-<company-or-topic>.md`. Make the slug yourself rather than pasting text from the request into the path: lowercase kebab-case, one path segment, and nothing with `/`, `..` or characters outside `a-z0-9-`. Open the file with:

   ```yaml
   ---
   type: doc
   owner: "[Owner]"
   status: active
   date: YYYY-MM-DD
   topic: "[Company or topic]"
   source_files: [every selected source]
   last_updated: YYYY-MM-DD
   last_updated_by: "[Owner]"
   edit_policy: team
   ---
   ```

   Fill in the owner, the dates and the person you are working for. The recap is a message about the evidence, not new evidence.
7. **Say what you did:** what was included, and whether anything was saved or sent. If the person said no, say that nothing outside the workspace changed.

## Done when

- The person has the recap, and it was saved or sent only where they said.
- Every quote in it is verbatim and attributed.
