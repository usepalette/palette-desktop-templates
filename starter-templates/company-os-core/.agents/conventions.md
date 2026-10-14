---
type: doc
owner: Shared
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: everyone
read_when:
  - "You're creating, renaming, moving or archiving a file"
---

# File conventions

How a file is made here. Look-it-up reference: read it when you create, rename, move or archive a file. The rules for behaving are in the root [`AGENTS.md`](../AGENTS.md).

## The files in a folder

- **`README.md` is the front door of every content folder.** It says what the folder is for, what belongs in it and how to add to it. Where a folder *is* the content (`company/README.md`, a customer's or a project's `README.md`), it holds that content directly.
- **`lessons.md` and `log.md`** sit beside it in the root, every top-level folder, every space and every person's folder. They are standard furniture and don't need listing in a folder's contents.
- Technical folders used only by a host (such as `.vibe/`) need no README or memory files. Deeper content folders need a README, but use the nearest existing parent lessons/log unless they are themselves a space or person. A collection has a mold only when it creates repeated items.
- **`AGENTS.md`** exists only in a space whose work has its own way of thinking that differs from the root rules. If the guidance is just what is here and where things go, that is a README. `AGENTS.md` and the pointer files beside it carry no frontmatter. The pointer files in `.claude/commands/` carry only a `description` and an `argument-hint`, which is what the command menu reads.

## Frontmatter

Every folder's README, and every substantial page, opens with:

```
---
type: index                 # what this file is; see the list below
owner: <person or role responsible>
status: active              # draft | active | archived
last_updated: YYYY-MM-DD
last_updated_by: <person>   # the person behind the change, never an agent's name
edit_policy: everyone       # everyone | team | owner-only
---
```

- **`type`**: `index` for a folder's front page, `doc` by default. Others, extend as needed: `person`, `customer`, `project`, `meeting`, `product`, `competitor`, `playbook`, `process`, `template`, `command`, `lessons`, `log`.
- **`status`** describes lifecycle. Ordinary drafts become `active` when confirmed; navigation, procedures and empty memory files start `active`. A README containing a company or customer brief is content, not merely navigation. Record types such as projects follow their collection's lifecycle independently of editorial review. See [page states](page-states.md).
- **`last_updated` and `last_updated_by`**: change them when the content really changed, not when a sweep merely touched the file. `YYYY-MM-DD` means the page has not changed since the workspace was created; that is not a fault.
- **`edit_policy`** is a soft rule that agents respect, not a lock. `owner-only`: ask unless you are acting for the owner. `team`: anyone with a folder in `people/` may edit. `everyone`: open. Real access limits come from the file store's permissions.
- **A value that starts with `[`** is quoted (`owner: "[Owner]"`) so it stays text.
- **A command page** (`type: command`, in `.agents/commands/`) carries the full block plus a one-line `description` and, when it takes input, an `argument-hint`. Quote both. `argument-hint` is written with a hyphen because that is the name command menus read.
- **Small pages** (one meeting note) need only `type` and what their mold already carries.
- **Optional fields**, only where they earn their place: `read_when: [..]` (when to open the page), `tags: [..]`, `resource: <url>` (the live system this page mirrors), `cadence: weekly|monthly|quarterly`, `review_by: YYYY-MM-DD`, `maintained_by: machine` (a generated file; don't hand-edit).

## Naming

- Folder and file names in `kebab-case`. A dated file is `YYYY-MM-DD-slug.md`. Dates are always written out, never "yesterday".
- Name a file for the subject it is about, not for the round of work that produced it: could someone who never saw the work guess what the file holds?
- When files form a sequence, number them (`01-`, `02-`).
- A file's heading matches its filename, except for `README.md`, `lessons.md`, `log.md` and dated notes, whose heading says what they are about.
- Reserve `AGENTS.md`, `CLAUDE.md` and `GEMINI.md` for agent instructions or pointers, and `README.md` for a folder's front door. Don't use these reserved names for an unrelated content page.

## Links

Use normal markdown links to connect related pages: a customer's brief to its projects, a project to its customer, a space to the company pages it builds on. Never link to a file that doesn't exist yet.

## Archiving

A retired page gets a tombstone so nothing looks live when it isn't:

```
---
status: archived
archived: YYYY-MM-DD
replaced_by: <path to the current version>
reason: <why it was retired>
---
```

## Changing structure

Update indexes, trees (the one in the root `README.md` and the one on `welcome.html`), links and heading references in the same change as a move, rename or deletion. Remove obsolete instructions too: setup steps, meeting routing, brand prerequisites and commands may depend on the path. A command whose folder is removed goes with it: its page in `.agents/commands/`, its row there, and its pointer file in `.claude/commands/`. Never create a stub merely to satisfy a list.

Delete a folder only within the person's request; explain any loss of real content or dependent behavior before a consequential removal. Company and brand context remain part of a professional workspace, even when work starts in one team or project. Optional collections can be removed deliberately once their references and workflows are adjusted. Do not present required setup content that went missing as completed.

When optional local `AGENTS.md` is removed from a copied space, remove its vendor pointers, the local-rules sentence, navigation row and tree entries as well; keep the reference to root rules.

## Copying a mold

Copy the complete folder. Fill actual navigation and record headings, known owners, dates, attribution and the chosen edit policy in every non-mold Markdown file, including nested READMEs. Keep unknown facts visibly unknown. Preserve reusable `_template.md` slots for future copies. If a space sets an edit policy, carry it into its nested molds too so new items inherit it; an edit policy never grants access or makes content confidential.

Seed frontmatter uses generic dates and authors intentionally. When a copy becomes real workspace content, stamp it with the current date and the acting person. Keep template-authoring history outside the distributable seed.
