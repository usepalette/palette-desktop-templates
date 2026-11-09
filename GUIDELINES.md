# Palette Desktop template guidelines

These guidelines define the kinds of item that Palette Desktop offers as templates, and the format of each one. Every template in this repo follows them, and the Templates page reads only what they describe.

## Three types

| Type | What it is | Where it lands | How it installs | Example |
|---|---|---|---|---|
| **Starter** | A whole workspace | A new workspace | The app copies it. No session. | `starters/company-os-core` |
| **Space** | A folder with its own rules for one team or area | `spaces/<folder>/` | The app copies it. A session fits it to the workspace. | `spaces/design-os` |
| **Artifact** | One page, skill or file | A folder the person picks | The app copies it. A session makes the first version. | `artifacts/weekly-update` |

## How they fit together

- A **starter** sets the structure: `company/`, `people/`, `projects/`, `spaces/`, and the rules in `AGENTS.md` and `.agents/`.
- A **space** goes in `spaces/`. Its pages link to the starter's pages, so **a space needs `spaces/README.md`**. Only a workspace made from Company OS Core, or from a starter that extends it, has that file.
- An **artifact** goes in any folder: `company/`, a project or a space. A page artifact brings its own process, so it works in any workspace.
- A starter can ship artifacts already in place. They are added when the starter is built, not at install.
- A page that covers what Core or a space already keeps is a **view, never a second store**. Its process reads those files and writes only to its own page. For example, Project overview reads `projects/` and never writes to it.

## Repo layout

```
GUIDELINES.md       this file: the kinds of template and the format of each
categories.yaml     the categories, shared by spaces and artifacts
featured.md         the banner and the featured row
starters/          whole workspaces; README.md says how a starter is built
spaces/            folders for one area of work; README.md says how a space is built
artifacts/         pages, skills and files; README.md says how an artifact is built
```

## Categories and featured

### `categories.yaml`

A YAML list. The page shows the categories in the order of the list.

```yaml
- id: product            # what `category` and `also` name
  name: Product          # the label on the page
  summary: Plan, build and ship, from what customers ask for to what goes out.
  hue: blue              # the colour of the category's pages
  cover: "#92bffc"       # the background of the category's cover images
```

| Field | Format |
|---|---|
| `id` | Lowercase, one word or kebab-case. Unique. Never change it after a template uses it. |
| `name` | One or two words, in sentence case. |
| `summary` | One sentence, under 80 characters, ending with a full stop. |
| `hue` | One of the eight brand colours: `blue`, `cyan`, `green`, `orange`, `pink`, `red`, `violet`, `yellow`. Each category has its own hue. |
| `cover` | A quoted six-digit hex colour: the hue's tint mixed with 15% white. Each category has its own cover colour. |

No other fields. The page hides a category that no template names in `category` or `also`.

### `featured.md`

Frontmatter that names the templates, then the banner's copy.

```markdown
---
banner: artifacts/weekly-update
row:
  - spaces/design-os
  - artifacts/roadmap
---

# Friday's update, written for you

Linear, GitHub, Slack and the calendar on one page your team reads in a minute.
```

| Part | Format |
|---|---|
| `banner` | The path of one space or artifact from the repo root: `spaces/<slug>` or `artifacts/<slug>`. |
| `row` | A list of exactly two such paths, shown as large cards under the banner. |
| Heading | One `#` heading: the banner's headline, under 50 characters. |
| Text | One paragraph of one or two sentences, under 200 characters. Nothing else in the body. |

- The banner shows the template's cover, the headline and the text, and opens the template's detail page.
- The three paths are different, and each folder exists.
- Never feature a starter: a starter is picked when a workspace is made, not from this page.

### Keeping them consistent

A card, a cover and a page each show the category, so a change in one place needs the same change in the others.

| When you | Also do this |
|---|---|
| Add a space or an artifact | Name a `category` that exists, and list other categories in `also` only. Give it the next `order` in its category. Make its cover on the category's `cover` colour, and set `data-hue` on its pages to the category's `hue`. Add it to the list in its folder's `README.md`, in its category and order. |
| Remove a space or an artifact | Take it out of `featured.md` first. Renumber `order` in its category, with no gaps. Take it out of its folder's `README.md`. |
| Move a template to another category | Change `category`, give it the next `order` there, renumber the old category, and make its cover and `data-hue` again in the new colours. |
| Add a category | Pick a `hue` and a `cover` that no other category uses. Before a page uses the hue, make sure the page style has its `data-hue` rule. |
| Change a category's `hue` or `cover` | Make every cover again whose `category` is that one, and change `data-hue` on their pages. Templates that list it only in `also` keep their own colours. |
| Remove a category | First move every template whose `category` names it, and remove it from every `also`. |
| Change `featured.md` | Check the paths exist and are not starters, and that the row has two. |
| Change the files in `_install/` | Raise `version`, and the stamps that copy it. A change to the card alone, such as `order`, `tags` or `summary`, keeps the version. |

## A template folder

