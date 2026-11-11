---
type: process
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
cadence: ""
---

# Capture feedback

Saves one new piece of product signal as it came, links it to its company and to any explicit ask, and brings the dashboard up to date. It runs whenever someone passes on what a user said.

## When to run this

- Someone passes on what a user said: "a customer just told me…", "capture this feedback", "save this from support".
- Someone hands over interview notes, a research session or a call recap: "here are my notes from the interview".
- Someone points to a message, a ticket, an email or a meeting note in the workspace that holds feedback. A meeting note stays where it is; the capture names it as its source.

It captures. Finding the pattern across several sources is [synthesise feedback](synthesise-feedback.md).

## Steps

1. **Load the playbook.** Read [`../playbooks/feedback-synthesis.md`](../playbooks/feedback-synthesis.md) before you interpret the source.
2. **Read the source.** Use the text in the request, a file the person names, or a connected tool they asked you to read. Take out:
   - the date, the source (chat, interview, email, support, call or other) and its link or reference
   - the capture mode: verbatim, paraphrase or summary
   - the person and the company, the topic, the tags and the sentiment
   - each explicit feature request
   - the pains it suggests, without assuming they recur

   A source with no date gets today's date, and you say it is the capture date. An identity you don't know is `Unknown`, and you say why; never guess one. With no link or reference, `source_url` is `unavailable`.
3. **Keep only what may be shared.** Keep the product context everyone who reads the space may see. Never copy credentials, private personal details, restricted transcript text or a whole raw export: link to the source, anonymise or summarise.
4. **Show the capture.** Show the metadata, where it goes, the text as it will be saved, the explicit asks and anything you assumed. Write after a yes. When the person handed you the words themselves and nothing is uncertain, a one-line summary of the plan is enough.
5. **Save the raw source** from its folder's mold.
   - An interview goes to `user-feedback/user-interviews/`, from the mold there. Everything else goes to `user-feedback/feedback/`, from `user-feedback/_template.md`.
   - Name it `YYYY-MM-DD_company_person_topic.md`: each field in lowercase kebab-case, underscores only between the fields.
   - Keep `source_url` and `capture_mode`. Exact quotes go under `## Their words`; a summary or a paraphrase never becomes a quote.
   - Set `status: active` and delete the mold box: the person has seen the capture.
6. **Handle each explicit ask.** Search `user-feedback/feature-requests/` for the same underlying job. If it exists, add the new source to its `source_files` and update its evidence. If not, create `YYYY-MM-DD_company_topic.md` from the mold in that folder.
7. **Leave the pattern for later.** Never make a recurring painpoint from one casual comment. Say which pains could be checked with [synthesise feedback](synthesise-feedback.md).
8. **Update the company's profile.** Create or update `user-feedback/_companies/<company>.md` from its mold, named in lowercase kebab-case. Link the raw source and any request you created or updated, and add only the context needed to read the feedback. If the company is a customer with a folder in `customers/` at the workspace root, link its brief; never copy from it.
9. **Rebuild the dashboard** with [rebuild the feedback dashboard](rebuild-feedback-dashboard.md).
10. **Say what you did:** the raw source file, the requests created or updated, the company profile, the pains left for synthesis, and what stayed unknown or uncertain.

## Done when

- The source is saved once, in `user-feedback/feedback/` or `user-feedback/user-interviews/`, with its link or `unavailable`, and with no quote that isn't verbatim.
- Each explicit ask is in one feature request that lists this source.
- The company's profile links the source.
- The dashboard shows the new entry.
