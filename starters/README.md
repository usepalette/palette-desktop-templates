# Starters

A starter is a whole workspace. The person picks one when they make a new workspace, and the app copies it as it is. No session runs at install.

The rules for every template are in [`../GUIDELINES.md`](../GUIDELINES.md). This page covers what is particular to a starter.

## Format

```
starters/<slug>/
├── README.md     frontmatter: the card; body: the detail page
├── cover.png     1260×812, on a neutral grey
└── _install/     the whole workspace, copied into the new folder
```

A starter has no `_scaffold/` and no `preview.html`.

**`README.md` frontmatter:** `title`, `summary`, `type: starter`, `order`, `tags`, `version`, `author`, `updated`. A starter has no `category` or `request`.

**`_install/`** is the workspace as the person first sees it. It must hold:

- A root `README.md` that maps the workspace. Its frontmatter carries the stamp `template: <slug>@<version>`, so the app knows which starter made the workspace.
- A root `AGENTS.md`, and the `CLAUDE.md` and `GEMINI.md` pointers beside it.
- A `SETUP.md`. The Set up step on Home starts a session that follows it. The file is deleted when setup is done.
- A `spaces/README.md`, if spaces are to install in the workspace.

## How it installs

1. The app copies `_install/` into the new workspace folder.
2. On Home, Set up starts a session that follows `SETUP.md`.

## Starters

| Starter | What it is |
|---|---|
| [Company OS Core](company-os-core/README.md) | The whole company: the company itself, people, spaces, customers and projects |
