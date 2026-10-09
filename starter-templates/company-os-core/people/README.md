---
type: index
owner: Shared
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: everyone
---

# People

One folder per person. Agents read your folder at the start of every conversation to adapt to how you work, and to write in your voice when they write as you.

The folder itself is open (`edit_policy: everyone`), but each existing `people/<name>/` profile is **owner-only**: edit it for its owner, or with their authorization. Creating a requested colleague's factual starter is covered under **Add a person**. These editing rules do not make profiles private.

## You need to…

| You need to… | Go to |
|---|---|
| Get set up here yourself | Say "help me get set up in this workspace"; the steps are under **Getting started here** |
| Add a teammate | Say "add a colleague"; the steps are under **Add a person** |
| Know how to work with someone | `<name>/README.md`, then their `lessons.md` |
| Write as someone (a post, an email, a page in their name) | `<name>/tone-of-voice.md` |
| Park a draft that has no home yet | `<name>/scratchpad/` |
| Record something learned about working with a person | `<name>/lessons.md`. A correction the person states themselves is their OK; ask only for a lesson you inferred, or one about someone else |
| Record a correction about how this folder works | [`lessons.md`](lessons.md) |
| Find an area of work rather than a person | [`spaces/`](../spaces/README.md) |

## How it works

1. **Identify you.** If the host or person supplies an email, match it to an `email:` field in a profile; otherwise use an unambiguous full name. A first name, folder name or email's name part is only a clue. Ask when identity is unclear before attributing a write or changing owner-only content; continue independent reading.
2. **Read your folder.** `README.md` (who you are, how to work with you) and `lessons.md` (what has been learned about working with you).
3. **Adapt.** Tone, style and behavior follow your preferences.

**Profile too thin?** An agent offers to fill it in, asking you or reading a live connector, never inventing.

## Getting started here

For anyone who is new in this workspace, whenever they arrive: the first person in a new workspace and every colleague who joins later. It takes a few minutes, one step at a time, and the person can stop after any step.

1. **Your folder.** An email from the host that matches no profile means a new person, so their folder is made straight away, before anything is asked:
   - First look for a profile that has no email yet and could be them (a colleague someone added by name). If there is one, ask "are you …?" and, on a yes, put their email on that profile instead of making a new folder.
   - Otherwise copy the mold to `people/<the email's name part>/` (`name@…` → `people/name/`) and set the email. If that folder already belongs to someone else, ask for their full name first and name the folder from it.
   - Name and role stay in brackets, the profile keeps a box that says "**Not filled in yet.**" and `status: draft`, and the roster row shows the email. `owner` and `last_updated_by` carry the email until the name is known.
   - Then ask for their full name and role. What a person says about themselves is confirmed: if they already gave both, don't ask again. Fill them in everywhere (heading, `owner`, roster row), take the box off and set `status: active`. The folder keeps its name.
   - If the host supplied no email, ask for full name, role and work email first, then create the folder (the steps are under **Add a person**).
2. **How to work with you.** Two or three questions: how much they want to read, whether to propose or to ask first, what annoys them. The answers go in their `README.md`, in their words.
3. **How you write,** if they write things that go out under their name. Two or three things they wrote and were happy with go into their `tone-of-voice.md`, which says how to fill it in. Skip it if they don't.
4. **What you already have.** Documents, or what another AI tool knows about their work, get filed where they belong. Optional, and it can come later.

After step 1 the person is set up. Tell them so before you ask anything else: their profile is ready, and if the app has a step for saving their work to the shared workspace, this is the moment for it. The rest makes the work better. Then look at the workspace itself:

- **If a file called `SETUP.md` exists at the root,** the workspace is still being set up. Read it, say in one line where it stands, and offer the next step. Anyone can help with it, and nobody has to: if the person says it is not theirs, note that in their `lessons.md` and don't offer it again.
- **If there is no `SETUP.md`,** the workspace is set up. Say so. If something in their own profile is still blank ("How to work with me", their `tone-of-voice.md`), offer to fill that in; otherwise ask what they want to work on.

## What is in a person folder

Copied from [`_template/`](_template/README.md):

