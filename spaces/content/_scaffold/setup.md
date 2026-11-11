# Setting up Content

What the agent does in the session that installs this template. Read it with the template's README.

The app placed the Content space at `spaces/content/`, the home for the writing the company ships. It holds every piece from the first draft to the published link (`pieces/`), how the team thinks about content (`playbooks/content.md`), and the steps for starting, refining, checking, distributing and publishing a piece (`processes/`). Nothing was placed outside `spaces/content/`.

It ships as a **first version**: the content playbook is marked "Not confirmed yet", with the length, place and cadence of each channel left in brackets for the team; the processes work from day one; the list of pieces is empty. There is no sample data. The voice is not in the space: it is the company's, in `company/brand/voice.md`, and the space's setup offers to fill it in while that page is empty.

## What to do

1. **Say what it is.** Tell the person in one or two sentences what the Content space is. Don't read `AGENTS.md` or the README to them.

2. **If the install replaced a content space,** the app says so in its message. Say in one line that the earlier `spaces/content/` was replaced and that the checkpoint before the install still holds it. Offer to bring back pages from it, such as its pieces, its `lessons.md` or its `log.md`, and copy them only after a yes. Never copy them without asking. A page from a space made by hand goes where `spaces/content/AGENTS.md` → Bringing pieces in says.

3. **Register the space**, the way `spaces/README.md` → Add a space, steps 7 and 8, describes. The space is already in place: don't copy `spaces/_template/` and don't recreate any of its files.
   - Its name is Content, its folder `spaces/content/`, and what it is for: the writing the company ships, from the first draft to the published link. Its edit policy is `team`.
   - Its owner is the person installing unless they name someone else. Ask in the same round as the setup questions in step 6, not as a question of its own.
   - Add its row to the list of spaces in `spaces/README.md`, the area and its owner to **Areas and owners** in `company/how-we-work.md`, and one dated line to `spaces/log.md`. If either list already has a row for Content, which happens when this install replaced a content space, update that row; never add a second one.

4. **Stamp every page.** In each page under `spaces/content/` that has frontmatter, `[Owner]` becomes the owner, `last_updated` becomes today and `last_updated_by` becomes the person you are working for. Leave `pieces/_template.md`, `playbooks/_template.md` and `processes/_template.md` as they are: they are molds, and their slots are filled when a piece, a playbook or a process is made. Never change `template` in `spaces/content/README.md`: the app reads it to find the space and its version.

5. **Check for a second content playbook.** Read the list of spaces in `spaces/README.md`. If another space there already keeps a content playbook, such as a GTM space's `playbooks/content.md`, show the person what each of the two says, in a few lines each, and ask which one is the home for how the company approaches content. Ask in the same round as the setup questions in step 6. After the answer, the space whose copy is not the home links to the home page from its `README.md` and `AGENTS.md`. Its own copy is removed only after a yes, and then its row in that space's `playbooks/README.md` and every link to it change in the same step (`.agents/conventions.md` → Changing structure). Until that yes, both copies stay. If no other space keeps one, skip this step.

6. **Start the content setup now**, following `spaces/content/SETUP.md` as written. The person's profile is the one in the root `people/`; if they have none yet, the root rules make it. Then ask once for what they have, using what the request already says: the channels the team writes for and how often, where pieces get published, two or three pieces the company was happy with if `company/brand/voice.md` still says "Not filled in yet", and drafts or published pieces to bring in. Whatever they have is enough to start: one channel is fine. Show where each piece of existing material would go and write after their yes; never invent a channel, a cadence, a voice or a number.

   A `SETUP.md` at the workspace root is the company's setup, separate from this one. If it is still running, the content space counts as its first space when there was none, and the voice page is one of its four core pages: filling it in here moves that setup on as well.

7. **Sum up the first pass:**
   - Where the space is listed, and who owns it.
   - What you filled in, and which pages still say "Not filled in yet" or "Not confirmed yet" and need a person to read them: the content playbook, and the voice page if it was written now.
   - Which space keeps the content playbook, if there were two.
   - That the processes work from today: "help me write a post about…" starts a piece.
   - How it grows: each piece's status and link in `pieces/README.md`, a correction in the space's `lessons.md`, and what happened in its `log.md`.

## Notes

- The root `AGENTS.md` always applies; `spaces/content/AGENTS.md` adds how to write, and the `CLAUDE.md` and `GEMINI.md` beside it point to it.
- The voice is the company's. It lives in `company/brand/voice.md` and is never copied into the space; a person's own voice is their `people/<name>/tone-of-voice.md`, on top of it.
- Writers are people like everyone else: their profiles live in the root `people/`, never in the space. Their pieces go in `spaces/content/pieces/`.
- Published pieces stay where they were published, and `pieces/README.md` links to them. Images and video stay in the tool named in `company/tools.md`.
- `spaces/content/SETUP.md` is deleted when the content setup is done. Until then, the next agent to work in the space picks setup up where it stands.
