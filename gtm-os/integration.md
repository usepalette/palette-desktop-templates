# GTM-OS — install guide

You just installed GTM-OS into the user's project. It's a go-to-market
operating system — a folder structure for foundations (brand, market,
strategy), playbooks, accounts, team, and active work. Most of the
files are templates with `[bracket placeholders]` waiting to be filled
in with the user's real context.

## What to do

1. Tell the user briefly what GTM-OS is — one or two sentences. Don't
   read the whole `GTM-OS.md` to them; they can read it themselves if
   they're curious.

2. Run the `/onboard` command. It walks through company basics,
   product, market, team, and stage — then populates the foundation
   files with real content. The full conversational flow is defined in
   `.claude/commands/onboard.md` (already placed). Follow it as written.

3. After `/onboard` finishes, do a quick summary:
   - Which files you filled in.
   - What's still placeholder-shaped (most things under `accounts/`,
     `work/`, `log/` are intentionally empty — they fill up as the user
     uses the system).
   - Mention that `/review` exists for periodic check-ins on the
     foundations.

## Notes

- The user can revert this install from the History timeline if they
  want to start over — a checkpoint was created before the files were
  placed.

- If Palette MCP is connected, prefer pulling org context via
  `get-orgtology` rather than asking the user manually. The `/onboard`
  flow handles this branching internally.

- `GTM-OS.md` is the user-facing readme for the system. Leave it in
  place; users may refer to it later.
