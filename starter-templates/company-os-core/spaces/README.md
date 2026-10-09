---
type: index
owner: Shared
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: everyone
---

# Spaces

One folder per area of work. A space is a folder you can turn into whatever the company needs, with its own front door, its own rules and its own memory.

**Spaces are not only for teams.** A space can be a team's home (go-to-market, product, engineering), a discipline several people share (design), or a body of work that needs its own place (content, a marketplace, documentation). What makes a folder a space is what it carries: a `README.md` that says what is here, its own `lessons.md` and `log.md`, and an `AGENTS.md` when the work needs its own rules. That is what lets the work in it keep its own context, shared by everyone who works there.

There is no separate team folder: a team that needs a home gets a space, like any other area of work. Some common ones:

| Space | What typically lives there |
|---|---|
| `go-to-market/` | The sales and marketing strategy, channels, campaigns, the sales playbook, launch formats |
| `product/` | The product strategy, what users say, discovery notes, specs |
| `design/` | Design principles, the design system, review routines |
| `engineering/` | The architecture, technical decisions, standards, runbooks |
| `content/` | What gets published: the plan, the drafts, the formats for each channel |
| `operations/` | Finance, legal, hiring and admin routines |

These are examples, not folders that exist yet. A space is created when someone asks for one, never to give a single piece of work somewhere to live.

## When something deserves a space

- **The work is ongoing.** Work with a start and an end is a project, not a space.
- **It has its own way of working:** its own reference material, its own formats, sometimes its own rules.
- **It builds up its own lessons and decisions**, which would get lost in the company-wide `lessons.md` and `log.md`.

One document is not a space. It is a file in [`company/`](../company/README.md) or in a space that already exists.

## You need to…

| You need to… | Go to |
|---|---|
| Work in an area such as go-to-market, product or design | that space's `README.md`, then its `lessons.md`, and its `AGENTS.md` if it has one |
| Set up a new space | Say "we need a space for design"; the steps are under **Add a space** |
| Capture how something is done in an area | that space's `README.md` says which of its four folders it goes in |
| Find a person rather than an area of work | [`people/`](../people/README.md) |
| Record a correction about how spaces work in general | [`lessons.md`](lessons.md) |

## Spaces

| Space | What it is for | Owner | Updated |
|---|---|---|---|
| _None yet._ | | | |

## What is in a space

Copied from [`_template/`](_template/README.md):

```
<space>/
├── README.md        # the front door: what the space is for and what it holds
├── AGENTS.md        # how to think and behave here (only when the work needs its own rules)
├── CLAUDE.md · GEMINI.md   # thin pointers so each agent loads AGENTS.md
├── foundations/     # what is known here: the reference to load before working
├── playbooks/       # how to think: one file per domain
├── processes/       # how things are done: step-by-step checklists
├── templates/       # the fill-in formats for recurring outputs
├── lessons.md       # what to do differently here
└── log.md           # what happened here
```

Each of the four folders starts with a `README.md` and a `_template.md`. Files arrive with real work; a space is never filled with empty stubs. A space is yours to shape: add the folders the work needs, and remove the ones it doesn't.

## What goes in a space, and what doesn't

| It is… | It lives in |
|---|---|
| Something that belongs to one area of work: what it knows, decides or repeats | that space |
| Something the whole company needs: the voice, the messaging, a product description, the ideal customer | [`company/`](../company/README.md). The space links to it and never copies it |
| Work with a start and an end | [`projects/`](../projects/README.md), run with the space's playbooks and templates |
| A customer's brief and meeting notes | [`customers/`](../customers/README.md) |
| How to work with a person | [`people/`](../people/README.md) |

## Add a space

1. **Make sure someone asked for it.** A space is created when a person asks for one, or says yes when you offer.
2. **Name it for what it is**, in kebab-case: `go-to-market`, `product`, `design`, `content`. Not a name that is already in the list.
3. **Get three facts:** what the space is for in one line, who owns it, and who may edit it (`team` by default; `owner-only` for restricted editing, `everyone` for open editing). Editing policy is not confidentiality: ask about the audience and verify the store's access before saving sensitive content.
4. **Copy [`_template/`](_template/README.md)** to `spaces/<name>/`, whole: copy the folder in one go, don't write its files again one by one. Every file comes along, the four `_template.md` files too; the furniture is the point.
5. **Fill and stamp, page by page.** Seven pages in the copy are not molds: the `README.md`, `lessons.md`, `log.md`, and the `README.md` in each of the four folders. In each of them, `[Space]` and `[space]` become the name, `[Owner]` the owner, `last_updated` today and `last_updated_by` the person you are working for. Apply the chosen `edit_policy` to all seven pages and to the four nested `_template.md` files so future content inherits it; preserve the molds' unknown slots. On the front `README.md`, set `status: active` for the real space. Remove its mold box when the purpose and facts came directly from the person; otherwise replace it with a review box following `.agents/page-states.md` at the root.
6. **Decide on `AGENTS.md`.** Keep it only if the work here has a distinct way of thinking or acting that differs from the root rules: a voice to protect, an approval flow, a discretion rule. If it stays, `[space]` in it becomes the name too. If the guidance is just what is here and where things go, that is the README: delete the space's `AGENTS.md`, `CLAUDE.md` and `GEMINI.md`, and the local-rules sentence, the row and the two tree lines in the README that point to them. Keep the sentence linking to the root rules. It can be added back later.
7. **Register it.** Add the row to the list above, replacing the "None yet" row if it is the first. Add the supplied space and owner to **Areas and owners** in [`company/how-we-work.md`](../company/how-we-work.md); this does not confirm the rest of an unfinished page.
8. **Check the links** in the new folder, then say what was created.

## Retire a space

A space that is no longer used keeps its folder as the record: set `status: archived` in its README, move its row to the bottom of the list, and add a line to [`log.md`](log.md) saying why. Delete a space only when it never held real content.
