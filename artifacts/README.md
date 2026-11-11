# Artifacts

An artifact is one page, skill or file. A page installs into a folder the person picks in a workspace they already have, a skill installs where agents look for skills, and a session makes the first version.

The rules for every template are in [`../GUIDELINES.md`](../GUIDELINES.md). This page covers what is particular to an artifact. The artifacts here are pages and one skill; the format of file artifacts is not defined yet.

## Format of a page artifact

```
artifacts/<slug>/
├── README.md          frontmatter: the card; body: the detail page
├── cover.png          1260×812, on the category's cover colour
├── preview.html       the page after a run, with made-up content; never lands
└── _install/
    ├── <slug>.html                 one page, or for one page per item:
    │                               <subfolder>/_template.html and <subfolder>/README.md
    └── processes/<slug>.md         the sources, the steps and the cadence
```

A page artifact has no `_scaffold/`: its install steps are the same for every one.

**`README.md` frontmatter:** `title`, `summary`, `type: artifact`, `artifact_kind: page`, `category`, `also`, `order`, `tags`, `request`, `version`, `updated`.

**The page** is one self-contained HTML file: the style, the script, the fonts and the images are in it, and a link goes only to a web address or to a place on the same page. Its content comes first, before an `end of content` comment. The process writes only inside elements with `data-slot`, and never rewrites an element with `data-kept`.

**The process** follows Core's process format. It holds the sources, how the page is built, the steps for a first run and a refresh, and every action in an outside tool, each after a preview and a yes.

The page and the process both carry the stamp `template: <slug>@<version>`. `preview.html` never does.

### How a page artifact installs

1. The person picks a folder.
2. The app takes a checkpoint.
3. The app copies `_install/` into the folder, and makes `processes/` with a `README.md` if the folder has none.
4. A session fills in the owner and the dates, adds the process to `processes/README.md`, and runs the process once.

## Format of a skill artifact

```
artifacts/<slug>/
├── README.md          frontmatter: the card; body: the detail page
├── cover.png          1260×812, on the category's cover colour
└── _install/
    └── .claude/skills/<slug>/
        ├── SKILL.md   the skill
        └── …          files the skill reads, such as a format; never workspace content
```

A skill artifact has no `_scaffold/` and no `preview.html`. Its detail page ends with an example of what the skill produces, with made-up content.

**`README.md` frontmatter:** `title`, `summary`, `type: artifact`, `artifact_kind: skill`, `category`, `also`, `order`, `tags`, `request`, `version`, `updated`.

**`SKILL.md`** starts with `name` (the slug), `description` (what it does, and when to use it) and the stamp in `metadata`:

```yaml
---
name: workspace-heal
description: "Check a workspace for broken links … Reports first and changes nothing until asked to fix."
metadata:
  template: workspace-heal@2611111
---
```

The skill reads the workspace's own rules before it acts, finds where things live from the map and the folders on disk instead of assuming folder names, and writes where the workspace already keeps that kind of thing. A first run that needs answers is a section of `SKILL.md`. [How a skill fits the workspace](../GUIDELINES.md#how-a-skill-fits-the-workspace) has the rules.

### How a skill artifact installs

1. The app takes a checkpoint.
2. The app copies `_install/` to the root of the workspace, so the skill lands in `.claude/skills/<slug>/`. An earlier folder with that name is replaced.
3. A session says what the skill does and how to ask for it, and runs the skill's first run when it has one.

## Artifacts

| Artifact | Category | Shape |
|---|---|---|
| [Projects overview](project-overview/README.md) | Product | One page |
| [Sprint review](sprint-review/README.md) | Product | One page, a new cycle on top |
| [Roadmap](roadmap/README.md) | Product | One page, with a version for customers |
| [Release notes](release-notes/README.md) | Product | One page, a new week on top, with a version for customers |
| [Feedback digest](feedback-digest/README.md) | Product | One page, a new week on top |
| [Content calendar](content-calendar/README.md) | Marketing | One page |
| [Marketing scoreboard](marketing-scoreboard/README.md) | Marketing | One page |
| [Launch plan](launch-plan/README.md) | Marketing | One page per launch, in `launches/` |
| [Competitor watch](competitor-watch/README.md) | Marketing | One page, a new week on top |
| [Weekly update](weekly-update/README.md) | Team | One page, a new week on top |
| [Decision log](decision-log/README.md) | Team | One page, a log |
| [Team capacity](team-capacity/README.md) | Team | One page |
| [Goals check-in](goals-checkin/README.md) | Team | One page for the current quarter, with its earlier weeks inside each key result and earlier quarters summarised below |
| [Workspace heal](workspace-heal/README.md) | Team | A skill: a report first, then the safe fixes when asked |