| File | What it holds |
|---|---|
| `README.md` | Frontmatter: the card on the Templates page. Body: the detail page. |
| `cover.png` | The card image, 1260×812, on the category's `cover` colour. A starter has no category; its cover is a neutral grey. |
| `preview.html` | Page artifacts only: the page after a run, with made-up content. It never lands. |
| `_install/` | The files that land in the workspace, with paths relative to the target folder. |
| `_scaffold/` | Extra instructions for the agent session that finishes the install. The app gives them to the session but never copies them into the workspace. Add the folder only when the template needs more than the standard steps for its type (see [How each type installs](#how-each-type-installs)). Design OS has one; Weekly update does not. |

## README frontmatter

| Field | Value |
|---|---|
| `title`, `summary` | The card's name and one line. |
| `type` | `starter`, `space` or `artifact`. |
| `artifact_kind` | Artifacts only: `page`, `skill` or `file`. |
| `folder` | Spaces only: the folder under `spaces/`. |
| `category`, `also` | Spaces and artifacts only: where the card shows. |
| `order`, `tags` | The card's place in its category (1, 2, 3, no gaps, unique in the category), and the words search matches. |
| `request` | Spaces and artifacts only: what the person would say. The install session starts from it. |
| `version` | `YYMMDDN`. See below. |
| `author`, `updated` | Who made it, and the date of the last change. |

## Version and stamp

- `version` is the release date and the build number on that day. `2611092` is the second build on 9 November 2026.
- Every file the app must find carries `template: <slug>@<version>`, for example `weekly-update@2611092`.
- To compare two versions, read the first six digits as the date and the rest as the build number. Do not compare the whole value as a number: `26110910` (build 10 on 9 November) is larger than `2611101` (build 1 on 10 November).
- Never stamp `preview.html`.

| Type | Where the stamp is |
|---|---|
| Starter | The frontmatter of the new workspace's root `README.md`. It says which starter, at which version, made the workspace. |
| Space | The frontmatter of `spaces/<folder>/README.md` |
| Page artifact | The header comment of each page and of `_template.html`, and the frontmatter of the process |
| Skill artifact | `metadata.template` in `SKILL.md` |

## How each type installs

**Starter**

1. The app copies `_install/` into the new workspace.
2. The starter's `SETUP.md` runs the first session from Home.

**Space**

A space needs `spaces/README.md`. If the workspace has no such file, the card says so and does not install.

1. The app takes a checkpoint.
2. The app copies `_install/` to `spaces/<folder>/`. An earlier folder with that name is replaced, and the checkpoint keeps it.
3. A session follows `_scaffold/setup.md`. It registers the space, fills in the owner and the dates, and starts the space's own setup. The app's message says if a folder was replaced.

**Page artifact**

1. The person picks a folder.
2. The app takes a checkpoint.
3. The app copies `_install/` into the folder. It makes `processes/` with a `README.md` if the folder has none.
4. A session fills in the owner and the dates, adds the process to `processes/README.md`, and runs the process once.

These steps are the same for every page artifact, so a page artifact has no `_scaffold/`.

## How a page stays current

A page artifact is a process and either one page or one page per item. Both land in the folder the person picks.

| Shape | What lands | Example |
|---|---|---|
| One page | `<slug>.html` and `processes/<slug>.md` | Weekly update |
| One page per item | `<subfolder>/_template.html`, `<subfolder>/README.md` and `processes/<slug>.md` | Launch plan, in `launches/` |

```
weekly-update.html             one page
launches/
├── _template.html             the mold for a new launch
├── README.md                  the list of launches
└── portals-2.html             one page per launch
processes/weekly-update.md     the sources, the steps and the cadence
processes/launch-plan.md
```

For one page per item, the subfolder holds every item. The process copies `_template.html` to make a new item, and adds a row to the subfolder's `README.md`. An item is named for its subject (`portals-2.html`), or for its date when it has one (`2026-11-02.html`).

**The page is self-contained.** Sharing uploads one file, so the page must read the same with no other file next to it.

- The style, the script, the fonts and the images are in the file. An image is a `data:` URI.
- A link goes to a web address (an issue, a pull request, a thread) or to a place on the same page. It never goes to another file in the workspace.
- Content that is too long for a row goes in a row that opens, on the same page. A content brief, a comms piece, a competitor profile and a decision's detail are all rows that open.
- A version for readers outside the team is a second self-contained file, not a view of the first. The parts only the team reads carry `data-internal`, and the process leaves them out of that file. Roadmap writes `roadmap-customers.html` on the first share, for example.

**The page's structure:**

- The comment at the top is the frontmatter: `type`, `owner`, `last_updated`, `period`, `template`.
- The content comes first. An `end of content` comment follows it, then the template's script and style. An agent reads only down to that comment.
- The process writes only inside elements with `data-slot`. Everything outside a slot belongs to the team.
- An element with `data-kept="YYYY-MM-DD"` was changed at someone's request. The process never rewrites it while its period lasts. At a new period it belongs to the earlier one: it leaves with that period, into the page's earlier list or only the checkpoint, and the new period starts without it.
- Every section and row has a stable `id`. Comments on a shared page attach to it.

**A run of the process** starts when someone asks for it, or presses Refresh on the page. Each run:

1. Reads the sources and says which ones answered.
2. Rewrites the slots.
3. Shows what changed, and saves after a yes.
4. Updates `last_updated`, `period` and `template`.
5. Posts after a yes, and offers to update the shared copy.

`cadence` in the process says how often it runs. The app does not schedule runs.

**A new version** replaces the process and `_template.html`, and everything after `end of content` in each page. The content stays as it is.

## What the app reads

The app finds installed templates by their stamps, not by file or folder names.

| It finds | The card shows |
|---|---|
| No stamp | Install |
| A stamp at the current version | Open, and Install in another folder |
| A stamp at an earlier version | Update |
| A process with no page or `_template.html` | Finish the install |

## Not decided yet

- The page style has `data-hue` rules for blue, green and violet only. A page in design, sales or operations needs the pink, orange or yellow rule added first.
- The format of skill and file artifacts.
- The shared style has no rule for links, so a link in a row's sources shows in the browser's default blue.
- The toolbar's `.btn` (the week, the quarter, "For customers") is a `<button>` that does nothing on every page. Make it a label, or give it a job in the shared script.
- How a space updates without losing the team's changes.
