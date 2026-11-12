# Spaces

A space is a folder for one area of work, such as product or design, with its own rules, lessons and log. It installs into `spaces/<folder>/` of a workspace the person already has, and a session fits it to that workspace.

The rules for every template are in [`../GUIDELINES.md`](../GUIDELINES.md). This page covers what is particular to a space.

## Format

```
spaces/<slug>/
├── README.md     frontmatter: the card; body: the detail page
├── cover.png     1260×812, on the category's cover colour
├── _install/     the space, with paths relative to spaces/<folder>/
└── _scaffold/
    └── setup.md  what the install session does
```

**`README.md` frontmatter:** `title`, `summary`, `type: space`, `folder` (the name under `spaces/`), `contents` (the folders and files the space brings, each with one line on what it is for; the page lists them under "What is inside"), `category`, `also`, `order`, `tags`, `request`, `version`, `updated`.

**`_install/`** follows the shape of a space in Company OS Core:

- `README.md`: the space's front door. Its frontmatter carries the stamp `template: <slug>@<version>`.
- `AGENTS.md`: how to work in the space. It adds to the workspace's root rules. `CLAUDE.md` and `GEMINI.md` point to it.
- `lessons.md` and `log.md`: the space's memory.
- `SETUP.md`, when the space needs a setup of its own that can take more than one session. It is deleted when that setup is done.
- The space's own folders. A space links to `company/`, `people/`, `customers/` and `projects/`, and never copies them. The records a space works on, such as a customer or a project, stay in those folders.

**`_scaffold/setup.md`** is what the install session does, once:

1. Say what the space is.
2. If the install replaced a folder, say so, and offer to bring pages back from the checkpoint.
3. Register the space in `spaces/README.md`, `company/how-we-work.md` and `spaces/log.md`. When work for the space often starts in another folder, such as `customers/` or `projects/`, point that folder's README to the space's process too.
4. When another space already keeps the same kind of page, such as a sales or a content playbook, show both and ask which one is the home.
5. Fill in the owner and the dates on every page.
6. Start the space's own setup.

## How it installs

A space needs `spaces/README.md` in the workspace. Without it, the card says so and does not install.

1. The app takes a checkpoint.
2. The app copies `_install/` to `spaces/<folder>/`. A folder with that name is replaced, and the checkpoint keeps it.
3. A session follows `_scaffold/setup.md`. The app's message says if a folder was replaced.

## Spaces

| Space | Category | What it is |
|---|---|---|
| [Product](product/README.md) | Product | What users say, the open questions, the strategy and the specs, each linked to its evidence |
| [Design](design/README.md) | Design | The design team's principles, rules, process and design system |
| [GTM](gtm/README.md) | Marketing | The go-to-market strategy and sales story, the playbooks for selling, content and launches, and a launch kit |
| [Content](content/README.md) | Marketing | Every piece the company ships, from the first draft to the published link, with the playbook and the voice check |
| [Accounts](accounts/README.md) | Sales | How the team works its accounts: the sales approach, call prep, account health and reviews |
| [Project](project/README.md) | Team | How the team runs its projects: starting one, recording its decisions, the ways of working and the formats |
