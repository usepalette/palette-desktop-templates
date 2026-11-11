# Setting up Product

What the agent does in the session that installs this template. Read it with the template's README.

The app placed the Product space at `spaces/product/`, the product team's home inside the company OS. It holds what users say (`user-feedback/`, with a dashboard), the questions still open (`discovery/`), the claims about how the product wins (`strategy/`), the briefs for what gets built (`specs/`) and what each person is pushing for (`team-input/`), with a playbook for synthesis (`playbooks/`) and a page for each recurring flow (`processes/`). Nothing was placed outside `spaces/product/`.

It ships as a **first version**: the playbook is marked "Not confirmed yet", the processes are first drafts too, the folders hold only their READMEs and molds, and the dashboard has no data yet. The line in the README that says what the space covers is a slot for setup to fill. There is no sample data.

## What to do

1. **Say what it is.** Tell the person in one or two sentences what the Product space is. Don't read `AGENTS.md` or the README to them.

2. **If the install replaced a product space,** the app says so in its message. Say in one line that the earlier `spaces/product/` was replaced and that the checkpoint before the install still holds it. Offer to bring back pages from it, such as its `lessons.md`, `log.md`, feedback or specs, and copy them only after a yes. Never copy them without asking. If feedback comes back, rebuild the dashboard afterwards.

3. **Register the space**, the way `spaces/README.md` → Add a space, steps 7 and 8, describes. The space is already in place: don't copy `spaces/_template/` and don't recreate any of its files.
   - Its name is Product, its folder `spaces/product/`, and what it is for: what users say, discovery, strategy and specs, each linked to its evidence. Its edit policy is `team`.
   - Its owner is the person installing unless they name someone else. Ask in the same round as the setup questions in step 5, not as a question of its own.
   - Add its row to the list of spaces in `spaces/README.md`, the area and its owner to **Areas and owners** in `company/how-we-work.md`, and one dated line to `spaces/log.md`. Adding the area does not confirm the rest of an unfinished `company/how-we-work.md`. If either list already has a row for Product, which happens when this install replaced a product space or when the company already named a product area, update that row; never add a second one.

4. **Stamp every page.** In each page under `spaces/product/` that has frontmatter, `[Owner]` becomes the owner, `last_updated` becomes today and `last_updated_by` becomes the person you are working for. Leave the molds as they are: every page that opens with a **Mold** box, which is each folder's `_template` file and the two formats in `team-input/`. Their slots are filled when a copy is made. Never change `template` in `spaces/product/README.md`: the app reads it to find the space and its version.

5. **Start the product setup now**, following `spaces/product/SETUP.md` as written. The person's profile is the one in the root `people/`; if they have none yet, the root rules make it. Then ask once for what they have: what the space covers (one product, a product area, a platform or a portfolio), where feedback arrives today, which tools hold the work (a tracker, analytics, a support or research tool), where their existing research, specs and strategy are, and what they want to do first. Whatever they have is enough to start: a product name alone is fine, and so is feedback captured by hand. Show where each piece of existing material would go and write after their yes; never invent product facts, users, quotes, numbers or tools.

   A `SETUP.md` at the workspace root is the company's setup, separate from this one. If it is still running, the product space now counts as its first space. `company/tools.md` is one of its pages too, so what the person tells you about their tools counts for both setups.

6. **Sum up the first pass:**
   - Where the space is listed, and who owns it.
   - What you filled in, in the space and in `company/`, and which pages still say "Not filled in yet" or "Not confirmed yet" and need a person to read them.
   - That the playbook in `playbooks/` and the processes in `processes/` are there to be changed as the team works. They aren't part of setup.
   - How the space is used: "a customer just told me…" captures feedback, "we keep hearing this" finds the pattern, and "write this up for engineering" starts a spec. A correction goes into the space's `lessons.md`, and what happened into its `log.md`.
   - If the company's setup at the root is still running, one line on where it stands now, the way its own `SETUP.md` counts it.

## Notes

- The root `AGENTS.md` always applies; `spaces/product/AGENTS.md` adds how to do product work, and the `CLAUDE.md` and `GEMINI.md` beside it point to it.
- Product people are people like everyone else: their profiles live in the root `people/`, never in the space. What a person is pushing for now goes in `spaces/product/team-input/`, linking their profile.
- What the product is, its words and its competitors live in `company/products/`, `company/glossary.md` and `company/market/competitors/`. The space links to them and never copies them.
- The tracker named in `company/tools.md` owns tasks, the roadmap, status and delivery dates. The space holds the evidence and the reasoning, and links to the tracker.
- `spaces/product/user-feedback/index.html` is a self-contained page built from the markdown beside it. Its data is never edited by hand: `spaces/product/processes/rebuild-feedback-dashboard.md` rebuilds it.
- `spaces/product/SETUP.md` is deleted when the product setup is done. Until then, the next agent to work in the space picks setup up where it stands.
