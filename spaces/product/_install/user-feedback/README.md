---
type: index
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
---

# User feedback

Product signal kept close to its source, in a shape the team can search, compare and synthesise without losing who said it.

## You need to…

| You need to… | Go to |
|---|---|
| Save what a user said, an interview or an explicit ask | Say "capture this feedback": [`../processes/capture-feedback.md`](../processes/capture-feedback.md) |
| Find the pattern across several sources | Say "we keep hearing this": [`../processes/synthesise-feedback.md`](../processes/synthesise-feedback.md) |
| See all of it, filtered by company, type, sentiment or tag | Open [`index.html`](index.html) |
| Bring the dashboard up to date | Say "rebuild the feedback dashboard": [`../processes/rebuild-feedback-dashboard.md`](../processes/rebuild-feedback-dashboard.md) |
| Share a sourced recap | Say "recap the feedback on [a company or a topic]": [`../processes/share-feedback.md`](../processes/share-feedback.md) |

## Structure

```text
user-feedback/
├── feedback/            # short raw signals
├── user-interviews/     # longer conversations and research sessions
├── feature-requests/    # explicit asks, each linked to its sources
├── painpoints/          # problems synthesised from one or more sources
├── _companies/          # one profile per company the feedback comes from
├── recaps/              # sourced summaries saved for sharing
├── _template.md         # the mold for a piece of raw feedback
└── index.html           # the dashboard, built from the files above
```

## Lifecycle

```text
raw feedback ──┬──> explicit ask ──> feature request
               │
               └──> repeated or blocking problem ──> painpoint
user interview ┘
```

Raw input stays raw. A derived file always links back to its sources in `source_files`. When a raw source graduates is in [`../playbooks/feedback-synthesis.md`](../playbooks/feedback-synthesis.md).

## The dashboard

[`index.html`](index.html) is one self-contained page: the viewer and the data are both in the file, so it opens in any browser and can be shared as it is. The markdown is the source of truth. After a change here, rebuild the page with [`../processes/rebuild-feedback-dashboard.md`](../processes/rebuild-feedback-dashboard.md). Never edit its data by hand: the next rebuild replaces it.

## Data boundaries

- Keep only the product context everyone who reads the space may see.
- Secrets, private personal details, restricted transcripts and bulk raw exports stay in their access-controlled source. Link, anonymise or summarise instead.
- Access to a source is not permission to pass it on.

## Naming

- Feedback and interviews: `YYYY-MM-DD_company_person_topic.md`
- Feature requests and painpoints: `YYYY-MM-DD_company_topic.md`
- Company profiles: `_companies/<company>.md`
- Recaps: `recaps/YYYY-MM-DD-<company-or-topic>.md`

Each field is lowercase kebab-case. Underscores separate the fields, so the date, the company, the person and the topic can be read from the name: the one exception to the workspace's kebab-case names.
