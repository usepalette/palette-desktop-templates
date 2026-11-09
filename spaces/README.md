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

**`README.md` frontmatter:** `title`, `summary`, `type: space`, `folder` (the name under `spaces/`), `category`, `also`, `order`, `tags`, `connectors`, `request`, `version`, `author`, `updated`.

**`_install/`** follows the shape of a space in Company OS Core:

- `README.md`: the space's front door. Its frontmatter carries the stamp `template: <slug>@<version>`.
- `AGENTS.md`: how to work in the space. It adds to the workspace's root rules. `CLAUDE.md` and `GEMINI.md` point to it.
- `lessons.md` and `log.md`: the space's memory.
- `SETUP.md`, when the space needs a setup of its own that can take more than one session. It is deleted when that setup is done.
- The space's own folders. A space links to `company/`, `people/` and `projects/`, and never copies them.

**`_scaffold/setup.md`** is what the install session does, once:

1. Say what the space is.
2. If the install replaced a folder, say so, and offer to bring pages back from the checkpoint.
3. Register the space in `spaces/README.md`, `company/how-we-work.md` and `spaces/log.md`.
4. Fill in the owner and the dates on every page.
5. Start the space's own setup.

## How it installs

A space needs `spaces/README.md` in the workspace. Without it, the card says so and does not install.

1. The app takes a checkpoint.
2. The app copies `_install/` to `spaces/<folder>/`. A folder with that name is replaced, and the checkpoint keeps it.
3. A session follows `_scaffold/setup.md`. The app's message says if a folder was replaced.

## Spaces

| Space | Category | What it is |
|---|---|---|
| [Design OS](design-os/README.md) | Design | The design team's principles, rules, process and design system |
