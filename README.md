# Palette Desktop templates

The templates that the Templates page in Palette Desktop shows and installs.

## Structure

| Path | What it holds |
|---|---|
| [`starters/`](starters/) | Whole workspaces. The app copies one when a workspace is made. |
| [`spaces/`](spaces/) | A folder for one area of work, added to an existing workspace and set up in a session. |
| [`artifacts/`](artifacts/) | One page, skill or file, added to a folder of a workspace and set up in a session. |
| [`categories.yaml`](categories.yaml) | The categories that spaces and artifacts show under. |
| [`featured.md`](featured.md) | The banner and the two featured cards at the top of the page. |
| [`GUIDELINES.md`](GUIDELINES.md) | The kinds of template and the format of each. |

Each of the three folders has a `README.md` that describes its format and lists what it holds.

## Create or change a template

1. Read [`GUIDELINES.md`](GUIDELINES.md). It defines each kind of template, its folder format, how it installs and stays current, and what else to change to keep the catalog consistent.
2. For a new template, open an issue first. The catalog is curated.
3. Open a pull request that changes one template, or one catalog file.

## Legacy folders

These folders serve earlier Palette Desktop releases. Change them only to fix one of those releases, and never add a template in their format. They will be removed soon.

`accounts/` · `company-os/` · `competitor-analysis/` · `content/` · `design-os/` · `gtm-os/` · `presentations/` · `product-os/` · `project-os/` · `starter-templates/` · `workspace-heal/`
