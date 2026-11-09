---
type: doc
owner: "[Owner]"
status: draft
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
read_when:
  - You are setting up on a new computer
  - You are about to read or change code in one of the team's repos
---

# Repos

The code repositories and design files the team works in, and how to give agents access to them.

> **Not filled in yet.** Add one row per repo or design file the team works in. Say "add [repo name] to repos.md" and an agent fills in what it can read from the repo itself, then asks you for the rest.

## The repos

| Repo | What it holds | Where it is | Access |
|---|---|---|---|
| [repo-name] | [what the repo is: the design system package, the web app, the marketing site] | [link to the repo on GitHub or GitLab] | [read-only or editable] |
| [design file] | [what the file is: the component library, the product screens] | [link to the file] | [read-only or editable] |

## Give agents access

The repos stay where they are, outside this workspace. An agent reads them from there. Access is personal: it doesn't travel with the workspace, so every designer does this once on their own computer.

1. **Clone each repo** to the same place on your computer, for example `~/Developer/<repo-name>`. Using the same folder as your teammates makes the notes below easier to follow.
2. **Give the agent the folder.**
   - **In Palette Desktop** — Open **References** in the left sidebar, select `+` and choose the repo folder. A reference added there is available in every workspace you open.
   - **In another agent** — Add the repo folder to the session the way that agent does it, such as an added directory or a folder opened next to this one. Say the path in the chat if the agent has no setting for it.
3. **Choose the access.**
   - **Read-only** for repos you read but don't change, such as the design system when you are designing a product screen. This is the safe default.
   - **Editable** for the repos you design in, if the team designs in code. Changes in an editable repo go straight into the repo, outside any review of this workspace.
4. **Repeat for each repo** in the table above.
5. **Check it works.** Ask the agent to read the repo's `README.md` and tell you what the repo holds.

For design files, connect the design tool to the agent through its connector or MCP server, such as the one Figma provides, then ask the agent to list the components in the library to check it works.

## Notes per repo

Things an agent or a new teammate needs to know before working in a repo: how to run it, where the tokens and components live, the gotchas. One heading per repo. Agents add a dated line here when they learn something about a repo that the repo's own README doesn't say.

### [repo-name]

- **Run it:** [the command that starts it locally]
- **Tokens live in:** [path]
- **Components live in:** [path]
- **Documentation:** [Storybook, a docs site, or the folder of docs in the repo]
- **Instructions for agents:** [the repo's `AGENTS.md`, `CLAUDE.md` or contributing guide, if it has one]
- **Before a pull request:** [the checks to run: lint, types, tests, visual review]
- **How a change ships:** [branch naming, who reviews, how releases go out]
