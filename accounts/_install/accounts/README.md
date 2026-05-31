# Accounts

Working memory for companies you're actively engaged with.

What goes here is the stuff that doesn't fit in a CRM field: what you actually
think about an account, your strategy, meeting takeaways, what they care
about, internal dynamics. Driven by the `/account` skill — but everything is
just markdown you can edit by hand.

## Layout

```text
accounts/
├── accounts.md        # the roster — one row per account, skim to see where things stand
├── approach.md        # how you sell — discovery questions, qualification, next steps
├── _template/         # the files a new account starts with
└── <company>/         # one folder per account
    ├── README.md      #   the brief — the one file you read to understand the account
    ├── health.md      #   health signals — usage, communication, engagement
    ├── meetings/      #   one file per meeting (added after the first one)
    └── shareables/    #   customer-facing materials (added when you have one)
```

## When to create a folder

Create a folder when there's real engagement — meetings have happened, a Slack
channel exists, or they've signed up. A name in your CRM doesn't need a folder.
If you don't have enough context to write anything meaningful, you don't need
one. Use `/account new "<company>"` to scaffold it.

## File conventions

Every account starts with two files (see `_template/`):

| File | Purpose | Update cadence |
|------|---------|---------------|
| `README.md` | The account brief — identity, people, what they care about, strategy, open threads | After meetings, strategy shifts |
| `health.md` | Health signals, product usage, communication activity | Regular check-ins |

Add these folders as needed:

| Folder | Purpose | When to create |
|--------|---------|---------------|
| `meetings/` | One file per meeting — summary, notes, follow-ups | After your first meeting |
| `shareables/` | Customer-facing materials (decks, docs, exports) | When you have something to share |

## README.md principles

The README is the one file you read to understand an account. Keep it
scannable — detail belongs in meeting files.

- **Stay under ~120 lines.** If it's growing, move detail to meeting files.
- **"What they care about" is a summary, not a transcript.** One line per theme.
- **"About them" gets replaced, not appended.** It's a snapshot, not a history.
- **Open threads is a working list.** Remove items when done.

## Stages

| Stage | Meaning |
|-------|---------|
| **Lead** | Identified, no engagement yet |
| **Outreach** | Actively reaching out |
| **Engaged** | Conversations happening, mutual interest |
| **Onboarding** | Signed up, getting started |
| **Active** | Using the product, regular engagement |
| **Paused** | Went quiet, no recent activity |
| **Churned** | Left or explicitly declined |
