# Setting up Project

What the agent does in the session that installs this template. Read it with the template's README.

The app placed the Project space at `spaces/project/`: how the team runs its projects. It holds the steps to start a project and to record a decision (`processes/`), how the team works on a project and how someone joins one (`playbooks/`), and the formats a project's pages use, from the brief to the decision record (`templates/`). The projects themselves live in the root `projects/`, one folder each, made the way the workspace makes every project. Nothing was placed outside `spaces/project/`.

It ships as a **first version**: the two processes work from day one, the formats in `templates/` are molds that a project copies, and the two playbooks are marked "Not filled in yet". There is no sample data: no project, customer or person comes with it.

## What to do

1. **Say what it is.** Tell the person in one or two sentences what the Project space is: how the team runs its projects, while each project keeps its own folder in `projects/`. Don't read `AGENTS.md` or the README to them.

2. **If the install replaced a project space,** the app says so in its message. Say in one line that the earlier `spaces/project/` was replaced and that the checkpoint before the install still holds it. Offer to bring back pages from it, such as its `lessons.md`, `log.md`, its playbooks or the formats the team had changed, and copy them only after a yes. Never copy them without asking.

3. **Register the space**, the way `spaces/README.md` → Add a space, steps 7 and 8, describes. The space is already in place: don't copy `spaces/_template/` and don't recreate any of its files.
   - Its name is Project, its folder `spaces/project/`, and what it is for: how the team runs its projects, with the steps to start one and record its decisions, the ways of working and the formats. Its edit policy is `team`.
   - Its owner is the person installing unless they name someone else. Ask in the same round as the setup questions in step 5, not as a question of its own.
   - Add its row to the list of spaces in `spaces/README.md`, the area and its owner to **Areas and owners** in `company/how-we-work.md`, and one dated line to `spaces/log.md`. If either list already has a row for Project, which happens when this install replaced a project space, update that row; never add a second one.
   - Point the project pages to the space, so a project started from them gets the team's way of running it. In `projects/README.md` → You need to…, the **Start a project** row keeps its steps and adds that `spaces/project/processes/start-a-project.md` gives a project the pages this team's projects use, and the **Record a decision** row adds that a decision with real options or consequences also gets a numbered record, through `spaces/project/processes/record-a-decision.md`. Update the rows; never add a second one. Stamp the page.

4. **Stamp every page.** In each page under `spaces/project/` that has frontmatter, `[Owner]` becomes the owner, `last_updated` becomes today and `last_updated_by` becomes the person you are working for. Leave the molds unstamped: `playbooks/_template.md`, `processes/_template.md`, `templates/_template.md`, and every format in `templates/` that opens with a **Mold** box. Their slots are filled when a copy is made. Never change `template` in `spaces/project/README.md`: the app reads it to find the space and its version.

5. **Start the project setup now**, following `spaces/project/SETUP.md` as written. The person's profile is the one in the root `people/`; if they have none yet, the root rules make it. Then ask once for what they have: whether the team runs client engagements, internal projects or both, which pages a new project gets beyond its `README.md`, who sits on the other side of the team's projects, and where tasks live. Whatever they have is enough to start. Never invent a project, a customer or a person, and start a project only after a yes.

   A `SETUP.md` at the workspace root is the company's setup, separate from this one. If it is still running, the project space now counts as its first space.

6. **Sum up the first pass:**
   - Where the space is listed, and who owns it.
   - What you filled in, and which pages still say "Not filled in yet": the two playbooks, until the team says how it works.
   - That each project lives in `projects/`, made the workspace's way with `space: project`, and that the Projects overview template, if they add it, shows every project's status on one page.
   - How the method grows: a format the team changes in `templates/` holds for every new project, a correction goes into the space's `lessons.md`, and a change in how projects are run goes into its `log.md`.

## Notes

- The root `AGENTS.md` always applies; `spaces/project/AGENTS.md` adds how to run a project, and the `CLAUDE.md` and `GEMINI.md` beside it point to it.
- Projects are never filed in the space. Each lives in the root `projects/`, with its meeting notes in its own meetings folder. People live in the root `people/` and customers in the root `customers/`; a project links to them.
- Tasks have one home, the one `company/tools.md` names. A project links to its tasks and never keeps a second list.
- `spaces/project/SETUP.md` is deleted when the project setup is done. Until then, the next agent to work in the space picks setup up where it stands.
