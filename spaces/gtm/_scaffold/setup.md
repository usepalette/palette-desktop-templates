# Setting up GTM

What the agent does in the session that installs this template. Read it with the template's README.

The app placed the GTM space at `spaces/gtm/`, the go-to-market team's home inside the company OS. It holds what the team knows about how it goes to market (`foundations/`), how it thinks about selling, content and launches (`playbooks/`), how GTM work is reviewed before it is shared (`processes/`), the launch kit (`templates/`) and what the team has found out (`research/`). Nothing was placed outside `spaces/gtm/`.

It ships as a **first version**: the three playbooks are a starter point of view marked "Not confirmed yet", the launch formats are starter formats usable as they stand, the strategy and the sales story are marked "Not filled in yet", and research is empty. There is no sample data. The space ships no brand, market or product pages: it reads the workspace's own, in `company/`.

## What to do

1. **Say what it is.** Tell the person in one or two sentences what the GTM space is. Don't read `AGENTS.md` or the README to them.

2. **If the install replaced a GTM space,** the app says so in its message. Say in one line that the earlier `spaces/gtm/` was replaced and that the checkpoint before the install still holds it. Offer to bring back pages from it, such as its `lessons.md`, `log.md`, strategy, playbooks or research, and copy them only after a yes. Never copy them without asking.

3. **Register the space**, the way `spaces/README.md` → Add a space, steps 7 and 8, describes. The space is already in place: don't copy `spaces/_template/` and don't recreate any of its files.
   - Its name is GTM, its folder `spaces/gtm/`, and what it is for: the go-to-market strategy, the sales story, the playbooks for selling, content and launches, and the launch kit. Its edit policy is `team`.
   - Its owner is the person installing unless they name someone else. Ask in the same round as the setup questions in step 6, not as a question of its own.
   - Add its row to the list of spaces in `spaces/README.md`, the area and its owner to **Areas and owners** in `company/how-we-work.md`, and one dated line to `spaces/log.md`. If either list already has a row for GTM, which happens when this install replaced a GTM space, update that row; never add a second one.

4. **Stamp every page.** In each page under `spaces/gtm/` that has frontmatter, `[Owner]` becomes the owner, `last_updated` becomes today and `last_updated_by` becomes the person you are working for. Leave the four molds as they are: `foundations/_template.md`, `playbooks/_template.md`, `processes/_template.md` and `templates/_template.md`. Their slots are filled when a page is made from them. The launch formats in `templates/launch/` are not molds: stamp them, and keep the brackets under their "Fill in". Never change `template` in `spaces/gtm/README.md`: the app reads it to find the space and its version.

5. **Check what the other spaces already keep.** Read `spaces/README.md`, and the README of each space it lists.
   - If one keeps a sales playbook, as an Accounts space does in `spaces/accounts/playbooks/sales-approach.md`, or a content playbook, as a Content space does in `spaces/content/playbooks/content.md`, show the person both pages and ask which one is the home. The other space links to the home from its `README.md` and its `AGENTS.md`. Its own copy is removed only after a yes, together with every link and list row that pointed to it.
   - If one already covers go-to-market as a whole, such as a space someone made before this install, say so and ask how the two should fit together. Change neither without a yes.
   - Ask in the same round as the setup questions in step 6. Until the person answers, both pages stay as they are.

6. **Start the GTM setup now**, following `spaces/gtm/SETUP.md` as written. The person's profile is the one in the root `people/`; if they have none yet, the root rules make it. Then ask once for what they have: how the team sells today, the channels it uses, its sales deck or pitch, and the GTM material it already has written down, such as a positioning doc, a strategy or past launch posts. Whatever they have is enough to start: a sales deck alone is fine. Show where each piece of existing material would go and write after their yes; never invent a strategy, a customer, a number or a quote.

   A `SETUP.md` at the workspace root is the company's setup, separate from this one. If it is still running, the GTM space now counts as its first space. The company's voice and messaging pages belong to that setup too: filled in here, they are filled in there, so never ask for them twice.

7. **Sum up the first pass:**
   - Where the space is listed, and who owns it.
   - What you filled in, in the space and in `company/`, and which pages still say "Not filled in yet" or "Not confirmed yet" and need a person to read them.
   - Which space is the home of the sales and the content playbooks, if step 5 asked.
   - That the playbooks in `playbooks/` and the formats in `templates/launch/` are there to be changed as the team works. They aren't part of setup.
   - How the guidance grows: a better way of thinking goes into its playbook, a format made twice becomes a template, a correction goes into the space's `lessons.md`, and what happened goes into its `log.md`.

## Notes

- The root `AGENTS.md` always applies; `spaces/gtm/AGENTS.md` adds how to do GTM work, and the `CLAUDE.md` and `GEMINI.md` beside it point to it.
- The company's voice, messaging and positioning, ideal customer, competitors and products live in `company/`, never in the space. The space links to them, and its setup offers to fill in the ones that are still empty.
- The people who sell and write are people like everyone else: their profiles live in the root `people/`, and how each one writes is in their own `people/<name>/tone-of-voice.md`. Customers live in the root `customers/`. Campaigns and launches are projects in the root `projects/`, with `space: gtm` in their frontmatter.
- `spaces/gtm/SETUP.md` is deleted when the GTM setup is done. Until then, the next agent to work in the space picks setup up where it stands.
