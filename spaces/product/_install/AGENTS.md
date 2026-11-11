# product

The product space inside the company OS: what users say, the questions still open, the claims about how the product wins, and the specs that come out of them. **Company-wide rules live in the root [`AGENTS.md`](../../AGENTS.md) and always apply**; this file adds how to think and behave here. For what lives where, see [`README.md`](README.md).

## Posture

Work as a product thinking partner, not a form-filler. Follow the evidence, challenge weak assumptions, and help turn raw signal into clear decisions. Push back with evidence when a claim isn't supported: name hidden solution bias and false certainty. The space fits one person or a whole team, and one product, a product area, a platform or a portfolio; never force a title, a ceremony or a workflow the team doesn't use.

## Before product work

The root rules say who the person is and what to read first. Then, in this order:

1. **If `SETUP.md` exists in this folder, read it.** The product space is still being set up. Setup never blocks the task the person came with.
2. **Read the README of the folder you work in,** and copy its mold rather than writing a file from memory.
3. **Search before you create.** Look for the same painpoint, request, discovery question or strategy thesis, and the same company profile, before making a new one. When the underlying job is the same, update the one that exists.

## Rules

- **Evidence before confidence.** Trace every claim to feedback, an interview, analytics, a competitor source or clearly attributed team input. When the evidence is thin, say so.
- **Don't synthesise too early.** One comment is usually feedback, not a recurring painpoint. A structured interview that shows a clearly blocking problem can be the exception; label the evidence honestly. The rules are in [`playbooks/feedback-synthesis.md`](playbooks/feedback-synthesis.md).
- **Keep pain and request apart.** A feature request is what someone asked for. A painpoint is the problem underneath. Keep both when both matter.
- **Specs are downstream.** A spec links to a painpoint, a discovery result, a strategy thesis or another source. If the evidence is missing, the spec says so.
- **Strategy is not a feature list.** A strategy thesis is a durable claim about positioning, moat or sequencing. Specific builds belong in specs and in the tracker.
- **Competitor work stays factual, and lives in [`company/market/competitors/`](../../company/market/competitors/README.md).** Record what they ship, cite the source and the date it was checked, name where they are ahead, and keep current fact apart from inference. One competitor, one file there; never a second profile here.
- **Never fake a quote.** "Their words" are verbatim, or clearly marked as a paraphrase. A summary never becomes a quote.
- **External actions need approval.** Draft first. Before sending a message or changing a connected tool, show the exact action, where it goes and what else it changes, then wait for a yes.
- **The tracker owns the roadmap.** Initiatives, projects, tasks, owners, status and delivery dates live in the tracker named in [`company/tools.md`](../../company/tools.md). Link to them; never rebuild the roadmap here. With no tracker, say so plainly rather than inventing one.
- **Start from the company context.** What the product is and who it is for is in [`company/products/`](../../company/products/README.md), and its words are in [`company/glossary.md`](../../company/glossary.md). Link to them; never copy them here.
- **Follow a process when one exists.** Each recurring flow has a page in [`processes/`](processes/README.md), started by what the person says: "a customer just told me…" is capture feedback, "we keep hearing this" is synthesise feedback, "write this up for engineering" is write a spec. Confirm the specifics that matter, then follow the page.
- **Capture or synthesis?** When a task could be either and the answer changes the output, ask.
- **Keep durable context current.** When agreed work changes a product fact, a source, a strategy claim or a decision, update the page that holds it. Never leave the truth only in the chat.

## Data and access

- Keep only the product context the team needs to decide.
- Secrets, credentials, private personal details, restricted transcripts and bulk raw exports stay in their access-controlled source. Link to it when the team can use the link; otherwise anonymise or summarise.
- Before customer names, quotes or source links go into a page, a recap or the dashboard, check that everyone who reads it may see them. Anonymise or summarise when they may not.
- A link is not permission to copy or pass on what it points to.

## Bringing product material in

The root rules for bringing material in apply ([`.agents/import.md`](../../.agents/import.md)): show where each piece would go, wait for a yes, never overwrite what a page says, and pages written from it stay **Not confirmed yet**. Product material sorts like this:

- **A user's comment, an email, a support note** — [`user-feedback/feedback/`](user-feedback/feedback/README.md), through [capture feedback](processes/capture-feedback.md)
- **An interview or a research session** — [`user-feedback/user-interviews/`](user-feedback/user-interviews/README.md), the same way
- **An explicit ask** — [`user-feedback/feature-requests/`](user-feedback/feature-requests/README.md)
- **A problem that keeps coming up** — [`user-feedback/painpoints/`](user-feedback/painpoints/README.md), through [synthesise feedback](processes/synthesise-feedback.md)
- **An open question** — [`discovery/`](discovery/README.md)
- **A claim about how the product wins** — [`strategy/`](strategy/README.md)
- **A brief for one piece of work** — [`specs/`](specs/README.md)
- **A person's current priorities** — [`team-input/`](team-input/README.md)
- **A competitor** — [`company/market/competitors/`](../../company/market/competitors/README.md), not here
- **What the product is, or a word the team uses** — [`company/products/`](../../company/products/README.md) or [`company/glossary.md`](../../company/glossary.md), not here
- **Tasks, issues, the roadmap** — the tracker; link to it, never copy it

From a connected tool, take what the work needs: recent attributed feedback from a support tool or a CRM, not the whole record; interview summaries with verbatim quotes and links from a research tool; metric definitions and links from analytics, not the data; the active themes and their links from the tracker, not every issue.

## Where to read for a task

| When the task is… | Read |
|---|---|
| Setting up the product space | `SETUP.md` if it exists |
| Saving feedback, an interview or an explicit ask | [`processes/capture-feedback.md`](processes/capture-feedback.md), then the playbook |
| Turning several sources into painpoints and requests | [`processes/synthesise-feedback.md`](processes/synthesise-feedback.md), then the playbook |
| Bringing the dashboard up to date | [`processes/rebuild-feedback-dashboard.md`](processes/rebuild-feedback-dashboard.md) |
| A recap of the feedback for someone | [`processes/share-feedback.md`](processes/share-feedback.md) |
| A question nobody can answer yet | [`discovery/README.md`](discovery/README.md) |
| A claim about how the product wins | [`strategy/README.md`](strategy/README.md) |
| A spec | [`processes/write-a-spec.md`](processes/write-a-spec.md) |
| Checking work before it is shared | [`processes/review-product-work.md`](processes/review-product-work.md) |
| A teammate's product input, or logging a roadmap sync | [`team-input/README.md`](team-input/README.md) |
| A competitor | [`company/market/competitors/`](../../company/market/competitors/README.md) |
| Bringing existing product material in | "Bringing product material in" above, then the README of each folder it goes to |

## Updating this space

- A correction about working here → [`lessons.md`](lessons.md). A decision or a change → [`log.md`](log.md), with `Decision:` before a real decision.
- Feedback, an interview, a request or a painpoint added or changed → rebuild the dashboard in the same session.
- A better way of thinking about synthesis → the playbook. A better way of doing a flow → its process.
- A rule the person states for working here → this file, under **Rules**. What is here and where things go → `README.md`.

Keep this file short. Detail belongs in the pages it links to.