- **`README.md`**: your profile. Identity frontmatter (`email`, `role`, optional `slack`, `github`, `linkedin`), who you are, and a **How to work with me** section: tone, what to avoid, how to push back, how you like work broken down.
- **`tone-of-voice.md`**: how you sound in writing that goes out under your name. Used whenever an agent writes as you. The company's shared voice lives in [`company/brand/voice.md`](../company/brand/voice.md); this file is only what is specific to you.
- **`lessons.md`**: what to do *differently* with you. Dated, person-specific corrections. Read at the start of every session.
- **`log.md`**: what *happened*. Durable milestones and decisions about how you work here. Read on demand, not every session.
- **`scratchpad/`**: the workbench. Drafts, experiments and imports whose final home is not clear yet. Everything in it is a proposal, not a source of truth. Promote what becomes useful to the right folder and clear the scratch copy.
- **`notes/`** (created the first time it is needed): notes you make for yourself and want to keep, such as reading notes or reflections. One dated file each, `YYYY-MM-DD-slug.md`, with a link to what the note is about. The scratchpad is temporary; notes are kept. Notes that belong to shared work go where that work lives: a customer meeting in that customer's `meetings/`. The folder gets a `README.md` (`type: index`, owned by the person) that says what it is, and each note starts with `type: doc`, the owner and the date.

**These aren't frozen.** Agents *offer to add* to your profile, lessons and voice as they learn how you work; you confirm. A lesson that stays true moves up into "How to work with me", so the lessons file stays short. Profiles are readable by teammates.

**Two different things.** Your `README.md` is how to talk *to* you. Your `tone-of-voice.md` is how to write *as* you. Don't mix them.

## Add a person

1. **Confirm who they are.** A colleague who is not in the session needs their full name and role, plus their email when it is supplied; leave an unknown email visibly unknown and never guess it. The person in the session is different: the host's email is enough to start their folder, as described under **Getting started here**.
2. **Check they don't exist.** Match the supplied email or verified full name against existing profiles and the roster. Reuse a folder only when it is the same person. A shared first name is not a match: use a distinct full-name folder, and ask if identities remain ambiguous. Never overwrite another person's profile to reuse a folder name.
3. **Copy [`_template/`](_template/README.md)** to `people/<name>/`, whole: `README.md`, `tone-of-voice.md`, `lessons.md`, `log.md` and `scratchpad/`. Name the folder in kebab-case: the first name, or first and last name when a first name isn't unique.
4. **Stamp every copied file:** `owner` is the person's name, `last_updated` is today, `last_updated_by` is the person setting it up; preserve `edit_policy: owner-only`. Fill the headings, including the scratchpad's. Set the known `email` and `role` only on the profile README, with `status: active`. Remove its mold box for directly supplied identity facts; imported or drafted content follows `.agents/page-states.md` at the workspace root.
5. **Leave the rest as it is.** "How to work with me", "What I own" and the voice file are for the person to fill in, or for agents to propose over time. A thin but correct profile is fine. Never invent a working style or a writing voice. The voice file keeps its "Not filled in yet" box until the person has filled it in.
6. **Add the row** to the roster below, replacing the "None yet" row if it is the first.

## Static and live context

Files in your folder are **static**: they only change when you edit them. That is for stable preferences: tone, working style, how agents should behave with you.

For **live context** (current focus, active projects, blockers) agents use a live connector if one is set up. Don't duplicate it here.

**Your files = how to work with you. The connector = what you are working on.**

## Roster

| Folder | Person | Role |
|---|---|---|
| _None yet._ | | |

## Rules

- **Only edit your own folder unless authorized by its owner.** An explicit request to add a colleague permits an initial factual profile from supplied facts; it does not permit invented preferences or changes to an existing owner-only profile.
- **Start from [`_template/`](_template/README.md)**, never from scratch.
- **People are not filed under spaces.** A person has one folder here, whichever spaces they work in.
- **Keep it useful.** These files shape how agents work with you, so keep them honest and up to date.
- **No HR here.** Employment records, compensation, contracts, ID numbers and home addresses live wherever the company keeps them, not in this folder. This folder is *how to work with* a person.
